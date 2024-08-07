---
description: Dies ist das primäre Protokoll, das alle HTTP-Anfragen verfolgt, die an den  [!DNL Platform Server] gesendet wurden. Wenn das Image Rendering aktiviert ist, werden die Zugriffsprotokolldaten in dieselbe Datei geschrieben.
solution: Experience Manager
title: Zugriffsprotokoll
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: e7f9d935-cb98-404c-8922-6420a4217733
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '135'
ht-degree: 0%

---

# Zugriffsprotokoll{#access-log}

Dies ist das primäre Protokoll, das alle HTTP-Anfragen verfolgt, die an die [!DNL Platform Server] gesendet werden. Wenn das Image Rendering aktiviert ist, werden die Zugriffsprotokolldaten in dieselbe Datei geschrieben.

Das Zugriffsprotokoll wird in server.xml konfiguriert.

>[!NOTE]
>
>Zusätzlich zum Client-Traffic für Image Serving ( [!DNL /is/image/*]) und Image Rendering ( [!DNL /ir/render/*]) kann das Zugriffsprotokoll bestimmten internen Traffic enthalten: Zugriff auf das [!DNL Platform Server] -Katalogsystem ( [!DNL /is-catalog/*]), Cache-Freigabe- und Fehler-Weiterleitungsanfragen ( [!DNL /is/cache/*]), Zugriff auf andere Pakete, die für [!DNL Platform Server] bereitgestellt werden, wie z. B. die Dynamic Media-Viewer ( [!DNL /is-viewers/*]), statischer Traffic und statische Inhaltsanforderungen, die von [!DNL Platform Server] , [!DNL /is-docs/*]).

Anforderungen mit den Stammpfaden [!DNL /is-catalog] und [!DNL /is/cache] sollten immer von jeder Client-Traffic-Analyse ausgeschlossen werden.
