---
title: Textpositionierung
description: Der Renderer text= positioniert Text grundlegend anders als der Renderer textPs= , wenn er auf Ebenen mit vordefinierter Größe angewendet wird (d. h. wenn auch size= angegeben wird).
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 092444bf-9964-4d97-b06e-3add033da284
source-git-commit: 24667a5ebab54ba22c4a3f6b52d19d7a31a93576
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# Textpositionierung{#text-positioning}

Der Renderer `text=` positioniert Text grundlegend anders als der Renderer textPs= , wenn er auf Ebenen mit vordefinierter Größe angewendet wird (d. h. wenn auch size= angegeben wird).

Die Ebenen `text=`und `textPs=`, die sich selbst anpassen, weisen ein ähnliches Erscheinungsbild und eine ähnliche Positionierung auf.

Der `textPs=` richtet den oberen Rand der Zeichenzelle am Anfang des Textfelds aus (unter Annahme von `\vertalt`), selbst wenn dadurch Teile der gerenderten Textzeichen teilweise außerhalb der Textfeldgrenze liegen. Gerenderte Glyphen bestimmter Schriftarten können auch geringfügig über die linke und rechte Kante des Textfelds hinausragen. Bei Anwendungen, bei denen der gesamte gerenderte Text im Ebenenrechteck enthalten sein muss, können die RTF-Befehle `\marg*` oder `textFlowPath=` verwendet werden, um den Textwiedergabebereich anzupassen.

Im Gegensatz dazu verschiebt `text=` den gerenderten Text nach Bedarf und gewährleistet, dass alle gerenderten Glyphen vollständig in das angegebene Textfeld passen.

`text=` ist zwar für einfache Anwendungen etwas einfacher zu verwenden, `textPs=` bietet jedoch eine genaue Positionierung, unabhängig von Schriftflächen und Texteffekten.

## Beispiele {#section-1b6bdf2ea34447528188ae4e1430ee71}

Die folgenden Beispiele beziehen sich auf vorformatierten Text. Das Verhalten bei der selbstdimensionierten Textgröße unterscheidet sich.

** `Text=` bietet immer einen schmalen Rand oben:**

![Textpositionierungsbeispiel für ein Bild](assets/tp01.png)

`/is/image/?size=230,50&bgc=f0f0f0&fmt=png&text=\fs40Normal%20Normal%20Normal`

** `textPs=` rendert Text eng am oberen Rand des Textfelds ausgerichtet, was zu einer leichten Beschneidung führt, selbst bei gängigen Schriftarten wie Arial®:**

![Textpositionierung Beispiel für zwei Bilder](assets/tp02.png)

`/is/image/?size=230,50&bgc=f0f0f0&fmt=png&textPs=\fs40Normal%20Normal%20Normal`

** `text=` verschiebt den gerenderten Text automatisch nach unten, um das Beschneiden zu vermeiden:**

![Textpositionierungsbeispiel für drei Bilder](assets/tp03.png)

`/is/image?size=230,50&bgc=f0f0f0&fmt=png&text=\fs40Normal%20{\up20Raised%20}Normal`

** `textPs=` verschiebt keinen Text, der erhöhte Teile enthält, was zu einer erheblichen Beschneidung führt, wenn sich der Text auf Ebene 0 befindet:**

![Textpositionierung Beispiel für vier Bilder](assets/tp04.png)

`/is/image?size=230,50&bgc=f0f0f0&fmt=png&textPs=\fs40Normal%20{\up20Raised%20}Normal`

**Ein Ränder von 10 pt (200 Twips) oben rendert diesen Text ohne Beschneiden:**

![Textpositionierungsbeispiel für fünf Bilder](assets/tp05.png)

`/is/image?size=230,50&bgc=f0f0f0&fmt=png&textPs=\margt200\fs40Normal%20{\up20Raised}%20Normal`

**Gerenderte Glyphen bestimmter Skriptschriftarten können sich deutlich außerhalb des Textfelds erstrecken:**

![Textpositionierungsbeispiel sechs Bild](assets/tp06.png)

`/is/image?size=230,50&bgc=f0f0f0&fmt=png&textPs={\fonttbl{\f1\fcharset0%20FluffyFont;}}\f1\fs88%20fluffy%20font%20problems`
