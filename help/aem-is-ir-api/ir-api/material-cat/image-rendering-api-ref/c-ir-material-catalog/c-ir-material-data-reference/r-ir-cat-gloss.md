---
description: Oberflächenglanz Gibt den relativen Glanz der Materialoberfläche an.
solution: Experience Manager
title: Glanz
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 72c5d2f9-a7e6-4ad3-aebe-6a1b1fa5453f
TQID: 'https://experienceleague.adobe.com/Q1mOPjFXFnSPVRsvYpKs3a-15g1BfxQRCsFaMRBZNTw'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 49c3ac586f6fb17608838f8dcf2c637822314fc7
workflow-type: tm+mt
source-wordcount: 121
ht-degree: 2%

---

# Glanz{#gloss}

Oberflächenglanz Gibt den relativen Glanz der Materialoberfläche an.

Dieser Wert wird vom Renderer für die folgenden Zwecke verwendet:

* Wählen Sie die Beleuchtungskarte, wenn `catalog::Illum` -1 ist.
* Steuert das Rendering des Glanzeffekts (Spiegelreflexion) in Verbindung mit `catalog::Type`.
* Steuert 3D-Reflexions-Rendereffekte in Verbindung mit `catalog::Type` und `catalog::Roughness`.

## Eigenschaften {#section-ddc475c0556f4f67b4cf62bd1bcd4bf7}

Ganze Zahl. Prozentzahl im Bereich 0 bis 100. Optional für alle Materialien. Wird nur für Vignetten mit mehreren Reflexionskarten oder Vignetten mit 3D-Reflexionsfähigkeit verwendet. Leer lassen oder auf -1 setzen, falls nicht bekannt oder nicht benötigt.

## Standard {#section-2352721073524f1a8d461f64a363aac9}

Ein Standardwert wird von der Vignette bereitgestellt, wenn dieser Wert auf -1 festgelegt ist.

## Verwandte Themen {#section-0213bbdb7d6d4974a7c53822957717c1}

[gloss=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-gloss.md#reference-325aef2ee51e4e1584a06047427340ca) , [catalog::rauHness](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-roughness.md#reference-79f748ac642745e3b81795a99f61fa99), [catalog::type](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-cat-type.md#reference-9bea147dda9f4e74bc0ec79dcc0d9161)

