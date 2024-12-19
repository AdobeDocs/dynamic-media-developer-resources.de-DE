---
title: Beispiel A
description: Erstellen Sie eine Vorlage mit fester Größe und einem statischen Hintergrundbild, einem variablen Bild, das links in der Mitte mit dem Hintergrund ausgerichtet und auf maximal 80 % der Breite und Höhe des Hintergrunds skaliert ist. Und schließlich eine Textebene mit vertikalem Text, der am rechten Rand der Arbeitsfläche zentriert ist.
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

Erstellen Sie eine Vorlage mit fester Größe und einem statischen Hintergrundbild, einem variablen Bild, das links in der Mitte mit dem Hintergrund ausgerichtet und auf maximal 80 % der Breite und Höhe des Hintergrunds skaliert ist. Und schließlich eine Textebene mit vertikalem Text, der am rechten Rand der Arbeitsfläche zentriert ist.

![Beispiel eines Bildes](assets/examplea.png)

## Der Vorlagendatensatz {#section-32f54710593e438fa0622224c89380af}

Objekt einfügen

<table id="simpletable_97ECA49445634F59B3F1D100412EFC70"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph">::ID </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> myTemplate1-</span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph">::Modifier </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> src=backgroundImage&amp;size=1000,1000&amp;originN=0,0&amp; layer=1&amp;src=$object$&amp;size=800,800&amp;originN=-0,5,0&amp;posN=-0,5,0&amp; layer=2&amp;$text=layer+2+text+gos+here&amp;text=rtf…$text$..rtf-encoding&amp;rotation=-90&amp;originN=0,5,0&amp;posN=0,5,0 </span> </p> </td> 
 </tr> 
</table>

Die `origin=` Werte aller Ebenen werden in der Vorlage explizit angegeben, um die Positionierung und Ausrichtung der Ebenen streng zu steuern. Jeder Ebenenursprung ist so eingestellt, dass er der gewünschten Ausrichtung für diese Ebene entspricht. Der `origin=` für den Hintergrund (Ebene 0) ist auf die Mitte gesetzt. Dieser Wert ist beliebig, da sich das Hintergrundbild zur Laufzeit nicht ändert. Es kann ein beliebiger Wert für den Ursprung der Ebene 0 verwendet werden.

Die `pos=` Werte liefern die notwendigen Versätze zwischen den Ebenenursprungspunkten, um die gewünschte Ebenenpositionierung zu erreichen.

Der Anker für das Bild der Ebene 1 wird mit dem `pos=` Wert in der linken Mitte platziert. Mit dieser Einstellung wird die linkszentrierte Ausrichtung zwischen Hintergrund- und Ebenenbild 1 unabhängig vom Seitenverhältnis des Ebenenbildes erreicht.

Ebenso wird der Anker für die Textebene rechts in der Mitte des automatisch skalierten Textfelds mit dem Wert `pos=` positioniert. Mit dieser Einstellung wird die gewünschte Ausrichtung des gedrehten Textes in der rechten Mitte erreicht, unabhängig von der Schriftgröße und der Zeichenfolgenlänge.

Der tatsächliche Anzeigetext wird zur Laufzeit bereitgestellt, sodass eine Variable verwendet wird, um den Text von der RTF-Formatierungshülle zu trennen. Die Standardvariable `$object` wird für das Bild der Ebene 1 verwendet. Mit dieser Variablen können Sie dieses Bild im Anfragepfad angeben.

Jedes Bild kann für das Hintergrundbild und das Bild der Ebene 1 verwendet werden. Wenn das Hintergrundbild eine Maske aufweist, werden die nicht maskierten Bereiche mit der standardmäßigen Hintergrundfarbe ( `attribute::BkgColor`) gefüllt oder beim `fmt=png-alpha` oder `fmt=tif-alpha` transparent gelassen. Wenn das Hintergrundbild ein nicht quadratisches Seitenverhältnis aufweist, wird es im Antwortbild zentriert und der zusätzliche Platz wird mit `attribute::BkgColor` ausgefüllt. Wenn das Bild der Ebene 1 Alpha-Daten oder eine Maske enthält, bleibt das Hintergrundbild (oder die Hintergrundfarbe) in den transparenten Bereichen sichtbar. Wenn das Bild keine Maske aufweist, wird das gesamte zugewiesene Rechteck ausgefüllt.

## Verwenden der Vorlage {#section-3e04eedc268c482db5a8cfc662c0f327}

` http:// *`server`*/myRootId/anotherImage?template=myTemplate1&$text=about+the+image`

Die folgende Abbildung zeigt das zusammengesetzte Ergebnis für verschiedene Seitenverhältnisse des Bildes der Ebene 1 und verschiedene Textzeichenfolgen.

![Beispiel: Ein zusammengesetztes Ergebnisbild](assets/exampleausing.png)
