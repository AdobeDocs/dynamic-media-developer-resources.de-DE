---
description: textPs= implementiert einen proprietären Kopiereinpassungsalgorithmus, der die Schriftgröße(n) automatisch anpassen wird, um den Textbereich optimal mit Text zu füllen, wodurch zusätzlicher Platz am unteren Rand minimiert wird und gleichzeitig ein Überlauf vermieden wird.
solution: Experience Manager
title: Nachrüstung
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: d1a560f3-f92c-4143-b80a-e1674c8a4207
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '528'
ht-degree: 0%

---

# Nachrüstung{#copy-fitting}

textPs= implementiert einen proprietären Kopiereinpassungsalgorithmus, der die Schriftgröße(n) automatisch anpassen wird, um den Textbereich optimal mit Text zu füllen, wodurch zusätzlicher Platz am unteren Rand minimiert wird und gleichzeitig ein Überlauf vermieden wird.

Die Kopieranpassung kann kollektiv für die gesamte Textebene aktiviert und gesteuert werden, auf Absatzbasis, auch für einen einzelnen Textbereich.

Geben Sie die minimale Schriftgröße mit `\fs` und die maximale Schriftgröße mit `\copyfit` an. In derselben RTF-Zeichenfolge ist eine beliebige Anzahl von Bereichen zulässig. Die Größen für alle Bereiche werden proportional variiert, sodass das gewünschte Schriftgrößenverhältnis beibehalten wird.

`\copyfit` wird als Zeichenformatierungsbefehl betrachtet und hat Bereichsregeln wie  `\fs` und  `\b`.

Die Kopieranpassung wird deaktiviert, indem `\copyfit` mit einer Größe angegeben wird, die der mit `\fs` angegebenen Größe entspricht oder kleiner ist.

## Anzahl Zeilen begrenzen {#section-e5aee0f039e04842afc3d6884ed681ac}

Zusätzlich zur Angabe des Schriftartbereichs kann das Verhalten des Kopiereinpassungsalgorithmus auch mit den Befehlen `\copyfitlines` oder `\copyfitmaxlines` weiter gesteuert werden, die die Anzahl der Zeilen begrenzen, die der Algorithmus generieren wird. Beide Befehle akzeptieren einen Zeilenanzahl-Parameter oder 0, um die Anzahl der Zeilen im kopierten Bereich nicht zu begrenzen.

`\copyfitlines` ermöglicht den Überlauf von Text in zusätzliche Zeilen, wenn er nicht in die angegebene Anzahl von Zeilen passt. Explizite Zeilenumbrüche im Textsegment, das kopiert werden soll, werden immer berücksichtigt.

`\copyfitmaxlines` schneidet immer zusätzliche Ausgabezeilen ab, die den festgelegten Grenzwert überschreiten. Die angegebene Zeilenanzahl wird nicht überschritten, auch wenn explizite Zeilenumbrüche vorhanden sind. Für diese Version von Image Serving dürfen in der kopierangepassten Textspanne maximal N-1 `\line` Markierungen vorhanden sein. Das Verhalten ist nicht definiert, wenn diese Grenze überschritten wird.

## Beispiele {#section-f4ddbbfade444560be30a813d90c2c1b}

In den folgenden Beispielen wird davon ausgegangen, dass Textkörper mit Variablen namens *[!DNL $A$]*, *[!DNL $B$]* und *[!DNL $C$]* bereitgestellt werden.

**Behalten Sie das gleiche Verhältnis zwischen Schriftgrößen im gesamten Bereich bei:**

`{\fs10\copyfit100 $A${\fs20\copyfit200 $B$}$C$}`

*[!DNL $B$]* wird immer doppelt so groß wie der Rest des Textes gerendert. Wenn viel Text angegeben ist, werden *[!DNL $A$]* und *[!DNL $C$]* mit `\fs10` und *[!DNL $B$]* mit `\fs20` gerendert. Mit wenig Text verwenden *[!DNL $A$]* und *[!DNL $C$]* `\fs100` und *[!DNL $B$]* `\fs200`.

**Wenn nur eine kleine Textmenge gezeichnet wird, wird die Schriftgröße in eine gemeinsame große Schriftgröße konvertiert:**

`{\copyfit100\fs10 $A${\fs20 $B$}$C$}`

Am kleinsten Ende des Bereichs wird *[!DNL $B$]* mit `\fs20`, zweimal so groß wie *[!DNL $A$]* und *[!DNL $C$]* unter `\fs10` gerendert. Der gesamte Text wird an `\fs100` (50 Pkt.) am anderen Ende des Bereichs gezeichnet.

**Wenn viel Text gerendert werden soll, konvertieren Sie ihn in eine übliche kleine Schriftgröße:**

`{\fs10\copyfit100 $A${\copyfit200 $B$}$C$}`

Der gesamte Text wird mit \fs10 am kleinen Ende des Bereichs gezeichnet, während am größten *[!DNL $A$]* und *[!DNL $C$]* mit `\fs100` und *[!DNL $B$]* mit `\fs200` gerendert werden.

**Deaktivieren Sie die Kopiereinfügung für einen inneren Textbereich:**

`{\fs10\copyfit100 $A${\fs50\copyfit0 $B$}$C$}`

Die Schriftgröße für *[!DNL $A$]* und *[!DNL $C$]* kann zwischen 10 und 100 variieren, während *[!DNL $B$]* immer mit `\fs50` gerendert wird.

**Begrenzen Sie die Ausgabe auf eine einzelne Zeile, selbst wenn mehr vertikaler Raum verfügbar ist, überlaufen Sie jedoch zusätzliche Zeilen, wenn zu viel Text angegeben ist, um in eine einzelne Zeile zu passen  `\fs10`:**

`{\fs10\copyfit100 \copyfitlines1 $A$}`

**Beschränken Sie die Ausgabe auf eine einzelne Zeile, auch wenn mehr vertikaler Raum verfügbar ist. Wenn zu viel Text angegeben ist, um in eine einzelne Zeile unter `\fs10` zu passen, wird er abgeschnitten:**

`{\fs10\copyfit100 \copyfitmaxlines1 $A$}`
