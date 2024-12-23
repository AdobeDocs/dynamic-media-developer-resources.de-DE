---
title: Farbmanagement für Bildbereitstellung
description: Die Bildbereitstellung unterstützt Farbraumkonvertierungen auf der Grundlage von Farbraumprofilen, die der ICC-Spezifikation (International Color Consortium) entsprechen.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 0c9a489c-36e0-4934-b9c5-33414a9ce0b8
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '1220'
ht-degree: 0%

---

# Farbmanagement für Bildbereitstellung{#image-serving-color-management}

Die Bildbereitstellung unterstützt Farbraumkonvertierungen auf der Grundlage von Farbraumprofilen, die der ICC-Spezifikation (International Color Consortium) entsprechen.

## Standardfarbräume {#section-8cfe60808bce49968091995e4e521dba}

Jeder Bildkatalog (und der Standardkatalog) kann eine Reihe von ICC-Profilen definieren, die die Standardfarbräume für diesen Katalog bilden - je ein Eingabe- und ein Ausgabeprofil für Graustufen-, RGB- und CMYK-Daten. Siehe
[attribute::IccProfileRgb](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilergb.md)
[attribute::IccProfileGray](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilegray.md)
[attribute::IccProfileCmyk](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilecmyk.md)
[attribute::IccProfileSrcRgb](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilesrcrgb.md)
[attribute::IccProfileSrcGray](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilesrcgray.md)
[attribute::IccProfileSrcCmyk](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilesrccmyk.md).

## Eingabe-Farbraum {#section-9f08e2c1b6aa4fe4815be174972c1944}

Source-Bilder können ICC-Profile einbetten, um den Eingabefarbraum zu definieren. Wenn in ein Quellbild kein Profil eingebettet ist, wird `attribute::IccProfileSrc*` des entsprechenden Bildkatalogs verwendet, der dem Pixeltyp des Quellbilds entspricht. Wenn dieses Attribut im Bildkatalog nicht definiert ist, wird `attribute::IccProfile*` verwendet. Wenn auch dieses Katalogattribut nicht definiert ist, wird das Bild nicht farbverwaltet und es werden nur naive Transformationen angewendet.

## Ausgabe-Farbraum {#section-b517bca622b64dcfa7defba6035d0716}

Der Farbraum des endgültigen Bildergebnisses einer Anfrage wird mit dem Befehl `icc=` definiert. Wenn `icc=` nicht angegeben ist, wird der standardmäßige Ausgabefarbraum (aus dem Hauptkatalog der Anfrage), der dem Pixeltyp des Ausgabebilds entspricht, als Ausgabefarbraum verwendet. Wenn im Haupt- oder Standardkatalog kein Ausgabefarbprofil definiert ist und die Basisebene ein Bild mit einem eingebetteten Profil ist, das dem Ausgabepixeltyp entspricht, wird dieses Profil für den Ausgabefarbraum verwendet. Andernfalls bleibt der Ausgabefarbraum undefiniert. Bei der Konvertierung zwischen Pixeltypen werden nur naive Farbkonvertierungen angewendet, und es kann kein Farbprofil in das Ausgabebild eingebettet werden.

Der Ausgabefarbraum einer verschachtelten/eingebetteten Bildbereitstellungsanfrage ist immer derselbe wie der Ausgabefarbraum der äußeren, eingebetteten Anfrage.

## Volltonfarben {#section-df03a5c5ca894e6f8b9a5ba02cf6ac03}

Mit `color=`, `bgcolor=` oder dem RTF-`\iscolortbl` angegebene Farbwerte werden dem Eingabefarbraum zugeordnet, wenn der Farbwert das Suffix „S“ enthält. Andernfalls werden sie dem Ausgabefarbraum zugeordnet. Mit `bgc=` oder den RTF-Befehlen `\colortbl` und `\cmykcolortbl` angegebene Farbwerte sind stets mit dem entsprechenden standardmäßigen oder tatsächlichen Ausgabefarbraum verknüpft.

>[!NOTE]
>
>Zu diesem Zeitpunkt ist `bgc=` nicht vollständig am Farbmanagement beteiligt - das Suffix „S“ wird ignoriert, wenn es mit `bgc=` angegeben wird, und die naive Konvertierung wird angewendet, wenn der Pixeltyp des mit `bgc=` angegebenen Farbwerts vom Pixeltyp des Ausgabebilds abweicht. Andernfalls wird `bgc=` dem tatsächlichen Ausgabefarbraum zugeordnet.

