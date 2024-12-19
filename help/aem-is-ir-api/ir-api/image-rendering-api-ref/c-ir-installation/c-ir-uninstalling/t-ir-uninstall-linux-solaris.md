---
title: Deinstallation unter Linux® und Solaris™
description: Folgen Sie diesen Anweisungen, um Image Rendering auf einem Linux®- oder Solaris™-System zu deinstallieren.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: c81feaba-18da-441a-bfd5-40275558a384
source-git-commit: 8454991568374ecd1c4babdd3210250ea7988c4c
workflow-type: tm+mt
source-wordcount: '119'
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

