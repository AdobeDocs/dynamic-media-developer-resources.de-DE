---
title: IccRenderIntent
description: Farbkonvertierung - Rendering-Absicht. Stellt die standardmäßige Rendering-Absicht für Farbkonvertierungen bereit, wenn der Rendering-Intent nicht mit icc= angegeben ist.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 86cc907d-556c-40ec-a104-2f0dcf9ed1ce
source-git-commit: 8454991568374ecd1c4babdd3210250ea7988c4c
workflow-type: tm+mt
source-wordcount: '93'
ht-degree: 4%

---

# IccRenderIntent{#iccrenderintent}

Farbkonvertierung - Rendering-Absicht. Stellt die standardmäßige Rendering-Absicht für Farbkonvertierungen bereit, wenn die Renderpriorität nicht mit `icc=`.

## Eigenschaften {#section-0a38c60e1525426185616c42824aee2c}

Enum. Setzen Sie den Wert auf 0 für wahrnehmungsorientiert, 1 für relativ farbmetrisch, 2 für Sättigung, 3 für absolut farbmetrisch. Leer lassen oder auf einen anderen Wert setzen, um den im Farbprofil definierten Standard-Rendering-Intent zu verwenden.

## Standard {#section-9301e3b7d0184ec5bf54a6eb73a6d3c1}

Vererbt von `default::IccRenderIntent`falls nicht definiert. Wenn leer, wird &quot;relativ farbmetrisch&quot;angewendet.

## Verwandte Themen {#section-e77bcdfef6d2486ebd545631ccb40ebd}

[attribute::IccProfile*](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccprofilecmyk.md#reference-55aead2d924847ffbd1be4c46add7127) , [attribute::IccBlackPointCompensation](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccblackpointcompensation.md#reference-d939b0cdf6564baaa88deb1059e3b7f0), [icc=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-icc.md#reference-86a2fff3cef24982ad2063d977a16e06)
