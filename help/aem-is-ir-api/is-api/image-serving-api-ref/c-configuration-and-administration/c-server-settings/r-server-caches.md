---
description: Verwenden Sie diese Servereinstellungen für Server-Caches.
solution: Experience Manager
title: Server-Caches
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 6a8d44d3-ecac-4fe0-9f81-28b1cd55e7e1
source-git-commit: 38afaf2ed0f01868f02e236e941b23eed5b790aa
workflow-type: tm+mt
source-wordcount: '305'
ht-degree: 0%

---

# Server-Caches{#server-caches}

Verwenden Sie diese Servereinstellungen für Server-Caches.

## PS::cache.rootPaths - Cache Data Folders {#section-f0aa808304d74ecdb0c3644f11906c53}

Die Stammordner für den Datenträgercache des Platform-Servers. Mindestens ein absoluter Dateipfad oder Pfad relativ zu *[!DNL install_folder]*, getrennt durch Semikolons (;). Die Daten für den HTTP-Antwort-Cache werden gleichmäßig über alle angegebenen Ordner verteilt. Die Caches für die zusätzlichen Caches (kompilierte Bildkataloge und ausländische Bilddaten) befinden sich im primären Cache-Ordner (dem ersten Ordner in der Liste).

## PS::cache.maxSize - Response Data Cache Size {#section-ed2e1e7ba4bd4e13b77bb20c4cacddb4}

Die maximale Größe des HTTP-Antwort-Cache in Byte. Mit dieser Einstellung wird die Menge der tatsächlich zwischengespeicherten Daten begrenzt. wird der Verwaltungsaufwand des Dateisystems nicht berücksichtigt. (Siehe [Response Data Cache](../../../../is-api/image-serving-api-ref/c-configuration-and-administration/c-data-caches/c-response-data-cache.md#concept-81ea996c242441f2a69f7e9d9b3a29ca).) Wenn mehrere Cache-Datenordner angegeben sind, werden die Cachedaten gleichmäßig über alle Ordner verteilt. Der Wert von `cache.maxSize` in [!DNL PlatformServer.conf] wird in Byte angegeben.

## PS::cache.maxEntries - Response Data Cache Max Entries {#section-5603e327e90542a5b50aeeb27b080410}

Die Anzahl der Einträge, die für den Cache-Index der HTTP-Antworten im Arbeitsspeicher zugewiesen sind.

>[!NOTE]
>
>Stellen Sie unter Linux sicher, dass ausreichende i-Knoten für die Cache-Partition zugewiesen sind, um zu vermeiden, dass i-Knoten ausgehen.

## IS::TempDirectory - Temporärer Ordner für Image-Server-Dateien {#section-42ea1e7a68c444878f7245c5bbcb1672}

Der Image-Server muss gelegentlich Zwischendaten auf der Festplatte speichern. Der Pfad kann absolut oder relativ zu *[!DNL install_folder]* sein.

>[!NOTE]
>
>Der neue Ordner muss erstellt werden, bevor diese Einstellung geändert werden kann. Stellen Sie sicher, dass die Zugriffsberechtigungen so festgelegt sind, dass der Image-Server die volle Kontrolle über den Ordner hat.

## SV::temp - Temporärer Ordner für Server-Supervisor-Dateien {#section-fd2cd5ef7e814a4bb56aaf5525e1a154}

Der Server Supervisor muss gelegentlich Zwischendaten auf der Festplatte speichern. Der Pfad kann absolut oder relativ zu *[!DNL install_folder]* sein. Die Standardeinstellung ist [!DNL *[!DNL install_folder]*/temp].

>[!NOTE]
>
>Der neue Ordner muss erstellt werden, bevor diese Einstellung geändert werden kann. Stellen Sie sicher, dass die Zugriffsberechtigungen so festgelegt sind, dass der Server Supervisor die volle Kontrolle über den Ordner hat.
