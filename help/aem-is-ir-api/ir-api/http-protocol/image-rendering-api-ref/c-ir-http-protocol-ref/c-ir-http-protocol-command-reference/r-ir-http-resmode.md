---
description: Resamplingmodus. Wählt den Resampling- und/oder Interpolationsalgorithmus aus, um das gerenderte Bild auf die mit wid=, hei= oder scl= angegebene Größe zu skalieren.
solution: Experience Manager
title: resMode
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 0926dcfe-881c-4b52-b08d-c56afa0ba04d
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '181'
ht-degree: 13%

---

# resMode{#resmode}

Resamplingmodus. Wählt den Resampling- und/oder Interpolationsalgorithmus aus, um das gerenderte Bild auf die mit wid=, hei= oder scl= angegebene Größe zu skalieren.

` `resMode=bilin|bicub|sharp2|bisharp&quot;

<table id="table_AF954C101B30473FAFE9930C7B694305"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="+ topic/ph pr-d/codeph codeph"> bilin  </span> </p> </td> 
   <td colname="col2"> <p>Wählt die standardmäßige bilineare Interpolation aus. Schnellste Neuberechnungsmethode; einige Aliasing-Artefakte sind möglicherweise bemerkbar. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="+ topic/ph pr-d/codeph codeph"> bicub  </span> </p> </td> 
   <td colname="col2"> <p>Wählt bikubische Interpolation aus. CPU-intensiver als bilineare Interpolation, liefert jedoch schärfere Bilder mit weniger deutlichen Aliasing-Artefakten. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="+ topic/ph pr-d/codeph codeph"> sharp2  </span> </p> </td> 
   <td colname="col2"> <p>Wählt eine modifizierte Lanczos-Fensterfunktion als Interpolationsalgorithmus aus. Kann bei höheren CPU-Kosten etwas schärfere Ergebnisse als bikubisch liefern. </p> <p> <span class="codeph"> " </span> scharf"wurde durch " <span class="codeph"> schärfer2"ersetzt,  </span>was die Wahrscheinlichkeit verringert, Aliasing-Artefakte zu verursachen, auch Moiré genannt. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Bischarp  </span> </p> </td> 
   <td colname="col2"> <p>Wählt den standardmäßigen <span class="keyword"> Adobe Photoshop </span>-Resampler zum Reduzieren der Bildgröße aus, der in <span class="keyword"> Adobe Photoshop </span> als "bikubisch schärfer"bezeichnet wird. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschaften {#section-ea7029f37e094d9cb85646b85fbac0ce}

Kann an einer beliebigen Stelle in der Anfrage auftreten. Wird ignoriert, wenn keine endgültige Bildskalierung angewendet wird.

## Standard {#section-900872fb93dc41efb3e8ad5b62aadc38}

`attribute::ResMode`

## Verwandte Themen {#section-16c557a2250e4f04b3e6cbef18add9ce}

[attribute::ResMode](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-cat-resmode.md#reference-fdca7eb6d5104fdeae9d6ac42251db82) ,  [wid=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-wid.md#reference-b7e691b0624941168c94b2749ae233ec),  [hei=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-hei.md#reference-1c08f60365a94417a39867c09cac5478),  [scl=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-scl.md#reference-b14b51a6cbe34f0bba42880540592f29)
