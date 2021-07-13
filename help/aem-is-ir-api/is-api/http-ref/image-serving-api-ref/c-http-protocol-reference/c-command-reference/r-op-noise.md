---
description: Rauschen hinzufügen. Fügt zufällige Geräusche zu den Vordergrundbilddaten oder zum Vordergrund einer Effektebene hinzu.
solution: Experience Manager
title: op_geräusch
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: eeadd3ab-80ff-4f9b-b5b7-4f3da6feebde
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '96'
ht-degree: 2%

---

# op_geräusch{#op-noise}

Rauschen hinzufügen. Fügt zufällige Geräusche zu den Vordergrundbilddaten oder zum Vordergrund einer Effektebene hinzu.

`op_noise= *``*[,uniform|gaussian[, *`Valmonochrome`*]]`

<table id="table_40675464E5824D52BF392ECCE2DDC03C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> val</span> </p> </td> 
   <td colname="col2"> <p>Rauschmenge in Prozent (0...100 int). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> einheitlich</span> </p> </td> 
   <td colname="col2"> <p>Wählen Sie die gleichmäßige Rauschverteilung aus. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> gaussisch</span> </p> </td> 
   <td colname="col2"> <p>Wählen Sie die gaussische Rauschverteilung aus. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="varname"> monochrome</span> </p> </td> 
   <td colname="col2"> <p>Für Farbrauschen auf 0, für Grauschärfe auf 1 gesetzt. </p> </td> 
  </tr> 
 </tbody> 
</table>

*`monochrome`* wird bei Graustufenbildern ignoriert.

## Eigenschaften {#section-1f1a64c791f545a3bf1abd0b0e575d87}

Ebenenbefehl. Gilt für die aktuelle Ebene oder für das zusammengesetzte Bild, wenn `layer=comp`

## Standard {#section-d548868fa4b64a60bcb481cad1f8113e}

`op_noise=0,uniform,0`, ohne Rauschen.
