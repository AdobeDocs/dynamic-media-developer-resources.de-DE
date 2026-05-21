---
description: Cache-Clustering ermöglicht es mehreren Servern mit Lastenausgleich, Cache-Einträge im primären Antwort-Cache und im sekundären Daten-Cache (für verschachtelte/eingebettete Anforderungen) auszutauschen, wodurch die Reaktionsgeschwindigkeit des Servers erheblich gesteigert werden kann, da nicht mehr derselbe Cache-Eintrag auf mehreren Servern generiert werden muss.
solution: Experience Manager
title: Cache-Clustering
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: d1bea565-ac4e-4717-a53f-cbe706664598
TQID: 'https://experienceleague.adobe.com/J1QtNEy9i67oveb1oS2V6-fagqrrlC30oih8AS1g-N4'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 305
ht-degree: 0%

---

# Cache-Clustering{#cache-clustering}

Cache-Clustering ermöglicht es mehreren Servern mit Lastenausgleich, Cache-Einträge im primären Antwort-Cache und im sekundären Daten-Cache (für verschachtelte/eingebettete Anforderungen) auszutauschen, wodurch die Reaktionsgeschwindigkeit des Servers erheblich gesteigert werden kann, da nicht mehr derselbe Cache-Eintrag auf mehreren Servern generiert werden muss.

Wenn dies konfiguriert ist und ein Server eine Anfrage für ein Element empfängt, das sich nicht im lokalen Cache befindet, kontaktiert er die Peer-Server im Cluster. Dabei wird geprüft, ob das Datenelement bereits vorhanden ist, bevor der Bildserver aufgefordert wird, das Element zu generieren.

Das Cache-Clustering kommt in erster Linie Anwendungen zugute, die hochgradig zwischengespeicherte Inhalte enthalten. Die Serverauslastung sollte bei der erstmaligen Bereitstellung und der Live-Schaltung mit neuen Inhalten erheblich reduziert werden.

Zeitüberschreitungen und andere Sicherheitsmaßnahmen stellen sicher, dass das System weiterhin mit voller Kapazität funktioniert, auch wenn einer oder mehrere der Peer-Server offline sind.

Der Cache-Cluster kann in einer von zwei grundlegenden Konfigurationen ausgeführt werden:

* Wenn `PS::cacheCluster.updateLocalCache` aktiviert ist (Standard), wird jeder auf einem Peer-Server gefundene Cache-Eintrag in den lokalen Cache kopiert.

  Diese Konfiguration reduziert den Traffic zwischen den Peer-Servern. Außerdem werden die schnellsten Antwortzeiten geboten, während alle Cache-Einträge auf alle Server im Cluster repliziert werden. Dies ist die empfohlene Konfiguration.

* Wenn `PS::cacheCluster.updateLocalCache` deaktiviert ist, werden Daten von anderen Servern nicht in den lokalen Cache kopiert.

  Dadurch wird der verfügbare Speicherplatz für Cache-Daten multipliziert. Dadurch wird jedoch der Traffic zwischen den Peer-Servern erhöht und die Antwortzeiten insgesamt verringert. Verwenden Sie diese Konfiguration nur, wenn Sie niedrige Cache-Trefferraten sehen.
