---
description: Aktualisiert das mit einem Bild-Asset verknüpfte Bildfeld.
solution: Experience Manager
title: ImageFieldUpdate
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 82bc016b-8a2b-4811-a0b4-1e2a93add3b6
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '56'
ht-degree: 8%

---

# [!DNL ImageFieldUpdate]{#imagefieldupdate}

Aktualisiert das mit einem Bild-Asset verknüpfte Bildfeld.

Syntax

## Parameter {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Name | Typ | Beschreibung |
|---|---|---|
| assetHandle | `xsd:string` | Asset-Handle. |
| [!DNL resolution] | `xsd:double` | Bildauflösung in Pixel pro Zoll. |
| [!DNL anchorX] | `xsd:int` | X-Achsen-Bildanker. |
| [!DNL anchorY] | `xsd:int` | Y-Achsen-Bildanker. |
| [!DNL userData] | `xsd:string` | Wert des Metadatenfelds &quot;`userData`&quot;, das in das Feld für den Bilddienst des Benutzerdatenkatalogfelds veröffentlicht wird. |
