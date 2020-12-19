---
description: textPs= unterstützt eine Reihe verschiedener Nutzungsmodelle, die in diesem Abschnitt beschrieben werden.
seo-description: textPs= unterstützt eine Reihe verschiedener Nutzungsmodelle, die in diesem Abschnitt beschrieben werden.
seo-title: Textebenen
solution: Experience Manager
title: Textebenen
topic: Scene7 Image Serving - Image Rendering API
uuid: 9ccef969-7c54-49ce-b6ff-ae4eabfcf99b
translation-type: tm+mt
source-git-commit: e8e5b07329bde3e23ee095d5022da62d67e9478c
workflow-type: tm+mt
source-wordcount: '900'
ht-degree: 0%

---


# Textebenen{#text-layers}

textPs= unterstützt eine Reihe verschiedener Nutzungsmodelle, die in diesem Abschnitt beschrieben werden.

>[!NOTE]
>
>Dieser Abschnitt gilt nicht für `text=`.

Die gemeinsamen Regeln und Definitionen lauten wie folgt:

* Selbstgrößenverändernde Textebenen sind Ebenen, die keinen Befehl `size=` enthalten oder für die `size=0,0` angegeben ist.

* Die Ebenengröße der Textebenen mit Selbstgrößenänderung wird vom tatsächlichen wiedergegebenen Text bestimmt.
* Der standardmäßige Ebenenanker für selbstgrößende Textebenen ist im Allgemeinen *nicht* in der Mitte der Ebene (siehe unten).
* Wenn `anchor=` oder `origin=` für die Selbstgrößenänderung von Textebenen angegeben ist, wird die Position der Textebene durch den Textinhalt beeinflusst.

* Wenn `size=` angegeben ist, können Teile von Zeichen-Glyphen außerhalb des Ebenenrechtecks gerendert werden.
* `pos=` kann in allen Fällen verwendet werden, um eine Textebene neu zu positionieren.

## Punkttext (Selbstgrößenänderung) {#section-db99ec98eb114458b2dbc9911a58f74a}

Punkttext im Photoshop-Stil wird simuliert, wenn `textPs=` ohne `size=`, `textPath=` oder `textFlowPath=` angegeben wird. Die Ebenengröße wird horizontal durch die Breite des gerenderten Textes und vertikal durch den Zeilenabstand bestimmt. Text wird nie automatisch umgebrochen.

Wenn weder `anchor=` noch `origin=` angegeben sind, wird die erste Textzeile direkt über der Herkunft der Ebene positioniert. Absätze, die mit `\ql` markiert sind, werden rechts von der Herkunft der Ebene positioniert, Absätze, die `\qr` enthalten, werden links von der Herkunft gerendert und Absätze mit `\qc` werden horizontal um die Herkunft zentriert. Wenn `anchor=` oder `origin=` angegeben sind, gelten Standardregeln für die Positionierung von Ebenen.

Wenn `color=` angegeben ist, füllt es den Begrenzungsrahmen des tatsächlichen wiedergegebenen Texts.

Die folgenden RTF-Befehle werden ignoriert: `\qj`, `\marg*`, `\hyph*`, `\vertal*`.

## Rechteckiges Textfeld {#section-1d3ab11df26d4004a1a801546756475d}

Wenn `size=` zusätzlich zu `textPs=` (ohne `textPath=` und `textFlowPath=`) angegeben ist, wird der Text auf das angegebene Rechteck beschränkt. Die Ebene wird wie gewohnt positioniert. Zeichen-Glyphen in der Nähe der Textrahmenkanten können teilweise außerhalb des Textfelds gerendert werden.

`color=` füllt den von  `size=`definierten Bereich.

Alle RTF-Befehle werden erwartungsgemäß angewendet.

## Textfeld mit variabler Höhe {#section-e1233d1c9f8e43218667361dc0c4fd06}

Wenn Sie `size=` mit 0 Höhe angeben, kann die Größe des Textfelds vertikal angepasst werden, um den gesamten Inhalt aufzunehmen. Die Ebenenbreite wird durch die Breite von `size=` und die Ebenenhöhe durch die Höhe des tatsächlichen gerenderten Textes definiert. Die Ebene wird wie gewohnt positioniert. Zeichen-Glyphen am linken und rechten Rand des Textfelds können teilweise außerhalb des Textfelds gerendert werden.

`color=` füllt das Rechteck, das durch die angegebene Breite  `size=` und Höhe des tatsächlichen wiedergegebenen Textes definiert wird.

Die folgenden RTF-Befehle werden ignoriert:

`\vertal*`

## Selbstgrößender Text im Pfad {#section-d26685e7085847efaaeba64b9cb5ed9f}

