---
description: Datendateien mit statischen Inhalten werden nur vom Plattformserver aufgerufen.
seo-description: Datendateien mit statischen Inhalten werden nur vom Plattformserver aufgerufen.
seo-title: Statische Inhaltsquellendaten
solution: Experience Manager
title: Statische Inhaltsquellendaten
topic: Scene7 Image Serving - Image Rendering API
uuid: a3280ce7-20d7-4f4b-bf3e-e77cc7aca35f
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '135'
ht-degree: 0%

---


# Statische Inhaltsquellendaten{#static-content-source-data}

Datendateien mit statischen Inhalten werden nur vom Plattformserver aufgerufen.

Der Pfad für Datendateien mit statischen Inhalten wird wie folgt aufgelöst:

`PS::staticContent.rootPaths/attribute::StaticContentRootPath/static::Path`

Der Server kombiniert Pfadsegmente von rechts nach links, bis ein absoluter Dateipfad festgelegt ist.

Alle ` *[!DNL rootPath]*`-Segmente können leere, relative oder absolute Pfadsegmente sein.

` *[!DNL catalogPath]*` ist entweder ein absoluter oder ein relativer Dateipfad/Name. *[!DNL requestPath]* muss ein relativer Dateipfad/Name sein.

Mehrere `PS::staticContent.rootPaths`-Werte können in [!DNL PlatformServer.conf] definiert werden. Dadurch können Quelldatendateien über mehrere Dateisysteme verteilt werden. Der Plattformserver versucht alternative Pfade in der angegebenen Reihenfolge zu verwenden, bis die Datendatei gefunden wurde.
