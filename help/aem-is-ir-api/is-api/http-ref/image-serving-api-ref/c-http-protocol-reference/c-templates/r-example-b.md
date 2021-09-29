---
description: Ähnliche Anforderungen wie Beispiel A, verwenden jedoch einen einfarbigen Hintergrund und ermöglichen es, die Höhe des Composite zu variieren, um Bilder mit unterschiedlichen Seitenverhältnissen aufzunehmen.
solution: Experience Manager
title: Beispiel B
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 90ef96fc-c12f-4fc8-b465-6520b71f4e7b
source-git-commit: 24667a5ebab54ba22c4a3f6b52d19d7a31a93576
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# Beispiel B{#example-b}

Ähnliche Anforderungen wie Beispiel A, verwenden jedoch einen einfarbigen Hintergrund und ermöglichen es, die Höhe des Composite zu variieren, um Bilder mit unterschiedlichen Seitenverhältnissen aufzunehmen.

<table id="simpletable_37BA3B2A75A9468C9ADEBBC034BADAE7"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> catalog::Id</span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> catalog::Modifier</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> myTemplate2</span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> $text=layer+1+text+go+here&amp; layer=0&amp;size=800,0&amp;extend=0,100,200,100&amp;src=$object$&amp;originN=.5,0&amp; layer=1&amp;text=rtf..$text$...rtf-encoding&amp;rotate=-90&amp;originN=.5,0&amp;posN=0.5,0</span> </p></td> 
 </tr> 
</table>

Das Bild wird in Ebene 0 platziert und der Höhenwert von `size=` ist auf 0 gesetzt. Diese Einstellung bewirkt, dass die tatsächliche Höhe durch die Höhe des Bildes bestimmt wird, nachdem es auf eine Breite von 800 Pixel skaliert wurde.

Die Variable `extend=` fügt oben und unten 100 Pixel und rechts 200 Pixel hinzu.

Die Ursprünge für Ebene 0 und Ebene 1 werden in der Mitte rechts des Kompositionbereichs platziert, um die gewünschte Textposition zu erreichen.

Die folgende Abbildung zeigt das zusammengesetzte Ergebnis für verschiedene Seitenverhältnisse des Bildes und für verschiedene Textzeichenfolgen.

![Beispiel B Bild](assets/exampleb.png)
