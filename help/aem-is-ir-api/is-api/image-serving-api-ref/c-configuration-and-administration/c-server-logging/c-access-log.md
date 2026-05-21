---
description: Dies ist das primäre Protokoll, in dem alle HTTP-Anfragen an das  [!DNL Platform Server] protokolliert werden. Image Rendering schreibt, sofern aktiviert, die Zugriffsprotokolldaten in dieselbe Datei.
solution: Experience Manager
title: Zugriffsprotokoll
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: e7f9d935-cb98-404c-8922-6420a4217733
TQID: 'https://experienceleague.adobe.com/PXdlJ0gBGbq4FFhoG6gtmG3hrWVWsXIPelL9xXy5ESk'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 135
ht-degree: 0%

---

# Zugriffsprotokoll{#access-log}

Dies ist das primäre Protokoll, in dem alle HTTP-Anfragen, die an den [!DNL Platform Server] gesendet werden, protokolliert werden. Image Rendering schreibt, sofern aktiviert, die Zugriffsprotokolldaten in dieselbe Datei.

Das Zugriffsprotokoll wird in server.xml konfiguriert.

>[!NOTE]
>
>Zusätzlich zum Client-Traffic für Image-Serving ([!DNL /is/image/*]) und Image-Rendering ([!DNL /ir/render/*]) kann das Zugriffsprotokoll bestimmten internen Traffic enthalten: Zugriff auf das [!DNL Platform Server]-Katalogsystem ([!DNL /is-catalog/*]), Cache-Freigabe- und Fehler-Umleitungsanfragen ([!DNL /is/cache/*]), Zugriff auf andere Pakete, die für die [!DNL Platform Server] bereitgestellt werden, wie die Dynamic Media-Viewer ( [!DNL /is-viewers/*]), statischer Traffic und statische Inhaltsanfragen, die vom [!DNL Platform Server] bedient werden (z. B. [!DNL /is-docs/*]).

Anfragen mit [!DNL /is-catalog] und [!DNL /is/cache] Stammverzeichnis-Pfaden sollten immer aus jeder Client-Traffic-Analyse ausgeschlossen werden.