## Verschachtelte und eingebettete Anforderungen {#section-bdda638c31504f26a77e51ebb1ea6e3b}

Der Ausgabefarbraum für verschachtelte IS-Anfragen und eingebettete IR-Anfragen wird automatisch auf den Ausgabefarbraum der äußersten Anfrage festgelegt, es sei denn, die verschachtelte Anfrage gibt einen expliziten Ausgabefarbraum mit `icc=` an. Darüber hinaus übernehmen verschachtelte oder eingebettete Anforderungen auch die standardmäßigen Ausgabefarbräume aus dem Hauptkatalog der äußersten Anforderung, um eine konsistente Verarbeitung von Solid-Color-Werten sicherzustellen.

## Farbraumkonvertierung {#section-ca87b80b8e364ea59d8a92d87121b0fb}

Die Bildbereitstellung versucht im Allgemeinen, Farbkonvertierungen während der Verarbeitung zu verzögern. Wenn alle Ebenen eines Bildes denselben Ebenenfarbraum haben, erfolgt die Konvertierung in den Ausgabefarbraum nach der Zusammenführung und endgültigen Skalierung. Wenn mehrschichtige Farbräume betroffen sind, wird jede Ebene vor dem Zusammenführen in den Ausgabefarbraum umgewandelt.

>[!NOTE]
>
>Die Befehle `op_brightness=`, `op_colorbalance=`, `op_colorize=`, `op_contrast=`, `op_hue=` und `op_saturation=` sind RGB-Vorgänge. Diese Vorgänge behalten die Farbtreue nur bei, wenn der Ebenenfarbraum vom Typ RGB-Pixel ist. Wenn es sich nicht um RGB handelt, werden die Daten mithilfe der naiven Farbkonvertierung in RGB konvertiert, und das Ergebnis weist eine eingeschränkte Farbtreue auf. Der Ebenenfarbraum für solche Ebenen sollte als unbestimmt betrachtet werden.

Die Farbkonvertierungsoptionen werden mit `icc=` oder, falls `icc=` nicht angegeben ist, mit `attribute::IccRenderIntent`, `attribute::IccBlackPointCompensation` und `attribute::IccDither` bereitgestellt.

## Einbetten von Farbprofilen {#section-261ebbae5ce046589a776ca972380052}

Das ICC-Farbprofil des Ausgabefarbraums kann, sofern verfügbar, durch Angabe von `iccEmbed=` in das Antwortbild eingebettet werden.

## ICC-Profile verwalten {#section-eb210e4b44e64e2c8b80ee59216c5555}

Alle vom Server verwendeten Farbprofile müssen der ICC-Spezifikation entsprechen. ICC-Profildateien haben in der Regel eine [!DNL .icc] oder eine [!DNL .icm] Dateiendung und befinden sich zusammen mit Bilddatendateien.

Während Ausgabeprofile durch Dateipfad/Namen im `icc=`-Befehl angegeben werden können, wird empfohlen, alle Profildateien in der ICC-Profilzuordnung des Standardkatalogs oder Bildkatalogs zu registrieren und Verknüpfungskennungen ( `icc::Name`) anstelle von Dateipfaden zu verwenden.

Alle in `catalog::IccProfile` und in `attribute::IccProfile*` referenzierten ICC-Profile müssen in der ICC-Profilzuordnung des Bildes oder Standardkatalogs registriert sein.

## Einschränkungen {#section-fb50ede40b124b89b30679da29782ab5}

Derzeit werden nur CMYK-, RGB- und Graustufen-Farbräume unterstützt.

## Eingeschlossene ICC-Farbprofile {#section-98b4a7d9f9814e8ba27d6dcf3dcf850c}

Die Bildbereitstellung umfasst die meisten standardmäßigen Adobe-ICC-Profile im Standardbildkatalog. Auf diese Profile kann entweder über ihre allgemeinen Namen (wie in Photoshop zu sehen) oder mit einer etwas kürzeren Kennung zugegriffen werden. In der folgenden Tabelle sind alle standardmäßigen ICC-Profile aufgeführt. Wenn im `icc=`-Befehl über den allgemeinen Namen auf ein Profil verwiesen wird, müssen Leerzeichen als `%20` codiert werden.

