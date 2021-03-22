---
description: Zwischenbilddaten, die von verschachtelten/eingebetteten Image Serving- und Image Rendering-Anforderungen erzeugt werden, können zwischengespeichert werden, indem Sie cache=on in der verschachtelten/eingebetteten Anforderung angeben. Diese Daten werden im proprietären Format im Antwortdaten-Cache gespeichert.
seo-description: Zwischenbilddaten, die von verschachtelten/eingebetteten Image Serving- und Image Rendering-Anforderungen erzeugt werden, können zwischengespeichert werden, indem Sie cache=on in der verschachtelten/eingebetteten Anforderung angeben. Diese Daten werden im proprietären Format im Antwortdaten-Cache gespeichert.
seo-title: Hilfedatenzwischenspeicher
solution: Experience Manager
title: Hilfedatenzwischenspeicher
uuid: 10ce998e-e300-4d24-9d92-a8693dade327
feature: Dynamic Media Classic, SDK/API
role: Entwickler, Administrator, Business Practitioner
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '173'
ht-degree: 0%

---


# Zusätzliche Daten-Caches{#auxiliary-data-caches}

Zwischenbilddaten, die von verschachtelten/eingebetteten Image Serving- und Image Rendering-Anforderungen erzeugt werden, können zwischengespeichert werden, indem Sie cache=on in der verschachtelten/eingebetteten Anforderung angeben. Diese Daten werden im proprietären Format im Antwortdaten-Cache gespeichert.

Bilder von ausländischen HTTP-Servern werden auch im Antwortdaten-Cache gespeichert. Solche Bilder werden automatisch mit dem Überprüfungsprogramm validiert, bevor der Cache-Eintrag generiert wird.

Der Plattformserver erstellt Bildkatalogdaten für einen effizienten Zugriff. Diese Daten werden in `CS::CatalogCacheFolder` gespeichert.
