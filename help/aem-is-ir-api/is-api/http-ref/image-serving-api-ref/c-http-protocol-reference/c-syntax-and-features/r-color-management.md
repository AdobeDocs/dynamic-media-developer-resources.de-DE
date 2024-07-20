---
title: Image Serving-Farbmanagement
description: Image Serving unterstützt Farbraumkonvertierungen basierend auf Farbraumprofilen, die der ICC (International Color Consortium)-Spezifikation entsprechen.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 0c9a489c-36e0-4934-b9c5-33414a9ce0b8
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '1220'
ht-degree: 0%

---

# Image Serving-Farbmanagement{#image-serving-color-management}

Image Serving unterstützt Farbraumkonvertierungen basierend auf Farbraumprofilen, die der ICC (International Color Consortium)-Spezifikation entsprechen.

## Standardfarbräume {#section-8cfe60808bce49968091995e4e521dba}

Jeder Bildkatalog (und der Standardkatalog) kann eine Reihe von ICC-Profilen definieren, die die standardmäßigen Farbräume für diesen Katalog bilden - jeweils ein Eingabe- und ein Ausgabedarstellungsprofil für Graustufen-, RGB- und CMYK-Daten. Siehe
[attribute::IccProfileRgb](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilergb.md)
[attribute::IccProfileGray](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilegray.md)
[attribute::IccProfileCmyk](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilecmyk.md)
[attribute::IccProfileSrcRgb](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilesrcrgb.md)
[attribute::IccProfileSrcGray](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilesrcgray.md)
[attribute::IccProfileSrcCmyk](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilesrccmyk.md).

## Eingabefarbraum {#section-9f08e2c1b6aa4fe4815be174972c1944}

Source-Bilder können ICC-Profile einbetten, um den Eingabefarbraum zu definieren. Wenn kein Profil in ein Quellbild eingebettet ist, wird `attribute::IccProfileSrc*` des entsprechenden Bildkatalogs verwendet, der dem Pixeltyp des Quellbilds entspricht. Wenn dieses Attribut nicht im Bildkatalog definiert ist, wird `attribute::IccProfile*` verwendet. Wenn dieses Katalogattribut ebenfalls nicht definiert ist, wird das Bild nicht farbverwaltet und es werden nur naive Transformationen angewendet.

## Ausgabefarbraum {#section-b517bca622b64dcfa7defba6035d0716}

Der Farbraum des endgültigen Bildergebnisses einer Anforderung wird mit dem Befehl `icc=` definiert. Wenn `icc=` nicht angegeben ist, wird der standardmäßige Ausgabefarbraum (aus dem Hauptkatalog der Anforderung), der dem Pixeltyp des Ausgabebilds entspricht, als Ausgabefarbraum verwendet. Wenn kein Ausgabeprofil im Haupt- oder Standardkatalog definiert ist und die Basisebene ein Bild mit einem eingebetteten Profil ist, das dem Ausgabepipeltyp entspricht, wird dieses Profil für den Ausgabefarbraum verwendet. Andernfalls bleibt der Ausgabefarbraum nicht definiert - beim Konvertieren zwischen Pixeltypen werden nur naive Farbkonvertierungen angewendet und im Ausgabebild kann kein Farbprofil eingebettet werden.

Der Ausgabefarbraum einer verschachtelten/eingebetteten Image Serving-Anforderung entspricht immer dem Ausgabefarbraum der äußeren Einbettungsanforderung.

## Feste Farben {#section-df03a5c5ca894e6f8b9a5ba02cf6ac03}

Die mit `color=`, `bgcolor=` oder dem RTF-Befehl `\iscolortbl` angegebenen Farbwerte werden dem Eingabefarbraum zugeordnet, wenn der Farbwert das Suffix &quot;S&quot;enthält. Andernfalls werden sie dem Ausgabefarbraum zugeordnet. Farbwerte, die mit `bgc=` oder den RTF-Befehlen `\colortbl` und `\cmykcolortbl` angegeben werden, werden immer dem entsprechenden standardmäßigen oder tatsächlichen Ausgabefarbraum zugeordnet.

>[!NOTE]
>
>Derzeit nimmt `bgc=` nicht vollständig am Farbmanagement teil. Das S-Suffix wird ignoriert, wenn es mit `bgc=` angegeben wird, und eine naive Konvertierung wird angewendet, wenn der mit `bgc=` angegebene Pixeltyp des Farbwerts vom Pixeltyp des Ausgabebilds abweicht. Andernfalls wird `bgc=` mit dem tatsächlichen Ausgabefarbraum verknüpft.

