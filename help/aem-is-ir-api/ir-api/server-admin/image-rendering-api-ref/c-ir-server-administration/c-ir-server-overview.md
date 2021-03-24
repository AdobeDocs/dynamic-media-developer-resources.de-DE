---
description: In dieser Dokumentation wird beschrieben, wie Sie den Dynamic Media Image Rendering-Server verwalten.
solution: Experience Manager
title: Übersicht zur Serververwaltung
feature: Dynamic Media Classic, SDK/API
role: Entwickler, Administrator, Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '172'
ht-degree: 0%

---


# Überblick über die Serververwaltung{#server-administration-overview}

In dieser Dokumentation wird beschrieben, wie Sie den Dynamic Media Image Rendering-Server verwalten.

Das Image Rendering besteht aus zwei Hauptkomponenten:

* Ein Java-Paket wird mit dem Image Serving Platform Server bereitgestellt und verwaltet Client-Verbindungen, Zwischenspeicherung und Materialkataloge.
* Ein natives Codemodul wird als Erweiterungsbibliothek für den Image-Server bereitgestellt und implementiert die wichtigsten Bildwiedergabefunktionen.

Beide Komponenten werden kollektiv als *Render-Server* bezeichnet.

Beim Image Rendering werden viele Server-Funktionen mit Image Serving gemeinsam verwendet. Alle Optionen werden durch Bearbeiten einer Konfigurationsdatei konfiguriert. Weitere Konfigurationsattribute werden vom Standardkatalog ( [!DNL default.ini]) oder bestimmten Materialkatalogen bereitgestellt. Weitere Informationen finden Sie unter Materialkataloge.

Der Installationsordner für das Image Rendering ( *[!DNL install_folder]*) ist [!DNL *[!DNL install_root]*/ImageRendering]. Unter Windows ist der Standardwert *[!DNL install_root]* `C:\Program Files\Scene7`. Während der Installation kann ein anderer Ordner angegeben werden. Unter Linux muss *[!DNL install_root]* immer [!DNL /usr/local/scene7] sein. Symbolische Links können verwendet werden.

Bei allen Dateipfaden wird unter UNIX die Groß-/Kleinschreibung beachtet und unter Windows wird nicht zwischen Groß- und Kleinschreibung unterschieden.
