---
description: Datendateien mit statischen Inhalten werden nur vom Plattformserver aufgerufen.
seo-description: Datendateien mit statischen Inhalten werden nur vom Plattformserver aufgerufen.
seo-title: Statische Inhaltsquellendaten
solution: Experience Manager
title: Statische Inhaltsquellendaten
uuid: a3280ce7-20d7-4f4b-bf3e-e77cc7aca35f
feature: Dynamic Media Classic, SDK/API
role: Entwickler, Administrator, Business Practitioner
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '144'
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
