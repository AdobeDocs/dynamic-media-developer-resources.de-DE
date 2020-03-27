---
description: Dies ist das primäre Protokoll, das alle HTTP-Anforderungen verfolgt, die an den Plattformserver gesendet werden. Bei aktiviertem Image Rendering werden die Daten des Zugriffsprotokolls in dieselbe Datei geschrieben.
seo-description: Dies ist das primäre Protokoll, das alle HTTP-Anforderungen verfolgt, die an den Plattformserver gesendet werden. Bei aktiviertem Image Rendering werden die Daten des Zugriffsprotokolls in dieselbe Datei geschrieben.
seo-title: Zugriffsprotokoll
solution: Experience Manager
title: Zugriffsprotokoll
topic: Scene7 Image Serving - Image Rendering API
uuid: 33cd4338-1fe7-46ac-83f5-200ea26f1e22
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Zugriffsprotokoll{#access-log}

Dies ist das primäre Protokoll, das alle HTTP-Anforderungen verfolgt, die an den Plattformserver gesendet werden. Bei aktiviertem Image Rendering werden die Daten des Zugriffsprotokolls in dieselbe Datei geschrieben.

Das Zugriffsprotokoll ist in server.xml konfiguriert.

>[!NOTE] {class=&quot;- topic/note &quot;
>
>Zusätzlich zum Client-Traffic für Image Serving ( [!DNL /is/image/*]) und Image Rendering ( [!DNL /ir/render/*]) kann das Zugriffsprotokoll auch bestimmten internen Traffic enthalten: Zugriff auf das Plattformserver-Katalogsystem ( [!DNL /is-catalog/*]), Cache-Freigabe und Fehler-Umleitungsanfragen ( [!DNL /is/cache/*]), Zugriff auf andere Pakete, die auf dem Plattformserver bereitgestellt werden, wie z. B. Scene7-Viewer ( [!DNL /is-viewers/*]), statischer Traffic und statische Inhaltsanforderungen, die vom Plattformserver gewartet werden (z. B. [!DNL /is-docs/*]).

Anforderungen mit [!DNL /is-catalog] und [!DNL /is/cache] Stamm-Pfaden sollten immer von jeder Client-Traffic-Analyse ausgeschlossen werden.
