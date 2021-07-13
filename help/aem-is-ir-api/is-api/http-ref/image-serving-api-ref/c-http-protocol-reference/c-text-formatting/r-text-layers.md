---
description: textPs= unterstützt eine Reihe verschiedener Nutzungsmodelle, die in diesem Abschnitt beschrieben werden.
solution: Experience Manager
title: Textebenen
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 6793eb7d-6c10-4136-b6d4-186a698a8e52
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '891'
ht-degree: 0%

---

# Textebenen{#text-layers}

textPs= unterstützt eine Reihe verschiedener Nutzungsmodelle, die in diesem Abschnitt beschrieben werden.

>[!NOTE]
>
>Dieser Abschnitt gilt nicht für `text=`.

Die gemeinsamen Regeln und Definitionen lauten wie folgt:

* Selbstdimensionierende Textebenen sind Ebenen, die keinen `size=`-Befehl enthalten oder für die `size=0,0` angegeben ist.

* Die Ebenengröße von selbstskalierenden Textebenen wird durch den tatsächlichen wiedergegebenen Text bestimmt.
* Der standardmäßige Ebenenanker der selbstdimensionierenden Textebenen ist im Allgemeinen *nicht* in der Mitte der Ebene (siehe unten).
* Wenn `anchor=` oder `origin=` für die Selbstdimensionierung von Textebenen angegeben ist, wird die Position der Textebene durch den Textinhalt beeinflusst.

* Wenn `size=` angegeben ist, können Teile von Zeichen außerhalb des Ebenenrechtecks gerendert werden.
* `pos=` kann in allen Fällen verwendet werden, um eine Textebene neu zu positionieren.

## Punkttext (selbstskalieren) {#section-db99ec98eb114458b2dbc9911a58f74a}

Punkttext im Photoshop-Stil wird simuliert, wenn `textPs=` ohne `size=`, `textPath=` oder `textFlowPath=` angegeben wird. Die Ebenengröße wird horizontal durch die Breite des gerenderten Texts und vertikal durch den Zeilenabstand bestimmt. Text wird nie automatisch umgebrochen.

Wenn weder `anchor=` noch `origin=` angegeben sind, wird die erste Zeile des Textes direkt über dem Ebenenursprung positioniert. Absätze, die mit `\ql` markiert sind, werden rechts neben dem Ebenenursprung positioniert, Absätze, die `\qr` enthalten, werden links vom Ursprung gerendert und Absätze mit `\qc` werden horizontal um den Ursprung zentriert. Wenn `anchor=` oder `origin=` angegeben ist, gelten die standardmäßigen Ebenenpositionierungsregeln.

Wenn `color=` angegeben ist, wird der Begrenzungsrahmen des tatsächlichen gerenderten Texts gefüllt.

Die folgenden RTF-Befehle werden ignoriert: `\qj`, `\marg*`, `\hyph*`, `\vertal*`.

## Rechteckiges Textfeld {#section-1d3ab11df26d4004a1a801546756475d}

Wenn `size=` zusätzlich zu `textPs=` (ohne `textPath=` und `textFlowPath=`) angegeben ist, wird der Text auf das angegebene Rechteck beschränkt. Die Ebene wird wie gewohnt positioniert. Zeichen in der Nähe der Kanten des Textfelds können teilweise außerhalb des Textfelds gerendert werden.

`color=` füllt den durch definierten Bereich  `size=`.

Alle RTF-Befehle werden erwartungsgemäß angewendet.

## Textfeld &quot;Variablenhöhe&quot; {#section-e1233d1c9f8e43218667361dc0c4fd06}

Durch die Angabe von `size=` mit 0 Höhe kann das Textfeld vertikal skaliert werden, um alle Inhalte aufzunehmen. Die Ebenenbreite wird durch die Breite von `size=` und die Ebenenhöhe durch die Höhe des tatsächlichen gerenderten Texts definiert. Die Ebene wird wie gewohnt positioniert. Zeichen in der Nähe der linken und rechten Kante des Textfelds können teilweise außerhalb des Textfelds gerendert werden.

`color=` füllt das Rechteck, das durch die mit angegebene Breite  `size=` und Höhe des tatsächlichen gerenderten Texts definiert wird.

Die folgenden RTF-Befehle werden ignoriert:

`\vertal*`

## Selbstdimensionierender Text im Pfad {#section-d26685e7085847efaaeba64b9cb5ed9f}

`textFlowPath=` in Verbindung mit  `textPs=` können verwendet werden, um einen oder mehrere Bereiche zu definieren, in die Text fließen soll. `textFlowXPath=` kann optional angegeben werden, um den Textfluss in einen oder mehrere Bereiche auszuschließen. Wenn `size=` nicht angegeben ist, wird die resultierende Textebene selbst skaliert und die Ebenengröße wird durch den Begrenzungsrahmen des tatsächlich gerenderten Texts bestimmt.

