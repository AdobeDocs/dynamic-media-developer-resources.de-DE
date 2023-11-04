---
description: textPs= unterstützt eine Reihe verschiedener Nutzungsmodelle, die in diesem Abschnitt beschrieben werden.
solution: Experience Manager
title: Textebenen
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 6793eb7d-6c10-4136-b6d4-186a698a8e52
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '883'
ht-degree: 0%

---

# Textebenen{#text-layers}

textPs= unterstützt eine Reihe verschiedener Nutzungsmodelle, die in diesem Abschnitt beschrieben werden.

>[!NOTE]
>
>Dieser Abschnitt gilt nicht für `text=`.

Die gemeinsamen Regeln und Definitionen lauten wie folgt:

* Selbstdimensionierende Textebenen sind Ebenen, die keine `size=` oder `size=0,0` festgelegt ist.

* Die Ebenengröße von selbstskalierenden Textebenen wird durch den tatsächlichen wiedergegebenen Text bestimmt.
* Der standardmäßige Ebenenanker für die selbstdimensionierende Textebene ist im Allgemeinen *not* in der Mitte der Ebene (siehe unten).
* Wenn `anchor=` oder `origin=` wird für die Selbstdimensionierung von Textebenen angegeben, wird die Position der Textebene durch den Textinhalt beeinflusst.

* Wann `size=` festgelegt ist, können Teile von Zeichen außerhalb des Ebenenrechtecks gerendert werden.
* `pos=` kann in allen Fällen verwendet werden, um eine Textebene neu zu positionieren.

## Punkttext (selbstskalieren) {#section-db99ec98eb114458b2dbc9911a58f74a}

Punkttext im Photoshop-Stil wird bei `textPs=` angegeben wird, ohne `size=`, `textPath=`oder `textFlowPath=`. Die Ebenengröße wird horizontal durch die Breite des gerenderten Texts und vertikal durch den Zeilenabstand bestimmt. Text wird nie automatisch umgebrochen.

Wenn `anchor=` nor `origin=` angegeben werden, wird die erste Zeile des Textes direkt über dem Ebenenursprung positioniert; Absätze, die mit `\ql` werden rechts neben dem Ebenenursprung positioniert, wobei Absätze, die `\qr` werden links neben der Quelle und Absätze mit `\qc` werden horizontal um den Ursprung zentriert. Es gelten die Regeln für die Positionierung von Standardebenen `anchor=` oder `origin=` angegeben werden.

Wenn `color=` festgelegt ist, wird der Begrenzungsrahmen des tatsächlichen gerenderten Texts gefüllt.

Die folgenden RTF-Befehle werden ignoriert: `\qj`, `\marg*`, `\hyph*`, `\vertal*`.

## Rechteckiges Textfeld {#section-1d3ab11df26d4004a1a801546756475d}

Wenn `size=` wird zusätzlich zu `textPs=` (ohne `textPath=` und `textFlowPath=`), wird der Text auf das angegebene Rechteck beschränkt. Die Ebene wird wie gewohnt positioniert. Zeichen in der Nähe der Kanten des Textfelds können teilweise außerhalb des Textfelds gerendert werden.

`color=` füllt den von `size=`.

Alle RTF-Befehle werden erwartungsgemäß angewendet.

## Textfeld &quot;Variablenhöhe&quot; {#section-e1233d1c9f8e43218667361dc0c4fd06}

Festlegen `size=` mit 0 Höhe ermöglicht es, die Größe des Textfelds vertikal zu ändern, um alle Inhalte aufzunehmen. Die Ebenenbreite wird durch die Breite von `size=`, und die Ebenenhöhe um die Höhe des tatsächlichen gerenderten Textes. Die Ebene wird wie gewohnt positioniert. Zeichen in der Nähe der linken und rechten Kante des Textfelds können teilweise außerhalb des Textfelds gerendert werden.

`color=` füllt das Rechteck aus, das durch die mit `size=` und die Höhe des tatsächlichen wiedergegebenen Texts.

Die folgenden RTF-Befehle werden ignoriert:

`\vertal*`

## Selbstdimensionierender Text im Pfad {#section-d26685e7085847efaaeba64b9cb5ed9f}

`textFlowPath=` in Verbindung mit `textPs=` kann verwendet werden, um einen oder mehrere Bereiche zu definieren, in die Text fließen soll. `textFlowXPath=` kann optional angegeben werden, um den Textfluss in einen oder mehrere Bereiche auszuschließen. Wenn `size=` nicht angegeben ist, wird die resultierende Textebene selbst skaliert und die Ebenengröße wird durch den Begrenzungsrahmen des tatsächlich gerenderten Textes bestimmt.

