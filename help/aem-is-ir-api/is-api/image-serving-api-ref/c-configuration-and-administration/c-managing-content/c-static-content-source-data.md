---
description: Datendateien mit statischen Inhalten werden nur vom Plattformserver aufgerufen.
solution: Experience Manager
title: Statische Inhaltsquellendaten
feature: Dynamic Media Classic, SDK/API
role: Entwickler, Administrator, Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '128'
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
