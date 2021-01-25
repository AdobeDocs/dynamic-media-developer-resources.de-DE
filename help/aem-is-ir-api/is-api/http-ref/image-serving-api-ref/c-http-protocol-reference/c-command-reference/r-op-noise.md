---
description: hinzufügen Rauschen. Fügt dem Vordergrund oder dem Vordergrund einer Effektebene zufällige Geräusche hinzu.
seo-description: hinzufügen Rauschen. Fügt dem Vordergrund oder dem Vordergrund einer Effektebene zufällige Geräusche hinzu.
seo-title: op_geräusch
solution: Experience Manager
title: op_geräusch
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 531f7a94-149b-4090-a163-a1895156250b
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '111'
ht-degree: 1%

---


# op_geräusch{#op-noise}

hinzufügen Rauschen. Fügt dem Vordergrund oder dem Vordergrund einer Effektebene zufällige Geräusche hinzu.

`op_noise= *``*[,uniform|gaussian[, *`Valmonochrom`*]]`

<table id="table_40675464E5824D52BF392ECCE2DDC03C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> val</span> </p> </td> 
   <td colname="col2"> <p>Rauschmenge in Prozent (0...100 int). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> einheitlich</span> </p> </td> 
   <td colname="col2"> <p>Wählen Sie eine einheitliche Rauschverteilung. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> gaussisch</span> </p> </td> 
   <td colname="col2"> <p>Wählen Sie die gaussische Rauschverteilung. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="varname"> Monochrom</span> </p> </td> 
   <td colname="col2"> <p>Für Farbrauschen auf 0 eingestellt, für Grauschall auf 1. </p> </td> 
  </tr> 
 </tbody> 
</table>

*`monochrome`* bei Graustufenbildern ignoriert.

## Eigenschaften {#section-1f1a64c791f545a3bf1abd0b0e575d87}

Ebene, Befehl. Gilt für die aktuelle Ebene oder für das Composite-Bild, wenn `layer=comp`.

## Standard {#section-d548868fa4b64a60bcb481cad1f8113e}

`op_noise=0,uniform,0`, ohne Lärm.
