---
title: Deinstallation unter Linux® und Solaris™
description: Folgen Sie diesen Anweisungen, um Image Rendering auf einem Linux®- oder Solaris™-System zu deinstallieren.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: c81feaba-18da-441a-bfd5-40275558a384
TQID: 'https://experienceleague.adobe.com/RmD5z5300Nw12kSsOretyAl5p-TeFkox-Cyqm1MrF5w'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 120
ht-degree: 4%

---

# Deinstallation unter Linux® und Solaris™{#uninstalling-on-linux-and-solaris}

Folgen Sie diesen Anweisungen, um Image Rendering auf einem Linux®- oder Solaris™-System zu deinstallieren. Es gibt zwei verschiedene Methoden, die Sie verwenden können. Führen Sie einen der folgenden Schritte aus:

## Methode 1

1. [!DNL uninstall.sh] suchen.

   Sie befindet sich in dem Verzeichnis, aus dem ImageRendering installiert wurde. Wenn dieses Verzeichnis entfernt wurde, muss das ursprüngliche Installationspaket unkomprimiert und enttarnt werden, um [!DNL uninstall.sh] zu extrahieren.
1. Führen Sie [!DNL uninstall.sh] aus und folgen Sie den Anweisungen auf dem Bildschirm.

## Methode 2

1. Beenden Sie das ImageRendering wie folgt:

   ` *[!DNL install_folder]*/bin/ImageRendering.sh stop.`

1. Entfernen Sie ImageRendering aus Ihrem System. Der von Ihnen verwendete Befehl hängt von Ihrem System ab.
   * Linux®: `rpm -e ImageRendering`

   * Solaris™: `pkgrm ImageRendering`

1. Löschen Sie alle Ordner oder Dateien, die in Schritt 2 nicht entfernt wurden.

