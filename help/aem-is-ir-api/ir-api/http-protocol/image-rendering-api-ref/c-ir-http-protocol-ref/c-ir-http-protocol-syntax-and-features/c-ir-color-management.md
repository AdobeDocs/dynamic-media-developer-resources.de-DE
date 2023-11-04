---
description: Image Rendering unterstützt Farbraumkonvertierungen basierend auf Farbraumprofilen, die der ICC (International Color Consortium)-Spezifikation entsprechen.
solution: Experience Manager
title: Farbmanagement für das Rendern von Bildern *
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: fa772ab2-8a32-4c1a-9ee3-c1cf4a0b3095
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '733'
ht-degree: 0%

---

# Farbmanagement für das Rendern von Bildern *{#image-rendering-color-management}

Image Rendering unterstützt Farbraumkonvertierungen basierend auf Farbraumprofilen, die der ICC (International Color Consortium)-Spezifikation entsprechen.

**Einschränkungen**

Derzeit werden nur CMYK-, RGB- und Graustufen-Farbräume unterstützt.

Kabinettsstil-Dateien (.vnc) und Fensterverkleidungsstil ( [!DNL .vnw]) werden nicht farbverwaltet und werden im Arbeitsfarbraum als vorhanden angenommen.

**Verwandte Themen**

