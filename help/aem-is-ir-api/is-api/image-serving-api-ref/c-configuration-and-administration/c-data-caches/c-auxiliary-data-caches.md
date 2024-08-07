---
description: Zwischenbilddaten, die von verschachtelten/eingebetteten Image Serving- und Image Rendering-Anforderungen erzeugt werden, können zwischengespeichert werden, indem Sie in der verschachtelten/eingebetteten Anforderung cache=on angeben. Diese Daten werden im Cache der Antwortdaten im proprietären Format gespeichert.
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

Zwischenbilddaten, die von verschachtelten/eingebetteten Image Serving- und Image Rendering-Anforderungen erzeugt werden, können zwischengespeichert werden, indem Sie in der verschachtelten/eingebetteten Anforderung cache=on angeben. Diese Daten werden im Cache der Antwortdaten im proprietären Format gespeichert.

Bilder, die von ausländischen HTTP-Servern abgerufen werden, werden auch im Cache für Antwortdaten gespeichert. Solche Bilder werden automatisch mit dem Überprüfungsdienstprogramm validiert, bevor der Cache-Eintrag generiert wird.

Der [!DNL Platform Server] kompiliert Bildkatalogdaten für einen effizienten Zugriff. Diese Daten werden in `CS::CatalogCacheFolder` gespeichert.
