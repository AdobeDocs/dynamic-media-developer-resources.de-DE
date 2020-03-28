---
description: Image Serving unterstützt Farbraumkonvertierungen, die auf Farbraum-Profilen basieren, die der ICC-Spezifikation (International Color Consortium) entsprechen.
seo-description: Image Serving unterstützt Farbraumkonvertierungen, die auf Farbraum-Profilen basieren, die der ICC-Spezifikation (International Color Consortium) entsprechen.
seo-title: Image Serving-Farbmanagement
solution: Experience Manager
title: Image Serving-Farbmanagement
topic: Scene7 Image Serving - Image Rendering API
uuid: 6291372e-ec4c-4fbd-bffc-b55b1bf2f8cf
translation-type: tm+mt
source-git-commit: 4439103ccd0d63afdd9ec20bd475560e8f84dcba

---


# Image Serving-Farbmanagement{#image-serving-color-management}

Image Serving unterstützt Farbraumkonvertierungen, die auf Farbraum-Profilen basieren, die der ICC-Spezifikation (International Color Consortium) entsprechen.

## Standardfarbräume {#section-8cfe60808bce49968091995e4e521dba}

Jeder Bildkatalog (und der Standardkatalog) kann eine Reihe von ICC-Profilen definieren, die die Standardfarbräume für diesen Katalog bilden - ein Eingabe- und ein Ausgabeformat-Profil jeweils für Graustufen-, RGB- und CMYK-Daten. See ` [attribute::IccProfileRgb](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilergb.md#reference-3479e7daac54404f84b06b98ca07b9df)`, ` [attribute::IccProfileGray](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilegray.md#reference-13822a1596e440eea0492e86d88dad35)`, ` [attribute::IccProfileCmyk](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilecmyk.md#reference-db89f9dac33e447cadb359ec1ba27ee0)`, ` [attribute::IccProfileSrcRgb](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilesrcrgb.md#reference-b8e576d075b44f5c94d95bfb5aa22ae2)`, ` [attribute::IccProfileSrcGray](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilesrcgray.md#reference-a717831da24d43f680d01393660f12f9)`, and ` [attribute::IccProfileSrcCmyk](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilesrccmyk.md#reference-b57196dfe5db41fe88bd0828ed4ec728)`.

## Eingabefarbraum {#section-9f08e2c1b6aa4fe4815be174972c1944}

Quellbilder können ICC-Profile einbetten, um den Eingabefarbraum zu definieren. Wenn kein Profil in ein Quellbild eingebettet ist, wird `attribute::IccProfileSrc*` der entsprechende Bildkatalog, der dem Pixeltyp des Quellbilds entspricht, verwendet. Wenn dieses Attribut nicht im Bildkatalog definiert ist, wird es verwendet `attribute::IccProfile*` . Wenn auch dieses Katalogattribut nicht definiert ist, wird das Bild nicht farbverwaltet und es werden nur naive Transformationen angewendet.

## Ausgabefarbraum {#section-b517bca622b64dcfa7defba6035d0716}

Der Farbraum des endgültigen Bildergebnisses einer Anforderung wird mit dem `icc=` Befehl definiert. Wenn `icc=` keine Angabe gemacht wird, wird der Standardfarbraum für die Ausgabe (aus dem Hauptkatalog der Anforderung), der dem Pixeltyp des Ausgabebilds entspricht, als Ausgabefarbraum verwendet. Wenn im Haupt- oder Standardkatalog kein Output-Profil definiert ist und die Basisebene ein Bild mit einem eingebetteten Profil ist, das dem Ausgabepildtyp entspricht, wird dieses Profil für den Ausgabefarbraum verwendet. Andernfalls bleibt der Ausgabefarbraum nicht definiert. Bei der Konvertierung zwischen Pixeltypen werden nur naive Farbkonvertierungen angewendet, und im Ausgabebild kann kein Profil eingebettet werden.

Der Ausgabefarbraum einer verschachtelten/eingebetteten Image Serving-Anforderung ist immer identisch mit dem Ausgabefarbraum der äußeren Einbettungsanforderung.

## Feste Farben {#section-df03a5c5ca894e6f8b9a5ba02cf6ac03}

Farbwerte, die mit `color=`, `bgcolor=`oder dem Befehl RTF angegeben werden, `\iscolortbl` werden mit dem Eingabefarbraum verknüpft, wenn der Farbwert das Suffix &#39;S&#39; enthält, andernfalls werden sie mit dem Ausgabefarbraum verknüpft. Farbwerte, die mit `bgc=` oder den RTF-Befehlen angegeben werden `\colortbl` und immer mit dem entsprechenden Standard- oder tatsächlichen Ausgabefarbraum verknüpft `\cmykcolortbl` sind.

