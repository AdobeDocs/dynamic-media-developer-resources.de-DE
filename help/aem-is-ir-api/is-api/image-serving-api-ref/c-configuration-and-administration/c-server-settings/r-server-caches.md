---
description: Verwenden Sie diese Server-Einstellungen für Server-Caches.
solution: Experience Manager
title: Server-Caches
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 6a8d44d3-ecac-4fe0-9f81-28b1cd55e7e1
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '296'
ht-degree: 0%

---

# Server-Caches{#server-caches}

Verwenden Sie diese Server-Einstellungen für Server-Caches.

## PS:cache.rootPaths - Zwischenspeichern von Datenordnern {#section-f0aa808304d74ecdb0c3644f11906c53}

Die Stammordner für den Datenträger-Cache des [!DNL Platform Server]. Ein oder mehrere absolute Dateipfade oder -pfade relativ zu *[!DNL install_folder]*, getrennt durch Semikolons (;). Die Daten für den HTTP-Antwort-Cache sind gleichmäßig über alle angegebenen Ordner verteilt. Die Caches für die zusätzlichen Caches (kompilierte Bildkataloge und Fremdbilddaten) befinden sich im primären Cache-Ordner (dem ersten Ordner in der Liste).

## PS::cache.maxSize - Größe des Antwort-Daten-Caches {#section-ed2e1e7ba4bd4e13b77bb20c4cacddb4}

Die maximale Größe des HTTP-Antwort-Caches in Byte. Mit dieser Einstellung wird die Menge der tatsächlich im Cache zu speichernden Daten begrenzt; der Dateisystem-Overhead wird nicht berücksichtigt. (Siehe [Antwort-Daten-Cache](../../../../is-api/image-serving-api-ref/c-configuration-and-administration/c-data-caches/c-response-data-cache.md#concept-81ea996c242441f2a69f7e9d9b3a29ca).) Wenn mehrere Cache-Daten-Ordner angegeben sind, werden die Cache-Daten gleichmäßig auf alle Ordner verteilt. Der Wert von `cache.maxSize` in [!DNL PlatformServer.conf] ist in Byte.

## PS::cache.maxEntries - Antwort Data Cache Max Entries {#section-5603e327e90542a5b50aeeb27b080410}

Die Anzahl der Einträge, die für den Cache-Index der speicherinternen HTTP-Antwort zugewiesen sind.

>[!NOTE]
>
>Stellen Sie unter Linux sicher, dass ausreichend i-Knoten für die Cache-Partition zugewiesen sind, um zu vermeiden, dass die i-Knoten ausgehen.

## IS::TempDirectory - Ordner für temporäre Dateien des Bildservers {#section-42ea1e7a68c444878f7245c5bbcb1672}

Der Bildserver muss gelegentlich Zwischendaten auf der Festplatte speichern. Der Pfad kann absolut oder relativ zu *[!DNL install_folder]* sein.

>[!NOTE]
>
>Der neue Ordner muss erstellt werden, bevor diese Einstellung geändert werden kann. Stellen Sie sicher, dass die Zugriffsberechtigungen so festgelegt sind, dass der Bildserver die volle Kontrolle über den Ordner hat.

## SV::temp - Ordner für temporäre Dateien des Server-Verantwortlichen {#section-fd2cd5ef7e814a4bb56aaf5525e1a154}

Der Server Supervisor muss gelegentlich Zwischendaten auf der Festplatte speichern. Der Pfad kann absolut oder relativ zu *[!DNL install_folder]* sein. Die Standardeinstellung ist [!DNL *[!DNL install_folder]*/temp].

>[!NOTE]
>
>Der neue Ordner muss erstellt werden, bevor diese Einstellung geändert werden kann. Stellen Sie sicher, dass die Zugriffsberechtigungen so festgelegt sind, dass der Server Supervisor die volle Kontrolle über den Ordner hat.
