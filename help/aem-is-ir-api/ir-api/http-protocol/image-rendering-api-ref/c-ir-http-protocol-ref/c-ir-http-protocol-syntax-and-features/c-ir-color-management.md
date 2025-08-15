---
description: Das Bild-Rendering unterstützt Farbraumkonvertierungen auf der Grundlage von Farbraumprofilen, die der ICC-Spezifikation (International Color Consortium) entsprechen.
solution: Experience Manager
title: Farbmanagement für das Rendern von Bildern *
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: fa772ab2-8a32-4c1a-9ee3-c1cf4a0b3095
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '731'
ht-degree: 0%

---

# Farbmanagement für das Rendern von Bildern *{#image-rendering-color-management}

Das Bild-Rendering unterstützt Farbraumkonvertierungen auf der Grundlage von Farbraumprofilen, die der ICC-Spezifikation (International Color Consortium) entsprechen.

**Einschränkungen**

Derzeit werden nur CMYK, RGB und Graustufen-Farbräume unterstützt.

Kabinettstildateien (.vnc) und Fensterabdeckungs-Stildateien (.[!DNL .vnw]) werden nicht farbverwaltet und es wird davon ausgegangen, dass sie im Arbeitsfarbraum vorhanden sind.

**Siehe auch**

[International Color Consortium](https://www.color.org/index.xalter) , [`icc=`](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-icc.md#reference-86a2fff3cef24982ad2063d977a16e06) , [`iccEmbed=`](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-iccembed.md#reference-47a433138c7c4b29b9b29871b2491a7f) , `attribute::IccProfile*` , `attribute::IccProfileSrc*`, `attribute::IccRenderIntent` , `attribute::IccBlackPointCompensation` , `attribute::IccDither` , ICC-Profilzuordnungen

## Standardfarbräume {#section-8ce27edf42e746febe4654f8f19b9c0c}

Jeder Bildkatalog (und der Standardkatalog) kann einen Satz von ICC-Profilen definieren. Diese Profile bilden die Standardfarbräume für diesen Katalog - jeweils ein Eingabe- und ein Ausgabeprofil für Graustufen-, RGB- und CMYK-Daten ( `attribute::IccProfileRgb`, `attribute::IccProfileGray`, `attribute::IccProfileCmyk`, `attribute::IccProfileSrcRgb`, `attribute::IccProfileSrcGray` und `attribute::IccProfileSrcCmyk`).

Der Standardfarbraum für ein bestimmtes Bild oder ein anderes Objekt wird aus den Standardprofilen des Katalogs basierend auf dem Pixeltyp des Bildes ausgewählt.

## Eingabe-Farbraum {#section-660f661a7e954df4b451e34134195276}

Materialbilder können ICC-Profile einbetten, um den Eingabefarbraum zu definieren. Wenn in ein Quellbild kein Profil eingebettet ist, wird `attribute::IccProfileSrc*` des entsprechenden Bildkatalogs verwendet, der dem Pixeltyp des Quellbilds entspricht. Wenn dieses Attribut im Bildkatalog nicht definiert ist, wird `attribute::IccProfile*` verwendet. Wenn auch dieses Katalogattribut nicht definiert ist, wird das Bild nicht farbverwaltet und es werden nur naive Transformationen angewendet.

## Arbeitsfarbraum {#section-645d9cfa5b0347a190a0ece218f5b5e1}

Normalerweise wird der Arbeitsfarbraum durch das in die Vignette eingebettete ICC-Farbprofil definiert. Wenn die Vignette kein Profil enthält, wird das standardmäßige RGB-Eingabeprofil (`attribute::IccProfileSrcRgb` des Sitzungskatalogs) für den Arbeitsfarbraum verwendet.

Alle Render-Vorgänge werden im Arbeitsfarbraum ausgeführt.

**Wichtig:** Das ICC-Profil für den Arbeitsfarbraum muss Eingabe- und Ausgabetransformationen unterstützen. Wenn ein reines Ausgabeprofil als Arbeitsfarbraum verwendet wird, kann IR keine Materialien in dieses Profil konvertieren. Ein solches Farbprofil kann auch dann noch verwendet werden, wenn im selben Arbeitsfarbraum Materialien vorhanden sind. Der Versuch, Materialien in anderen Farbräumen aufzubringen, schlägt fehl.

## Explizite Farbwerte {#section-31727bf1b23e477ca92572fbbf422d2f}

RGB-Farbwerte, die mit `color=`, `bgc=`, `catalog::BgColor` und `catalog::Color` angegeben wurden, werden als im aktuellen Arbeitsfarbraum vorhanden angenommen.

## Materialdatendateien {#section-33f7a170a6664c02b8479fb89cc0aea3}

Materialbilddateien (Textur- und Abziehbilddateien) können den Pixeltyp RGB, Graustufen oder CMYK aufweisen und in ein Farbprofil eingebettet werden. Wenn kein Farbprofil eingebettet ist, wird dem Bild der standardmäßige Eingabefarbraum zugeordnet (z. B. das Farbprofil aus dem Materialkatalog, das dem Pixeltyp des Bildes entspricht).

Materialbilder, die aus verschachtelten Bildbereitstellungs- oder Bild-Rendering-Anfragen stammen, enthalten in der Regel ein Farbprofil. Ist dies nicht der Fall, werden die Bilder mit dem dem Pixeltyp entsprechenden Standard-Eingabefarbraum verknüpft.

Wenn sich der Farbraum der Bilddatei vom Arbeitsfarbraum unterscheidet, wird zur Konvertierung in den Arbeitsfarbraum eine genaue Farbkonvertierung verwendet. Die Konvertierung eines naiven Typs wird verwendet, wenn kein Profil eingebettet ist und kein Standardeingabeprofil definiert ist.

Andere Materialdatendateien, z. B. Kabinettstildateien ( [!DNL .vnc]) oder Fensterabdeckungsdateien ( [!DNL .vnw]), betten keine Farbprofile ein und werden immer als im Arbeitsfarbraum befindlich angenommen.

## Ausgabe-Farbraum {#section-4c2c4dfedbb8429ba5cfddc3d3eab6c4}

Alle Render-Vorgänge finden im Arbeitsfarbraum statt. Wenn die Anfrage mit dem Befehl `icc=` ein anderes Farbprofil angibt, werden die Daten in diesen Farbraum konvertiert, unmittelbar bevor sie kodiert werden, und an den Client zurückgegeben. Wenn das Farbmanagement deaktiviert ist, wird bei Bedarf die naive Konvertierung verwendet, um in Graustufen oder CMYK zu konvertieren.

## Eingebettete Farbprofile {#section-5ff733832d38429fbe02b3c1e9bb94a9}

Das mit dem gerenderten Bild verknüpfte Farbprofil kann in das Antwortbild eingebettet werden, indem `iccEmbed=` für die Anfrage angegeben werden.

Wenn `icc=` nicht angegeben ist, wird das ICC-Profil für den Arbeitsfarbraum eingebettet. Wenn das Farbmanagement deaktiviert ist und bei `icc=` kein Profil angegeben wurde, wird kein Profil eingebettet.

## ICC-Profile {#section-afeb76068b5042adb83261638e450140}

Alle vom Server verwendeten Farbprofile müssen der ICC-Spezifikation entsprechen. ICC-Profildateien haben in der Regel die Dateiendung [!DNL .icc] oder [!DNL .icm] und befinden sich am selben Speicherort wie Materialdatendateien.

Zwar können Ausgabeprofile durch den Dateipfad/Dateinamen im Befehl `icc=` angegeben werden, doch wird empfohlen, alle Profildateien im ICC-Profilplan des Standardkatalogs oder eines bestimmten Materialkatalogs zu registrieren und Tastaturbefehle (`icc::Name`) anstelle von Dateipfaden zu verwenden.

Arbeitsprofile müssen in der ICC-Profilkarte des Materialkatalogs oder des Standardkatalogs registriert werden.
