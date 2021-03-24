---
description: Zwischenbilddaten, die von verschachtelten/eingebetteten Image Serving- und Image Rendering-Anforderungen erzeugt werden, können zwischengespeichert werden, indem Sie cache=on in der verschachtelten/eingebetteten Anforderung angeben. Diese Daten werden im proprietären Format im Antwortdaten-Cache gespeichert.
solution: Experience Manager
title: Hilfedatenzwischenspeicher
feature: Dynamic Media Classic, SDK/API
role: Entwickler, Administrator, Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '133'
ht-degree: 0%

---


# Zusätzliche Daten-Caches{#auxiliary-data-caches}

Zwischenbilddaten, die von verschachtelten/eingebetteten Image Serving- und Image Rendering-Anforderungen erzeugt werden, können zwischengespeichert werden, indem Sie cache=on in der verschachtelten/eingebetteten Anforderung angeben. Diese Daten werden im proprietären Format im Antwortdaten-Cache gespeichert.

Bilder von ausländischen HTTP-Servern werden auch im Antwortdaten-Cache gespeichert. Solche Bilder werden automatisch mit dem Überprüfungsprogramm validiert, bevor der Cache-Eintrag generiert wird.

Der Plattformserver erstellt Bildkatalogdaten für einen effizienten Zugriff. Diese Daten werden in `CS::CatalogCacheFolder` gespeichert.
