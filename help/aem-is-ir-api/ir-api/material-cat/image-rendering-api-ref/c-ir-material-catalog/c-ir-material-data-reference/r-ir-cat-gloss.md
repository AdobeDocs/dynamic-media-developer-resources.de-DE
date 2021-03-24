---
description: Oberflächenglanz Gibt die relative Glanz der Materialoberfläche an.
solution: Experience Manager
title: Glanz
feature: Dynamic Media Classic, SDK/API
role: Entwickler, Geschäftspraktiker
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '124'
ht-degree: 3%

---


# Glanz{#gloss}

Oberflächenglanz Gibt die relative Glanz der Materialoberfläche an.

Dieser Wert wird vom Renderer für folgende Zwecke verwendet:

* Wählen Sie die Beleuchtungskarte aus, wenn `catalog::Illum` -1 ist.
* Steuert das Rendern des Glanz-Effekts (Spiegelreflexion) in Verbindung mit `catalog::Type`.
* Steuert 3D-Reflektionseffekte in Verbindung mit `catalog::Type` und `catalog::Roughness`.

## Eigenschaften {#section-ddc475c0556f4f67b4cf62bd1bcd4bf7}

Ganzzahl. Prozentzahl im Bereich 0...100. Optional für alle Materialien. Wird nur für Vignetten mit mehreren Reflexionskarten oder Vignetten mit 3D-Reflektionsfähigkeit verwendet. Leer lassen oder auf -1 setzen, wenn nicht bekannt oder nicht erforderlich.

## Standard {#section-2352721073524f1a8d461f64a363aac9}

Ein Standardwert wird von der Vignette bereitgestellt, wenn dieser Wert auf -1 festgelegt ist.

## Verwandte Themen {#section-0213bbdb7d6d4974a7c53822957717c1}

[gloss=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-gloss.md#reference-325aef2ee51e4e1584a06047427340ca) ,  [catalog::Roughness](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-roughness.md#reference-79f748ac642745e3b81795a99f61fa99),  [catalog::Type](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-cat-type.md#reference-9bea147dda9f4e74bc0ec79dcc0d9161)
