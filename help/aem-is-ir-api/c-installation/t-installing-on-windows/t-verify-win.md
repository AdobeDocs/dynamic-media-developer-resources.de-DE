---
title: Überprüfen der Installation
description: Nach der Installation von Dynamic Media Image Serving sollten Sie die Installation überprüfen.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 3fcb1f20-8334-497e-8b3e-9097751ca5c1
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '104'
ht-degree: 0%

---

# Überprüfen der Installation {#verifying-the-installation}

Nach der Installation von Dynamic Media Image Serving sollten Sie die Installation überprüfen.

Der Image-Server wird als Windows-Dienst installiert.

1. Öffnen Sie die Systemsteuerung Dienste und überprüfen Sie, ob `Dynamic Media Image Serving` mit dem Status `Started` vorhanden ist.
1. Öffnen Sie einen Internet-Browser auf demselben oder einem anderen Host und überprüfen Sie die Antworten des Standard-Servers:

   `http:// server:port /is/image`

[!DNL  http:// *[!DNL server:port]*/ir/render]

Überprüfen Sie, ob in der Antwort &quot;`imageServer.`&quot;-Elemente vorhanden sind, die darauf hinweisen, dass der Bild-Server wartet.
>Zusätzliche Verifizierungen können mit den Beispielseiten der Dokumentations- und Demopakete durchgeführt werden, sofern diese installiert sind.
