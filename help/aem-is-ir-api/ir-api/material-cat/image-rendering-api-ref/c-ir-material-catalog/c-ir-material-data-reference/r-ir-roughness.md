---
description: Oberflächenrauigkeit. Gibt das relative Glanz der Materialoberfläche an. Wird zusammen mit Katalogtyp und Katalogglanz verwendet, um 3D-Reflexeffekte zu steuern.
solution: Experience Manager
title: Rauigkeit
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 61d956ec-62dd-4879-877e-2ac422396e2e
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '107'
ht-degree: 3%

---

# Rauigkeit{#roughness}

Oberflächenrauigkeit. Gibt das relative Glanz der Materialoberfläche an. Wird zusammen mit catalog::Type und catalog::Gloss verwendet, um 3D-Reflektionseffekte zu steuern.

## Eigenschaften {#section-70c3f2394fd8477ca83a369448907971}

Ganzzahl. Prozentwert im Bereich 0...100. Optional für alle Materialien. Wird nur für Vignetten mit mehreren Reflektionskarten oder Vignetten mit 3D-Reflektionsfunktion verwendet. Leer lassen oder auf -1 setzen, falls nicht bekannt oder nicht erforderlich.

## Standard {#section-c6d5c0613a8745ddbd9f43c8c90b1580}

-1; wird eine Server-Standardeinstellung verwendet.

## Verwandte Themen {#section-d08b59eb76824226b89c6fdf86bb5ce5}

[raw=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-rough.md#reference-00add846b09f4dc39420bda1ca414180) ,  [catalog::Gloss](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-cat-gloss.md#reference-5277f62a67e2408ab94699aa712f1eeb),  [catalog::Type](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-cat-type.md#reference-9bea147dda9f4e74bc0ec79dcc0d9161)
