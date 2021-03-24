---
description: Ähnliche Anforderungen wie Beispiel A, verwenden Sie jedoch einen Hintergrund mit fester Farbe und lassen Sie die Höhe des Composite variieren, um Bilder mit unterschiedlichen Seitenverhältnissen aufzunehmen.
solution: Experience Manager
title: Beispiel B
feature: Dynamic Media Classic, SDK/API
role: Entwickler, Geschäftspraktiker
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '176'
ht-degree: 0%

---


# Beispiel B{#example-b}

Ähnliche Anforderungen wie Beispiel A, verwenden Sie jedoch einen Hintergrund mit fester Farbe und lassen Sie die Höhe des Composite variieren, um Bilder mit unterschiedlichen Seitenverhältnissen aufzunehmen.

<table id="simpletable_37BA3B2A75A9468C9ADEBBC034BADAE7"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> Katalog::ID</span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> Katalog::Modifier</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> myTemplate2</span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> $text=layer+1+text+go+here&amp; layer=0&amp;size=800,0&amp;extended=0,100,200,100&amp;src=$object$&amp;originN=.5,0&amp; layer=1&amp;text=rtf...$text$..rtf-encoding&amp;rotate=-90&amp;originN.5,0&amp;posN=0.5,0</span> </p></td> 
 </tr> 
</table>

Das Bild wird in Ebene 0 platziert und der Höhenwert von `size=` ist auf 0 eingestellt, wodurch die tatsächliche Höhe durch die Höhe des Bilds bestimmt wird, nachdem es auf eine Breite von 800 Pixeln skaliert wurde.

`extend=` fügt oben und unten 100 Pixel und rechts 200 Pixel hinzu.

Die Herkünfte für Ebene 0 und Ebene 1 werden in der Mitte rechts des Kompositionsbereichs platziert, um die gewünschte Textposition zu erreichen.

Die folgende Abbildung zeigt das zusammengesetzte Ergebnis für verschiedene Seitenverhältnisse des Bildes und für verschiedene Textzeichenfolgen.

![](assets/exampleb.png)

