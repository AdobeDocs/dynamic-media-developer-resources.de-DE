---
description: Image Rendering unterstützt Farbraumkonvertierungen auf der Grundlage von Farbraum-Profilen, die der ICC-Spezifikation (International Color Consortium) entsprechen.
seo-description: Image Rendering unterstützt Farbraumkonvertierungen auf der Grundlage von Farbraum-Profilen, die der ICC-Spezifikation (International Color Consortium) entsprechen.
seo-title: Image Rendering-Farbmanagement *
solution: Experience Manager
title: Image Rendering-Farbmanagement *
topic: Scene7 Image Serving - Image Rendering API
uuid: 9c47f584-645f-4eb7-bdc0-fdef459da3b2
translation-type: tm+mt
source-git-commit: b27327f940202b1883a654702aa386c7ae83c856

---


# Image Rendering-Farbmanagement *{#image-rendering-color-management}

Image Rendering unterstützt Farbraumkonvertierungen auf der Grundlage von Farbraum-Profilen, die der ICC-Spezifikation (International Color Consortium) entsprechen.

**Einschränkungen**

Derzeit werden nur CMYK-, RGB- und Graustufen-Farbräume unterstützt.

Mögliche Dateien im Möbelstil (.vnc) und im Fensterstil (. [!DNL .vnw]) werden nicht farbverwaltet und werden im Arbeitsfarbraum als vorhanden angesehen.

**Verwandte Themen**

