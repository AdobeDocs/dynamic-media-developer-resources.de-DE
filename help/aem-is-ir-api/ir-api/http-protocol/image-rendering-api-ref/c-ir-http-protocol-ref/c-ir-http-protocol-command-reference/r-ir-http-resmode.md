---
title: resMode
description: Resampling-Modus. Wählt den Resampling- und/oder Interpolationsalgorithmus aus, um das gerenderte Bild auf die mit wid=, hei= oder scl= angegebene Größe zu skalieren.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 0926dcfe-881c-4b52-b08d-c56afa0ba04d
TQID: 'https://experienceleague.adobe.com/VLg7JU1aiA7tRGG6vmoHciv-hDIZftbYtU4hAE5N0DY'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 70c478ebbe0b38d9e35c1bb26074a458c0197b2b
workflow-type: tm+mt
source-wordcount: 172
ht-degree: 6%

---

# resMode{#resmode}

Resampling-Modus. Wählt den Resampling- und/oder Interpolationsalgorithmus aus, um das gerenderte Bild auf die mit `wid=`, `hei=` oder `scl=` angegebene Größe zu skalieren.

` `resMode=bilin|bicub|sharp2|bisharp“

<table id="table_AF954C101B30473FAFE9930C7B694305"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="+ topic/ph pr-d/codeph codeph"> Bilin </span> </p> </td> 
   <td colname="col2"> <p>Wahl der standardmäßigen bilinearen Interpolation Schnellste Neuberechnungsmethode; einige Aliasing-Artefakte sind möglicherweise bemerkbar. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="+ topic/ph pr-d/codeph codeph"> Bicub-</span> </p> </td> 
   <td colname="col2"> <p>Wählt bikubische Interpolation. CPU-intensiver als bilineare Interpolation, liefert jedoch schärfere Bilder mit weniger bemerkbaren Aliasing-Artefakten. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="+ topic/ph pr-d/codeph codeph"> Sharp2-</span> </p> </td> 
   <td colname="col2"> <p>Wählt eine modifizierte Lanczos-Fensterfunktion als Interpolationsalgorithmus. Kann zu einem höheren CPU-Preis etwas schärfere Ergebnisse als bikubisch liefern. </p> <p> <span class="codeph"> scharfe </span> wurde durch <span class="codeph"> scharfe2-</span> ersetzt, wodurch die Wahrscheinlichkeit, Alias-Artefakte zu verursachen, geringer ist (auch bekannt als Moiré). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Bisharp </span> </p> </td> 
   <td colname="col2"> <p>Wählt das <span class="keyword"> Adobe Photoshop </span> standardmäßige Resampler zur Reduzierung der Bildgröße aus, das in <span class="keyword"> Adobe Photoshop-</span> als „bikubisch schärfer“ bezeichnet wird. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschaften {#section-ea7029f37e094d9cb85646b85fbac0ce}

Kann überall in der Anfrage auftreten. Wird ignoriert, wenn keine endgültige Bildskalierung angewendet wird.

## Standard {#section-900872fb93dc41efb3e8ad5b62aadc38}

`attribute::ResMode`

## Verwandte Themen {#section-16c557a2250e4f04b3e6cbef18add9ce}

[attribute::ResMode](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-cat-resmode.md#reference-fdca7eb6d5104fdeae9d6ac42251db82) , [wid=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-wid.md#reference-b7e691b0624941168c94b2749ae233ec), [hei=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-hei.md#reference-1c08f60365a94417a39867c09cac5478), [scl=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-scl.md#reference-b14b51a6cbe34f0bba42880540592f29)