## Verschachtelte und eingebettete Anforderungen {#section-bdda638c31504f26a77e51ebb1ea6e3b}

Der Ausgabefarbraum für verschachtelte IS-Anforderungen und eingebettete IR-Anforderungen wird automatisch auf den Ausgabefarbraum der äußersten Anforderung festgelegt, es sei denn, die verschachtelte Anforderung gibt einen expliziten Ausgabefarbraum mit `icc=` an. Darüber hinaus übernehmen verschachtelte/eingebettete Anforderungen auch die standardmäßigen Ausgabefarbräume aus dem Hauptkatalog der äußersten Anforderung, um eine konsistente Verarbeitung der Farbwerte sicherzustellen.

## Farbraum-Konversion {#section-ca87b80b8e364ea59d8a92d87121b0fb}

Image Serving versucht im Allgemeinen, Farbkonvertierungen während der Verarbeitung zu verzögern. Wenn alle Ebenen eines Bildes denselben Ebenenfarbraum haben, erfolgt die Konvertierung in den Ausgabefarbraum nach der Zusammenführung und endgültigen Skalierung. Wenn mehrere Ebenenfarbräume beteiligt sind, wird jede Ebene vor der Zusammenführung in den Ausgabefarbraum umgewandelt.

>[!NOTE]
>
>Die Befehle `op_brightness=`, `op_colorbalance=`, `op_colorize=`, `op_contrast=`, `op_hue=` und `op_saturation=` sind RGB-Vorgänge. Diese Vorgänge behalten die Farbtreue nur bei, wenn der Farbraum der Ebene den Typ RGB-Pixel aufweist. Wenn es sich nicht um RGB handelt, werden die Daten mithilfe einer naiven Farbkonvertierung in RGB konvertiert, was zu einer eingeschränkten Farbtreue führt. Der Ebenenfarbraum für solche Ebenen sollte als unbestimmt betrachtet werden.

Farbkonvertierungsoptionen werden mit `icc=` oder, wenn `icc=` nicht angegeben ist, mit `attribute::IccRenderIntent`, `attribute::IccBlackPointCompensation` und `attribute::IccDither` bereitgestellt.

## Einbetten von Farbprofilen {#section-261ebbae5ce046589a776ca972380052}

Das ICC-Farbprofil des Ausgabefarbraums kann, sofern verfügbar, durch Angabe von `iccEmbed=` in das Antwortbild eingebettet werden.

## Verwalten von ICC-Profilen {#section-eb210e4b44e64e2c8b80ee59216c5555}

Alle vom Server verwendeten Farbprofile müssen der ICC-Spezifikation entsprechen. ICC-Profildateien haben in der Regel das Suffix &quot;[!DNL .icc]&quot; oder &quot;[!DNL .icm]&quot; und befinden sich gemeinsam mit Bilddatendateien.

Während Ausgabeprofile im Befehl `icc=` durch Dateipfad/Namen angegeben werden können, wird empfohlen, alle Profildateien in der ICC-Profilzuordnung des Standardkatalogs oder -bildkatalogs zu registrieren und anstelle von Dateipfaden Verknüpfungs-IDs ( `icc::Name`) zu verwenden.

Alle ICC-Profile, auf die in `catalog::IccProfile` und in `attribute::IccProfile*` verwiesen wird, müssen in der ICC-Profilzuordnung des Bildes oder Standardkatalogs registriert sein.

## Einschränkungen {#section-fb50ede40b124b89b30679da29782ab5}

Derzeit werden nur CMYK-, RGB- und Graustufen-Farbräume unterstützt.

## Enthaltene ICC-Farbprofile {#section-98b4a7d9f9814e8ba27d6dcf3dcf850c}

Image Serving enthält die meisten standardmäßigen Adobe ICC-Profile im Standard-Bildkatalog. Auf diese Profile kann entweder mit ihren allgemeinen Namen (z. B. in Photoshop) oder mit einer etwas kürzeren Kennung zugegriffen werden. In der folgenden Tabelle sind alle standardmäßigen ICC-Profile aufgeführt. Wenn ein Profil im Befehl `icc=` anhand seines allgemeinen Namens referenziert wird, müssen Leerzeichen als `%20` kodiert werden.

