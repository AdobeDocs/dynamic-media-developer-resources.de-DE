---
description: Erstellen Sie eine Vorlage mit fester Größe mit einem statischen Hintergrundbild, einem variablen Bild, das mit dem Hintergrund in der linken Mitte ausgerichtet und auf maximal 80 % der Breite und Höhe des Hintergrunds skaliert ist, und einer Textebene mit vertikalem Text, der am rechten Rand der Arbeitsfläche zentriert ist.
solution: Experience Manager
title: Beispiel A
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 7f731b41-994d-4f1d-b42d-e14db47e4d6c
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '453'
ht-degree: 0%

---

# Beispiel A{#example-a}

Erstellen Sie eine Vorlage mit fester Größe mit einem statischen Hintergrundbild, einem variablen Bild, das mit dem Hintergrund in der linken Mitte ausgerichtet und auf maximal 80 % der Breite und Höhe des Hintergrunds skaliert ist, und einer Textebene mit vertikalem Text, der am rechten Rand der Arbeitsfläche zentriert ist.

![](assets/examplea.png)

## Vorlagendatensatz {#section-32f54710593e438fa0622224c89380af}

Objekt einfügen

<table id="simpletable_97ECA49445634F59B3F1D100412EFC70"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> catalog::Id  </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> myTemplate1  </span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> catalog::Modifier  </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> src=backgroundImage&amp;size=1000,1000&amp;originN=0,0&amp; layer=1&amp;src=$object$&amp;size=800,800&amp;originN=-0.5,0&amp;posN=-0.5,0&amp; layer=2&amp;$text=layer+2+text+goes&amp;text=here&amp;text rtf..$text$...rtf-encoding&amp;rotate=-90&amp;originN=0.5,0&amp;posN=0.5,0  </span> </p> </td> 
 </tr> 
</table>

Die `origin=`-Werte aller Ebenen werden explizit in der Vorlage angegeben, um die Positionierung und Ausrichtung der Ebenen genau zu steuern. Jeder Ebenenursprung wird so eingestellt, dass er der gewünschten Ausrichtung für diese Ebene entspricht. Die `origin=` für den Hintergrund (Ebene 0) ist auf die Mitte eingestellt. Dies ist willkürlich, da sich das Hintergrundbild zur Laufzeit nicht ändert. jeder Wert für die Ebene 0-Herkunft verwendet werden kann.

Die `pos=`-Werte stellen die erforderlichen Versätze zwischen den Ebenen-Ausgangspunkten bereit, um die gewünschte Ebenenpositionierung zu erreichen.

Der Anker für das Bild der Ebene 1 wird in der linken Mitte platziert. In Verbindung mit dem Wert `pos=` wird dabei unabhängig vom Seitenverhältnis der Ebene 1 die linke Mittelausrichtung zwischen Hintergrund und Ebene 1 erreicht.

Auf ähnliche Weise wird der Anker für die Textebene in der rechten Mitte des automatisch angepassten Textfelds positioniert. In Verbindung mit pos= wird die gewünschte Rechtsmittelausrichtung für den gedrehten Text erreicht, unabhängig von Schriftgröße und Zeichenfolgenlänge.

Der tatsächliche Anzeigetext wird zur Laufzeit bereitgestellt, sodass eine Variable verwendet wird, um den Text von der Umschlagfläche für die RTF-Formatierung zu trennen. Wir verwenden die Standardvariable `$object` für das Bild der Ebene 1. Dadurch kann dieses Bild im Anfragepfad angegeben werden.

Für das Hintergrundbild und das Bild der Ebene 1 kann jedes Bild verwendet werden. Wenn das Hintergrundbild eine Maske hat, werden die nicht maskierten Bereiche mit der standardmäßigen Hintergrundfarbe ( `attribute::BkgColor`) gefüllt oder sind transparent, wenn `fmt=png-alpha` oder `fmt=tif-alpha`. Wenn das Hintergrundbild ein nicht quadratisches Seitenverhältnis aufweist, wird es im Antwortbild zentriert und der zusätzliche Platz mit `attribute::BkgColor` gefüllt. Wenn das Bild der Ebene 1 Alphakanäle oder eine Maske enthält, bleibt das Hintergrundbild (oder die Hintergrundfarbe) in den transparenten Bereichen sichtbar. Wenn das Bild keine Maske hat, wird das gesamte zugewiesene Rechteck gefüllt.

## Vorlage verwenden {#section-3e04eedc268c482db5a8cfc662c0f327}

` http:// *`Server`*/myRootId/anotherImage?template=myTemplate1&$text=about+the+image`

Die folgende Abbildung zeigt das zusammengesetzte Ergebnis für verschiedene Seitenverhältnisse des Bilds der Ebene 1 und für verschiedene Textzeichenfolgen.

![](assets/exampleausing.png)
