---
description: Befolgen Sie diese Anweisungen, um das Image Rendering auf einem Linux- oder Solaris-System zu deinstallieren.
seo-description: Befolgen Sie diese Anweisungen, um das Image Rendering auf einem Linux- oder Solaris-System zu deinstallieren.
seo-title: Deinstallation unter Linux und Solaris
solution: Experience Manager
title: Deinstallation unter Linux und Solaris
topic: Scene7 Image Serving - Image Rendering API
uuid: 80c0d6ec-985b-4596-bd67-22e5029f7b37
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Deinstallation unter Linux und Solaris{#uninstalling-on-linux-and-solaris}

Befolgen Sie diese Anweisungen, um das Image Rendering auf einem Linux- oder Solaris-System zu deinstallieren.

Es gibt zwei Möglichkeiten, das Image Rendering auf einem Linux- oder Solaris-System zu deinstallieren.

**Methode 1**

1. Suchen [!DNL uninstall.sh].

   Sie befindet sich im Ordner, aus dem ImageRendering installiert wurde. Wenn dieser Ordner entfernt wurde, muss das ursprüngliche Installationspaket dekomprimiert und untariert sein, um extrahiert zu werden [!DNL uninstall.sh].
1. Führen Sie die Anweisungen auf dem Bildschirm aus [!DNL uninstall.sh] und befolgen Sie sie.
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



