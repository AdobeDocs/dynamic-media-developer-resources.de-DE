---
description: Verwenden Sie diese Servereinstellungen für das Cache-Clustering.
seo-description: Verwenden Sie diese Servereinstellungen für das Cache-Clustering.
seo-title: Cache-Clustering
solution: Experience Manager
title: Cache-Clustering
topic: Scene7 Image Serving - Image Rendering API
uuid: ed6335d7-26c9-45d8-95f6-6c05e788e449
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Cache-Clustering{#cache-clustering}

Verwenden Sie diese Servereinstellungen für das Cache-Clustering.

## PS::cacheCluster.hosts - Hosts {#section-319d2ba2915e40ac8b5ea9b4fe26a88b}

Liste von IP-Adressen, durch Semikolons getrennt. Schließen Sie die IP-Adressen aller Peer-Server ein, von denen dieser Host Cachedaten abrufen soll. Die IP-Adresse des lokalen Hosts kann aus praktischen Gründen angegeben werden; Dies ermöglicht für alle Server im Cluster dieselben Konfigurationseinstellungen.

## PS::cacheCluster.updateLocalCache - Lokaler Cache aktualisieren {#section-154c2c0af4544200a3499232bb130dde}

Auf &quot;Ja&quot;setzen, wenn ein von einem Peer-Server bereitgestellter Cache-Eintrag in den lokalen Antwortcache kopiert werden soll.

## PS::cacheCluster.queryTimeout - Abfrage Timeout {#section-8d2b10e15b3e44078d2d9bdb7c25bde0}

Beim Anfordern eines Cache-Eintrags von Peer-Servern wartet der Server, bis ein Server antwortet, dass er dieses bestimmte Datenelement enthält, oder bis alle Peer-Server darauf geantwortet haben, dass sie das Datenelement nicht haben, oder bis die mit dieser Einstellung angegebene Zeit (in msec) abgelaufen ist.

## PS::cacheCluster.fetchTimeout - Fetch Timeout {#section-41c42a29a26f43dc9cff50ad9fae1f14}

Gibt die maximale Anzahl von msec an, die der Server auf die Bereitstellung der tatsächlichen Cachedaten vom Peer-Server wartet. Wenn die vollständigen Daten nicht vor Ablauf des Timeouts bereitgestellt wurden, geht der Server davon aus, dass der Peer nicht mehr verfügbar ist. Der Cache-Eintrag wird dann lokal generiert.
