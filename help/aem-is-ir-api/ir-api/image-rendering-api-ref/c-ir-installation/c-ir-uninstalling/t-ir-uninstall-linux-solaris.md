---
description: Befolgen Sie diese Anweisungen, um das Image Rendering auf einem Linux- oder Solaris-System zu deinstallieren.
seo-description: Befolgen Sie diese Anweisungen, um das Image Rendering auf einem Linux- oder Solaris-System zu deinstallieren.
seo-title: Deinstallation unter Linux und Solaris
solution: Experience Manager
title: Deinstallation unter Linux und Solaris
uuid: 80c0d6ec-985b-4596-bd67-22e5029f7b37
feature: Dynamic Media Classic, SDK/API
role: Entwickler, Geschäftspraktiker
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '146'
ht-degree: 0%

---


# Deinstallation unter Linux und Solaris{#uninstalling-on-linux-and-solaris}

Befolgen Sie diese Anweisungen, um das Image Rendering auf einem Linux- oder Solaris-System zu deinstallieren.

Es gibt zwei Möglichkeiten, das Image Rendering auf einem Linux- oder Solaris-System zu deinstallieren.

**Methode 1**

1. Suchen [!DNL uninstall.sh].

   Sie befindet sich im Ordner, aus dem ImageRendering installiert wurde. Wenn dieser Ordner entfernt wurde, muss das ursprüngliche Installationspaket unkomprimiert und untariert sein, um [!DNL uninstall.sh] zu extrahieren.
1. Führen Sie [!DNL uninstall.sh] aus und befolgen Sie die Anweisungen auf dem Bildschirm.

>**Methode 2**
>
>1. ImageRendering beenden mit: ` *[!DNL install_folder]*/bin/ImageRendering.sh stop.`
>1. Entfernen Sie ImageRendering von Ihrem System.

>
>   
Der Befehl zum Entfernen von ImageRendering hängt von Ihrem System ab:
>
>   Linux: `rpm -e ImageRendering`
>
>   Solaris: `pkgrm ImageRendering`
>
>1. Löschen Sie alle Ordner oder Dateien, die in Schritt 2 nicht entfernt wurden.

>



