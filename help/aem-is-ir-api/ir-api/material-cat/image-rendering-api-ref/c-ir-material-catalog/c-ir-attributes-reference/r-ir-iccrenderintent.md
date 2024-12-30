---
title: IccRenderIntent
description: Rendering-Intent für Farbkonvertierung. Sie bietet den standardmäßigen Rendering-Intent für Farbkonvertierungen, wenn der Render-Intent nicht mit „icc=" angegeben ist.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 86cc907d-556c-40ec-a104-2f0dcf9ed1ce
source-git-commit: 163ac6a6f44193f1b66ae24059630521d7247eae
workflow-type: tm+mt
source-wordcount: '100'
ht-degree: 3%

---

# IccRenderIntent{#iccrenderintent}

Rendering-Intent für Farbkonvertierung. Stellt den standardmäßigen Rendering-Intent für Farbkonvertierungen bereit, wenn der Render-Intent nicht mit `icc=` angegeben wird.

## Eigenschaften {#section-0a38c60e1525426185616c42824aee2c}

Aufzählung. Festgelegt auf 0 für wahrnehmungsorientiert, 1 für relativ farbmetrisch, 2 für Sättigung, 3 für absolut farbmetrisch. Lassen Sie es leer oder legen Sie einen beliebigen anderen Wert fest, damit Sie den standardmäßigen Rendering-Intent verwenden können, der im Farbprofil definiert ist.

## Standard {#section-9301e3b7d0184ec5bf54a6eb73a6d3c1}

Vererbt von (`default::IccRenderIntent` nicht definiert). Wenn leer, wird „relativ farbmetrisch“ angewendet.

## Verwandte Themen {#section-e77bcdfef6d2486ebd545631ccb40ebd}

[attribute::IccProfile*](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccprofilecmyk.md#reference-55aead2d924847ffbd1be4c46add7127) , [attribute::IccBlackPointCompensation](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccblackpointcompensation.md#reference-d939b0cdf6564baaa88deb1059e3b7f0), [`icc=`](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-icc.md#reference-86a2fff3cef24982ad2063d977a16e06)
