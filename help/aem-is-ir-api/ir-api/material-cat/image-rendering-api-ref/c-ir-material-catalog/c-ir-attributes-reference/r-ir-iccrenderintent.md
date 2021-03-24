---
description: Renderpriorität für Farbkonvertierung. Stellt die standardmäßige Renderpriorität für Farbkonvertierungen bereit, wenn die Renderpriorität nicht mit icc= angegeben wurde.
solution: Experience Manager
title: IccRenderIntent
feature: Dynamic Media Classic, SDK/API
role: Entwickler, Geschäftspraktiker
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '104'
ht-degree: 3%

---


# IccRenderIntent{#iccrenderintent}

Renderpriorität für Farbkonvertierung. Stellt die standardmäßige Renderpriorität für Farbkonvertierungen bereit, wenn die Renderpriorität nicht mit icc= angegeben wurde.

## Eigenschaften {#section-0a38c60e1525426185616c42824aee2c}

Enum. Für die Wahrnehmbarkeit auf 0 gesetzt, für die relative Farbmetrik auf 1, für die Sättigung auf 2, für die absolute Farbmetrik auf 3. Lassen Sie den Wert leer oder legen Sie ihn auf einen anderen Wert fest, um die im Profil &quot;Farbe&quot;definierte standardmäßige Renderpriorität zu verwenden.

## Standard {#section-9301e3b7d0184ec5bf54a6eb73a6d3c1}

Vererbt von `default::IccRenderIntent`wenn nicht definiert. Ist der Wert leer, wird &quot;relativ farbmetrisch&quot;angewendet.

## Verwandte Themen {#section-e77bcdfef6d2486ebd545631ccb40ebd}

[attribute::IccProfile*](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccprofilecmyk.md#reference-55aead2d924847ffbd1be4c46add7127) ,  [attribute::IccBlackPointCompensation](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccblackpointcompensation.md#reference-d939b0cdf6564baaa88deb1059e3b7f0),  [icc=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-icc.md#reference-86a2fff3cef24982ad2063d977a16e06)
