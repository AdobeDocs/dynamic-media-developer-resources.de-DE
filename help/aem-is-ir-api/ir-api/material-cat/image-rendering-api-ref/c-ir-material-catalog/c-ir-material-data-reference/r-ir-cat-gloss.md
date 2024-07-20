---
description: Oberflächenglanz Gibt das relative Glanz der Materialoberfläche an.
solution: Experience Manager
title: Glanz
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 72c5d2f9-a7e6-4ad3-aebe-6a1b1fa5453f
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '121'
ht-degree: 2%

---

# Glanz{#gloss}

Oberflächenglanz Gibt das relative Glanz der Materialoberfläche an.

Dieser Wert wird vom Renderer für die folgenden Zwecke verwendet:

* Wählen Sie die Beleuchtungskarte aus, wenn `catalog::Illum` -1 ist.
* Steuert das Rendering des Glanzeffekts (spekuläre Reflexion) in Verbindung mit `catalog::Type`.
* Steuert die 3D-Reflektion in Verbindung mit `catalog::Type` und `catalog::Roughness`.

## Eigenschaften {#section-ddc475c0556f4f67b4cf62bd1bcd4bf7}

Ganzzahl. Prozentzahl im Bereich 0...100. Optional für alle Materialien. Wird nur für Vignetten mit mehreren Reflektionskarten oder Vignetten mit 3D-Reflektionsfunktion verwendet. Leer lassen oder auf -1 setzen, falls nicht bekannt oder nicht erforderlich.

## Standard {#section-2352721073524f1a8d461f64a363aac9}

Ein Standardwert wird von der Vignette bereitgestellt, wenn dieser Wert auf -1 festgelegt ist.

## Verwandte Themen {#section-0213bbdb7d6d4974a7c53822957717c1}

[gloss=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-gloss.md#reference-325aef2ee51e4e1584a06047427340ca) , [catalog::Roughness](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-roughness.md#reference-79f748ac642745e3b81795a99f61fa99), [catalog::Type](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-cat-type.md#reference-9bea147dda9f4e74bc0ec79dcc0d9161)
