---
description: Bildzwischendaten, die von verschachtelten/eingebetteten Bildbereitstellungs- und Bildbereitstellungsanfragen erzeugt werden, können zwischengespeichert werden, indem in der verschachtelten/eingebetteten Anfrage „cache=on“ angegeben wird. Diese Daten werden im proprietären Format im Antwortdaten-Cache gespeichert.
solution: Experience Manager
title: Zusätzliche Daten-Caches
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 39906c86-fd9e-4961-a8ba-2ac44c4214a2
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '122'
ht-degree: 0%

---

# Zusätzliche Daten-Caches{#auxiliary-data-caches}

Bildzwischendaten, die von verschachtelten/eingebetteten Bildbereitstellungs- und Bildbereitstellungsanfragen erzeugt werden, können zwischengespeichert werden, indem in der verschachtelten/eingebetteten Anfrage „cache=on“ angegeben wird. Diese Daten werden im proprietären Format im Antwortdaten-Cache gespeichert.

Bilder von fremden HTTP-Servern werden ebenfalls im Cache für Antwortdaten gespeichert. Solche Bilder werden automatisch mit dem Validierungsprogramm validiert, bevor der Cache-Eintrag generiert wird.

Die [!DNL Platform Server] kompiliert Bildkatalogdaten für einen effizienten Zugriff. Diese Daten werden in `CS::CatalogCacheFolder` gespeichert.
