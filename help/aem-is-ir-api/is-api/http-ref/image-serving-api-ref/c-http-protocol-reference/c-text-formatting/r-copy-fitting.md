---
description: textPs= implementiert einen proprietären Kopiereinpassungsalgorithmus, der die Schriftgrößen automatisch anpasst, um den Textbereich optimal mit Text zu füllen, wodurch zusätzlicher Platz am unteren Rand minimiert und gleichzeitig ein Überlauf vermieden wird.
solution: Experience Manager
title: Nachrüstung
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: d1a560f3-f92c-4143-b80a-e1674c8a4207
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '511'
ht-degree: 0%

---

# Nachrüstung{#copy-fitting}

textPs= implementiert einen proprietären Kopiereinpassungsalgorithmus, der die Schriftgrößen automatisch anpasst, um den Textbereich optimal mit Text zu füllen, wodurch zusätzlicher Platz am unteren Rand minimiert und gleichzeitig ein Überlauf vermieden wird.

Die Kopieranpassung kann kollektiv für die gesamte Textebene aktiviert und gesteuert werden, auf Absatzbasis, auch für einen einzelnen Textbereich.

Geben Sie die Mindestschriftgröße mit `\fs` und die maximale Schriftgröße mit `\copyfit`. In derselben RTF-Zeichenfolge ist eine beliebige Anzahl von Bereichen zulässig. Die Größen für alle Bereiche werden proportional variiert, sodass das gewünschte Schriftgrößenverhältnis beibehalten wird.

`\copyfit` wird als Zeichenformatierungsbefehl betrachtet und enthält Bereichsregeln wie `\fs` und `\b`.

Die Nachbearbeitung wird durch Angabe von `\copyfit` mit einer Größe, die kleiner oder gleich der angegebenen Größe ist, mit `\fs`.

## Anzahl Zeilen begrenzen {#section-e5aee0f039e04842afc3d6884ed681ac}

Zusätzlich zur Angabe des Schriftgrößenbereichs kann das Verhalten des Kopiereinpassungsalgorithmus mit der `\copyfitlines` oder `\copyfitmaxlines` -Befehle, die die Anzahl der vom Algorithmus generierten Zeilen begrenzen. Beide Befehle akzeptieren einen Zeilenanzahl-Parameter oder 0, um die Anzahl der Zeilen im kopierten Bereich nicht zu begrenzen.

`\copyfitlines` ermöglicht den Überlauf von Text in zusätzliche Zeilen, wenn er nicht in die angegebene Anzahl von Zeilen passt. Explizite Zeilenumbrüche im Textsegment, das kopiert werden soll, werden immer berücksichtigt.

`\copyfitmaxlines` schneidet immer zusätzliche Ausgabezeilen ab, die den festgelegten Grenzwert überschreiten. Die angegebene Zeilenanzahl wird nicht überschritten, auch wenn explizite Zeilenumbrüche vorhanden sind. Für diese Version von Image Serving dürfen Sie maximal N-1 verwenden. `\line` -Markierungen können in der kopierten Textabdeckung vorhanden sein. Das Verhalten ist nicht definiert, wenn diese Grenze überschritten wird.

## Beispiele {#section-f4ddbbfade444560be30a813d90c2c1b}

In den folgenden Beispielen wird davon ausgegangen, dass Textkörper mit Variablen mit dem Namen *[!DNL $A$]*, *[!DNL $B$]*, und *[!DNL $C$]*.

**Behalten Sie das gleiche Verhältnis zwischen Schriftgrößen im gesamten Bereich bei:**

`{\fs10\copyfit100 $A${\fs20\copyfit200 $B$}$C$}`

*[!DNL $B$]* wird immer doppelt so groß wie der Rest des Textes gerendert. Wenn viel Text angegeben wird, *[!DNL $A$]* und *[!DNL $C$]* wird gerendert mit `\fs10` und *[!DNL $B$]* mit `\fs20`. Mit wenig Text *[!DNL $A$]* und *[!DNL $C$]* use `\fs100` und *[!DNL $B$]* `\fs200`.

**Wenn nur eine kleine Textmenge gezeichnet wird, wird die Schriftgröße in eine gemeinsame große Schriftgröße konvertiert:**

`{\copyfit100\fs10 $A${\fs20 $B$}$C$}`

Am kleinsten Ende des Bereichs *[!DNL $B$]* wird gerendert mit `\fs20`, doppelt so groß wie *[!DNL $A$]* und *[!DNL $C$]* at `\fs10`. Der gesamte Text wird unter `\fs100` (50 pt) am anderen Ende des Bereichs.

**Wenn viel Text gerendert werden soll, konvertieren Sie ihn in eine übliche kleine Schriftgröße:**

`{\fs10\copyfit100 $A${\copyfit200 $B$}$C$}`

Der gesamte Text wird am kleinen Ende des Bereichs mit \fs10 gezeichnet, während am größten, *[!DNL $A$]* und *[!DNL $C$]* werden mit `\fs100` und *[!DNL $B$]* mit `\fs200`.

**Deaktivieren Sie die Kopiereinfügung für einen inneren Textbereich:**

`{\fs10\copyfit100 $A${\fs50\copyfit0 $B$}$C$}`

Die Schriftgröße für *[!DNL $A$]* und *[!DNL $C$]* kann zwischen 10 und 100 variieren, während *[!DNL $B$]* wird immer mit gerendert `\fs50`.

**Begrenzen Sie die Ausgabe auf eine einzelne Zeile, selbst wenn mehr vertikaler Raum verfügbar ist. Sie können jedoch den Überlauf auf zusätzliche Zeilen zulassen, wenn zu viel Text angegeben ist, um in eine einzelne Zeile unter `\fs10`:**

`{\fs10\copyfit100 \copyfitlines1 $A$}`

**Beschränken Sie die Ausgabe auf eine einzelne Zeile, auch wenn mehr vertikaler Raum verfügbar ist. Wenn zu viel Text angegeben ist, um in eine einzelne Zeile unter `\fs10` abgeschnitten wird:**

`{\fs10\copyfit100 \copyfitmaxlines1 $A$}`
