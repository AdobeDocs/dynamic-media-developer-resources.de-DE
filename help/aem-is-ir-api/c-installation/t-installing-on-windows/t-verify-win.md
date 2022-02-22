---
title: Installation überprüfen
description: Nachdem Sie Dynamic Media Image Serving installiert haben, sollten Sie die Installation überprüfen.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 3fcb1f20-8334-497e-8b3e-9097751ca5c1
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '104'
ht-degree: 0%

---

# Installation überprüfen {#verifying-the-installation}

Nachdem Sie Dynamic Media Image Serving installiert haben, sollten Sie die Installation überprüfen.

Der Image-Server wird als Windows-Dienst installiert.

1. Öffnen Sie das Control Panel für Dienste und überprüfen Sie, ob `Dynamic Media Image Serving` ist mit dem Status `Started`.
1. Öffnen Sie einen Internet-Browser auf demselben oder einem anderen Host und überprüfen Sie die standardmäßigen Server-Antworten:

   `http:// server:port /is/image`

[!DNL  http:// *[!DNL server:port]*/ir/render]

Auf Vorhandensein von &quot; `imageServer.`&quot;Elemente in der Antwort, die darauf hinweisen, dass der Image-Server überwacht.
>Zusätzliche Überprüfungen können mit den Beispielseiten der Dokumentations- und Demopakete durchgeführt werden, sofern sie installiert sind.
