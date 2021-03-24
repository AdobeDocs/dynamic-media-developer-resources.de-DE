---
description: Dies ist das primäre Protokoll, das alle HTTP-Anforderungen verfolgt, die an den Plattformserver gesendet werden. Bei aktiviertem Image Rendering werden die Daten des Zugriffsprotokolls in dieselbe Datei geschrieben.
solution: Experience Manager
title: Zugriffsprotokoll
feature: Dynamic Media Classic, SDK/API
role: Entwickler, Administrator, Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '153'
ht-degree: 0%

---


# Zugriffsprotokoll{#access-log}

Dies ist das primäre Protokoll, das alle HTTP-Anforderungen verfolgt, die an den Plattformserver gesendet werden. Bei aktiviertem Image Rendering werden die Daten des Zugriffsprotokolls in dieselbe Datei geschrieben.

Das Zugriffsprotokoll ist in server.xml konfiguriert.

>[!NOTE]
>
>Neben dem Client-Traffic für Image Serving ( [!DNL /is/image/*]) und Image Rendering ( [!DNL /ir/render/*]) kann das Zugriffsprotokoll auch bestimmten internen Traffic enthalten: Zugriff auf das Plattformserver-Katalogsystem ( [!DNL /is-catalog/*]), Cache-Freigabe- und Fehlerumleitungsanfragen ( [!DNL /is/cache/*]), Zugriff auf andere auf dem Plattformserver bereitgestellte Pakete, wie z. B. die Dynamic Media-Viewer ( [!DNL /is-viewers/*]), statische Traffic- und statische Inhaltsanforderungen, die vom Plattformserver gewartet werden (z. B. [!DNL /is-docs/*]).

Anforderungen mit [!DNL /is-catalog]- und [!DNL /is/cache]-Stammpfaden sollten immer von jeder Client-Traffic-Analyse ausgeschlossen werden.
