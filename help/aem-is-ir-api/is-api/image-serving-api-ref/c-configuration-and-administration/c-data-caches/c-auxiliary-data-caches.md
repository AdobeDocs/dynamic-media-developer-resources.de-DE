---
description: Bildzwischendaten, die von verschachtelten/eingebetteten Bildbereitstellungs- und Bildbereitstellungsanfragen erzeugt werden, können zwischengespeichert werden, indem in der verschachtelten/eingebetteten Anfrage „cache=on“ angegeben wird. Diese Daten werden im proprietären Format im Antwortdaten-Cache gespeichert.
solution: Experience Manager
title: Zusätzliche Daten-Caches
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 39906c86-fd9e-4961-a8ba-2ac44c4214a2
TQID: 'https://experienceleague.adobe.com/oRZFSXKaBE9q7liBPRVCheL-NPTriPJkWZFqgMBcoaQ'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 122
ht-degree: 0%

---

# Zusätzliche Daten-Caches{#auxiliary-data-caches}

Bildzwischendaten, die von verschachtelten/eingebetteten Bildbereitstellungs- und Bildbereitstellungsanfragen erzeugt werden, können zwischengespeichert werden, indem in der verschachtelten/eingebetteten Anfrage „cache=on“ angegeben wird. Diese Daten werden im proprietären Format im Antwortdaten-Cache gespeichert.

Bilder von fremden HTTP-Servern werden ebenfalls im Cache für Antwortdaten gespeichert. Solche Bilder werden automatisch mit dem Validierungsprogramm validiert, bevor der Cache-Eintrag generiert wird.

Die [!DNL Platform Server] kompiliert Bildkatalogdaten für einen effizienten Zugriff. Diese Daten werden in `CS::CatalogCacheFolder` gespeichert.