Den Standardprofilen können zusätzliche Profile hinzugefügt werden, entweder zum Standardkatalog oder einem bestimmten Bildkatalog. Weitere Informationen finden Sie in der [Referenz zur ICC-Profilzuordnung](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-icc-profile-map-reference/c-icc-profile-map-reference.md#concept-57b9148ce55249cd825cb7ee19ed057c) .

>[!NOTE]
>
>Die folgende Tabelle gilt nur für *Dynamic Media Hybrid* (wird im Ausführungsmodus `dynamicmedia` ausgeführt).

| Kennung | Gebrauchsname | Dateiname |
|-- |-- |-- |
| **RGB** |  |  |
| `AdobeRGB` | Adobe RGB (1998) | AdobeRGB1998.icc |
| `AppleRGB` | Apple RGB | AppleRGB.icc |
| `CIERGB` | CIE-RGB | CIERGB.icc |
| `ColorMatchRGB` | ColorMatch-RGB | ColorMatchRGB.icc |
| `NTSC` | NTSC (1953) | NTSC1953.icc |
| `PAL` | PAL/SECAM | PAL_SECAM.icc |
| `ProPhoto` | ProFoto-RGB | ProPhoto.icm |
| `SMPTE` | SMPTE-C | SMPTE-C.icc |
| `sRGB` | sRGB IEC61966-2.1 | sRGB-Farbraumprofil.icm |
| `WideGamutRGB` | Wide Gamut-RGB | WideGamutRGB.icc |
| **CMYK** |  |  |
| `CoatedFogra27` | Überzogene FOGRA27 (ISO 12647-2:2004) | CoatedFOGRA27.icc |
| `CoatedFogra39` | Überzogene FOGRA39 (ISO 12647-2:2004) | CoatedFOGRA39.icc |
| `CoatedGraCol` | Coated GRACoL 2006 (ISO 12647-2:2004) | CoatedGRACoL2006.icc |
| `EuropeISOCoated` | Europe ISO Coated FOGRA27 | EuropeISOCoatedFOGRA27.icc |
| `EuroscaleCoated` | Euroscale Coated | EuroscaleCoated.icc |
| `EuroscaleUncoated` | Euroscale Unbeschichtv2 | EuroscaleUncoated.icc |
| `JapanColorCoated` | Japan Color 2001 Coated | JapanColor2001Coated.icc |
| `JapanColorNewspaper` | Japan Color 2002 Newspaper | JapanColor2002Newspaper.icc |
| `JapanColorUncoated` | Japan Color 2001 Ungestrichen | JapanColor2001Uncoated.icc |
| `JapanColorWebCoated` | Japan Color 2003 Web Coated | JapanColor2003WebCoated.icc |
| `JapanWebCoated` | Japan Web Coated (Ad) | JapanWebCoated.icc |
| `NewsprintSNAP2007` | US Newsprint (SNAP 2007) | USNewsprintSNAP2007.icc |
| `PS4Default` | Photoshop 4-Standard-CMYK | Photoshop4DefaultCMYK.icc |
| `PS5Default` | Photoshop 5-Standard-CMYK | Photoshop5DefaultCMYK.icc |
| `SheetfedCoated` | U.S. Sheetfed Coated v2 | USSheetfedCoated.icc |
| `SheetfedUncoated` | U.S. Sheetfed Unbeschichtete Version 2 | USSheetfedUncoated.icc |
| `UncoatedFogra29` | Unbeschichtetes FOGRA29 (ISO 12647-2:2004) | UncoatedFOGRA29.icc |
| `WebCoated` | U.S. Web Coated (SWOP) v2 | USWebCoatedSWOP.icc |
| `WebCoatedFogra28` | Web Coated FOGRA28 (ISO 12647-2:2004) | WebCoatedFOGRA28.icc |
| `WebCoatedGrade3` | Webbeschichteter SWOP 2006 Grad 3 Papier | WebCoatedSWOP2006Grade3.icc |
| `WebCoatedGrade5` | Webbeschichtetes SWOP 2006 Grade 5 Papier | WebCoatedSWOP2006Grade5.icc |
| `WebUncoated` | U.S. Web Unbeschichtete v2 | USWebUncoated.icc |

Die folgende Tabelle gilt für *Dynamic Media Classic Image Serving* und *Dynamic Media* (wird im Ausführungsmodus `dynamicmedia_scene7` ausgeführt).

| Kennung | Gebrauchsname | Dateiname |
|-- |-- |-- |
| **RGB** |  |  |
| `AdobeRGB` | Adobe RGB (1998) | AdobeRGB1998.icc |
| `AppleRGB` | Apple RGB | AppleRGB.icc |
| `CIERGB|CIE RGB` | CIERGB.icc |
| `ColorMatchRGB` | ColorMatch-RGB | ColorMatchRGB.icc |
| `NTSC` | NTSC (1953) | NTSC1953.icc |
| `PAL` | PAL/SECAM | PAL_SECAM.icc |
| `ProPhoto RGB` | ProFoto-RGB | ProFoto RGB.icm |
| `SMPTE` | SMPTE-C | SMPTE-C.icc |
| `sRGB` | sRGB IEC61966-2.1 | sRGB-Farbraumprofil.icm |
| `WideGamutRGB` | Wide Gamut-RGB | WideGamutRGB.icc |
| **CMYK** |  |  |
| `CoatedFogra27` | Überzogene FOGRA27 (ISO 12647-2:2004) | CoatedFOGRA27.icc |
| `CoatedFogra39` | Überzogene FOGRA39 (ISO 12647-2:2004) | CoatedFOGRA39.icc |
| `Coated GRACoL 2006 (ISO 12647-2:2004)` | Coated GRACoL 2006 (ISO 12647-2:2004) | CoatedGRACoL2006.icc |
| `EuropeISOCoated` | Europe ISO Coated FOGRA27 | EuropeISOCoatedFOGRA27.icc |
| `Euroscale Coated v2` | Euroscale Coated v2 | EuroscaleCoated.icc |
| `EuroscaleUncoated` | Euroscale Unbeschichtv2 | EuroscaleUncoated.icc |
| `JapanColorCoated` | Japan Color 2001 Coated | JapanColor2001Coated.icc |
| `JapanColorNewspaper` | Japan Color 2002 Newspaper | JapanColor2002Newspaper.icc |
| `JapanColorUncoated` | Japan Color 2001 Ungestrichen | JapanColor2001Uncoated.icc |
| `Japan Color 2003 Web Coated` | Japan Color 2003 Web Coated | JapanColor2003WebCoated.icc |
| `JapanWebCoated` | Japan Web Coated (Ad) | JapanWebCoated.icc |
| `PS4Default` | Photoshop 4-Standard-CMYK | Photoshop4DefaultCMYK.icc |
| `PS5Default` | Photoshop 5-Standard-CMYK | Photoshop5DefaultCMYK.icc |
| `SheetfedCoated` | U.S. Sheetfed Coated v2 | USSheetfedCoated.icc |
| `SheetfedUncoated` | U.S. Sheetfed Unbeschichtete Version 2 | USSheetfedUncoated.icc |
| `UncoatedFogra29` | Unbeschichtetes FOGRA29 (ISO 12647-2:2004) | UncoatedFOGRA29.icc |
| `US Newsprint (SNAP 2007)` | US Newsprint (SNAP 2007) | USNewsprintSNAP2007.icc |
| `WebCoated` | U.S. Web Coated (SWOP) v2 | USWebCoatedSWOP.icc |
| `WebCoatedFogra28` | Web Coated FOGRA28 (ISO 12647-2:2004) | WebCoatedFOGRA28.icc |
| `Web Coated SWOP 2006 Grade 3 Paper` | Webbeschichteter SWOP 2006 Grad 3 Papier | WebCoatedSWOP2006Grade3.icc |
| `Web Coated SWOP Grade 5 Paper` | Webbeschichtetes SWOP 2006 Grade 5 Papier | WebCoatedSWOP2006Grade5.icc |
| `WebUncoated` | U.S. Web Unbeschichtete v2 | USWebUncoated.icc |

## Verwandte Themen {#section-39159397e80b4efca5f631eab8b9aa06}

[International Color Consortium](https://www.color.org/index.xalter), [icc=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-icc.md#reference-182b5679e21e4df3b4d330535a5a7517), [iccEmbed=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-iccembed.md#reference-e3b774fb322046a2a6dde3a7bab5583e), [attribute::IccProfile](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilecmyk.md#reference-db89f9dac33e447cadb359ec1ba27ee0)&#42;, [attribute::IccProfileSrc](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilesrcgray.md#reference-a717831da24d43f680d01393660f12f9)&#42;, [attribute::IccRenderIntent](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccrenderintent.md#reference-012f207f28bd4406a5368d23ed95a51f), [attribute: ccBlackPointCompensation](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccblackpointcompensation.md#reference-357626375ee140d1807f0c05171c733f), [attribute::IccDither](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccdither.md#reference-914d0d0567364246b4016d45c0ada85b), [ICC Profile Map Reference](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-icc-profile-map-reference/c-icc-profile-map-reference.md#concept-57b9148ce55249cd825cb7ee19ed057c), [color=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md), [bgc=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-bgc.md#reference-53376175f617446fbe5c69120f834b88), [*`color`*](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md)
