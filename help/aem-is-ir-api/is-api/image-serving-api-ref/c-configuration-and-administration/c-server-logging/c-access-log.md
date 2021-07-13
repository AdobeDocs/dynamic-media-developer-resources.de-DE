---
description: Dies ist das primäre Protokoll, das alle HTTP-Anfragen verfolgt, die an den Platform Server gesendet werden. Wenn das Image Rendering aktiviert ist, werden die Zugriffsprotokolldaten in dieselbe Datei geschrieben.
solution: Experience Manager
title: Zugriffsprotokoll
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator,User
exl-id: e7f9d935-cb98-404c-8922-6420a4217733
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '149'
ht-degree: 0%

---

# Zugriffsprotokoll{#access-log}

Dies ist das primäre Protokoll, das alle HTTP-Anfragen verfolgt, die an den Platform Server gesendet werden. Wenn das Image Rendering aktiviert ist, werden die Zugriffsprotokolldaten in dieselbe Datei geschrieben.

Das Zugriffsprotokoll wird in server.xml konfiguriert.

>[!NOTE]
>
>Zusätzlich zum Client-Traffic für Image Serving ( [!DNL /is/image/*]) und Image Rendering ( [!DNL /ir/render/*]) kann das Zugriffsprotokoll bestimmten internen Traffic enthalten: Zugriff auf das Platform Server-Katalogsystem ( [!DNL /is-catalog/*]), Cache-Freigabe und Fehler-Umleitungsanfragen ( [!DNL /is/cache/*]), Zugriff auf andere auf dem Platform Server bereitgestellte Pakete, wie z. B. die Dynamic Media-Viewer ( [!DNL /is-viewers/*]), statische Traffic- und statische Inhaltsanforderungen, die vom Platform-Server bereitgestellt werden (z. B. [!DNL /is-docs/*]).

Anforderungen mit [!DNL /is-catalog]- und [!DNL /is/cache]-Stammpfaden sollten immer von jeder Client-Traffic-Analyse ausgeschlossen werden.
