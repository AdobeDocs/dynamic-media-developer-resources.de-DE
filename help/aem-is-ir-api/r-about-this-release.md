---
description: Diese Version - Image Serving 6.6.1 und Image Rendering 6.6.1 - ersetzt Image Serving 6.5.3 und Image Rendering 6.5.3.
solution: Experience Manager
title: Über diese Version
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '128'
ht-degree: 0%

---


# Über diese Version{#about-this-release}

Diese Version - Image Serving 6.6.1 und Image Rendering 6.6.1 - ersetzt Image Serving 6.5.3 und Image Rendering 6.5.3.

## Bekannte Probleme und Verhaltensänderungen {#section-9dbc05206187477f926a78e8108a34e1}

* Die Verwendung des Fragezeichen in Asset-IDs wird nicht mehr unterstützt, auch wenn das Zeichen URL-kodiert ist.
* Dynamische Banner `/xfl/flash/`-Anforderungen werden nicht mehr unterstützt und geben jetzt einen http 404-Fehlercode zurück.
* W2P `/is/agm/`-Anforderungen werden nicht mehr unterstützt.
* Einige Fehlermeldungen werden nicht mehr an den Browser gerendert. Daher müssen Sie das Ablaufverfolgungsprotokoll überprüfen, um zu debuggen.

## Neue Funktionen {#section-b1386e36cb4544ebb79766a06b16842d}

* Smart-Muster
* Intelligente Beschneidung

## Fehlerbehebung {#section-58dff74d56f64edeadf8f8b97b7a4161}

* Korrektur des Problems, bei dem die RTF-Option `\qc` gefolgt von einem Leerzeichen dazu führte, dass eine Anforderung nicht gerendert wurde.

