---
title: op_rauschen
description: Rauschen hinzufügen. Fügt den Vordergrundbilddaten oder dem Vordergrund einer Effektebene Rauschen hinzu.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: eeadd3ab-80ff-4f9b-b5b7-4f3da6feebde
source-git-commit: 7a07ec9550c0685c908191dd6806d5b84678820d
workflow-type: tm+mt
source-wordcount: '93'
ht-degree: 1%

---

# op_rauschen{#op-noise}

Rauschen hinzufügen. Fügt den Vordergrundbilddaten oder dem Vordergrund einer Effektebene Rauschen hinzu.

`op_noise= *`val`*[,uniform|gaussian[, *`monochrome`*]]`

<table id="table_40675464E5824D52BF392ECCE2DDC03C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> Val</span> </p> </td> 
   <td colname="col2"> <p>Geräuschmenge in Prozent (0…100 int). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> Uniform</span> </p> </td> 
   <td colname="col2"> <p>Wählen Sie eine gleichmäßige Rauschverteilung. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> Gaussian</span> </p> </td> 
   <td colname="col2"> <p>Gaußsche Rauschverteilung auswählen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="varname"> monochrom</span> </p> </td> 
   <td colname="col2"> <p>Festlegung auf 0 für Farbrauschen, 1 für Grauraurauschen. </p> </td> 
  </tr> 
 </tbody> 
</table>

*`monochrome`* wird bei Graustufenbildern ignoriert.

## Eigenschaften {#section-1f1a64c791f545a3bf1abd0b0e575d87}

Ebenenbefehl. Gilt für die aktuelle Ebene oder das zusammengesetzte Bild, falls `layer=comp`.

## Standard {#section-d548868fa4b64a60bcb481cad1f8113e}

`op_noise=0,uniform,0`, für keinen Lärm.
