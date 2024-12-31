---
description: Verwenden Sie diese Server-Einstellungen für das Cache-Clustering.
solution: Experience Manager
title: Cache-Clustering
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: bd0267e7-ebf5-4995-b55e-89cb1a58de6d
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '199'
ht-degree: 0%

---

# Cache-Clustering{#cache-clustering}

Verwenden Sie diese Server-Einstellungen für das Cache-Clustering.

## PS::cacheCluster.hosts - Hosts {#section-319d2ba2915e40ac8b5ea9b4fe26a88b}

Liste der IP-Adressen, durch Semikolons getrennt Schließen Sie die IP-Adressen aller Peer-Server ein, von denen dieser Host Cache-Daten abrufen soll. Die IP-Adresse des lokalen Hosts kann aus praktischen Gründen eingeschlossen werden. Dies ermöglicht dieselben Konfigurationseinstellungen für alle Server im Cluster.

## PS::cacheCluster.updateLocalCache - Lokalen Cache aktualisieren {#section-154c2c0af4544200a3499232bb130dde}

Auf „Ja“ setzen, wenn ein von einem Peer-Server bereitgestellter Cache-Eintrag in den lokalen Antwort-Cache kopiert werden soll.

## PS::cacheCluster.queryTimeout - Abfrage-Timeout {#section-8d2b10e15b3e44078d2d9bdb7c25bde0}

Beim Anfordern eines Cache-Eintrags von Peer-Servern wartet der Server, bis ein Server antwortet, dass er dieses bestimmte Datenelement hat, oder bis alle Peer-Server geantwortet haben, dass sie das Datenelement nicht haben, oder bis die mit dieser Einstellung angegebene Zeit (in ms) abgelaufen ist.

## PS::cacheCluster.fetchTimeout - Fetch Timeout {#section-41c42a29a26f43dc9cff50ad9fae1f14}

Gibt die maximale Anzahl von ms an, die der Server auf die tatsächliche Bereitstellung der Cache-Daten vom Peer-Server wartet. Wenn die vollständigen Daten nicht vor Ablauf der maximalen Wartezeit bereitgestellt wurden, geht der Server davon aus, dass die Gegenstelle nicht mehr verfügbar ist. Der Cache-Eintrag wird dann lokal generiert.
