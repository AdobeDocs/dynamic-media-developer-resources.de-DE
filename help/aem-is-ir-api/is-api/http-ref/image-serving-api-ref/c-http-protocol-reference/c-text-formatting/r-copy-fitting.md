---
description: textPs= implementiert einen proprietären Einpassungsalgorithmus, der die Schriftgrößen automatisch so anpasst, dass der Textbereich optimal mit Text gefüllt wird. Dadurch wird zusätzlicher Platz am unteren Rand minimiert und ein Überlauf vermieden.
solution: Experience Manager
title: Einpassung
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: d1a560f3-f92c-4143-b80a-e1674c8a4207
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '516'
ht-degree: 0%

---

# Einpassung{#copy-fitting}

textPs= implementiert einen proprietären Einpassungsalgorithmus, der die Schriftgrößen automatisch so anpasst, dass der Textbereich optimal mit Text gefüllt wird. Dadurch wird zusätzlicher Platz am unteren Rand minimiert und ein Überlauf vermieden.

Das Kopieren kann für die gesamte Textebene gemeinsam auf Absatzbasis aktiviert und gesteuert werden, auch für einen einzelnen Textbereich.

Legen Sie mit `\fs` die minimale und mit `\copyfit` die maximale Schriftgröße fest. In derselben RTF-Zeichenfolge sind beliebig viele Bereiche zulässig. Die Größen für alle Bereiche werden proportional variiert, sodass die gewünschten Schriftgrößenverhältnisse erhalten bleiben.

`\copyfit` gilt als Zeichenformatierungsbefehl und verfügt über Bereichsregeln wie `\fs` und `\b`.

Das Kopieren-Fitting wird deaktiviert, indem `\copyfit` mit einer Größe angegeben werden, die gleich oder kleiner der mit `\fs` angegebenen Größe ist.

## Anzahl der Zeilen begrenzen {#section-e5aee0f039e04842afc3d6884ed681ac}

Neben der Angabe des Bereichs der Schriftgrößen kann das Verhalten des Kopiereinpassalgorithmus mit den `\copyfitlines`- oder `\copyfitmaxlines`-Befehlen, die die Anzahl der Zeilen begrenzen, die der Algorithmus erzeugt, weiter gesteuert werden. Beide Befehle akzeptieren einen Zeilenanzahl-Parameter oder 0, um die Anzahl der Zeilen im kopierangepassten Bereich nicht zu begrenzen.

`\copyfitlines` kann Text in zusätzliche Zeilen überlaufen werden, wenn er nicht in die angegebene Anzahl von Zeilen passt. Explizite Zeilenumbrüche im zu kopierenden Textsegment werden immer berücksichtigt.

`\copyfitmaxlines` kürzt immer die zusätzlichen Ausgabeleitungen, die den festgelegten Grenzwert überschreiten. Die angegebene Anzahl von Zeilen wird nie überschritten, auch wenn explizite Zeilenumbrüche vorhanden sind. Für diese Version von Image Serving dürfen nicht mehr als N-1 `\line` in der kopierangepassten Textspanne vorhanden sein. Das Verhalten ist undefiniert, wenn dieses Limit überschritten wird.

## Beispiele {#section-f4ddbbfade444560be30a813d90c2c1b}

Bei den folgenden Beispielen wird davon ausgegangen, dass Textkörper mit Variablen namens *[!DNL $A$]*, *[!DNL $B$]* und *[!DNL $C$]* bereitgestellt werden.

**Beibehaltung des Verhältnisses zwischen den Schriftgrößen im gesamten Bereich:**

`{\fs10\copyfit100 $A${\fs20\copyfit200 $B$}$C$}`

*[!DNL $B$]* wird immer doppelt so groß gerendert wie der Rest des Textes. Wenn ein großer Teil des Texts angegeben wird, werden *[!DNL $A$]* und *[!DNL $C$]* mit `\fs10` und *[!DNL $B$]* mit `\fs20` gerendert. Mit wenig Text verwenden *[!DNL $A$]* und *[!DNL $C$]* `\fs100` und *[!DNL $B$]* `\fs200`.

**Konvertieren Sie zu einer gemeinsamen großen Schriftgröße, wenn nur eine kleine Menge Text gezeichnet wird:**

`{\copyfit100\fs10 $A${\fs20 $B$}$C$}`

Am kleinsten Ende des Bereichs wird *[!DNL $B$]* mit `\fs20` gerendert, die doppelt so groß wie *[!DNL $A$]* sind und `\fs10` *[!DNL $C$]*. Der gesamte Text wird am gegenüberliegenden Ende des Bereichs in `\fs100` (50 Punkte) gezeichnet.

**Konvertieren Sie in eine gemeinsame kleine Schriftgröße, wenn ein großer Teil des Textes gerendert werden soll:**

`{\fs10\copyfit100 $A${\copyfit200 $B$}$C$}`

Der gesamte Text wird mit \fs10 am kleinen Ende des Bereichs gezeichnet, während in seiner größten Position *[!DNL $A$]* und *[!DNL $C$]* mit `\fs100` und *[!DNL $B$]* mit `\fs200` gerendert werden.

**Kopieranpassung für einen inneren Textbereich deaktivieren:**

`{\fs10\copyfit100 $A${\fs50\copyfit0 $B$}$C$}`

Die Schriftgröße für *[!DNL $A$]* und *[!DNL $C$]* kann zwischen 10 und 100 variieren, während *[!DNL $B$]* immer mit `\fs50` gerendert wird.

**Begrenzen Sie die Ausgabe auf eine einzelne Zeile, auch wenn mehr vertikaler Abstand verfügbar ist. Lassen Sie sie jedoch auf zusätzliche Zeilen überlaufen, wenn zu viel Text angegeben wurde, um in eine einzelne Zeile zu passen: `\fs10`:**

`{\fs10\copyfit100 \copyfitlines1 $A$}`

**Begrenzen Sie die Ausgabe auf eine Zeile, auch wenn mehr vertikaler Abstand verfügbar ist. Wenn zu viel Text angegeben wird, um in eine einzelne Zeile an `\fs10` zu passen, wird er abgeschnitten:**

`{\fs10\copyfit100 \copyfitmaxlines1 $A$}`
