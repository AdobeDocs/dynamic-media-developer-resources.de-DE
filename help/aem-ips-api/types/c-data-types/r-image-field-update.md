---
description: Aktualisiert das mit einem Bild-Asset verknüpfte Bildfeld.
seo-description: Aktualisiert das mit einem Bild-Asset verknüpfte Bildfeld.
seo-title: ImageFieldUpdate
solution: Experience Manager
title: ImageFieldUpdate
topic: Scene7 Image Production System API
uuid: 0262be3e-f840-41cd-bedc-cc37d9982235
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '71'
ht-degree: 8%

---


# ImageFieldUpdate{#imagefieldupdate}

Aktualisiert das mit einem Bild-Asset verknüpfte Bildfeld.

Syntax

## Parameter {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Name | Typ | Beschreibung |
|---|---|---|
| ` *`assetHandle`*` | `xsd:string` | Asset-Handle. |
| ` *`resolution`*` | `xsd:double` | Bildauflösung in Pixel pro Zoll |
| ` *`anchorX`*` | `xsd:int` | X-Achsen-Bildanker. |
| ` *`anchorY`*` | `xsd:int` | Y-Achsen-Bildanker. |
| ` *`Benutzerdaten`*` | `xsd:string` | Wert des Metadatenfelds `userData`, das im Feld für das Image Serving-Benutzerdatenkatalog veröffentlicht wird. |