>[!NOTE]
>
>Derzeit wird das Suffix &quot;S&quot;nicht vollständig am Farbmanagement `bgc=` beteiligt. Es wird ignoriert, wenn es mit angegeben wird, `bgc=`und es wird keine Konvertierung angewendet, wenn der Pixeltyp des mit angegebenen Farbwerts vom Pixeltyp des Ausgabebilds `bgc=` abweicht. Andernfalls `bgc=` wird der tatsächliche Ausgabefarbraum zugeordnet.

## Verschachtelte und eingebettete Anforderungen {#section-bdda638c31504f26a77e51ebb1ea6e3b}

Der Ausgabefarbraum für verschachtelte IS-Anforderungen und eingebettete IR-Anforderungen wird automatisch auf den Ausgabefarbraum der äußersten Anforderung eingestellt, es sei denn, die verschachtelte Anforderung gibt einen expliziten Ausgabefarbraum mit `icc=`an. Darüber hinaus übernehmen verschachtelte/eingebettete Anforderungen auch die standardmäßigen Ausgabefarbräume aus dem Hauptkatalog der Anforderung &quot;äußerste&quot;und sorgen so für eine einheitliche Behandlung der Farbwerte.

## Farbraumkonvertierung {#section-ca87b80b8e364ea59d8a92d87121b0fb}

Image Serving versucht im Allgemeinen, Farbkonvertierungen während der Verarbeitung zu verzögern. Wenn alle Ebenen eines Bildes denselben Farbraum haben, erfolgt die Konvertierung in den Ausgabefarbraum nach dem Zusammenführen und der endgültigen Skalierung. Sind mehrere Ebenenfarbräume beteiligt, wird jede Ebene vor dem Zusammenführen in den Ausgabefarbraum transformiert.

>[!NOTE]
>
>Die Befehle `op_brightness=`, `op_colorbalance=`, `op_colorize=`, `op_contrast=`, `op_hue=`und `op_saturation=` sind RGB-Vorgänge. Diese Vorgänge behalten die Farbtreue nur bei, wenn der Farbraum der Ebene den RGB-Pixeltyp aufweist. Wenn es sich nicht um RGB handelt, werden die Daten mit naiver Farbkonvertierung in RGB konvertiert, was zu einer eingeschränkten Farbtreue führt. Der Ebenenfarbraum für diese Ebenen sollte als unbestimmt betrachtet werden.

Farbkonvertierungsoptionen werden mit `icc=` oder, falls nicht angegeben, mit `icc=` , `attribute::IccRenderIntent`und `attribute::IccBlackPointCompensation``attribute::IccDither`bereitgestellt.

## Einbetten von Profilen {#section-261ebbae5ce046589a776ca972380052}

Das ICC-Profil des Ausgabefarbraums kann, sofern verfügbar, durch Angabe `iccEmbed=`in das Antwortbild eingebettet werden.

## Verwalten von ICC-Profilen {#section-eb210e4b44e64e2c8b80ee59216c5555}

Alle vom Server verwendeten Profil müssen der ICC-Spezifikation entsprechen. ICC-Profil-Dateien haben in der Regel ein [!DNL .icc] oder [!DNL .icm] -Dateisuffix und befinden sich zusammen mit Bilddatendateien.

Es wird empfohlen, alle Profil-Profile in der ICC-Profil-Map des Standardkatalogs oder -Bildkatalogs zu registrieren und anstelle von Dateipfaden Verknüpfungskennungen ( `icc=` `icc::Name`) zu verwenden.

Alle ICC-Profil, auf die in und in verwiesen wird, `catalog::IccProfile` `attribute::IccProfile*` müssen in der ICC-Profil-Map des Bildes oder Standardkatalogs registriert sein.

## Restrictions {#section-fb50ede40b124b89b30679da29782ab5}

Derzeit werden nur CMYK-, RGB- und Graustufen-Farbräume unterstützt.

## Einschließlich ICC-Profile {#section-98b4a7d9f9814e8ba27d6dcf3dcf850c}

Image Serving enthält die meisten standardmäßigen Adobe ICC-Profil im Standardbildkatalog. Auf diese Profile kann entweder mit einem gebräuchlichen Namen (z.B. in Fotoshop) oder mit einem etwas kürzeren Bezeichner zugegriffen werden. In der folgenden Tabelle sind alle standardmäßigen ICC-Profil Liste. Beim Referenzieren eines Profils im `icc=` Befehl mit dem allgemeinen Namen müssen Leerzeichen als `%20`kodiert werden.

