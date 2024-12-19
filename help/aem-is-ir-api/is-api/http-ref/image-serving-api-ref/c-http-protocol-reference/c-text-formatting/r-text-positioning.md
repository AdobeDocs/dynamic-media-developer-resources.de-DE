---
title: Textpositionierung
description: Der Text=-Renderer positioniert Text grundlegend anders als der TextPs=-Renderer, wenn er auf Ebenen mit vorab festgelegter Größe angewendet wird (d. h. wenn auch Größe= festgelegt ist).
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 092444bf-9964-4d97-b06e-3add033da284
source-git-commit: 67e12fae514341137e4218ea950f34da0d9997f3
workflow-type: tm+mt
source-wordcount: '306'
ht-degree: 0%

---

# Textpositionierung{#text-positioning}

Der `text=`-Renderer positioniert Text grundlegend anders als der textPs=-Renderer, wenn er auf Ebenen mit vorab festgelegter Größe angewendet wird (d. h. wenn auch Größe= festgelegt ist).

Selbstdimensionierende `text=`- und `textPs=` weisen ein ähnliches Erscheinungsbild und eine ähnliche Positionierung auf.

Der `textPs=` richtet die Oberseite der Zeichenzelle an der Oberseite des Textfelds aus (unter der Annahme von `\vertalt`), auch wenn dies dazu führt, dass sich Teile der gerenderten Textsymbole teilweise außerhalb der Begrenzung des Textfelds erstrecken. Gerenderte Symbole bestimmter Schriftarten können auch leicht über die linken und rechten Ränder des Textfelds hinausragen. Für Anwendungen, bei denen der gesamte gerenderte Text im Ebenenrechteck enthalten sein muss, können die RTF-`\marg*` oder -`textFlowPath=` verwendet werden, um den Textrenderbereich anzupassen.

Im Gegensatz dazu verschiebt `text=` den gerenderten Text nach Bedarf und stellt sicher, dass alle gerenderten Symbole vollständig in das angegebene Textfeld passen.

Während `text=` für einfache Anwendungen etwas einfacher zu bedienen sein mag, bietet `textPs=` eine genaue Positionierung unabhängig von Schriftflächen und Texteffekten.

## Beispiele {#section-1b6bdf2ea34447528188ae4e1430ee71}

Die folgenden Beispiele sind für Text in vorab festgelegter Größe. Das Verhalten bei der Größenanpassung von Text ist anders.

** `Text=` bietet immer einen schmalen Rand oben:**

![Beispiel für Textpositionierung mit einem Bild](assets/tp01.png)

`/is/image/?size=230,50&bgc=f0f0f0&fmt=png&text=\fs40Normal%20Normal%20Normal`

** `textPs=` rendert Text eng am oberen Rand des Textfelds, was zu einem leichten Abschneiden führt, selbst für gängige Schriftarten wie Arial®:**

![Beispiel für Textpositionierung, Bild zwei](assets/tp02.png)

`/is/image/?size=230,50&bgc=f0f0f0&fmt=png&textPs=\fs40Normal%20Normal%20Normal`

** `text=` verschiebt gerenderten Text automatisch nach unten, um das Zuschneiden zu vermeiden:**

![Beispiel für Textpositionierung - drei Bilder](assets/tp03.png)

`/is/image?size=230,50&bgc=f0f0f0&fmt=png&text=\fs40Normal%20{\up20Raised%20}Normal`

** `textPs=` verschiebt keinen Text mit erhabenen Bereichen, was zu einem erheblichen Zuschnitt führt, wenn der Text auf Ebene 0:** liegt

![Beispiel für Textpositionierung - vier Bilder](assets/tp04.png)

`/is/image?size=230,50&bgc=f0f0f0&fmt=png&textPs=\fs40Normal%20{\up20Raised%20}Normal`

**Ein Rand von 10 pt (200 Twips) oben rendert diesen Text ohne Beschneidung:**

![Beispiel für Textpositionierung - fünf Bilder](assets/tp05.png)

`/is/image?size=230,50&bgc=f0f0f0&fmt=png&textPs=\margt200\fs40Normal%20{\up20Raised}%20Normal`

**Gerenderte Glyphen bestimmter Skriptschriftarten können sich erheblich über das Textfeld hinaus erstrecken:**

![Beispiel für Textpositionierung, sechs Bilder](assets/tp06.png)

`/is/image?size=230,50&bgc=f0f0f0&fmt=png&textPs={\fonttbl{\f1\fcharset0%20FluffyFont;}}\f1\fs88%20fluffy%20font%20problems`
