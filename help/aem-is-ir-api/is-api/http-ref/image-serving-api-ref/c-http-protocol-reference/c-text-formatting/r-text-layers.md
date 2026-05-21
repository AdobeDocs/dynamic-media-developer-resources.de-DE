---
description: textPs= unterstützt eine Reihe verschiedener Nutzungsmodelle, die in diesem Abschnitt beschrieben werden.
solution: Experience Manager
title: Textebenen
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 6793eb7d-6c10-4136-b6d4-186a698a8e52
TQID: 'https://experienceleague.adobe.com/cIgicI7IPJKVWkhlyocD7g7nuXbJXaTAborYvt3Muyg'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 904
ht-degree: 0%

---

# Textebenen{#text-layers}

textPs= unterstützt eine Reihe verschiedener Nutzungsmodelle, die in diesem Abschnitt beschrieben werden.

>[!NOTE]
>
>Dieser Abschnitt gilt nicht für `text=`.

Die gemeinsamen Regeln und Definitionen lauten wie folgt:

* Textebenen mit automatischer Größenanpassung sind Ebenen, die keine `size=` enthalten oder für die `size=0,0` angegeben ist.

* Die Ebenengröße von Textebenen mit automatischer Skalierung wird durch den gerenderten Text bestimmt.
* Der standardmäßige Ebenenanker von Textebenen mit selbstskalierender Größe befindet *nicht* in der Mitte der Ebene (siehe unten).
* Wenn `anchor=` oder `origin=` für Textebenen mit automatischer Skalierung angegeben ist, wird die Position der Textebene durch den Textinhalt beeinflusst.

* Wenn `size=` angegeben ist, können Teile der Zeichenglyphen außerhalb des Ebenenrechtecks gerendert werden.
* `pos=` können in allen Fällen verwendet werden, um eine Textebene neu zu positionieren.

## Punkttext (automatische Größenanpassung) {#section-db99ec98eb114458b2dbc9911a58f74a}

Punkttext im Photoshop-Stil wird simuliert, wenn `textPs=` ohne `size=`, `textPath=` oder `textFlowPath=` angegeben wird. Die Ebenengröße wird horizontal durch die Breite des gerenderten Textes und vertikal durch den Zeilenabstand bestimmt. Text wird nie automatisch umgebrochen.

Wenn weder `anchor=` noch `origin=` angegeben sind, wird die erste Textzeile direkt über dem Ebenenursprung positioniert. Absätze, die mit `\ql` gekennzeichnet sind, werden rechts neben dem Ebenenursprung positioniert, Absätze, die `\qr` enthalten, werden links neben dem Ursprung gerendert, und Absätze mit `\qc` werden horizontal um den Ursprung zentriert. Wenn `anchor=` oder `origin=` angegeben sind, gelten die standardmäßigen Layerpositionierungsregeln.

Wenn `color=` angegeben ist, wird der Begrenzungsrahmen des tatsächlichen gerenderten Textes ausgefüllt.

Die folgenden RTF-Befehle werden ignoriert: `\qj`, `\marg*`, `\hyph*`, `\vertal*`.

## Rechteckiges Textfeld {#section-1d3ab11df26d4004a1a801546756475d}

Wenn `size=` zusätzlich zu `textPs=` angegeben wird (ohne `textPath=` und `textFlowPath=`), wird der Text auf das angegebene Rechteck beschränkt. Die Ebene wird wie gewohnt positioniert. Zeichensymbole in der Nähe der Textfeldränder können teilweise außerhalb des Textfelds gerendert werden.

`color=` füllt den durch `size=` definierten Bereich.

Alle RTF-Befehle werden erwartungsgemäß angewendet.

## Textfeld mit variabler Höhe {#section-e1233d1c9f8e43218667361dc0c4fd06}

Wenn Sie `size=` mit einer Höhe von 0 angeben, kann das Textfeld vertikal skaliert werden, um alle Inhalte aufzunehmen. Die Ebenenbreite wird durch die Breite von `size=` definiert und die Ebenenhöhe durch die Höhe des tatsächlichen gerenderten Texts. Die Ebene wird wie gewohnt positioniert. Zeichensymbole am linken und rechten Rand des Textfelds können teilweise außerhalb des Textfelds gerendert werden.

`color=` füllt das Rechteck, das durch die mit `size=` angegebene Breite und die Höhe des tatsächlichen gerenderten Textes definiert ist.

Die folgenden RTF-Befehle werden ignoriert:

`\vertal*`

## Automatische Größenanpassung des Texts im Pfad {#section-d26685e7085847efaaeba64b9cb5ed9f}

