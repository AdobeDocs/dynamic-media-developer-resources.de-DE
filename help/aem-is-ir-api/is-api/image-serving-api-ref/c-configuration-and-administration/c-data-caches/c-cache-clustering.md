---
description: Das Cache-Clustering ermöglicht es mehreren Servern mit Lastenausgleich, Cache-Einträge im primären Antwortcache und im sekundären Datencache (für verschachtelte/eingebettete Anforderungen) auszutauschen, wodurch die Reaktionsgeschwindigkeit des Servers erheblich gesteigert werden kann, da der Cache-Eintrag nicht mehr auf mehreren Servern generiert werden muss.
seo-description: Das Cache-Clustering ermöglicht es mehreren Servern mit Lastenausgleich, Cache-Einträge im primären Antwortcache und im sekundären Datencache (für verschachtelte/eingebettete Anforderungen) auszutauschen, wodurch die Reaktionsgeschwindigkeit des Servers erheblich gesteigert werden kann, da der Cache-Eintrag nicht mehr auf mehreren Servern generiert werden muss.
seo-title: Cache-Clustering
solution: Experience Manager
title: Cache-Clustering
topic: Scene7 Image Serving - Image Rendering API
uuid: 347165d6-a9e7-406e-81a8-8a91f745ce27
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '350'
ht-degree: 0%

---


# Cache-Clustering{#cache-clustering}

Das Cache-Clustering ermöglicht es mehreren Servern mit Lastenausgleich, Cache-Einträge im primären Antwortcache und im sekundären Datencache (für verschachtelte/eingebettete Anforderungen) auszutauschen, wodurch die Reaktionsgeschwindigkeit des Servers erheblich gesteigert werden kann, da der Cache-Eintrag nicht mehr auf mehreren Servern generiert werden muss.

Wenn dies so konfiguriert ist und ein Server eine Anforderung für ein Element erhält, das sich nicht im lokalen Cache befindet, kontaktiert er die Peer-Server im Cluster. Es wird überprüft, ob das Datenelement bereits vorhanden ist, bevor der Image-Server aufgefordert wird, das Element zu generieren.

Das Cache-Clustering nutzt in erster Linie Anwendungen mit hochgradig zwischenspeicherbaren Inhalten. Die Serverladezeit sollte während der ersten Bereitstellung und beim Einsatz neuer Inhalte erheblich reduziert werden.

Timeouts und andere Sicherheitsvorkehrungen stellen sicher, dass das System auch dann weiterhin mit voller Kapazität funktioniert, wenn ein oder mehrere Peer-Server offline sind.

Der Cache-Cluster kann in einer der beiden grundlegenden Konfigurationen ausgeführt werden:

* Ist `PS::cacheCluster.updateLocalCache` aktiviert (Standard), wird jeder auf einem Peer-Server gefundene Cache-Eintrag in den lokalen Cache kopiert.

   Diese Konfiguration verringert den Traffic zwischen den Peer-Servern. Es bietet außerdem die schnellsten Reaktionszeiten, sodass alle Cache-Einträge auf alle Server im Cluster repliziert werden müssen. Dies ist die empfohlene Konfiguration.

* Wenn `PS::cacheCluster.updateLocalCache` deaktiviert ist, werden Daten von anderen Servern nicht in den lokalen Cache kopiert.

   Dadurch wird der verfügbare Speicherplatz für Cachedaten multipliziert. Sie erhöht jedoch den Traffic zwischen den Peer-Servern und verringert die Gesamtansprechzeit. Verwenden Sie diese Konfiguration nur, wenn Sie niedrige Cache-Trefferraten sehen.

