---
description: Oberflächenrauigkeit. Gibt die relative Glanz der Materialoberfläche an. Wird in Verbindung mit Katalogtyp und Katalogglanz verwendet, um 3D-Reflektionseffekte zu steuern.
seo-description: Oberflächenrauigkeit. Gibt die relative Glanz der Materialoberfläche an. Wird in Verbindung mit Katalogtyp und Katalogglanz verwendet, um 3D-Reflektionseffekte zu steuern.
seo-title: Rauigkeit
solution: Experience Manager
title: Rauigkeit
topic: Dynamic Media Image Serving - Image Rendering API
uuid: d71e4411-dd59-4347-a7c2-132e130ff36b
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '128'
ht-degree: 3%

---


# Rauigkeit{#roughness}

Oberflächenrauigkeit. Gibt die relative Glanz der Materialoberfläche an. Wird in Verbindung mit Katalog::Type and catalog::Gloss verwendet, um 3D-Reflektions-Rendereffekte zu steuern.

## Eigenschaften {#section-70c3f2394fd8477ca83a369448907971}

Ganzzahl. Prozentwert im Bereich 0...100. Optional für alle Materialien. Wird nur für Vignetten mit mehreren Reflexionskarten oder Vignetten mit 3D-Reflektionsfähigkeit verwendet. Leer lassen oder auf -1 setzen, wenn nicht bekannt oder nicht erforderlich.

## Standard {#section-c6d5c0613a8745ddbd9f43c8c90b1580}

-1; Es wird ein Serverstandard verwendet.

## Verwandte Themen {#section-d08b59eb76824226b89c6fdf86bb5ce5}

[raw=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-rough.md#reference-00add846b09f4dc39420bda1ca414180) ,  [catalog::Gloss](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-cat-gloss.md#reference-5277f62a67e2408ab94699aa712f1eeb),  [catalog::Type](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-cat-type.md#reference-9bea147dda9f4e74bc0ec79dcc0d9161)