[International Color Consortium](http://www.color.org/index.xalter) , [ , `icc=`](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-icc.md#reference-86a2fff3cef24982ad2063d977a16e06) , [ , `iccEmbed=`](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-iccembed.md#reference-47a433138c7c4b29b9b29871b2491a7f) , `attribute::IccProfile*` , `attribute::IccProfileSrc*`, `attribute::IccRenderIntent` `attribute::IccBlackPointCompensation` `attribute::IccDither` , ICC Profil Maps

## Standardfarbräume {#section-8ce27edf42e746febe4654f8f19b9c0c}

Jeder Bildkatalog (und der Standardkatalog) kann eine Reihe von ICC-Profilen definieren. Diese Profile stellen die Standardfarbräume für diesen Katalog dar - ein Eingabe- und ein Ausgabeformat-Profil jeweils für Graustufen-, RGB- und CMYK-Daten ( `attribute::IccProfileRgb`, `attribute::IccProfileGray`, `attribute::IccProfileCmyk`, `attribute::IccProfileSrcRgb`, `attribute::IccProfileSrcGray`und `attribute::IccProfileSrcCmyk`).

Der Standardfarbraum für ein bestimmtes Bild oder ein anderes Objekt wird aus den Standardkatalog-Profilen basierend auf dem Pixeltyp des Bilds ausgewählt.

## Eingabefarbraum {#section-660f661a7e954df4b451e34134195276}

Materialbilder können ICC-Profile einbetten, um den Eingabefarbraum zu definieren. Wenn kein Profil in ein Quellbild eingebettet ist, wird `attribute::IccProfileSrc*` der entsprechende Bildkatalog, der dem Pixeltyp des Quellbilds entspricht, verwendet. Wenn dieses Attribut nicht im Bildkatalog definiert ist, wird es verwendet `attribute::IccProfile*` . Wenn auch dieses Katalogattribut nicht definiert ist, wird das Bild nicht farbverwaltet und es werden nur naive Transformationen angewendet.

## Arbeitsfarbraum {#section-645d9cfa5b0347a190a0ece218f5b5e1}

Normalerweise wird der Arbeitsfarbraum durch das in die Vignette eingebettete ICC-Profil definiert. Wenn die Vignette kein Profil enthält, wird für den Arbeitsfarbraum das standardmäßige RGB-Eingabefeld (&quot;RGB-Profil&quot; `attribute::IccProfileSrcRgb` des Sitzungskatalogs) verwendet.

Alle Render-Vorgänge werden im Arbeitsfarbraum ausgeführt.

**Wichtig:** Das ICC-Profil für den Arbeitsfarbraum muss Eingangs- und Ausgangstransformationen unterstützen. Wenn ein ausgangsgeschütztes Profil als Arbeitsfarbraum verwendet wird, ist IR nicht in der Lage, Materialien zu konvertieren. Ein solches Profil kann auch dann verwendet werden, wenn die Materialien im gleichen Arbeitsfarbraum vorhanden sind. Der Versuch, Materialien in anderen Farbräumen anzuwenden, schlägt fehl.

## Explizite Farbwerte {#section-31727bf1b23e477ca92572fbbf422d2f}

RGB-Farbwerte, die mit `color=`, `bgc=`, `catalog::BgColor`und `catalog::Color` angegeben wurden, werden im aktuellen Arbeitsfarbraum als vorhanden angenommen.

## Materialdatendateien {#section-33f7a170a6664c02b8479fb89cc0aea3}

Materialbilddateien (Textur- und Dezimalbilder) können den Pixeltyp RGB, Graustufen oder CMYK aufweisen und ein Profil einbetten. Wenn kein Profil eingebettet ist, wird der Standardfarbraum für die Eingabe mit dem Bild verknüpft (z. B. das Profil für die Farbe aus dem Materialkatalog, das dem Pixeltyp des Bilds entspricht).

Materialbilder, die aus verschachtelten Image Serving- oder Image Rendering-Anforderungen stammen, enthalten in der Regel ein Profil. Ist dies nicht der Fall, werden die Bilder mit dem Standardfarbraum für die Eingabe verknüpft, der dem Pixeltyp entspricht.

Wenn der Farbraum der Bilddatei sich vom Arbeitsfarbraum unterscheidet, wird eine genaue Farbkonvertierung verwendet, um in den Arbeitsfarbraum zu konvertieren. Eine naïve Typkonvertierung wird verwendet, wenn kein Profil eingebettet ist und kein standardmäßiges Eingabe-Profil definiert ist.

Andere Materialdatendateien, wie z. B. Möbeldateien ( [!DNL .vnc]) oder Fensterbedeckungsdateien ( [!DNL .vnw]), betten keine Profile ein und werden immer als Arbeitsfarbraum betrachtet.

## Ausgabefarbraum {#section-4c2c4dfedbb8429ba5cfddc3d3eab6c4}

Alle Render-Vorgänge finden im Arbeitsfarbraum statt. Wenn die Anforderung mit dem `icc=` Befehl ein anderes Profil angibt, werden die Daten in diesen Farbraum konvertiert, bevor sie kodiert werden, und an den Client zurückgegeben. Wenn das Farbmanagement deaktiviert ist, wird bei Bedarf naive Konvertierung verwendet, um in Graustufen oder CMYK umzuwandeln.

## Eingebettete Profile {#section-5ff733832d38429fbe02b3c1e9bb94a9}

Das mit dem gerenderten Profil verknüpfte Farbbild kann durch Angabe `iccEmbed=` der Anforderung in das Antwortbild eingebettet werden.

Wenn kein Wert angegeben `icc=` ist, wird das ICC-Profil für den Arbeitsfarbraum eingebettet. Es wird kein Profil eingebettet, wenn das Farbmanagement deaktiviert ist und kein Profil mit angegeben wurde `icc=`.

## ICC-Profile {#section-afeb76068b5042adb83261638e450140}

Alle vom Server verwendeten Profil müssen der ICC-Spezifikation entsprechen. ICC-Profil-Dateien haben in der Regel ein Suffix [!DNL .icc] oder eine [!DNL .icm] -Datei und befinden sich zusammen mit den Materialdatendateien.

Es wird empfohlen, alle Profil-Profile in der ICC-Profil-Map des Standardkatalogs oder eines bestimmten Materialkatalogs zu registrieren und anstelle von Dateipfaden Verknüpfungs-IDs ( `icc=` `icc::Name`) zu verwenden.

Die Profile müssen in der ICC-Profil-Map des Materialkatalogs oder im Standardkatalog registriert sein.