`textFlowPath=` in Verbindung mit `textPs=` können verwendet werden, um einen oder mehrere Bereiche zu definieren, in die Text fließen soll. `textFlowXPath=` können optional angegeben werden, um den Textfluss in einen oder mehrere Bereiche auszuschließen. Wenn `size=` nicht angegeben ist, wird die Größe der resultierenden Textebene selbst bestimmt und die Ebenengröße wird durch den Begrenzungsrahmen des tatsächlich gerenderten Textes bestimmt.

Wenn weder `origin=` noch `anchor=` angegeben sind, wird für den Ebenenanker standardmäßig (0,0) des Pixelkoordinatenraums verwendet, um den Pfad bzw. die Pfade zu definieren, wodurch die absolute Positionierung unabhängig vom gerenderten Text sichergestellt wird. Wenn `anchor=` oder `origin=` angegeben sind, wird die Ebene relativ zum Begrenzungsrahmen des tatsächlichen gerenderten Inhalts positioniert (und an diesen angepasst).

`color=` füllt den Begrenzungsrahmen des tatsächlichen gerenderten Textes aus.

Die folgenden RTF-Befehle werden ignoriert:

`\marg*`

## Text im Pfad in vorgegebener Größe {#section-ed492a8a54414cd4bde360500cec6968}

Wenn `size=` zusammen mit `textFlowPath=` angegeben wird, wird die Ebenengröße vorgegeben. (0,0) des Pixel-Koordinatenraums, der zum Definieren der Pfade verwendet wird, befindet sich in der oberen linken Ecke des Ebenenrechtecks.

Die `textFlowPath=` Bereiche können sich außerhalb des Schichtrechtecks befinden. Text wird immer in allen Pfadbereichen angezeigt, selbst wenn dabei Text außerhalb des Ebenenrechtecks gerendert wird. `extend=0,0,0,0`Kann verwendet werden, um den gerenderten Text auf das Ebenenrechteck zuzuschneiden.

Für Ebenenpositionierungszwecke basiert das Ebenenrechteck auf dem angegebenen `size=`, unabhängig davon, wie viel Text tatsächlich gerendert wird, auch wenn sich ein Teil außerhalb des Ebenenrechtecks befindet. Es gilt die standardmäßige Ebenenpositionierung.

`color=` füllt den durch `size=` definierten rechteckigen Bereich.

Die folgenden RTF-Befehle werden für `textFlowPath=` ignoriert:

`\marg*`

## Automatische Größenanpassung des Texts im Pfad {#section-7ce6b9b26b354ba381e4378703154062}

`textPath=` definiert einen oder mehrere Pfade, auf denen der mit `textPs=` angegebene Text gerendert werden soll. Wenn `size=` nicht angegeben ist, wird die Größe der resultierenden Textebene automatisch angepasst. Die Ebenengröße wird durch den Begrenzungsrahmen des tatsächlichen gerenderten Textes bestimmt.

Wenn weder `origin=` noch `anchor=` angegeben sind, wird für den Ebenenanker standardmäßig (0,0) des Pixelkoordinatenraums verwendet, der zum Definieren des Pfads verwendet wird. Die Position des gerenderten Texts ist unabhängig davon, wie viel Text gerendert wird, fest. Wenn `anchor=` oder `origin=` angegeben sind, wird die Ebene relativ zum Begrenzungsrahmen des tatsächlichen gerenderten Inhalts positioniert (und an diesen angepasst).

`color=` füllt den Begrenzungsrahmen des tatsächlichen gerenderten Textes aus.

Die folgenden RTF-Befehle werden ignoriert:

* `\marg*`
* `\hyph*`
* `\vertal*`

Jeder Text nach dem ersten `\par` oder `\line` wird ignoriert.

## Text im Pfad in vorgegebener Größe {#section-a3bbbc5187f448b192e53d27e2c53f2f}

Wenn `size=` zusammen mit `textPath=` angegeben wird, wird die Ebenengröße vorgegeben. (0,0) des Pixel-Koordinatenraums, der zum Definieren der Pfade verwendet wird, befindet sich in der oberen linken Ecke des Ebenenrechtecks.

Die Pfade können teilweise oder vollständig außerhalb des Ebenenrechtecks liegen. Text wird immer über den gesamten Pfad angewendet und gerendert, auch wenn er sich außerhalb des Ebenenrechtecks befindet. `extend=0,0,0,0` kann verwendet werden, um den gerenderten Text auf das Ebenenrechteck zuzuschneiden.

Zu Zwecken der Ebenenpositionierung basiert das Ebenenrechteck auf dem angegebenen `size=`, auch wenn ein Teil des Textes außerhalb des Ebenenrechtecks gerendert wird. Es gilt die standardmäßige Ebenenpositionierung.

`color=` füllt den durch `size=` definierten Bereich.

Die folgenden RTF-Befehle werden ignoriert:

* `\marg*`
* `\q*`
* `\marg*`
* `\hyph*`
* `\vertal*`

Jeder Text nach dem ersten `\par` oder `\line` wird ignoriert.
