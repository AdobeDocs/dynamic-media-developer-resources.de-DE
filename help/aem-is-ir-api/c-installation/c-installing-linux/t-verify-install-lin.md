---
description: Nachdem Sie Image Serving unter Linux installiert haben, überprüfen Sie die Installation.
solution: Experience Manager
title: Installation überprüfen
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 273478ab-f245-48ef-a125-fb738054484e
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '134'
ht-degree: 0%

---

# Installation überprüfen{#verifying-the-installation}

Nachdem Sie Image Serving unter Linux installiert haben, überprüfen Sie die Installation.

Der Image-Server wird als Linux-Daemon installiert.

**Überprüfen der Installation**

1. Stellen Sie sicher, dass Image Serving so konfiguriert ist, dass es automatisch gestartet wird und ausgeführt wird:

   `> /sbin/service ImageServing status`

   >[!NOTE]
   >
   >Sie müssen über Root-Berechtigungen verfügen, um diese Skripte ausführen zu können.

1. Öffnen Sie einen Internet-Browser auf demselben oder einem anderen Host und überprüfen Sie die standardmäßigen Server-Antworten:

[!DNL http:// *[!DNL server:port]*/is/image]

[!DNL http:// *[!DNL server:port]*/ir/render]

Überprüfen Sie in den Antworten, ob Elemente vorhanden sind, die mit &quot;`imageServer.`&quot;beginnen und angeben, dass der Platform-Server erfolgreich mit dem Image-Server kommunizieren konnte.
>Zusätzliche Überprüfungen können mit den Beispielseiten der Dokumentations- und Demopakete durchgeführt werden, sofern sie installiert sind.
