---
description: Diese Version - Image Serving 6.6.1 und Image Rendering 6.6.1 - ersetzt Image Serving 6.5.3 und Image Rendering 6.5.3.
solution: Experience Manager
title: Über diese Version
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: f837191b-1151-4c29-8059-b4d3e09e304e
TQID: 'https://experienceleague.adobe.com/Mv84kHB7jsBYAvY1j--l8Ly5VZtKwFq-SsNdz2TIQOE'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: null
workflow-type: tm+mt
source-wordcount: 130
ht-degree: 0%

---

# Über diese Version{#about-this-release}

Diese Version - Image Serving 6.6.1 und Image Rendering 6.6.1 - ersetzt Image Serving 6.5.3 und Image Rendering 6.5.3.

## Bekannte Probleme und Verhaltensänderungen {#section-9dbc05206187477f926a78e8108a34e1}

* Die Verwendung des Fragezeichen-Zeichens in Asset-IDs wird nicht mehr unterstützt, auch wenn das Zeichen URL-kodiert ist.
* Dynamische `/xfl/flash/` werden nicht mehr unterstützt und geben jetzt einen HTTP 404-Fehler-Code zurück.
* W2P-`/is/agm/` werden nicht mehr unterstützt.
* Einige Fehlermeldungen werden nicht mehr im Browser angezeigt. Daher müssen Sie zum Debuggen das Ablaufverfolgungsprotokoll überprüfen.

## Neue Funktionen {#section-b1386e36cb4544ebb79766a06b16842d}

* Smartes Farb-/Bildmuster
* Smartes Zuschneiden

## Fehlerbehebung {#section-58dff74d56f64edeadf8f8b97b7a4161}

* Es wurde ein Problem behoben, bei dem die `\qc` RTF-Option gefolgt von einem Leerzeichen dazu führte, dass eine Anfrage nicht gerendert wurde.
