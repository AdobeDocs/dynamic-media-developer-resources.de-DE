---
description: Dies ist das primäre Protokoll, in dem alle HTTP-Anfragen an das  [!DNL Platform Server] protokolliert werden. Image Rendering schreibt, sofern aktiviert, die Zugriffsprotokolldaten in dieselbe Datei.
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

Dies ist das primäre Protokoll, in dem alle HTTP-Anfragen, die an den [!DNL Platform Server] gesendet werden, protokolliert werden. Image Rendering schreibt, sofern aktiviert, die Zugriffsprotokolldaten in dieselbe Datei.

Das Zugriffsprotokoll wird in server.xml konfiguriert.

>[!NOTE]
>
>Zusätzlich zum Client-Traffic für Image-Serving ([!DNL /is/image/*]) und Image-Rendering ([!DNL /ir/render/*]) kann das Zugriffsprotokoll bestimmten internen Traffic enthalten: Zugriff auf das [!DNL Platform Server]-Katalogsystem ([!DNL /is-catalog/*]), Cache-Freigabe- und Fehler-Umleitungsanfragen ([!DNL /is/cache/*]), Zugriff auf andere Pakete, die für die [!DNL Platform Server] bereitgestellt werden, wie die Dynamic Media-Viewer ( [!DNL /is-viewers/*]), statischer Traffic und statische Inhaltsanfragen, die vom [!DNL Platform Server] bedient werden (z. B. [!DNL /is-docs/*]).

Anfragen mit [!DNL /is-catalog] und [!DNL /is/cache] Stammverzeichnis-Pfaden sollten immer aus jeder Client-Traffic-Analyse ausgeschlossen werden.
