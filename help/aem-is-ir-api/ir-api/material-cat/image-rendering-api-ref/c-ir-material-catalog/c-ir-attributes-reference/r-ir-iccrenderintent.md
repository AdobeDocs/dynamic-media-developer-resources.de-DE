---
title: IccRenderIntent
description: Rendering-Intent für Farbkonvertierung. Sie bietet den standardmäßigen Rendering-Intent für Farbkonvertierungen, wenn der Render-Intent nicht mit „icc=" angegeben ist.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 86cc907d-556c-40ec-a104-2f0dcf9ed1ce
TQID: 'https://experienceleague.adobe.com/5BehWh36v-kv7Z8kSj-WwoqBgyk4TC8srAhxKs89mnE'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 4339f336345d7d7f3c05c7f5a18fbd28bcfd382b
workflow-type: tm+mt
source-wordcount: 101
ht-degree: 2%

---

# IccRenderIntent{#iccrenderintent}

Rendering-Intent für Farbkonvertierung. Stellt den standardmäßigen Rendering-Intent für Farbkonvertierungen bereit, wenn der Render-Intent nicht mit `icc=` angegeben wird.

## Eigenschaften {#section-0a38c60e1525426185616c42824aee2c}

Aufzählung. Festgelegt auf 0 für wahrnehmungsorientiert, 1 für relativ farbmetrisch, 2 für Sättigung, 3 für absolut farbmetrisch. Lassen Sie es leer oder legen Sie einen beliebigen anderen Wert fest, damit Sie den standardmäßigen Rendering-Intent verwenden können, der im Farbprofil definiert ist.

## Standard {#section-9301e3b7d0184ec5bf54a6eb73a6d3c1}

Vererbt von (`default::IccRenderIntent` nicht definiert). Wenn leer, wird „relativ farbmetrisch“ angewendet.

## Verwandte Themen {#section-e77bcdfef6d2486ebd545631ccb40ebd}

[attribute::IccProfile*](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccprofilecmyk.md#reference-55aead2d924847ffbd1be4c46add7127) , [attribute::IccBlackPointCompensation](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccblackpointcompensation.md#reference-d939b0cdf6564baaa88deb1059e3b7f0), [`icc=`](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-icc.md#reference-86a2fff3cef24982ad2063d977a16e06)

