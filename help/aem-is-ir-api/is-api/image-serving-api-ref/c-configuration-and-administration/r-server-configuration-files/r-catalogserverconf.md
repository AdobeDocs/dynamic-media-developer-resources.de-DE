---
description: Enthält Einstellungen zum Verwalten von Bildkatalogen.
seo-description: Enthält Einstellungen zum Verwalten von Bildkatalogen.
seo-title: catalog-server.conf
solution: Experience Manager
title: catalog-server.conf
topic: Scene7 Image Serving - Image Rendering API
uuid: 797a43d2-18f5-4735-8b19-da231952b1a2
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '121'
ht-degree: 0%

---


# catalog-server.conf{#catalog-server-conf}

Enthält Einstellungen zum Verwalten von Bildkatalogen.

Diese Datei ist eine JAVA-Eigenschaftendatei. Es ist darauf zu achten, dass die entsprechenden Konventionen eingehalten werden. Andernfalls kann der Beginn des Plattformservers fehlschlagen. Verwenden Sie in Windows-Dateipfaden einen umgekehrten Schrägstrich (\\) oder einen einzelnen Schrägstrich (/) anstelle eines umgekehrten Schrägstrichs (\). Der umgekehrte Schrägstrich wird als Escape-Zeichen in diesem Dateityp verwendet.

Änderungen an dieser Datei werden kurz nach dem Speichern der Datei wirksam.

Nur die unten aufgeführten Einstellungen können in [!DNL catalog-service.conf] geändert werden. Wenn eine bestimmte Einstellung fehlt, kann sie an einer beliebigen Stelle in der Datei hinzugefügt werden. Es ist möglicherweise nur eine Instanz jeder Einstellung vorhanden.

`catalog.rootPath=./catalog`

`catalog.cacheRoot=./cache`

`catalog.modificationWaitTime=5000`

`catalog.refreshInterval=10000`
