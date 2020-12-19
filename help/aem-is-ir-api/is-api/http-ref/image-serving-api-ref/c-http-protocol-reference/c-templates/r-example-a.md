---
description: Erstellen Sie eine Vorlage mit fester Größe mit einem statischen Hintergrundbild, einem variablen Bild, das am Hintergrund in der linken Mitte ausgerichtet und auf maximal 80 % der Breite und Höhe des Hintergrunds skaliert ist, und einer Textebene mit vertikalem Text, der auf der rechten Kante der Arbeitsfläche zentriert ist.
seo-description: Erstellen Sie eine Vorlage mit fester Größe mit einem statischen Hintergrundbild, einem variablen Bild, das am Hintergrund in der linken Mitte ausgerichtet und auf maximal 80 % der Breite und Höhe des Hintergrunds skaliert ist, und einer Textebene mit vertikalem Text, der auf der rechten Kante der Arbeitsfläche zentriert ist.
seo-title: Beispiel A
solution: Experience Manager
title: Beispiel A
topic: Scene7 Image Serving - Image Rendering API
uuid: c250dbc8-1e32-46b8-ba55-c1fb0ae62695
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '499'
ht-degree: 0%

---


# Beispiel A{#example-a}

Erstellen Sie eine Vorlage mit fester Größe mit einem statischen Hintergrundbild, einem variablen Bild, das am Hintergrund in der linken Mitte ausgerichtet und auf maximal 80 % der Breite und Höhe des Hintergrunds skaliert ist, und einer Textebene mit vertikalem Text, der auf der rechten Kante der Arbeitsfläche zentriert ist.

![](assets/examplea.png)

## Der Vorlagendatensatz {#section-32f54710593e438fa0622224c89380af}

Objekt einfügen

<table id="simpletable_97ECA49445634F59B3F1D100412EFC70"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> Katalog::ID  </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> myTemplate1  </span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> Katalog::Modifier  </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> src=backgroundImage&amp;size=1000,1000&amp;originN=0,0&amp; layer=1&amp;src=$object$&amp;size=800,800&amp;originN=-0.5,0&amp;posN=-0.5,0&amp; layer=2&amp;$text=layer+2+text+goes+here&amp;text rtf..$text$...rtf-encoding&amp;rotate=-90&amp;originN=0.5,0&amp;posN=0.5,0  </span> </p> </td> 
 </tr> 
</table>

Die `origin=`-Werte aller Ebenen werden explizit in der Vorlage angegeben, um die Positionierung und Ausrichtung der Ebenen strikt zu steuern. Jede Herkunft der Ebene ist so eingestellt, dass sie der gewünschten Ausrichtung für diese Ebene entspricht. Für den Hintergrund (Ebene 0) ist `origin=` auf die Mitte eingestellt. Dies ist willkürlich, da sich das Hintergrundbild zur Laufzeit nicht ändert. Es kann jeder Wert für die Herkunft 0 verwendet werden.

Die `pos=`-Werte stellen die erforderlichen Versatzwerte zwischen den Ebenen-Herkünfte-Punkten bereit, um die gewünschte Ebenenpositionierung zu erzielen.

Der Anker für das Bild der Ebene 1 wird in der linken Mitte platziert. in Verbindung mit dem Wert `pos=` wird dadurch die linke Mitte-Ausrichtung zwischen Hintergrund und Ebene 1-Bild unabhängig vom Seitenverhältnis der Ebene 1 erreicht.

Gleichermaßen wird der Anker für die Textebene in der rechten Mitte des automatisch skalierten Textfelds positioniert. In Verbindung mit &quot;pos=&quot;wird die gewünschte Ausrichtung in der rechten Mitte für den gedrehten Text unabhängig von Schriftgröße und Zeichenfolgenlänge erreicht.

Der eigentliche Anzeigetext wird zur Laufzeit bereitgestellt, sodass eine Variable verwendet wird, um den Text vom Umschlag für die RTF-Formatierung zu trennen. Wir verwenden die Standardvariable `$object` für das Bild der Ebene 1. Dadurch kann dieses Bild im Anforderungspfad angegeben werden.

Für das Hintergrundbild und das Bild der Ebene 1 kann jedes beliebige Bild verwendet werden. Wenn das Hintergrundbild eine Maske hat, werden die nicht maskierten Bereiche mit der standardmäßigen Hintergrundfarbe ( `attribute::BkgColor`) oder mit der transparenten Farbe `fmt=png-alpha` oder `fmt=tif-alpha` gefüllt. Wenn das Hintergrundbild ein nicht quadratisches Seitenverhältnis hat, wird es im Antwortbild zentriert und der zusätzliche Abstand mit `attribute::BkgColor` gefüllt. Wenn das Bild der Ebene 1 über Alpha-Daten oder eine Maske verfügt, bleibt das Hintergrundbild (oder die Hintergrundfarbe) in den transparenten Bereichen sichtbar. Wenn das Bild keine Maske hat, füllt es das gesamte zugewiesene Rechteck.

## Verwenden der Vorlage {#section-3e04eedc268c482db5a8cfc662c0f327}

` http:// *`Server`*/myRootId/anotherImage?template=myTemplate1&$text=about+the+image`

Die folgende Abbildung zeigt das zusammengesetzte Ergebnis für verschiedene Seitenverhältnisse des Bilds der Ebene 1 und für verschiedene Textzeichenfolgen.

![](assets/exampleausing.png)

