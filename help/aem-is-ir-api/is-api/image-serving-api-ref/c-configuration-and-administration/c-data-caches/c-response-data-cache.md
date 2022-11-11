---
description: Die [!DNL Platform Server] speichert alle Antwortbilder und bestimmte Textdaten auf die Festplatte, es sei denn, eine Anforderung ist als nicht zwischenspeicherbar markiert.
solution: Experience Manager
title: Cache für Antwortdaten
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: f09e596d-2b85-4950-8515-d54a2c2e86ae
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '282'
ht-degree: 0%

---

# Cache für Antwortdaten{#response-data-cache}

Die [!DNL Platform Server] speichert alle Antwortbilder und bestimmte Textdaten auf die Festplatte, es sei denn, eine Anforderung ist als nicht zwischenspeicherbar markiert.

Der Speicherort der [!DNL Platform Server]Der Datenträgercache wird mit `PS::cache.rootPaths`.

Bei Anwendungen mit hohen Cache-Trefferraten können Sie die Serverleistung und -kapazität erhöhen, indem Sie den Cache für Antwortdaten auf mehrere Festplattengeräte verteilen. Erstellen Sie dazu einen Cache-Stammordner auf jedem Datenträger und registrieren Sie ihn in `PS::cache.rootPaths`.

`PS::cache.maxSize` gibt die Gesamtgröße aller Cache-Einträge an, ohne Berücksichtigung eines Mehraufwands für das Dateisystem. Der tatsächlich benötigte Speicherplatz hängt von den Eigenschaften des Dateisystems ab, wie z. B. der Größe des Festplattenblocks und der Anzahl der Cache-Einträge. Es wird empfohlen, doppelt so viel Festplattenspeicher für den HTTP-Datenträger-Cache zu reservieren wie den von `PS::cache.maxSize`. Es wird ein am wenigsten verwendeter Algorithmus verwendet, um die Menge der zwischengespeicherten Daten innerhalb der Grenze zu halten.

Zusätzlich zu `PS::cache.maxSize`, wird der Antwort-Cache auch verwaltet, indem die maximale Anzahl von Cache-Einträgen mit `PS::cache.maxEntries`. Unter Linux muss diese Einstellung einen Wert angeben, der nicht größer ist als die Anzahl der verfügbaren Inodes auf der Cache-Partition.

>[!NOTE]
>
>Die [!DNL Platform Server] verwaltet einen Cache-Index im Arbeitsspeicher. Die Größe dieses Index beträgt das 32-Byte-fache des Werts von `PS::cache.maxEntries`. Möglicherweise müssen Sie die [!DNL Platform Server] Heap-Größe für größere Caches.

Das System verwendet eine Cacheindexdatei, die auf der Festplatte gespeichert wird, wenn der Server ordnungsgemäß heruntergefahren wird. Bei unerwarteten Ereignissen wie einem Stromausfall kann diese Datei nicht gespeichert werden. Außerdem kann es mehrere Minuten dauern, bis die [!DNL Platform Server] bereit zu werden.
