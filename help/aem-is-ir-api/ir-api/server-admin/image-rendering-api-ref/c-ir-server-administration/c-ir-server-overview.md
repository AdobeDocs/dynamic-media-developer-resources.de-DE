---
description: In dieser Dokumentation wird erläutert, wie Sie den Dynamic Media Image Rendering-Server verwalten.
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

In dieser Dokumentation wird erläutert, wie Sie den Dynamic Media Image Rendering-Server verwalten.

Das Bild-Rendering besteht aus zwei Hauptkomponenten:

* Ein Java-Paket wird mit dem Image Serving-[!DNL Platform Server] bereitgestellt und verwaltet Client-Verbindungen, Caching und Materialkataloge.
* Ein Modul mit systemeigenem Code wird als Erweiterungsbibliothek für den Bild-Server bereitgestellt und implementiert die grundlegenden Funktionen zum Rendern von Bildern.

Beide Komponenten werden zusammen als „Render *Server“*.

Das Rendern von Bildern nutzt viele Server-Funktionen gemeinsam mit der Bildbereitstellung, und alle Optionen werden durch Bearbeiten einer Konfigurationsdatei konfiguriert. Zusätzliche Konfigurationsattribute werden durch den Standardkatalog ([!DNL default.ini]) oder bestimmte Materialkataloge bereitgestellt. Detaillierte Informationen finden Sie unter Materialkataloge .

Der Installationsordner für das Rendern von Bildern (*[!DNL install_folder]*) ist [!DNL *[!DNL install_root]*/ImageRendering]. Unter Windows ist der *[!DNL install_root]* `C:\Program Files\Scene7`. Während der Installation kann ein anderer Ordner angegeben werden. Unter Linux muss *[!DNL install_root]* immer [!DNL /usr/local/scene7] sein. Es können symbolische Links verwendet werden.

Bei allen Dateipfaden wird unter UNIX zwischen Groß- und Kleinschreibung unterschieden und unter Windows nicht zwischen Groß- und Kleinschreibung.
