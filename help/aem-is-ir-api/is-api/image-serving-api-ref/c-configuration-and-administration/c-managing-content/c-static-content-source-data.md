---
description: Auf statische Inhaltsquellendatendateien kann nur vom Platform Server zugegriffen werden.
solution: Experience Manager
title: Statische Inhaltsquellendaten
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator,User
exl-id: 3cf01fc2-c925-4039-8e03-cb909cca6a51
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '124'
ht-degree: 0%

---

# Statische Inhaltsquellendaten{#static-content-source-data}

Auf statische Inhaltsquellendatendateien kann nur vom Platform Server zugegriffen werden.

Der Pfad für statische Inhaltsdatendateien wird wie folgt aufgelöst:

`PS::staticContent.rootPaths/attribute::StaticContentRootPath/static::Path`

Der Server kombiniert Pfadsegmente von rechts nach links, bis ein absoluter Dateipfad festgelegt ist.

Alle ` *[!DNL rootPath]*`-Segmente können leere, relative oder absolute Pfadsegmente sein.

` *[!DNL catalogPath]*` ist entweder ein absoluter oder ein relativer Dateipfad/-name. *[!DNL requestPath]* muss ein relativer Dateipfad/Name sein.

In [!DNL PlatformServer.conf] können mehrere `PS::staticContent.rootPaths`-Werte definiert werden. Dadurch können Quelldatendateien über mehrere Dateisysteme verteilt werden. Der Platform Server versucht alternative Pfade in der angegebenen Reihenfolge, bis die Datendatei gefunden wird.
