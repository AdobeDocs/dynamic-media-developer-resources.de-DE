---
description: Das Cache-Clustering ermöglicht es mehreren Servern mit Lastenausgleich, Cache-Einträge im primären Antwort-Cache und im sekundären Daten-Cache (für verschachtelte/eingebettete Anforderungen) auszutauschen, wodurch die Reaktionsfähigkeit des Servers erheblich gesteigert werden kann, da nicht derselbe Cache-Eintrag auf mehreren Servern generiert werden muss.
solution: Experience Manager
title: Cache-Clustering
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: d1bea565-ac4e-4717-a53f-cbe706664598
source-git-commit: 38afaf2ed0f01868f02e236e941b23eed5b790aa
workflow-type: tm+mt
source-wordcount: '303'
ht-degree: 0%

---

# Cache-Clustering{#cache-clustering}

Das Cache-Clustering ermöglicht es mehreren Servern mit Lastenausgleich, Cache-Einträge im primären Antwort-Cache und im sekundären Daten-Cache (für verschachtelte/eingebettete Anforderungen) auszutauschen, wodurch die Reaktionsfähigkeit des Servers erheblich gesteigert werden kann, da nicht derselbe Cache-Eintrag auf mehreren Servern generiert werden muss.

Wenn dies konfiguriert ist und ein Server eine Anforderung für ein Element erhält, das sich nicht im lokalen Cache befindet, kontaktiert er die Peer-Server im Cluster. Er prüft, ob das Datenelement bereits vorhanden ist, bevor der Image-Server aufgefordert wird, das Element zu generieren.

Das Cache-Clustering profitiert in erster Linie von Anwendungen mit hochgradig zwischenspeicherbaren Inhalten. Das Laden von Servern sollte während der ersten Bereitstellung und beim Einsatz neuer Inhalte erheblich reduziert werden.

Timeouts und andere Sicherheitsmaßnahmen gewährleisten, dass das System auch dann weiterhin mit voller Kapazität funktioniert, wenn mindestens ein Peer-Server offline ist.

Der Cache-Cluster kann in einer von zwei grundlegenden Konfigurationen ausgeführt werden:

* Wenn `PS::cacheCluster.updateLocalCache` aktiviert ist (Standard), wird jeder Cache-Eintrag, der auf einem Peer-Server gefunden wird, in den lokalen Cache kopiert.

  Diese Konfiguration reduziert den Traffic zwischen den Peer-Servern. Es bietet außerdem die schnellsten Reaktionszeiten, um alle Cache-Einträge auf alle Server im Cluster replizieren zu können. Dies ist die empfohlene Konfiguration.

* Wenn `PS::cacheCluster.updateLocalCache` deaktiviert ist, werden Daten von anderen Servern nicht in den lokalen Cache kopiert.

  Dadurch wird der verfügbare Speicherplatz für Cache-Daten multipliziert. Es erhöht jedoch den Traffic zwischen den Peer-Servern und reduziert die Gesamtansprechzeiten. Verwenden Sie diese Konfiguration nur, wenn Sie niedrige Cache-Trefferraten sehen.
