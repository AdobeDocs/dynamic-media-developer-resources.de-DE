---
description: Nachdem Sie Dynamic Media Image Serving installiert haben, sollten Sie die Installation überprüfen.
solution: Experience Manager
title: Installation überprüfen
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 3fcb1f20-8334-497e-8b3e-9097751ca5c1
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '118'
ht-degree: 0%

---

# Installation überprüfen{#verifying-the-installation}

Nachdem Sie Dynamic Media Image Serving installiert haben, sollten Sie die Installation überprüfen.

Der Image-Server wird als Windows-Dienst installiert.

1. Öffnen Sie das Control Panel &quot;Dienste&quot;und überprüfen Sie, ob &quot;Dynamic Media Image Serving&quot;den Status &quot;Gestartet&quot;aufweist.
1. Öffnen Sie einen Internet-Browser auf demselben oder einem anderen Host und überprüfen Sie die standardmäßigen Server-Antworten:

   `http:// server:port /is/image`

[!DNL http:// *[!DNL server:port]*/ir/render]

Überprüfen Sie, ob in der Antwort `imageServer.` Elemente vorhanden sind, die darauf hinweisen, dass der Image-Server wartet.
>Zusätzliche Überprüfungen können mit den Beispielseiten der Dokumentations- und Demopakete durchgeführt werden, sofern sie installiert sind.