Zusätzliche Profile können den Standardkatalogen hinzugefügt werden, entweder zum Standardkatalog oder einem bestimmten Bildkatalog. Weitere Informationen finden Sie in der [ICC Profil Map Reference](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-icc-profile-map-reference/c-icc-profile-map-reference.md#concept-57b9148ce55249cd825cb7ee19ed057c) .

>[!NOTE]
>
>Die folgende Tabelle bezieht sich nur auf *Dynamic Media Hybrid* (wird im `dynamicmedia` Ausführungsmodus ausgeführt).

|Bezeichner|Allgemeiner Name|Dateiname||—|—|—||**RGB**||||`AdobeRGB`|Adobe RGB (1998)|AdobeRGB1998.icc||`AppleRGB`|Apple RGB|AppleRGB.icc||`CIERGB`|CIE RGB|CIERGB.icc||`ColorMatchRGB`|ColorMatch RGB|ColorMatchRGB.icc||`NTSC`|NTSC (1953)|NTSC1953.icc||`PAL`|PAL/SECAM|PAL_SECAM.icc||`ProPhoto`|ProPhoto RGB|ProPhoto.icm||`SMPTE`|SMPTE-C|SMPTE-C.icc||`sRGB`|sRGB IEC61966-2.1|sRGB Color Space Profil.icm||`WideGamutRGB`|Wide Gamut RGB|WideGamutRGB.icc||**CMYK**|||`CoatedFogra27`|Coated FOGRA27 (ISO 12647-2:2004)|CoatedFOGRA27.icc||`CoatedFogra39`|Coated FOGRA39 (ISO 12647-2:2004)|CoatedFOGRA39.icc||`CoatedGraCol`|Coated GRACoL 2006 (ISO 12647-2:2004)|CoatedGRACoL2006.icc||`EuropeISOCoated`|Europe ISO Coated FOGRA27|EuropeISOCoatedFOGRA27.icc||`EuroscaleCoated`|Euroscale Coated|EuroscaleCoated.icc||`EuroscaleUncoated`|Euroscale Ungestern v2|EuroscaleUnbeschichtet.icc||`JapanColorCoated`|Japan Color 2001 Coated|JapanColor2001Coated.icc||`JapanColorNewspaper`|Japan Color 2002 Newspaper|JapanColor2002Newspaper.icc||`JapanColorUncoated`|Japan Color 2001 Ungestrichen|JapanColor2001Ungestrichen.icc||`JapanColorWebCoated`|Japan Color 2003 Web Coated|JapanColor2003WebCoated.icc||`JapanWebCoated`|Japan Web Coated (Ad)|JapanWebCoated.icc||`NewsprintSNAP2007`|US Newsprint (SNAP 2007)|USNewsprintSNAP2007.icc||`PS4Default`|Fotoshop 4 Standard-CMYK|Fotoshop4DefaultCMYK.icc||`PS5Default`|Fotoshop 5 Standard-CMYK|Fotoshop5DefaultCMYK.icc||`SheetfedCoated`|USA Sheetfeed Coated v2|USSheetfeedCoated.icc||`SheetfedUncoated`|USA Sheetfeed Ungestern v2|USSheetfeedUnbeschichtete.icc||`UncoatedFogra29`|Ungestrichenes FOGRA29 (ISO 12647-2:2004)|Ungestrichenes FOGRA29.icc||`WebCoated`|USA Web Coated (SWOP) v2|USWebCoatedSWOP.icc||`WebCoatedFogra28`|Web Coated FOGRA28 (ISO 12647-2:2004)|WebCoatedFOGRA28.icc||`WebCoatedGrade3`|Web Coated SWOP 2006 Grade 3 Paper|WebCoatedSWOP2006Grade3.icc||`WebCoatedGrade5`|Web Coated SWOP 2006 Grade 5 Paper|WebCoatedSWOP2006Grade5.icc||`WebUncoated`|USA Web Ungestern v2|USWebUnbeschichtete.icc|

Die folgende Tabelle gilt für *Dynamic Media Classic (Scene7) Image Serving* und *Dynamic Media* (Ausführung im `dynamicmedia_scene7` Ausführungsmodus).

|Bezeichner|Allgemeiner Name|Dateiname||—|—|—||**RGB**||||`AdobeRGB`|Adobe RGB (1998)|AdobeRGB1998.icc||`AppleRGB`|Apple RGB|AppleRGB.icc||`CIERGB|CIE RGB`|CIERGB.icc||`ColorMatchRGB`|ColorMatch RGB|ColorMatchRGB.icc||`NTSC`|NTSC (1953)|NTSC1953.icc||`PAL`|PAL/SECAM|PAL_SECAM.icc||`ProPhoto RGB`|ProPhoto RGB|ProPhoto RGB.icm||`SMPTE`|SMPTE-C|SMPTE-C.icc||`sRGB`|sRGB IEC61966-2.1|sRGB Color Space Profil.icm||`WideGamutRGB`|Wide Gamut RGB|WideGamutRGB.icc||**CMYK**|||`CoatedFogra27`|Coated FOGRA27 (ISO 12647-2:2004)|CoatedFOGRA27.icc||`CoatedFogra39`|Coated FOGRA39 (ISO 12647-2:2004)|CoatedFOGRA39.icc||`Coated GRACoL 2006 (ISO 12647-2:2004)`|Coated GRACoL 2006 (ISO 12647-2:2004)|CoatedGRACoL2006.icc||`EuropeISOCoated`|Europe ISO Coated FOGRA27|EuropeISOCoatedFOGRA27.icc||`Euroscale Coated v2`|Euroscale Coated v2|EuroscaleCoated.icc||`EuroscaleUncoated`|Euroscale Ungestern v2|EuroscaleUnbeschichtet.icc||`JapanColorCoated`|Japan Color 2001 Coated|JapanColor2001Coated.icc||`JapanColorNewspaper`|Japan Color 2002 Newspaper|JapanColor2002Newspaper.icc||`JapanColorUncoated`|Japan Color 2001 Ungestrichen|JapanColor2001Ungestrichen.icc||`Japan Color 2003 Web Coated`|Japan Color 2003 Web Coated|JapanColor2003WebCoated.icc||`JapanWebCoated`|Japan Web Coated (Ad)|JapanWebCoated.icc||`PS4Default`|Fotoshop 4 Standard-CMYK|Fotoshop4DefaultCMYK.icc||`PS5Default`|Fotoshop 5 Standard-CMYK|Fotoshop5DefaultCMYK.icc||`SheetfedCoated`|USA Sheetfeed Coated v2|USSheetfeedCoated.icc||`SheetfedUncoated`|USA Sheetfeed Ungestern v2|USSheetfeedUnbeschichtete.icc||`UncoatedFogra29`|Ungestrichenes FOGRA29 (ISO 12647-2:2004)|Ungestrichenes FOGRA29.icc||`US Newsprint (SNAP 2007)`|US Newsprint (SNAP 2007)|USNewsprintSNAP2007.icc||`WebCoated`|USA Web Coated (SWOP) v2|USWebCoatedSWOP.icc||`WebCoatedFogra28`|Web Coated FOGRA28 (ISO 12647-2:2004)|WebCoatedFOGRA28.icc||`Web Coated SWOP 2006 Grade 3 Paper`|Web Coated SWOP 2006 Grade 3 Paper|WebCoatedSWOP2006Grade3.icc||`Web Coated SWOP Grade 5 Paper`|Web Coated SWOP 2006 Grade 5 Paper|WebCoatedSWOP2006Grade5.icc||`WebUncoated`|USA Web Ungestern v2|USWebUnbeschichtete.icc|

## Verwandte Themen {#section-39159397e80b4efca5f631eab8b9aa06}

[International Color Consortium](http://www.color.org/index.xalter), [icc=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-icc.md#reference-182b5679e21e4df3b4d330535a5a7517), [iccEmbed=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-iccembed.md#reference-e3b774fb322046a2a6dde3a7bab5583e), [attribute::IccProfile](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilecmyk.md#reference-db89f9dac33e447cadb359ec1ba27ee0)*, [attribute::IccProfileSrc](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilesrcgray.md#reference-a717831da24d43f680d01393660f12f9)*, [](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccrenderintent.md#reference-012f207f28bd4406a5368d23ed95a51f)[](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccblackpointcompensation.md#reference-357626375ee140d1807f0c05171c733f)[](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccdither.md#reference-914d0d0567364246b4016d45c0ada85b)[](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-icc-profile-map-reference/c-icc-profile-map-reference.md#concept-57b9148ce55249cd825cb7ee19ed057c)[](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md)[](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-bgc.md#reference-53376175f617446fbe5c69120f834b88)[ attribute: IccRenderIntent,attribute::IccBlackPointCompensationσattribute::Ic Dither, ICC-Profil-Referenz,color=,bgc= *`color`*](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md)
