---
title: SEL
description: Objekt nach Pixelposition auswählen.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: fac33287-ebcc-4995-b968-ac377065fdd4
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '189'
ht-degree: 1%

---

# SEL{#sel}

Objekt nach Pixelposition auswählen.

` sel= *`x`*, *`y`*[, *`level`*]`

<table id="simpletable_247FF35D791C43D3AB433B8CF49F8C91"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> x,y </span> </p> </td> 
  <td class="stentry"> <p>Ortskoordinaten in Pixeln (int, int) auswählen. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname">-</span> </p> </td> 
  <td class="stentry"> <p>Gruppenebene (int). </p> </td> 
 </tr> 
</table>

Wählt die Gruppe oder das Objekt mit den durch *`x, y`* angegebenen Pixelkoordinaten aus und startet eine neue MSS. Wenn sich kein auswählbares Objekt an der Entnahmeposition befindet oder die Entnahmeposition ungültig ist, wird die von `attribute::OnFailSel` angegebene Aktion ausgeführt.

*`level`* Gibt an, ob die äußerste Gruppe ausgewählt oder ein Drilldown zu einer verschachtelten Gruppe oder einem verschachtelten Objekt durchgeführt werden soll. Wenn *`level`* nicht angegeben ist, wird die äußerste Gruppe ausgewählt. Wählen Sie mit 1 eine Gruppenebene unterhalb der äußersten Gruppe aus. Legen Sie eine große Zahl (z. B. 99) fest, um das innerste auswählbare Objekt oder die Gruppe auszuwählen.

## Eigenschaften {#section-8f27e84d88734a62a5e398e0c9972bdc}

Auswahlbefehl; MS-Trennzeichen. Die Objektauswahl bleibt so lange bestehen, bis ein anderes Objekt ausgewählt wird, entweder mit `obj=` oder `sel=`.

*`x, y`* Muss im Bereich von 0, 0 (obere linke Ecke des Bildes) bis *`wid`*-1, *`hei`*-1 (untere rechte Ecke des Bildes) liegen, wobei *`wid`* und *`hei`* der Größe der nicht skalierten Vignettenansicht entsprechen.

Wenn angegeben, muss *`level`* 0 oder größer sein.

## Standard {#section-e13c705a3e76468894b4ec190ed8a893}

Keine für *`x, y`*. *`level`* Standardwert ist 0.

## Verwandte Themen {#section-486842570b4e4bf895f6ccc172ebd8b2}

[obj=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-obj.md#reference-31e7dac7931b4e0eb3c7589f120a1e6a) , [wid=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-wid.md#reference-b7e691b0624941168c94b2749ae233ec), [hei=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-hei.md#reference-1c08f60365a94417a39867c09cac5478), [attribute::DefaultPix](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-defaultpix.md#reference-102c98f9b5d24d2aaaeb756653fb0e6f), [attribute::OnFailSel](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-onfailsel.md#reference-f95e4a4a3c02412b87a2b0acca8a5513)
