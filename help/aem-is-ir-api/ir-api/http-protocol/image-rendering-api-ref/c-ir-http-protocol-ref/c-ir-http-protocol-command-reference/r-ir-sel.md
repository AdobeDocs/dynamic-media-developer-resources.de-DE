---
description: Wählen Sie das Objekt nach Pixelposition aus.
seo-description: Wählen Sie das Objekt nach Pixelposition aus.
seo-title: sel
solution: Experience Manager
title: sel
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 2a679284-9da4-44b6-b495-8e1a47296e7c
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '188'
ht-degree: 2%

---


# sel{#sel}

Wählen Sie das Objekt nach Pixelposition aus.

` sel= *``*, *``*[, *`xylevel`*]`

<table id="simpletable_247FF35D791C43D3AB433B8CF49F8C91"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> x,y  </span> </p> </td> 
  <td class="stentry"> <p>Wählen Sie die Koordinaten der Position in Pixel (int, int). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> Ebene </span> </p> </td> 
  <td class="stentry"> <p>Gruppenebene (int). </p> </td> 
 </tr> 
</table>

Wählt die Gruppe oder das Objekt mit den Pixelkoordinaten aus, die von *`x, y`* angegeben werden, und Beginn ein neues MSS. Wenn sich kein auswählbares Objekt an der Pickposition befindet oder die Pickposition ungültig ist, wird die von `attribute::OnFailSel` angegebene Aktion ausgeführt.

*`level`* gibt an, ob die Gruppe &quot;äußerste Kante&quot;oder ein Drilldown zu einer verschachtelten Gruppe oder einem verschachtelten Objekt ausgewählt werden soll. Wenn *`level`* nicht angegeben ist, wird die äußerste Gruppe ausgewählt. Auf 1 setzen, um eine Gruppenebene unterhalb der äußersten Gruppe auszuwählen. Auf eine große Zahl einstellen (z. B. 99), um das innerste auswählbare Objekt oder die innerste Gruppe auszuwählen.

## Eigenschaften {#section-8f27e84d88734a62a5e398e0c9972bdc}

Auswahlbefehl; MSS-Trennzeichen. Die Objektauswahl ist so lange persistent, bis ein anderes Objekt ausgewählt ist, entweder mit `obj=` oder `sel=`.

*`x, y`* muss zwischen 0, 0 (obere linke Ecke des Bilds) und  *`wid`*-1,  *`hei`*-1 (untere, rechte Ecke des Bilds) liegen, wobei  *`wid`* und  *`hei`* die Größe der nicht skalierten Vignettengröße beträgt.

Wenn angegeben, muss *`level`* 0 oder größer sein.

## Standard {#section-e13c705a3e76468894b4ec190ed8a893}

Keine für *`x, y`*. *`level`* ist standardmäßig 0.

## Verwandte Themen {#section-486842570b4e4bf895f6ccc172ebd8b2}

[obj=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-obj.md#reference-31e7dac7931b4e0eb3c7589f120a1e6a) ,  [wid=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-wid.md#reference-b7e691b0624941168c94b2749ae233ec),  [hei=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-hei.md#reference-1c08f60365a94417a39867c09cac5478),  [attribute::DefaultPix](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-defaultpix.md#reference-102c98f9b5d24d2aaaeb756653fb0e6f),  [attribute::OnFailSel](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-onfailsel.md#reference-f95e4a4a3c02412b87a2b0acca8a5513)
