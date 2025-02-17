---
title: IccRenderIntent
description: Rendering-Intent für Farbkonvertierung. Sie bietet den standardmäßigen Rendering-Intent für Farbkonvertierungen, wenn „icc=" für den Render-Intent nicht angegeben ist.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 732b1935-6556-4420-a056-4e00cb3ed152
source-git-commit: 163ac6a6f44193f1b66ae24059630521d7247eae
workflow-type: tm+mt
source-wordcount: '78'
ht-degree: 3%

---

# IccRenderIntent{#iccrenderintent}

Rendering-Intent für Farbkonvertierung. Stellt den standardmäßigen Rendering-Intent für Farbkonvertierungen bereit, wenn der Render-Intent nicht mit `icc=` angegeben wird.

## Eigenschaften {#section-2540099fb2fc47d29b04642da4f5922a}

Aufzählung. Festgelegt auf 0 für wahrnehmungsorientiert, 1 für relativ farbmetrisch, 2 für Sättigung, 3 für absolut farbmetrisch.

## Standard {#section-61a05067905b44099c228e15de279dbd}

Von `default::IccRenderIntent` geerbt, wenn nicht definiert oder leer.

## Verwandte Themen {#section-7da9ff3038ca452a9f7375a1ca0581af}

[attribute::IccProfile](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilecmyk.md#reference-db89f9dac33e447cadb359ec1ba27ee0) &#42;, [attribute::IccBlackPointCompensation](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccblackpointcompensation.md#reference-357626375ee140d1807f0c05171c733f), [`icc=`](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-icc.md#reference-182b5679e21e4df3b4d330535a5a7517)