Wenn weder `origin=` noch `anchor=` angegeben sind, wird der Ebenen-Anker standardmäßig auf (0,0) des Pixelkoordinatenraums gesetzt, der zum Definieren der Pfade verwendet wird. Dadurch wird unabhängig vom gerenderten Text eine absolute Position sichergestellt. Wenn `anchor=` oder `origin=` angegeben sind, wird die Ebene relativ zum Begrenzungsrahmen des tatsächlichen gerenderten Inhalts positioniert (und an diesen angepasst).

`color=` füllt den Begrenzungsrahmen des tatsächlichen gerenderten Texts.

Die folgenden RTF-Befehle werden ignoriert:

`\marg*`

## Vorformatierter Text im Pfad {#section-ed492a8a54414cd4bde360500cec6968}

Wenn `size=` zusammen mit `textFlowPath=` angegeben wird, wird die Ebenengröße vorab bestimmt. (0,0) des Pixelkoordinatenraums, der zur Definition des Pfads verwendet wird, befindet sich in der linken oberen Ecke des Ebenenrechtecks.

Die `textFlowPath=`-Bereiche können sich außerhalb des Ebenenrechtecks befinden. Text wird immer fließend in alle Pfadbereiche gerendert, auch wenn dadurch Text außerhalb des Ebenenrechtecks gerendert wird. `extend=0,0,0,0`kann verwendet werden, um den gerenderten Text auf das Ebenenrechteck zu beschneiden.

Für Ebenenpositionierungszwecke basiert das Ebenenrechteck auf dem angegebenen `size=`, unabhängig davon, wie viel Text tatsächlich gerendert wird, selbst wenn sich ein Teil außerhalb des Ebenenrechtecks befindet. Es gilt die standardmäßige Ebenenpositionierung.

`color=` füllt den durch  `size=`definierten rechteckigen Bereich.

Die folgenden RTF-Befehle werden für `textFlowPath=` ignoriert:

`\marg*`

## Selbstdimensionierender Text auf einem Pfad {#section-7ce6b9b26b354ba381e4378703154062}

`textPath=` definiert einen oder mehrere Pfade, auf die der mit angegebene Text gerendert werden  `textPs=` soll. Wenn `size=` nicht angegeben ist, wird die resultierende Textebene selbst skaliert. Die Ebenengröße wird durch den Begrenzungsrahmen des tatsächlichen gerenderten Texts bestimmt.

Wenn weder `origin=` noch `anchor=` angegeben sind, wird der Ebenen-Anker standardmäßig auf (0,0) des Pixelkoordinatenraums festgelegt, der zum Definieren des Pfads verwendet wird. die Position des gerenderten Textes ist unabhängig von der gerenderten Textmenge fest. Wenn `anchor=` oder `origin=` angegeben sind, wird die Ebene relativ zum Begrenzungsrahmen des tatsächlichen gerenderten Inhalts positioniert (und an diesen angepasst).

`color=` füllt den Begrenzungsrahmen des tatsächlichen gerenderten Texts.

Die folgenden RTF-Befehle werden ignoriert:

* `\marg*`
* `\hyph*`
* `\vertal*`

Jeder Text nach dem ersten `\par` oder `\line` wird ignoriert.

## Vorformatierter Text auf Pfad {#section-a3bbbc5187f448b192e53d27e2c53f2f}

Wenn `size=` zusammen mit `textPath=` angegeben wird, wird die Ebenengröße vorab bestimmt. (0,0) des Pixelkoordinatenraums, der zur Definition des Pfads verwendet wird, befindet sich in der linken oberen Ecke des Ebenenrechtecks.

Die Pfade können sich teilweise oder vollständig außerhalb des Ebenenrechtecks befinden. Text wird immer entlang des gesamten Pfads angewendet und gerendert, auch wenn er sich außerhalb des Ebenenrechtecks befindet. `extend=0,0,0,0` kann verwendet werden, um den gerenderten Text auf das Ebenenrechteck zu beschneiden.

Für die Positionierung der Ebene basiert das Ebenenrechteck auf dem angegebenen `size=`, selbst wenn ein Teil des Textes außerhalb des Ebenenrechtecks gerendert wird. Es gilt die standardmäßige Ebenenpositionierung.

`color=` füllt den durch definierten Bereich  `size=`.

Die folgenden RTF-Befehle werden ignoriert:

* `\marg*`
* `\q*`
* `\marg*`
* `\hyph*`
* `\vertal*`

Jeder Text nach dem ersten `\par` oder `\line` wird ignoriert.
