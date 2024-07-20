---
description: textPs= implementiert einen proprietären Kopiereinpassungsalgorithmus, der die Schriftgrößen automatisch anpasst, um den Textbereich optimal mit Text zu füllen, wodurch zusätzlicher Platz am unteren Rand minimiert und gleichzeitig ein Überlauf vermieden wird.
solution: Experience Manager
title: Nachrüstung
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: d1a560f3-f92c-4143-b80a-e1674c8a4207
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '516'
ht-degree: 0%

---

# Nachrüstung{#copy-fitting}

textPs= implementiert einen proprietären Kopiereinpassungsalgorithmus, der die Schriftgrößen automatisch anpasst, um den Textbereich optimal mit Text zu füllen, wodurch zusätzlicher Platz am unteren Rand minimiert und gleichzeitig ein Überlauf vermieden wird.

Die Kopieranpassung kann kollektiv für die gesamte Textebene aktiviert und gesteuert werden, auf Absatzbasis, auch für einen einzelnen Textbereich.

Geben Sie die minimale Schriftgröße mit `\fs` und die maximale Schriftgröße mit `\copyfit` an. In derselben RTF-Zeichenfolge ist eine beliebige Anzahl von Bereichen zulässig. Die Größen für alle Bereiche werden proportional variiert, sodass das gewünschte Schriftgrößenverhältnis beibehalten wird.

`\copyfit` wird als Zeichenformatierungsbefehl betrachtet und enthält Bereichsregeln wie `\fs` und `\b`.

Die Kopieranpassung wird deaktiviert, indem `\copyfit` mit einer Größe angegeben wird, die der mit `\fs` angegebenen Größe entspricht oder kleiner ist.

## Anzahl Zeilen begrenzen {#section-e5aee0f039e04842afc3d6884ed681ac}

Zusätzlich zur Angabe des Schriftgrößenbereichs kann das Verhalten des Kopiereinpassungsalgorithmus auch mit den Befehlen `\copyfitlines` oder `\copyfitmaxlines` weiter gesteuert werden, wodurch die Anzahl der vom Algorithmus generierten Zeilen begrenzt wird. Beide Befehle akzeptieren einen Zeilenanzahl-Parameter oder 0, um die Anzahl der Zeilen im kopierten Bereich nicht zu begrenzen.

Mit `\copyfitlines` kann Text in zusätzliche Zeilen überlaufen werden, wenn er nicht in die angegebene Anzahl von Zeilen passt. Explizite Zeilenumbrüche im Textsegment, das kopiert werden soll, werden immer berücksichtigt.

`\copyfitmaxlines` schneidet immer zusätzliche Ausgabezeilen ab, die die angegebene Grenze überschreiten. Die angegebene Zeilenanzahl wird nicht überschritten, auch wenn explizite Zeilenumbrüche vorhanden sind. Für diese Version von Image Serving dürfen in der kopierten Textspanne maximal N-1 `\line` -Markierungen vorhanden sein. Das Verhalten ist nicht definiert, wenn diese Grenze überschritten wird.

## Beispiele {#section-f4ddbbfade444560be30a813d90c2c1b}

In den folgenden Beispielen wird davon ausgegangen, dass Textkörper mit Variablen mit den Namen *[!DNL $A$]*, *[!DNL $B$]* und *[!DNL $C$]* versehen sind.

**Behalten Sie das gleiche Verhältnis zwischen Schriftgrößen im gesamten Bereich bei:**

`{\fs10\copyfit100 $A${\fs20\copyfit200 $B$}$C$}`

*[!DNL $B$]* wird immer doppelt so groß wie der Rest des Textes gerendert. Wenn viel Text angegeben ist, werden *[!DNL $A$]* und *[!DNL $C$]* mit `\fs10` und *[!DNL $B$]* mit `\fs20` gerendert. Mit wenig Text verwenden *[!DNL $A$]* und *[!DNL $C$]* `\fs100` und *[!DNL $B$]* `\fs200`.

**Konvertieren Sie in eine gemeinsame große Schriftgröße, wenn nur eine kleine Textmenge gezeichnet wird:**

`{\copyfit100\fs10 $A${\fs20 $B$}$C$}`

Am kleinsten Ende des Bereichs wird *[!DNL $B$]* mit `\fs20` gerendert, was doppelt so groß wie *[!DNL $A$]* und *[!DNL $C$]* bei `\fs10` ist. Der gesamte Text wird bei `\fs100` (50 pt) am anderen Ende des Bereichs gezeichnet.

**Konvertieren Sie in eine übliche kleine Schriftgröße, wenn viel Text gerendert werden soll:**

`{\fs10\copyfit100 $A${\copyfit200 $B$}$C$}`

Der gesamte Text wird mit \fs10 am kleinen Ende des Bereichs gezeichnet, während am größten *[!DNL $A$]* und *[!DNL $C$]* mit `\fs100` und *[!DNL $B$]* mit `\fs200` gerendert werden.

**Deaktivieren der Kopiereinfügung für einen inneren Textbereich:**

`{\fs10\copyfit100 $A${\fs50\copyfit0 $B$}$C$}`

Die Schriftgröße für *[!DNL $A$]* und *[!DNL $C$]* kann zwischen 10 und 100 variieren, während *[!DNL $B$]* immer mit `\fs50` gerendert wird.

**Begrenzen Sie die Ausgabe auf eine einzelne Zeile, selbst wenn mehr vertikaler Raum verfügbar ist, lassen Sie jedoch zu, dass die Ausgabe auf zusätzliche Zeilen überläuft, wenn zu viel Text für eine einzelne Zeile bei `\fs10`:** angegeben ist.

`{\fs10\copyfit100 \copyfitlines1 $A$}`

**Begrenzen Sie die Ausgabe auf eine einzelne Zeile, selbst wenn mehr vertikaler Raum verfügbar ist. Wenn zu viel Text angegeben ist, um in eine einzelne Zeile bei `\fs10` zu passen, wird er abgeschnitten:**

`{\fs10\copyfit100 \copyfitmaxlines1 $A$}`
