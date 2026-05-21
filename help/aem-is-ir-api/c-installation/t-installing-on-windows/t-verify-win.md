---
title: Überprüfen der Installation
description: Nach der Installation von Dynamic Media Image Serving sollten Sie die Installation überprüfen.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 3fcb1f20-8334-497e-8b3e-9097751ca5c1
TQID: 'https://experienceleague.adobe.com/2i1-Ncy7lyIbm8BHFZGVLNIDnZUOA9sr3tZ970WswL4'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: null
workflow-type: tm+mt
source-wordcount: 104
ht-degree: 0%

---

# Überprüfen der Installation {#verifying-the-installation}

Nach der Installation von Dynamic Media Image Serving sollten Sie die Installation überprüfen.

Der Image-Server wird als Windows-Dienst installiert.

1. Öffnen Sie die Systemsteuerung Dienste und überprüfen Sie, ob `Dynamic Media Image Serving` mit dem Status `Started` vorhanden ist.
1. Öffnen Sie einen Internet-Browser auf demselben oder einem anderen Host und überprüfen Sie die Antworten des Standard-Servers:

   `http:// server:port /is/image`

[!DNL &#x200B; http:// *[!DNL server:port]*/ir/render]

Überprüfen Sie, ob in der Antwort &quot;`imageServer.`&quot;-Elemente vorhanden sind, die darauf hinweisen, dass der Bild-Server wartet.

>Zusätzliche Verifizierungen können mit den Beispielseiten der Dokumentations- und Demopakete durchgeführt werden, sofern diese installiert sind.
