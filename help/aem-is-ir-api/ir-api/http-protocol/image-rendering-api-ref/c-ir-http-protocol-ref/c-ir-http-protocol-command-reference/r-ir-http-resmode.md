---
description: Resamplingmodus. Wählt den Resampling- und/oder Interpolationsalgorithmus für die Skalierung des gerenderten Bildes auf die mit wid=, hei= oder scl= angegebene Größe aus.
seo-description: Resamplingmodus. Wählt den Resampling- und/oder Interpolationsalgorithmus für die Skalierung des gerenderten Bildes auf die mit wid=, hei= oder scl= angegebene Größe aus.
seo-title: resMode
solution: Experience Manager
title: resMode
topic: Scene7 Image Serving - Image Rendering API
uuid: 106da74a-d7da-4998-a719-c4c69ae36f6b
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '203'
ht-degree: 12%

---


# resMode{#resmode}

Resamplingmodus. Wählt den Resampling- und/oder Interpolationsalgorithmus für die Skalierung des gerenderten Bildes auf die mit wid=, hei= oder scl= angegebene Größe aus.

` `resMode=bilin|bicub|sharp2|bisharp&quot;

<table id="table_AF954C101B30473FAFE9930C7B694305"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="+ topic/ph pr-d/codeph codeph"> bilin  </span> </p> </td> 
   <td colname="col2"> <p>Wählt die standardmäßige bilineare Interpolation aus. Schnellste Neuberechnungsmethode; einige Aliasing-Artefakte sind möglicherweise bemerkbar. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="+ topic/ph pr-d/codeph codeph"> bicub  </span> </p> </td> 
   <td colname="col2"> <p>Wählt bikubische Interpolation aus. CPU-intensiver als bilineare Interpolation, liefert aber schärfere Bilder mit weniger bemerkbaren Aliasing-Artefakten. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="+ topic/ph pr-d/codeph codeph"> sharp2  </span> </p> </td> 
   <td colname="col2"> <p>Wählt eine modifizierte Lanczos-Fensterfunktion als Interpolationsalgorithmus aus. Kann etwas schärfere Ergebnisse liefern als bikubisch bei höheren CPU-Kosten. </p> <p> <span class="codeph"> "sharp" </span> wurde durch " <span class="codeph"> sharp2"ersetzt  </span>, was eine geringere Wahrscheinlichkeit hat, Aliasing-Artefakte zu verursachen, auch bekannt als Moiré. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Bisharp  </span> </p> </td> 
   <td colname="col2"> <p>Wählt den standardmäßigen Resampler <span class="keyword"> Adobe Photoshop </span> zum Reduzieren der Bildgröße aus, der unter <span class="keyword"> Adobe Photoshop </span> als "bikubischer Scharfzeichner"bezeichnet wird. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschaften {#section-ea7029f37e094d9cb85646b85fbac0ce}

Kann an einer beliebigen Stelle innerhalb der Anforderung auftreten. Wird ignoriert, wenn keine endgültige Bildskalierung angewendet wird.

## Standard {#section-900872fb93dc41efb3e8ad5b62aadc38}

`attribute::ResMode`

## Verwandte Themen {#section-16c557a2250e4f04b3e6cbef18add9ce}

[attribute::ResMode](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-cat-resmode.md#reference-fdca7eb6d5104fdeae9d6ac42251db82) ,  [wid=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-wid.md#reference-b7e691b0624941168c94b2749ae233ec),  [hei=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-hei.md#reference-1c08f60365a94417a39867c09cac5478),  [scl=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-scl.md#reference-b14b51a6cbe34f0bba42880540592f29)
