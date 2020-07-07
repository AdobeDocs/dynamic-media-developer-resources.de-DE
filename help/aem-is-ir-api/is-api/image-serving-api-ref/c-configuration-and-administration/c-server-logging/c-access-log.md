---
description: Hierbei handelt es sich um das primäre Protokoll, das alle HTTP-Anfragen an den Platform Server verfolgt. Bei aktiviertem Image Rendering werden die Daten des Zugriffsprotokolls in dieselbe Datei geschrieben.
seo-description: Hierbei handelt es sich um das primäre Protokoll, das alle HTTP-Anfragen an den Platform Server verfolgt. Bei aktiviertem Image Rendering werden die Daten des Zugriffsprotokolls in dieselbe Datei geschrieben.
seo-title: Zugriffsprotokoll
solution: Experience Manager
title: Zugriffsprotokoll
topic: Scene7 Image Serving - Image Rendering API
uuid: 33cd4338-1fe7-46ac-83f5-200ea26f1e22
translation-type: tm+mt
source-git-commit: e8e5b07329bde3e23ee095d5022da62d67e9478c
workflow-type: tm+mt
source-wordcount: '175'
ht-degree: 0%

---


# Zugriffsprotokoll{#access-log}

Hierbei handelt es sich um das primäre Protokoll, das alle HTTP-Anfragen an den Platform Server verfolgt. Bei aktiviertem Image Rendering werden die Daten des Zugriffsprotokolls in dieselbe Datei geschrieben.

Das Zugriffsprotokoll ist in server.xml konfiguriert.

>[!NOTE]
>
>Zusätzlich zum Client-Traffic für Image Serving ( [!DNL /is/image/*]) und Image Rendering ( [!DNL /ir/render/*]) kann das Zugriffsprotokoll auch bestimmten internen Traffic enthalten: Zugriff auf das Katalogsystem der Platform Server ( [!DNL /is-catalog/*]), Cache-Freigabe- und Fehlerumleitungsanfragen ( [!DNL /is/cache/*]), Zugriff auf andere auf dem Platform Server bereitgestellte Pakete, z. B. Scene7-Viewer ( [!DNL /is-viewers/*]), statische Traffic- und statische Inhaltsanforderungen, die vom Platform Server gewartet werden (z. B. [!DNL /is-docs/*]).

Anforderungen mit [!DNL /is-catalog] und [!DNL /is/cache] Stamm-Pfaden sollten immer von jeder Client-Traffic-Analyse ausgeschlossen werden.
