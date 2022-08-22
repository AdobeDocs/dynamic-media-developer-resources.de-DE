---
title: Deinstallation unter Linux® und Solaris™
description: Befolgen Sie diese Anweisungen, um Image Rendering auf einem Linux®- oder Solaris™-System zu deinstallieren.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: c81feaba-18da-441a-bfd5-40275558a384
source-git-commit: 8454991568374ecd1c4babdd3210250ea7988c4c
workflow-type: tm+mt
source-wordcount: '116'
ht-degree: 5%

---

# Deinstallation unter Linux® und Solaris™{#uninstalling-on-linux-and-solaris}

Befolgen Sie diese Anweisungen, um Image Rendering auf einem Linux®- oder Solaris™-System zu deinstallieren. Sie können zwei verschiedene Methoden verwenden. Führen Sie einen der folgenden Schritte aus:

## Methode 1

1. Suchen [!DNL uninstall.sh].

   Sie befindet sich im Verzeichnis, von dem aus ImageRendering installiert wurde. Wenn dieses Verzeichnis entfernt wurde, muss das ursprüngliche Installationspaket dekomprimiert und unaktiviert sein, um extrahiert zu werden [!DNL uninstall.sh].
1. Ausführen [!DNL uninstall.sh] und befolgen Sie die Anweisungen auf dem Bildschirm.

## Methode 2

1. Beenden Sie das ImageRendering mit folgendem Code:

   ` *[!DNL install_folder]*/bin/ImageRendering.sh stop.`

1. Entfernen Sie ImageRendering aus Ihrem System. Der verwendete Befehl hängt von Ihrem System ab.
   * Linux®: `rpm -e ImageRendering`

   * Solaris™: `pkgrm ImageRendering`

1. Löschen Sie alle Ordner oder Dateien, die in Schritt 2 nicht entfernt wurden.

