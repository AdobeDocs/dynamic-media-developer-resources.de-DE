---
description: In dieser Dokumentation wird erläutert, wie Sie den Dynamic Media Image Rendering-Server verwalten.
solution: Experience Manager
title: Übersicht über die Serververwaltung
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 294cd068-8676-4932-a3ad-1a3c5bfa691e
TQID: 'https://experienceleague.adobe.com/t9zGehwMxhHq1HrP3mmNGvkthmqYxX2ijeyihn5OEWI'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 163
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
