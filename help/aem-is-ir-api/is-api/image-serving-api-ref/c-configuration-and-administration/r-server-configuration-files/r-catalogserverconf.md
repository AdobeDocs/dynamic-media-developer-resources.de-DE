---
description: Enthält Einstellungen zum Verwalten von Bildkatalogen.
solution: Experience Manager
title: catalog-server.conf
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 55e55381-3828-4937-8746-a74e82d6ca38
TQID: 'https://experienceleague.adobe.com/GdtVY3WMO9F6C5vzkOHdVoMW-f6-L1cJGUt1KUCvLJ8'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 113
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
