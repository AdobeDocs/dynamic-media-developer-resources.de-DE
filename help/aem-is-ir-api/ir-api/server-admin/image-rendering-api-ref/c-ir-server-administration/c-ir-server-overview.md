---
description: In dieser Dokumentation wird beschrieben, wie Sie den Dynamic Media Image Rendering-Server verwalten.
solution: Experience Manager
title: Übersicht über die Serververwaltung
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 294cd068-8676-4932-a3ad-1a3c5bfa691e
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '161'
ht-degree: 0%

---

# Übersicht über die Serververwaltung{#server-administration-overview}

In dieser Dokumentation wird beschrieben, wie Sie den Dynamic Media Image Rendering-Server verwalten.

Das Bild-Rendering besteht aus zwei Hauptkomponenten:

* Ein Java-Paket wird mit dem Image Serving bereitgestellt [!DNL Platform Server] und verwaltet Client-Verbindungen, Caching, Materialkataloge.
* Ein natives Codemodul wird als Erweiterungsbibliothek für den Image-Server bereitgestellt und implementiert die Kernfunktionen zum Rendern von Bildern.

Beide Komponenten werden zusammen als *Render Server*.

Das Bild-Rendering nutzt viele Server-Einrichtungen für das Image-Serving. Alle Optionen werden durch Bearbeiten einer Konfigurationsdatei konfiguriert. Weitere Konfigurationsattribute werden vom Standardkatalog bereitgestellt ( [!DNL default.ini]) oder spezifischen Materialkatalogen. Weitere Informationen finden Sie unter Materialkataloge .

Der Ordner &quot;Image Rendering install&quot;( *[!DNL install_folder]*) ist [!DNL *[!DNL install_root]*/ImageRendering]. Unter Windows wird die Standardeinstellung *[!DNL install_root]* is `C:\Program Files\Scene7`. Ein anderer Ordner kann während der Installation angegeben werden. Unter Linux: *[!DNL install_root]* muss immer [!DNL /usr/local/scene7]. Symbolische Links können verwendet werden.

Bei allen Dateipfaden wird unter UNIX zwischen Groß- und Kleinschreibung unterschieden und unter Windows wird zwischen Groß- und Kleinschreibung unterschieden.
