---
description: In dieser Dokumentation wird beschrieben, wie Sie den Dynamic Media Image Rendering-Server verwalten.
solution: Experience Manager
title: Übersicht über die Serververwaltung
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator,User
exl-id: 294cd068-8676-4932-a3ad-1a3c5bfa691e
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '168'
ht-degree: 0%

---

# Übersicht über die Serververwaltung{#server-administration-overview}

In dieser Dokumentation wird beschrieben, wie Sie den Dynamic Media Image Rendering-Server verwalten.

Das Bild-Rendering besteht aus zwei Hauptkomponenten:

* Ein Java-Paket wird mit dem Image Serving Platform Server bereitgestellt und verwaltet die Client-Verbindung, Zwischenspeicherung und Materialkataloge.
* Ein natives Codemodul wird als Erweiterungsbibliothek für den Image-Server bereitgestellt und implementiert die Kernfunktionen zum Rendern von Bildern.

Beide Komponenten werden zusammen als *Render Server* bezeichnet.

Das Bild-Rendering nutzt viele Server-Einrichtungen für das Image-Serving. Alle Optionen werden durch Bearbeiten einer Konfigurationsdatei konfiguriert. Zusätzliche Konfigurationsattribute werden vom Standardkatalog ( [!DNL default.ini]) oder spezifischen Materialkatalogen bereitgestellt. Weitere Informationen finden Sie unter Materialkataloge .

Der Ordner &quot;Image Rendering install&quot;( *[!DNL install_folder]*) ist [!DNL *[!DNL install_root]*/ImageRendering]. Unter Windows ist der Standardwert *[!DNL install_root]* `C:\Program Files\Scene7`. Ein anderer Ordner kann während der Installation angegeben werden. Unter Linux muss *[!DNL install_root]* immer [!DNL /usr/local/scene7] sein. Symbolische Links können verwendet werden.

Bei allen Dateipfaden wird unter UNIX zwischen Groß- und Kleinschreibung unterschieden und unter Windows wird zwischen Groß- und Kleinschreibung unterschieden.
