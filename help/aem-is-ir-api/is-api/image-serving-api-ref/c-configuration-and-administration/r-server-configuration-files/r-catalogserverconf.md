---
description: Enthält Einstellungen zum Verwalten von Bildkatalogen.
solution: Experience Manager
title: catalog-server.conf
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 55e55381-3828-4937-8746-a74e82d6ca38
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '111'
ht-degree: 0%

---

# catalog-server.conf{#catalog-server-conf}

Enthält Einstellungen zum Verwalten von Bildkatalogen.

Diese Datei ist eine JAVA-Eigenschaftendatei. Es muss darauf geachtet werden, dass die entsprechenden Konventionen eingehalten werden. Andernfalls kann es sein, dass der [!DNL Platform Server] nicht startet. Verwenden Sie in Windows-Dateipfaden einen doppelten umgekehrten Schrägstrich &quot;\\&quot; oder einen einzelnen Schrägstrich &quot;/&quot; anstelle eines umgekehrten Schrägstrichs &quot;\&quot;. Der umgekehrte Schrägstrich wird in diesem Dateityp als Escape-Zeichen verwendet.

Änderungen an dieser Datei werden kurz nach dem Speichern der Datei wirksam.

Nur die unten aufgeführten Einstellungen können in [!DNL catalog-service.conf] geändert werden. Wenn eine bestimmte Einstellung fehlt, kann sie an einer beliebigen Stelle in der Datei hinzugefügt werden. Es kann nur eine Instanz jeder Einstellung vorhanden sein.

`catalog.rootPath=./catalog`

`catalog.cacheRoot=./cache`

`catalog.modificationWaitTime=5000`

`catalog.refreshInterval=10000`