`textFlowPath=` in Verbindung mit  `textPs=` können Sie einen oder mehrere Bereiche definieren, in die Text fließen soll. `textFlowXPath=` kann optional angegeben werden, um den Textfluss in einen oder mehrere Bereiche auszuschließen. Wenn `size=` nicht angegeben ist, wird die resultierende Textebene von der eigenen Größe bestimmt und die Ebenengröße wird durch den Begrenzungsrahmen des tatsächlich gerenderten Textes bestimmt.

Wenn weder `origin=` noch `anchor=` angegeben sind, wird als Ebenenanker standardmäßig der Pixelkoordinatenraum (0,0) verwendet, der zum Definieren der Pfade verwendet wird (werden). Dadurch wird eine absolute Positionierung unabhängig vom gerenderten Text sichergestellt. Wenn `anchor=` oder `origin=` angegeben sind, wird die Ebene relativ zum Begrenzungsrahmen des tatsächlichen wiedergegebenen Inhalts positioniert (und an diesen angepasst).

`color=` füllt den Begrenzungsrahmen des tatsächlichen wiedergegebenen Texts.

Die folgenden RTF-Befehle werden ignoriert:

`\marg*`

## Vorformatierter Text im Pfad {#section-ed492a8a54414cd4bde360500cec6968}

Wenn `size=` zusammen mit `textFlowPath=` angegeben wird, wird die Ebenengröße vorab bestimmt. (0,0) Der Pixelkoordinatenraum, der zur Definition des Pfads verwendet wird, befindet sich in der oberen linken Ecke des Ebenenrechtecks.

Die Bereiche `textFlowPath=` befinden sich möglicherweise außerhalb des Ebenenrechtecks. Text wird immer fließend dargestellt und in alle Pfadbereiche gerendert, auch wenn dies dazu führt, dass Text außerhalb des Ebenenrechtecks wiedergegeben wird. `extend=0,0,0,0`kann verwendet werden, um den gerenderten Text auf das Ebenenrechteck zu beschneiden.

Bei der Positionierung der Ebene basiert das Rechteck der Ebene auf dem angegebenen `size=`, unabhängig davon, wie viel Text tatsächlich gerendert wird, auch wenn sich ein Teil des Rechtecks außerhalb der Ebene befindet. Es gilt die Standardpositionierung der Ebenen.

`color=` füllt den durch  `size=`definiert rechteckigen Bereich.

Die folgenden RTF-Befehle werden für `textFlowPath=` ignoriert:

`\marg*`

## Selbstgrößender Text auf Pfad {#section-7ce6b9b26b354ba381e4378703154062}

`textPath=` definiert einen oder mehrere Pfade, auf die der mit angegebene Text gerendert werden  `textPs=` soll. Wenn `size=` nicht angegeben ist, wird die resultierende Textebene selbst angepasst. Die Ebenengröße wird durch den Begrenzungsrahmen des tatsächlichen wiedergegebenen Texts bestimmt.

Wenn weder `origin=` noch `anchor=` angegeben sind, wird für den Ebenenanker standardmäßig der Pixelkoordinatenraum (0,0) verwendet, der zum Definieren des Pfads verwendet wird. Die Position des gerenderten Textes wird unabhängig von der Wiedergabemenge festgelegt. Wenn `anchor=` oder `origin=` angegeben sind, wird die Ebene relativ zum Begrenzungsrahmen des tatsächlichen wiedergegebenen Inhalts positioniert (und an diesen angepasst).

`color=` füllt den Begrenzungsrahmen des tatsächlichen wiedergegebenen Texts.

Die folgenden RTF-Befehle werden ignoriert:

* `\marg*`
* `\hyph*`
* `\vertal*`

Jeder Text nach dem ersten `\par` oder `\line` wird ignoriert.

## Vorformatierter Text auf Pfad {#section-a3bbbc5187f448b192e53d27e2c53f2f}

Wenn `size=` zusammen mit `textPath=` angegeben wird, wird die Ebenengröße vorab bestimmt. (0,0) Der Pixelkoordinatenraum, der zur Definition des Pfads verwendet wird, befindet sich in der oberen linken Ecke des Ebenenrechtecks.

Die Pfade können sich teilweise oder vollständig außerhalb des Ebenenrechtecks befinden. Text wird immer entlang des gesamten Pfads angewendet und gerendert, auch wenn er sich außerhalb des Ebenenrechtecks befindet. `extend=0,0,0,0` kann verwendet werden, um den gerenderten Text auf das Ebenenrechteck zu beschneiden.

Bei der Positionierung der Ebene basiert das Rechteck der Ebene auf dem angegebenen `size=`, auch wenn ein Teil des Textes außerhalb des Ebenenrechtecks wiedergegeben wird. Es gilt die Standardpositionierung der Ebenen.

`color=` füllt den durch  `size=`definiert Bereich.

Die folgenden RTF-Befehle werden ignoriert:

* `\marg*`
* `\q*`
* `\marg*`
* `\hyph*`
* `\vertal*`

Jeder Text nach dem ersten `\par` oder `\line` wird ignoriert.
