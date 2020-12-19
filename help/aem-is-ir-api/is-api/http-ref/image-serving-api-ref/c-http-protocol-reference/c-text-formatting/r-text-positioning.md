---
description: Der text=-Renderer positioniert Text grundlegend anders als der textPs=-Renderer, wenn er auf Ebenen mit vordefinierter Größe angewendet wird (d. h. auch bei Angabe von size=).
seo-description: Der text=-Renderer positioniert Text grundlegend anders als der textPs=-Renderer, wenn er auf Ebenen mit vordefinierter Größe angewendet wird (d. h. auch bei Angabe von size=).
seo-title: Textpositionierung
solution: Experience Manager
title: Textpositionierung
topic: Scene7 Image Serving - Image Rendering API
uuid: 77289c50-2f3a-4486-8274-eecfd6e5452f
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '300'
ht-degree: 0%

---


# Textpositionierung{#text-positioning}

Der text=-Renderer positioniert Text grundlegend anders als der textPs=-Renderer, wenn er auf Ebenen mit vordefinierter Größe angewendet wird (d. h. auch bei Angabe von size=).

Die Ebenen `text=`und `textPs=` mit der Selbstgrößenänderung haben ein ähnliches Aussehen und eine ähnliche Positionierung.

`textPs=` Richtet den oberen Rand der Zeichenzelle am oberen Rand des Textfelds aus (unter der Annahme  `\vertalt`), auch wenn dies dazu führt, dass Teile der gerenderten Textzeichen teilweise über die Begrenzung des Textfelds hinausgehen. Gerenderte Schriftzeichen bestimmter Schriften können auch etwas über den linken und rechten Rand des Textfelds hinaus ragen. Für Anwendungen, bei denen der gesamte gerenderte Text im Ebenenrechteck enthalten sein muss, können die RTF-Befehle `\marg*` oder `textFlowPath=` verwendet werden, um den Text-Renderbereich anzupassen.

Im Gegensatz dazu verschiebt `text=` den gerenderten Text nach Bedarf und gewährleistet, dass alle gerenderten Glyphen vollständig in das angegebene Textfeld passen.

Auch wenn `text=` für einfache Anwendungen leicht einfacher zu verwenden ist, ist die genaue Positionierung von `textPs=`-Angeboten unabhängig von Schriftarten und Texteffekten möglich.

## Beispiele {#section-1b6bdf2ea34447528188ae4e1430ee71}

Die folgenden Beispiele beziehen sich auf Text in vordefinierter Größe. Das Verhalten von Text mit Selbstgrößenänderung ist anders.

** `Text=` bietet immer einen engen Rand oben:**

![](assets/tp01.png)

`/is/image/?size=230,50&bgc=f0f0f0&fmt=png&text=\fs40Normal%20Normal%20Normal`

** `textPs=` rendert Text eng am oberen Rand des Textfelds ausgerichtet. Dies kann zu einer leichten Beschneidung führen, selbst bei gängigen Schriftarten wie Arial:***

![](assets/tp02.png)

`/is/image/?size=230,50&bgc=f0f0f0&fmt=png&textPs=\fs40Normal%20Normal%20Normal`

** `text=` verschiebt den gerenderten Text automatisch nach unten, um eine Beschneidung zu vermeiden:**

![](assets/tp03.png)

`/is/image?size=230,50&bgc=f0f0f0&fmt=png&text=\fs40Normal%20{\up20Raised%20}Normal`

** `textPs=` verschiebt keinen Text, der erhöhte Teile enthält, was zu einer erheblichen Beschneidung führt, wenn sich der Text auf Ebene 0 befindet:**

![](assets/tp04.png)

`/is/image?size=230,50&bgc=f0f0f0&fmt=png&textPs=\fs40Normal%20{\up20Raised%20}Normal`

**Mit einem oberen Rand von 10 pt (200 Twips) wird dieser Text ohne Beschneiden gerendert:**

![](assets/tp05.png)

`/is/image?size=230,50&bgc=f0f0f0&fmt=png&textPs=\margt200\fs40Normal%20{\up20Raised}%20Normal`

**Gerenderte Glyphen bestimmter Skriptschriftarten können erheblich über das Textfeld hinausgehen:**

![](assets/tp06.png)

`/is/image?size=230,50&bgc=f0f0f0&fmt=png&textPs={\fonttbl{\f1\fcharset0%20FluffyFont;}}\f1\fs88%20fluffy%20font%20problems`