Wenn `origin=` nor `anchor=` festgelegt sind, wird der Ebenen-Anker standardmäßig auf (0,0) des Pixelkoordinatenraums gesetzt, der zum Definieren der Pfade verwendet wird, wodurch unabhängig vom gerenderten Text eine absolute Position gewährleistet wird. Wenn `anchor=` oder `origin=` festgelegt sind, wird die Ebene relativ zum Begrenzungsrahmen des tatsächlichen gerenderten Inhalts positioniert (und an diesen angepasst).

`color=` füllt den Begrenzungsrahmen des tatsächlichen gerenderten Texts.

Die folgenden RTF-Befehle werden ignoriert:

`\marg*`

## Vorformatierter Text im Pfad {#section-ed492a8a54414cd4bde360500cec6968}

Wenn `size=` wird zusammen mit `textFlowPath=`festgelegt ist, wird die Ebenengröße vorab bestimmt. (0,0) des Pixelkoordinatenraums, der zur Definition des Pfads verwendet wird, befindet sich in der linken oberen Ecke des Ebenenrechtecks.

Die `textFlowPath=` -Regionen befinden sich möglicherweise außerhalb des Ebenenrechtecks. Text wird immer fließend in alle Pfadbereiche gerendert, auch wenn dadurch Text außerhalb des Ebenenrechtecks gerendert wird. `extend=0,0,0,0`kann verwendet werden, um den gerenderten Text auf das Ebenenrechteck zu beschneiden.

Für die Positionierung der Ebene basiert das Ebenenrechteck auf dem angegebenen `size=`, unabhängig davon, wie viel Text tatsächlich gerendert wird, auch wenn sich ein Teil außerhalb des Ebenenrechtecks befindet. Es gilt die standardmäßige Ebenenpositionierung.

`color=` füllt den rechteckigen Bereich, der durch `size=`.

Die folgenden RTF-Befehle werden für `textFlowPath=`:

`\marg*`

## Selbstdimensionierender Text auf einem Pfad {#section-7ce6b9b26b354ba381e4378703154062}

`textPath=` definiert einen oder mehrere Pfade für den Text, der mit `textPs=` sollte gerendert werden. Wann `size=` nicht angegeben ist, wird die resultierende Textebene selbst skaliert. Die Ebenengröße wird durch den Begrenzungsrahmen des tatsächlichen gerenderten Texts bestimmt.

Wenn `origin=` nor `anchor=` festgelegt sind, wird der Ebenen-Anker standardmäßig auf (0,0) des Pixelkoordinatenraums festgelegt, der zum Definieren des Pfads verwendet wird. Die Position des gerenderten Texts wird unabhängig von der Menge des wiedergegebenen Texts festgelegt. Wenn `anchor=` oder `origin=` festgelegt sind, wird die Ebene relativ zum Begrenzungsrahmen des tatsächlichen gerenderten Inhalts positioniert (und an diesen angepasst).

`color=` füllt den Begrenzungsrahmen des tatsächlichen gerenderten Texts.

Die folgenden RTF-Befehle werden ignoriert:

* `\marg*`
* `\hyph*`
* `\vertal*`

Beliebiger Text nach dem ersten `\par` oder `\line` wird ignoriert.

## Vorformatierter Text auf Pfad {#section-a3bbbc5187f448b192e53d27e2c53f2f}

Wenn `size=` wird zusammen mit `textPath=`festgelegt ist, wird die Ebenengröße vorab bestimmt. (0,0) des Pixelkoordinatenraums, der zur Definition des Pfads verwendet wird, befindet sich in der linken oberen Ecke des Ebenenrechtecks.

Die Pfade können sich teilweise oder vollständig außerhalb des Ebenenrechtecks befinden. Text wird immer entlang des gesamten Pfads angewendet und gerendert, auch wenn er sich außerhalb des Ebenenrechtecks befindet. `extend=0,0,0,0` kann verwendet werden, um den gerenderten Text auf das Ebenenrechteck zu beschneiden.

Für die Positionierung der Ebene basiert das Ebenenrechteck auf dem angegebenen `size=`, auch wenn ein Teil des Textes außerhalb des Ebenenrechtecks gerendert wird. Es gilt die standardmäßige Ebenenpositionierung.

`color=` füllt den Bereich, der durch `size=`.

Die folgenden RTF-Befehle werden ignoriert:

* `\marg*`
* `\q*`
* `\marg*`
* `\hyph*`
* `\vertal*`

Beliebiger Text nach dem ersten `\par` oder `\line` wird ignoriert.
