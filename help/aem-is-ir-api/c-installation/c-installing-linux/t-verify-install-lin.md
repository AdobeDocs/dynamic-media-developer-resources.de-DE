---
title: Überprüfen der Installation
description: Nachdem Sie Image Serving unter Linux® installiert haben, überprüfen Sie die Installation.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 273478ab-f245-48ef-a125-fb738054484e
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '118'
ht-degree: 0%

---

# Überprüfen der Installation{#verifying-the-installation}

Nachdem Sie Image Serving unter Linux® installiert haben, überprüfen Sie die Installation.

Der Image-Server wird als Linux®-Daemon installiert.

**So überprüfen Sie die Installation**

1. Stellen Sie sicher, dass die Bildbereitstellung so konfiguriert ist, dass sie automatisch gestartet wird, und dass sie ausgeführt wird:

   `> /sbin/service ImageServing status`

   >[!NOTE]
   >
   >Sie müssen über Stammberechtigungen verfügen, um diese Skripte auszuführen.

1. Öffnen Sie einen Internet-Browser auf demselben oder einem anderen Host und überprüfen Sie die Antworten des Standard-Servers:

[!DNL http:// *[!DNL server:port]*/is/image]

[!DNL  http:// *[!DNL server:port]*/ir/render]

Überprüfen Sie in den Antworten, ob Elemente vorhanden sind, die mit `imageServer` beginnen. Dies bedeutet, dass die [!DNL Platform Server] erfolgreich mit dem Bildserver kommunizieren konnte.

>Zusätzliche Verifizierungen können mit den Beispielseiten der Dokumentations- und Demopakete durchgeführt werden, sofern diese installiert sind.
