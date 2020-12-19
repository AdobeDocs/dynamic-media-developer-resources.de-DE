---
description: Nach der Installation von Scene7 Image Serving sollten Sie die Installation überprüfen.
seo-description: Nach der Installation von Scene7 Image Serving sollten Sie die Installation überprüfen.
seo-title: Installation überprüfen
solution: Experience Manager
title: Installation überprüfen
topic: Scene7 Image Serving - Image Rendering API
uuid: ccc7688d-3d7f-4066-a19e-8a36ca56d711
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '124'
ht-degree: 0%

---


# Überprüfen der Installation{#verifying-the-installation}

Nach der Installation von Scene7 Image Serving sollten Sie die Installation überprüfen.

Der Image-Server wird als Windows-Dienst installiert.

1. Öffnen Sie das Bedienfeld &quot;Dienste&quot;und überprüfen Sie, ob &quot;Scene7 Image Serving&quot;den Status &quot;Gestartet&quot;hat.
1. Öffnen Sie einen Internetbrowser auf demselben oder einem anderen Host und überprüfen Sie die standardmäßigen Serverantworten:

   `http:// server:port /is/image`

[!DNL http:// *[!DNL server:port]*/ir/render]

Überprüfen Sie, ob in der Antwort &quot; `imageServer.`&quot;Elemente vorhanden sind, die darauf hinweisen, dass der Image-Server überwacht.
>Zusätzliche Überprüfungen können mit den Beispielseiten der Dokumentation- und Demopakete durchgeführt werden, sofern sie installiert sind.

