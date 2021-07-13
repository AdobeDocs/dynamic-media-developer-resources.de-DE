---
description: Enthält Einstellungen zum Verwalten von Bildkatalogen.
solution: Experience Manager
title: catalog-server.conf
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator,User
exl-id: 55e55381-3828-4937-8746-a74e82d6ca38
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '118'
ht-degree: 0%

---

# catalog-server.conf{#catalog-server-conf}

Enthält Einstellungen zum Verwalten von Bildkatalogen.

Diese Datei ist eine JAVA-Eigenschaftendatei. Es ist darauf zu achten, dass die entsprechenden Konventionen eingehalten werden. Andernfalls kann der Platform Server möglicherweise nicht gestartet werden. Verwenden Sie in Windows-Dateipfaden einen doppelten umgekehrten Schrägstrich &quot;\&quot;oder einen einfachen Schrägstrich &quot;/&quot;anstelle eines umgekehrten Schrägstrichs &quot;\&quot;. Der umgekehrte Schrägstrich wird als Escape-Zeichen in diesem Dateityp verwendet.

Änderungen an dieser Datei werden kurz nach dem Speichern der Datei wirksam.

Nur die unten aufgeführten Einstellungen können in [!DNL catalog-service.conf] geändert werden. Wenn eine bestimmte Einstellung fehlt, kann sie an einer beliebigen Stelle in der Datei hinzugefügt werden. Es kann nur eine Instanz jeder Einstellung vorhanden sein.

`catalog.rootPath=./catalog`

`catalog.cacheRoot=./cache`

`catalog.modificationWaitTime=5000`

`catalog.refreshInterval=10000`
