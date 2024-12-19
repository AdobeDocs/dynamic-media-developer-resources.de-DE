---
description: Auf statische Inhaltsquellendatendateien kann nur über die [!DNL Platform Server] zugegriffen werden.
solution: Experience Manager
title: Statische Quelldaten für Inhalte
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 3cf01fc2-c925-4039-8e03-cb909cca6a51
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '112'
ht-degree: 0%

---

# Statische Quelldaten für Inhalte{#static-content-source-data}

Auf statische Inhaltsquellendatendateien kann nur über die [!DNL Platform Server] zugegriffen werden.

Der Pfad für statische Inhaltsdatendateien wird wie folgt aufgelöst:

`PS::staticContent.rootPaths/attribute::StaticContentRootPath/static::Path`

Der Server kombiniert Pfadsegmente von rechts nach links, bis ein absoluter Dateipfad festgelegt wird.

Alle ` *[!DNL rootPath]*` können leere, relative oder absolute Pfadsegmente sein.

` *[!DNL catalogPath]*` ist entweder ein absoluter oder relativer Dateipfad/-name. *[!DNL requestPath]* muss ein relativer Dateipfad/Dateiname sein.

In können mehrere `PS::staticContent.rootPaths` definiert [!DNL PlatformServer.conf]. Dadurch können Quelldatendateien über mehrere Dateisysteme verteilt werden. Der [!DNL Platform Server] versucht alternative Pfade in der angegebenen Reihenfolge, bis die Datendatei gefunden wird.
