---
description: Aktualisiert das Bildfeld, das mit einem Bild-Asset verknüpft ist.
solution: Experience Manager
title: ImageFieldUpdate
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 82bc016b-8a2b-4811-a0b4-1e2a93add3b6
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '61'
ht-degree: 11%

---

# ImageFieldUpdate{#imagefieldupdate}

Aktualisiert das Bildfeld, das mit einem Bild-Asset verknüpft ist.

Syntax

## Parameter {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Name | Typ | Beschreibung |
|---|---|---|
| assetHandle | `xsd:string` | Asset-Handle. |
| Auflösung | `xsd:double` | Bildauflösung in Pixel pro Zoll. |
| anchorX | `xsd:int` | X-Achsen-Bildanker. |
| anchorY | `xsd:int` | Y-Achsen-Bildanker. |
| Benutzerdaten | `xsd:string` | Wert von `userData` Metadatenfeld, das im Feld für den Bilddienst des Benutzerdatenkatalogfelds veröffentlicht wird. |
