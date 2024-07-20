---
title: Beispiel A
description: Erstellen Sie eine Vorlage mit fester Größe mit einem statischen Hintergrundbild, einem variablen Bild, das am Hintergrund in der linken Mitte ausgerichtet und auf maximal 80 % der Breite und Höhe des Hintergrunds skaliert ist. Und schließlich eine Textebene mit vertikalem Text, der am rechten Rand der Arbeitsfläche zentriert ist.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 7f731b41-994d-4f1d-b42d-e14db47e4d6c
source-git-commit: 24667a5ebab54ba22c4a3f6b52d19d7a31a93576
workflow-type: tm+mt
source-wordcount: '468'
ht-degree: 0%

---

# Beispiel A{#example-a}

Erstellen Sie eine Vorlage mit fester Größe mit einem statischen Hintergrundbild, einem variablen Bild, das am Hintergrund in der linken Mitte ausgerichtet und auf maximal 80 % der Breite und Höhe des Hintergrunds skaliert ist. Und schließlich eine Textebene mit vertikalem Text, der am rechten Rand der Arbeitsfläche zentriert ist.

![Beispiel für ein Bild](assets/examplea.png)

## Vorlagendatensatz {#section-32f54710593e438fa0622224c89380af}

Objekt einfügen

<table id="simpletable_97ECA49445634F59B3F1D100412EFC70"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> catalog::Id </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> myTemplate1 </span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> catalog::Modifier </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> src=backgroundImage&amp;size=1000,1000&amp;originN=0,0&amp; layer=1&amp;src=$object$&amp;size=800,800&amp;originN=-0.5,0&amp;posN=-0.5,0&amp; layer=2&amp; text=layer+2+text+here&amp;text=rtf..$text$...rtf-encoding&amp;rotate=-90&amp;originN=0.5,0&amp;posN=0.5,0 </span> </p> </td> 
 </tr> 
</table>

Die `origin=` -Werte aller Ebenen werden explizit in der Vorlage angegeben, um die Positionierung und Ausrichtung der Ebenen genau zu steuern. Jeder Ebenenursprung wird so eingestellt, dass er der gewünschten Ausrichtung für diese Ebene entspricht. Der Wert &quot;`origin=`&quot; für den Hintergrund (Ebene 0) wird auf die Mitte gesetzt. Dieser Wert ist beliebig, da sich das Hintergrundbild zur Laufzeit nicht ändert. Es kann ein beliebiger Wert für die Ebene 0 verwendet werden.

Die `pos=` -Werte stellen die erforderlichen Versätze zwischen den Ebenen-Ausgangspunkten bereit, um die gewünschte Ebenenpositionierung zu erreichen.

Der Anker für das Bild der Ebene 1 wird in der linken Mitte mit dem Wert `pos=` platziert. Mit dieser Einstellung wird die linke Mittelausrichtung zwischen Hintergrund und Ebene 1 erreicht, unabhängig vom Seitenverhältnis des Bilds Ebene 1.

Gleichermaßen wird der Anker für die Textebene in der rechten Mitte des automatisch angepassten Textfelds mit dem Wert `pos=` positioniert. Mit dieser Einstellung wird die gewünschte Rechtsmittelausrichtung für den gedrehten Text unabhängig von Schriftgröße und Zeichenfolgenlänge erreicht.

Der tatsächliche Anzeigetext wird zur Laufzeit bereitgestellt, sodass eine Variable verwendet wird, um den Text von der Umschlagfläche für die RTF-Formatierung zu trennen. Die Standardvariable `$object` wird für das Bild der Ebene 1 verwendet. Mit dieser Variablen können Sie dieses Bild im Anfragepfad angeben.

Für das Hintergrundbild und das Bild der Ebene 1 kann jedes Bild verwendet werden. Wenn das Hintergrundbild eine Maske hat, werden die nicht maskierten Bereiche mit der standardmäßigen Hintergrundfarbe ( `attribute::BkgColor`) gefüllt oder bei `fmt=png-alpha` oder `fmt=tif-alpha` transparent gelassen. Wenn das Hintergrundbild ein nicht quadratisches Seitenverhältnis aufweist, wird es im Antwortbild zentriert und der zusätzliche Platz wird mit `attribute::BkgColor` gefüllt. Wenn das Bild der Ebene 1 über Alphakatdaten oder eine Maske verfügt, bleibt das Hintergrundbild (oder die Hintergrundfarbe) in den transparenten Bereichen sichtbar. Wenn das Bild keine Maske hat, wird das gesamte zugewiesene Rechteck gefüllt.

## Vorlage verwenden {#section-3e04eedc268c482db5a8cfc662c0f327}

` http:// *`server`*/myRootId/anotherImage?template=myTemplate1&$text=about+the+image`

Die folgende Abbildung zeigt das zusammengesetzte Ergebnis für verschiedene Seitenverhältnisse des Bilds der Ebene 1 und für verschiedene Textzeichenfolgen.

![Beispiel Ein zusammengesetztes Ergebnisbild](assets/exampleausing.png)