[Internationales Farbkonsortium](https://www.color.org/index.xalter) , [`icc=`](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-icc.md#reference-86a2fff3cef24982ad2063d977a16e06) , [`iccEmbed=`](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-iccembed.md#reference-47a433138c7c4b29b9b29871b2491a7f) , `attribute::IccProfile*` , `attribute::IccProfileSrc*`, `attribute::IccRenderIntent` , `attribute::IccBlackPointCompensation` , `attribute::IccDither` , ICC-Profilzuordnungen

## Standardfarbräume {#section-8ce27edf42e746febe4654f8f19b9c0c}

Jeder Bildkatalog (und der Standardkatalog) kann einen Satz von ICC-Profilen definieren. Diese Profile stellen die standardmäßigen Farbräume für diesen Katalog dar - jeweils ein Eingabe- und ein Ausgabeprofil für Graustufen-, RGB- und CMYK-Daten ( `attribute::IccProfileRgb`, `attribute::IccProfileGray`, `attribute::IccProfileCmyk`, `attribute::IccProfileSrcRgb`, `attribute::IccProfileSrcGray`, und `attribute::IccProfileSrcCmyk`).

Der Standardfarbraum für ein bestimmtes Bild oder ein anderes Objekt wird basierend auf dem Pixeltyp des Bildes aus den Standardprofilen des Katalogs ausgewählt.

## Eingabefarbraum {#section-660f661a7e954df4b451e34134195276}

Materialbilder können ICC-Profile einbetten, um den Eingabefarbraum zu definieren. Wenn kein Profil in ein Quellbild eingebettet ist, `attribute::IccProfileSrc*` des entsprechenden Bildkatalogs verwendet wird, der dem Pixeltyp des Quellbilds entspricht. Wenn dieses Attribut nicht im Bildkatalog definiert ist, `attribute::IccProfile*` verwendet. Wenn dieses Katalogattribut ebenfalls nicht definiert ist, wird das Bild nicht farbverwaltet und es werden nur naive Transformationen angewendet.

## Arbeitsfarbraum {#section-645d9cfa5b0347a190a0ece218f5b5e1}

In der Regel wird der Arbeitsfarbraum durch das in die Vignette eingebettete ICC-Farbprofil definiert. Wenn die Vignette kein Profil enthält, wird das standardmäßige RGB-Eingabeprofil ( `attribute::IccProfileSrcRgb` des Sitzungskatalogs) für den Arbeitsfarbraum verwendet.

Alle Render-Vorgänge werden im Arbeitsfarbraum ausgeführt.

**Wichtig:** Das ICC-Profil für den Arbeitsfarbraum muss Eingabe- und Ausgabetransformationen unterstützen. Wenn ein reines Ausgabeprofil als Arbeitsfarbraum verwendet wird, kann die IR keine Materialien in dieses Profil konvertieren. Ein solches Farbprofil kann weiterhin verwendet werden, wenn Materialien im selben Arbeitsfarbraum vorhanden sind. Der Versuch, Materialien in anderen Farbräumen anzuwenden, schlägt fehl.

## Explizite Farbwerte {#section-31727bf1b23e477ca92572fbbf422d2f}

RGB-Farbwerte, angegeben mit `color=`, `bgc=`, `catalog::BgColor`, und `catalog::Color` im aktuellen Arbeitsfarbraum vorhanden sein.

## Materialdatendateien {#section-33f7a170a6664c02b8479fb89cc0aea3}

Materialbilddateien (Textur- und Dekorbilder) können den Pixeltyp RGB, Graustufen oder CMYK aufweisen und ein Farbprofil einbetten. Wenn kein Farbprofil eingebettet ist, wird dem Bild der standardmäßige Eingabefarbraum zugeordnet (z. B. das Farbprofil aus dem Materialkatalog, das dem Pixeltyp des Bildes entspricht).

Materialbilder, die von verschachtelten Image Serving- oder Image Rendering-Anforderungen erhalten wurden, enthalten normalerweise ein Farbprofil. Ist dies nicht der Fall, werden die Bilder dem Standardfarbraum für die Eingabefarben zugeordnet, der dem Pixeltyp entspricht.

Wenn sich der Farbraum der Bilddatei vom Arbeitsfarbraum unterscheidet, wird eine genaue Farbkonvertierung verwendet, um in den Arbeitsfarbraum zu konvertieren. Eine naïve Typkonvertierung wird verwendet, wenn kein Profil eingebettet und kein standardmäßiges Eingabeprofil definiert ist.

Andere Materialdatendateien, z. B. Kabinettsvorlagen ( [!DNL .vnc]) oder Fensterbedeckungsdateien ( [!DNL .vnw]) betten keine Farbprofile ein und werden immer als Arbeitsfarbraum angenommen.

## Ausgabefarbraum {#section-4c2c4dfedbb8429ba5cfddc3d3eab6c4}

Alle Render-Vorgänge finden im Arbeitsfarbraum statt. Wenn die Anforderung ein anderes Farbprofil mit der `icc=` -Befehl, werden die Daten in diesen Farbraum konvertiert, kurz bevor sie kodiert und an den Client zurückgegeben werden. Wenn das Farbmanagement deaktiviert ist, wird bei Bedarf eine naive Konversion verwendet, um in Graustufen- oder CMYK-Konvertierungen zu konvertieren.

## Eingebettete Farbprofile {#section-5ff733832d38429fbe02b3c1e9bb94a9}

Das dem wiedergegebenen Bild zugeordnete Farbprofil kann durch Angabe von `iccEmbed=` für die Anfrage.

Wenn `icc=` nicht angegeben ist, wird das ICC-Profil für den Arbeitsfarbraum eingebettet. Es wird kein Profil eingebettet, wenn das Farbmanagement deaktiviert ist und kein Profil mit `icc=`.

## ICC-Profile {#section-afeb76068b5042adb83261638e450140}

Alle vom Server verwendeten Farbprofile müssen der ICC-Spezifikation entsprechen. ICC-Profildateien weisen normalerweise eine [!DNL .icc] oder [!DNL .icm] -Dateisuffix und befinden sich gemeinsam mit Materialdatendateien.

Während Ausgabeprofile im `icc=` -Befehl verwenden, wird empfohlen, alle Profildateien in der ICC-Profilzuordnung des Standardkatalogs oder in einem bestimmten Materialkatalog zu registrieren und die Kurzbefehle ( `icc::Name`) anstelle von Dateipfaden.

Arbeitsprofile müssen in der ICC-Profilzuordnung des Materialkatalogs oder des Standardkatalogs registriert sein.
