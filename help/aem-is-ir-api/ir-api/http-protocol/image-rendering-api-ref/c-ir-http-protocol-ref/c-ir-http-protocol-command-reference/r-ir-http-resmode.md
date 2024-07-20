---
title: resMode
description: Resamplingmodus. Wählt den Resampling- und/oder Interpolationsalgorithmus aus, um das gerenderte Bild auf die mit wid=, hei= oder scl= angegebene Größe zu skalieren.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 0926dcfe-881c-4b52-b08d-c56afa0ba04d
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '171'
ht-degree: 7%

---

# resMode{#resmode}

Resamplingmodus. Wählt den Resampling- und/oder Interpolationsalgorithmus für die Skalierung des gerenderten Bildes auf die mit `wid=`, `hei=` oder `scl=` angegebene Größe aus.

` `resMode=bilin|bicub|sharp2|bisharp&quot;

<table id="table_AF954C101B30473FAFE9930C7B694305"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="+ topic/ph pr-d/codeph codeph"> bilin </span> </p> </td> 
   <td colname="col2"> <p>Wählt die standardmäßige bilaterale Interpolation aus. Schnellste Neuberechnungsmethode; einige Aliasing-Artefakte sind möglicherweise bemerkbar. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="+ topic/ph pr-d/codeph codeph"> bicub </span> </p> </td> 
   <td colname="col2"> <p>Wählt bikubische Interpolation aus. CPU-intensiver als bilineare Interpolation, liefert jedoch schärfere Bilder mit weniger deutlichen Aliasing-Artefakten. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="+ topic/ph pr-d/codeph codeph"> sharp2 </span> </p> </td> 
   <td colname="col2"> <p>Wählt eine modifizierte Lanczos Window-Funktion als Interpolationsalgorithmus aus. Kann bei höheren CPU-Kosten etwas schärfere Ergebnisse als bikubisch liefern. </p> <p> <span class="codeph"> scharf </span> wurde durch <span class="codeph"> scharf2 </span> ersetzt, was eine geringere Wahrscheinlichkeit hat, Aliasing-Artefakte zu verursachen, auch Moiré genannt. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> bisharp </span> </p> </td> 
   <td colname="col2"> <p>Wählt den standardmäßigen Resampler <span class="keyword"> Adobe Photoshop </span> zur Reduzierung der Bildgröße aus, der in <span class="keyword"> Adobe Photoshop </span> als "bikubische Scharfzeichnung"bezeichnet wird. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschaften {#section-ea7029f37e094d9cb85646b85fbac0ce}

Kann an einer beliebigen Stelle in der Anfrage auftreten. Wird ignoriert, wenn keine endgültige Bildskalierung angewendet wird.

## Standard {#section-900872fb93dc41efb3e8ad5b62aadc38}

`attribute::ResMode`

## Verwandte Themen {#section-16c557a2250e4f04b3e6cbef18add9ce}

[attribute::ResMode](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-cat-resmode.md#reference-fdca7eb6d5104fdeae9d6ac42251db82) , [wid=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-wid.md#reference-b7e691b0624941168c94b2749ae233ec), [hei=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-hei.md#reference-1c08f60365a94417a39867c09cac5478), [scl=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-scl.md#reference-b14b51a6cbe34f0bba42880540592f29)