Zusätzliche Profile können entweder zum Standardkatalog oder zu einem bestimmten Bildkatalog zu den Standardprofilen hinzugefügt werden. Weitere Informationen finden Sie in [ICC-](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-icc-profile-map-reference/c-icc-profile-map-reference.md#concept-57b9148ce55249cd825cb7ee19ed057c)-Referenz“.

>[!NOTE]
>
>Die folgende Tabelle gilt nur für *Dynamic Media Hybrid* (wird `dynamicmedia` Ausführungsmodus ausgeführt).

| Kennung | Allgemeiner Name | Dateiname |
|-- |-- |-- |
| **RGB** |  |  |
| `AdobeRGB` | Adobe RGB (1998) | AdobeRGB1998.icc |
| `AppleRGB` | Apple RGB | AppleRGB.icc |
| `CIERGB` | CIE RGB | CIERGB.icc |
| `ColorMatchRGB` | ColorMatch-RGB | ColorMatchRGB.icc |
| `NTSC` | NTSC (1953) | NTSC1953.icc |
| `PAL` | PAL/SECAM | PAL_SECAM.icc |
| `ProPhoto` | ProPhoto RGB | ProPhoto.icm |
| `SMPTE` | SMPTE-C | SMPTE-C.icc |
| `sRGB` | sRGB IEC61966-2.1 | sRGB-Farbraumprofil.icm |
| `WideGamutRGB` | Wide Gamut RGB | WideGamutRGB.icc |
| **CMYK** |  |  |
| `CoatedFogra27` | Coated FOGRA27 (ISO 12647-2:2004) | CoatedFOGRA27.icc |
| `CoatedFogra39` | Coated FOGRA39 (ISO 12647-2:2004) | CoatedFOGRA39.icc |
| `CoatedGraCol` | Coated GRACoL 2006 (ISO 12647-2:2004) | CoatedGRACoL2006.icc |
| `EuropeISOCoated` | Europa ISO Coated FOGRA27 | EuropeISOCoatedFOGRA27.icc |
| `EuroscaleCoated` | Euroscale Coated | EuroscaleCoated.icc |
| `EuroscaleUncoated` | Euroscale Uncoated v2 | EuroscaleUncoated.icc |
| `JapanColorCoated` | Japan Color 2001 Coated | JapanColor2001Coated.icc |
| `JapanColorNewspaper` | Japan Color 2002 Newspaper | JapanColor2002Newspaper.icc |
| `JapanColorUncoated` | Japan Color 2001 Uncoated | JapanColor2001Uncoated.icc |
| `JapanColorWebCoated` | Japan Color 2003 Web Coated | JapanColor2003WebCoated.icc |
| `JapanWebCoated` | Japan Web Coated (Ad) | JapanWebCoated.icc |
| `NewsprintSNAP2007` | US Newsprint (SNAP 2007) | USNewsprintSNAP2007.icc |
| `PS4Default` | Photoshop 4 Standard-CMYK | Photoshop4DefaultCMYK.icc |
| `PS5Default` | Photoshop 5-Standard-CMYK | Photoshop5DefaultCMYK.icc |
| `SheetfedCoated` | U.S. Sheetfed Coated v2 | USSheetfedCoated.icc |
| `SheetfedUncoated` | U.S. Sheetfed Uncoated v2 | USSheetfedUncoated.icc |
| `UncoatedFogra29` | Uncoated FOGRA29 (ISO 12647-2:2004) | UncoatedFOGRA29.icc |
| `WebCoated` | U.S. Web Coated (SWOP) v2 | USWebCoatedSWOP.icc |
| `WebCoatedFogra28` | Web Coated FOGRA28 (ISO 12647-2:2004) | WebCoatedFOGRA28.icc |
| `WebCoatedGrade3` | Web Coated SWOP 2006 Grade 3 Papier | WebCoatedSWOP2006Grade3.icc |
| `WebCoatedGrade5` | Web Coated SWOP 2006 Grade 5 Papier | WebCoatedSWOP2006Grade5.icc |
| `WebUncoated` | U.S. Web Uncoated v2 | USWebUncoated.icc |

Die folgende Tabelle gilt für *Dynamic Media Classic Image Serving* und *Dynamic Media* (wird `dynamicmedia_scene7` Ausführungsmodus ausgeführt).

| Kennung | Allgemeiner Name | Dateiname |
|-- |-- |-- |
| **RGB** |  |  |
| `AdobeRGB` | Adobe RGB (1998) | AdobeRGB1998.icc |
| `AppleRGB` | Apple RGB | AppleRGB.icc |
| `CIERGB|CIE RGB` | CIERGB.icc |
| `ColorMatchRGB` | ColorMatch-RGB | ColorMatchRGB.icc |
| `NTSC` | NTSC (1953) | NTSC1953.icc |
| `PAL` | PAL/SECAM | PAL_SECAM.icc |
| `ProPhoto RGB` | ProPhoto RGB | ProPhoto RGB.icm |
| `SMPTE` | SMPTE-C | SMPTE-C.icc |
| `sRGB` | sRGB IEC61966-2.1 | sRGB-Farbraumprofil.icm |
| `WideGamutRGB` | Wide Gamut RGB | WideGamutRGB.icc |
| **CMYK** |  |  |
| `CoatedFogra27` | Coated FOGRA27 (ISO 12647-2:2004) | CoatedFOGRA27.icc |
| `CoatedFogra39` | Coated FOGRA39 (ISO 12647-2:2004) | CoatedFOGRA39.icc |
| `Coated GRACoL 2006 (ISO 12647-2:2004)` | Coated GRACoL 2006 (ISO 12647-2:2004) | CoatedGRACoL2006.icc |
| `EuropeISOCoated` | Europa ISO Coated FOGRA27 | EuropeISOCoatedFOGRA27.icc |
| `Euroscale Coated v2` | Euroscale Coated v2 | EuroscaleCoated.icc |
| `EuroscaleUncoated` | Euroscale Uncoated v2 | EuroscaleUncoated.icc |
| `JapanColorCoated` | Japan Color 2001 Coated | JapanColor2001Coated.icc |
| `JapanColorNewspaper` | Japan Color 2002 Newspaper | JapanColor2002Newspaper.icc |
| `JapanColorUncoated` | Japan Color 2001 Uncoated | JapanColor2001Uncoated.icc |
| `Japan Color 2003 Web Coated` | Japan Color 2003 Web Coated | JapanColor2003WebCoated.icc |
| `JapanWebCoated` | Japan Web Coated (Ad) | JapanWebCoated.icc |
| `PS4Default` | Photoshop 4 Standard-CMYK | Photoshop4DefaultCMYK.icc |
| `PS5Default` | Photoshop 5-Standard-CMYK | Photoshop5DefaultCMYK.icc |
| `SheetfedCoated` | U.S. Sheetfed Coated v2 | USSheetfedCoated.icc |
| `SheetfedUncoated` | U.S. Sheetfed Uncoated v2 | USSheetfedUncoated.icc |
| `UncoatedFogra29` | Uncoated FOGRA29 (ISO 12647-2:2004) | UncoatedFOGRA29.icc |
| `US Newsprint (SNAP 2007)` | US Newsprint (SNAP 2007) | USNewsprintSNAP2007.icc |
| `WebCoated` | U.S. Web Coated (SWOP) v2 | USWebCoatedSWOP.icc |
| `WebCoatedFogra28` | Web Coated FOGRA28 (ISO 12647-2:2004) | WebCoatedFOGRA28.icc |
| `Web Coated SWOP 2006 Grade 3 Paper` | Web Coated SWOP 2006 Grade 3 Papier | WebCoatedSWOP2006Grade3.icc |
| `Web Coated SWOP Grade 5 Paper` | Web Coated SWOP 2006 Grade 5 Papier | WebCoatedSWOP2006Grade5.icc |
| `WebUncoated` | U.S. Web Uncoated v2 | USWebUncoated.icc |

## Verwandte Themen {#section-39159397e80b4efca5f631eab8b9aa06}

[International Color Consortium](https://www.color.org/index.xalter), [icc=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-icc.md#reference-182b5679e21e4df3b4d330535a5a7517), [iccEmbed=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-iccembed.md#reference-e3b774fb322046a2a6dde3a7bab5583e), [attribute::IccProfile](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilecmyk.md#reference-db89f9dac33e447cadb359ec1ba27ee0)&#42;, [attribute::IccProfileSrc](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilesrcgray.md#reference-a717831da24d43f680d01393660f12f9)&#42;, [attribute::IccRenderIntent](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccrenderintent.md#reference-012f207f28bd4406a5368d23ed95a51f), [attribute::IccPointCompensation](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccblackpointcompensation.md#reference-357626375ee140d1807f0c05171c733f): IccDither](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccdither.md#reference-914d0d0567364246b4016d45c0ada85b),ICC Profile Map](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-icc-profile-map-reference/c-icc-profile-map-reference.md#concept-57b9148ce55249cd825cb7ee19ed057c), [color=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md), [bgc=[, [ ](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-bgc.md#reference-53376175f617446fbe5c69120f834b88) [*`color`*](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md)
