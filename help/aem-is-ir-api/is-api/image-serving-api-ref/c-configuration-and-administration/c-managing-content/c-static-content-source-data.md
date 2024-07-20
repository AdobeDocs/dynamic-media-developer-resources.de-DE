---
description: Datendateien der statischen Inhaltsquelle werden nur durch den  [!DNL Platform Server] aufgerufen.
solution: Experience Manager
title: Statische Inhaltsquellendaten
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 3cf01fc2-c925-4039-8e03-cb909cca6a51
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '112'
ht-degree: 0%

---

# Statische Inhaltsquellendaten{#static-content-source-data}

Auf statische Inhaltsquellendatendateien kann nur mit dem Wert [!DNL Platform Server] zugegriffen werden.

Der Pfad für statische Inhaltsdatendateien wird wie folgt aufgelöst:

`PS::staticContent.rootPaths/attribute::StaticContentRootPath/static::Path`

Der Server kombiniert Pfadsegmente von rechts nach links, bis ein absoluter Dateipfad festgelegt ist.

Alle ` *[!DNL rootPath]*` -Segmente können leere, relative oder absolute Pfadsegmente sein.

` *[!DNL catalogPath]*` ist entweder ein absoluter oder relativer Dateipfad/Dateiname. *[!DNL requestPath]* muss ein relativer Dateipfad/Name sein.

In [!DNL PlatformServer.conf] können mehrere `PS::staticContent.rootPaths` -Werte definiert werden. Dadurch können Quelldatendateien über mehrere Dateisysteme verteilt werden. Der [!DNL Platform Server] versucht alternative Pfade in der angegebenen Reihenfolge, bis die Datendatei gefunden wird.
