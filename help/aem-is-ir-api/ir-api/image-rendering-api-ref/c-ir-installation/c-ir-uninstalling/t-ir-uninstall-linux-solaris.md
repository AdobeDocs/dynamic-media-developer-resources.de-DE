---
description: Befolgen Sie diese Anweisungen, um das Image Rendering auf einem Linux- oder Solaris-System zu deinstallieren.
solution: Experience Manager
title: Deinstallation unter Linux und Solaris
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: c81feaba-18da-441a-bfd5-40275558a384
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '125'
ht-degree: 0%

---

# Deinstallation unter Linux und Solaris{#uninstalling-on-linux-and-solaris}

Befolgen Sie diese Anweisungen, um das Image Rendering auf einem Linux- oder Solaris-System zu deinstallieren.

Es gibt zwei Möglichkeiten, das Image Rendering auf einem Linux- oder Solaris-System zu deinstallieren.

**Methode 1**

1. Suchen [!DNL uninstall.sh].

   Sie befindet sich in dem Ordner, von dem aus ImageRendering installiert wurde. Wenn dieses Verzeichnis entfernt wurde, muss das ursprüngliche Installationspaket dekomprimiert und unaktiviert sein, um [!DNL uninstall.sh] zu extrahieren.
1. Führen Sie [!DNL uninstall.sh] aus und befolgen Sie die Anweisungen auf dem Bildschirm.

>**Methode 2**
>
>1. ImageRendering beenden mit: ` *[!DNL install_folder]*/bin/ImageRendering.sh stop.`
>1. Entfernen Sie ImageRendering aus Ihrem System.

>
>   
Der Befehl zum Entfernen des ImageRendering hängt von Ihrem System ab:
>
>   Linux: `rpm -e ImageRendering`
>
>   Solaris: `pkgrm ImageRendering`
>
>1. Löschen Sie alle Verzeichnisse oder Dateien, die nicht in Schritt 2 entfernt wurden.

>


