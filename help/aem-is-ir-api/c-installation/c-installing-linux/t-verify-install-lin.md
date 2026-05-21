---
title: Überprüfen der Installation
description: Nachdem Sie Image Serving unter Linux® installiert haben, überprüfen Sie die Installation.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 273478ab-f245-48ef-a125-fb738054484e
TQID: 'https://experienceleague.adobe.com/LyHlwiFL1b-iwo1kSnUeNfNo3fZY6FZetHgnNFoxGZo'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 118
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

[!DNL &#x200B; http:// *[!DNL server:port]*/ir/render]

Überprüfen Sie in den Antworten, ob Elemente vorhanden sind, die mit `imageServer` beginnen. Dies bedeutet, dass die [!DNL Platform Server] erfolgreich mit dem Bildserver kommunizieren konnte.

>Zusätzliche Verifizierungen können mit den Beispielseiten der Dokumentations- und Demopakete durchgeführt werden, sofern diese installiert sind.
