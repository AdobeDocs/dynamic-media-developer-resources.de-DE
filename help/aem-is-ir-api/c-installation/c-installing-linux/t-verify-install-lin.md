---
description: Überprüfen Sie nach der Installation von Image Serving unter Linux die Installation.
seo-description: Überprüfen Sie nach der Installation von Image Serving unter Linux die Installation.
seo-title: Installation überprüfen
solution: Experience Manager
title: Installation überprüfen
topic: Scene7 Image Serving - Image Rendering API
uuid: 4fdf61c7-3c9f-4f3e-9696-60eb7e3f2209
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Installation überprüfen{#verifying-the-installation}

Überprüfen Sie nach der Installation von Image Serving unter Linux die Installation.

Der Image-Server wird als Linux-Daemon installiert.

**So überprüfen Sie die Installation**

1. Stellen Sie sicher, dass Image Serving für den automatischen Beginn konfiguriert ist und dass es ausgeführt wird:

   `> /sbin/service ImageServing status`

   >[!NOTE] {class=&quot;- topic/note &quot;
   >
   >Sie müssen über Root-Berechtigungen zum Ausführen dieser Skripten verfügen.

1. Öffnen Sie einen Internetbrowser auf demselben oder einem anderen Host und überprüfen Sie die StandardserAntwort(en):

[!DNL http:// *[!DNL server:port]*/is/image]

[!DNL http:// *[!DNL server:port]*/ir/render]

Überprüfen Sie in den Antworten, ob Elemente vorhanden sind, die mit &quot; `imageServer.`&quot; beginnen, was bedeutet, dass der Plattformserver erfolgreich mit dem Image-Server kommunizieren konnte.
>Zusätzliche Überprüfungen können mit den Beispielseiten der Dokumentation- und Demo-Pakete durchgeführt werden, sofern sie installiert sind.

