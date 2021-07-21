---
description: Verwenden Sie diese Servereinstellungen für das Cache-Clustering.
solution: Experience Manager
title: Cache-Clustering
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: bd0267e7-ebf5-4995-b55e-89cb1a58de6d
source-git-commit: 38afaf2ed0f01868f02e236e941b23eed5b790aa
workflow-type: tm+mt
source-wordcount: '206'
ht-degree: 0%

---

# Cache-Clustering{#cache-clustering}

Verwenden Sie diese Servereinstellungen für das Cache-Clustering.

## PS::cacheCluster.hosts - Hosts {#section-319d2ba2915e40ac8b5ea9b4fe26a88b}

Liste der IP-Adressen, durch Semikolons getrennt. Schließen Sie die IP-Adressen aller Peer-Server ein, von denen dieser Host Cachedaten abrufen soll. Die IP-Adresse des lokalen Hosts kann aus praktischen Gründen enthalten sein. Dies ermöglicht die gleichen Konfigurationseinstellungen für alle Server im Cluster.

## PS::cacheCluster.updateLocalCache - Update Local Cache {#section-154c2c0af4544200a3499232bb130dde}

Setzen Sie dies auf &quot;Ja&quot;, wenn ein von einem Peer-Server bereitgestellter Cache-Eintrag in den lokalen Antwort-Cache kopiert werden soll.

## PS::cacheCluster.queryTimeout - Query Timeout {#section-8d2b10e15b3e44078d2d9bdb7c25bde0}

Bei der Anforderung eines Cache-Eintrags von Peer-Servern wartet der Server, bis ein Server antwortet, dass dieses bestimmte Datenelement enthält, oder bis alle Peer-Server darauf reagiert haben, dass sie das Datenelement nicht haben, oder bis die mit dieser Einstellung festgelegte Zeit (in ms) abgelaufen ist.

## PS::cacheCluster.fetchTimeout - Fetch Timeout {#section-41c42a29a26f43dc9cff50ad9fae1f14}

Gibt die maximale Anzahl von ms an, die der Server auf die Bereitstellung der tatsächlichen Cache-Daten vom Peer-Server wartet. Wenn die vollständigen Daten nicht vor Ablauf der Zeitüberschreitung bereitgestellt wurden, geht der Server davon aus, dass der Peer nicht verfügbar ist. Der Cache-Eintrag wird dann lokal generiert.
