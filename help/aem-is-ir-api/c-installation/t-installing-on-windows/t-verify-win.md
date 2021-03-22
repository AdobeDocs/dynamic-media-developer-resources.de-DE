---
description: Nach der Installation von Dynamic Media Image Serving sollten Sie die Installation überprüfen.
seo-description: Nach der Installation von Dynamic Media Image Serving sollten Sie die Installation überprüfen.
seo-title: Installation überprüfen
solution: Experience Manager
title: Installation überprüfen
uuid: ccc7688d-3d7f-4066-a19e-8a36ca56d711
feature: Dynamic Media Classic, SDK/API
role: Entwickler, Geschäftspraktiker
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '136'
ht-degree: 0%

---


# Überprüfen der Installation{#verifying-the-installation}

Nach der Installation von Dynamic Media Image Serving sollten Sie die Installation überprüfen.

Der Image-Server wird als Windows-Dienst installiert.

1. Öffnen Sie das Bedienfeld &quot;Dienste&quot;und überprüfen Sie, ob &quot;Dynamic Media Image Serving&quot;den Status &quot;Gestartet&quot;hat.
1. Öffnen Sie einen Internetbrowser auf demselben oder einem anderen Host und überprüfen Sie die standardmäßigen Serverantworten:

   `http:// server:port /is/image`

[!DNL http:// *[!DNL server:port]*/ir/render]

Überprüfen Sie, ob in der Antwort &quot; `imageServer.`&quot;Elemente vorhanden sind, die darauf hinweisen, dass der Image-Server überwacht.
>Zusätzliche Überprüfungen können mit den Beispielseiten der Dokumentation- und Demopakete durchgeführt werden, sofern sie installiert sind.

