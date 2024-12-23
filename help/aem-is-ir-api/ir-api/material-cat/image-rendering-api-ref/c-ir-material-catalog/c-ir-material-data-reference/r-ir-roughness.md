---
description: Oberflächenrauheit. Gibt den relativen Glanz der Materialoberfläche an. Wird zusammen mit Katalogtyp und Katalogglanz verwendet, um 3D-Reflexions-Rendereffekte zu steuern.
solution: Experience Manager
title: Raueit
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 61d956ec-62dd-4879-877e-2ac422396e2e
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '106'
ht-degree: 2%

---

# Raueit{#roughness}

Oberflächenrauheit. Gibt den relativen Glanz der Materialoberfläche an. Wird zusammen mit catalog::Type und catalog::gloss verwendet, um die Rendereffekte der 3D-Reflexion zu steuern.

## Eigenschaften {#section-70c3f2394fd8477ca83a369448907971}

Ganze Zahl. Prozentwert im Bereich 0 bis 100. Optional für alle Materialien. Wird nur für Vignetten mit mehreren Reflexionskarten oder Vignetten mit 3D-Reflexionsfähigkeit verwendet. Leer lassen oder auf -1 setzen, falls nicht bekannt oder nicht benötigt.

## Standard {#section-c6d5c0613a8745ddbd9f43c8c90b1580}

-1; es wird ein Server-Standard verwendet.

## Verwandte Themen {#section-d08b59eb76824226b89c6fdf86bb5ce5}

[raw=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-rough.md#reference-00add846b09f4dc39420bda1ca414180) , [catalog::gloss](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-cat-gloss.md#reference-5277f62a67e2408ab94699aa712f1eeb), [catalog::Type](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-cat-type.md#reference-9bea147dda9f4e74bc0ec79dcc0d9161)
