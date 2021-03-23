---
description: Überprüfen Sie nach der Installation von Image Serving unter Linux die Installation.
seo-description: Überprüfen Sie nach der Installation von Image Serving unter Linux die Installation.
seo-title: Installation überprüfen
solution: Experience Manager
title: Installation überprüfen
uuid: 4fdf61c7-3c9f-4f3e-9696-60eb7e3f2209
feature: Dynamic Media Classic, SDK/API
role: Entwickler, Geschäftspraktiker
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '150'
ht-degree: 0%

---


# Überprüfen der Installation{#verifying-the-installation}

Überprüfen Sie nach der Installation von Image Serving unter Linux die Installation.

Der Image-Server wird als Linux-Daemon installiert.

**So überprüfen Sie die Installation**

1. Stellen Sie sicher, dass Image Serving für den automatischen Beginn konfiguriert ist und dass es ausgeführt wird:

   `> /sbin/service ImageServing status`

   >[!NOTE]
   >
   >Sie müssen über Root-Berechtigungen zum Ausführen dieser Skripten verfügen.

1. Öffnen Sie einen Internetbrowser auf demselben oder einem anderen Host und überprüfen Sie die StandardserAntwort(en):

[!DNL http:// *[!DNL server:port]*/is/image]

[!DNL http:// *[!DNL server:port]*/ir/render]

Überprüfen Sie in den Antworten, ob Elemente vorhanden sind, die mit &quot; `imageServer.`&quot;beginnen. Dies weist darauf hin, dass der Plattformserver erfolgreich mit dem Image-Server kommunizieren konnte.
>Zusätzliche Überprüfungen können mit den Beispielseiten der Dokumentation- und Demopakete durchgeführt werden, sofern sie installiert sind.

