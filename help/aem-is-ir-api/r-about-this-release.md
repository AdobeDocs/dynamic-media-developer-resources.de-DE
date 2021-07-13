---
description: Diese Version - Image Serving 6.6.1 und Image Rendering 6.6.1 - ersetzt Image Serving 6.5.3 und Image Rendering 6.5.3.
solution: Experience Manager
title: Über diese Version
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: f837191b-1151-4c29-8059-b4d3e09e304e
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '125'
ht-degree: 0%

---

# Über diese Version{#about-this-release}

Diese Version - Image Serving 6.6.1 und Image Rendering 6.6.1 - ersetzt Image Serving 6.5.3 und Image Rendering 6.5.3.

## Bekannte Probleme und Verhaltensänderungen {#section-9dbc05206187477f926a78e8108a34e1}

* Die Verwendung des Fragezeichen-Zeichens in Asset-IDs wird nicht mehr unterstützt, auch wenn das Zeichen URL-kodiert ist.
* Dynamische Banner `/xfl/flash/` -Anforderungen werden nicht mehr unterstützt und geben jetzt einen HTTP 404-Fehlercode zurück.
* W2P `/is/agm/` -Anforderungen werden nicht mehr unterstützt.
* Einige Fehlermeldungen werden nicht mehr im Browser gerendert. Daher müssen Sie das Ablaufverfolgungsprotokoll zum Debuggen überprüfen.

## Neue Funktionen {#section-b1386e36cb4544ebb79766a06b16842d}

* Smartes Muster
* Smartes Zuschneiden

## Fehlerbehebung {#section-58dff74d56f64edeadf8f8b97b7a4161}

* Es wurde ein Problem behoben, bei dem die RTF-Option `\qc` gefolgt von einem Leerzeichen dazu führte, dass eine Anforderung nicht gerendert wurde.
