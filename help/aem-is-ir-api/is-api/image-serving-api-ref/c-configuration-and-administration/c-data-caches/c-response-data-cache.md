---
description: Der Platform Server speichert alle Antwortbilder und bestimmte Textdaten auf dem Datenträger zwischen, es sei denn, eine Anforderung ist als nicht zwischenspeicherbar markiert.
solution: Experience Manager
title: Cache für Antwortdaten
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator,User
exl-id: f09e596d-2b85-4950-8515-d54a2c2e86ae
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '298'
ht-degree: 0%

---

# Cache für Antwortdaten{#response-data-cache}

Der Platform Server speichert alle Antwortbilder und bestimmte Textdaten auf dem Datenträger zwischen, es sei denn, eine Anforderung ist als nicht zwischenspeicherbar markiert.

Der Speicherort des Datenträgercache des Platform-Servers wird mit `PS::cache.rootPaths` festgelegt.

Bei Anwendungen mit hohen Cache-Trefferraten können Sie die Serverleistung und -kapazität erhöhen, indem Sie den Cache für Antwortdaten auf mehrere Festplattengeräte verteilen. Erstellen Sie dazu einen Cache-Stammordner auf jedem Datenträger und registrieren Sie ihn in `PS::cache.rootPaths`.

`PS::cache.maxSize` gibt die Gesamtgröße aller Cache-Einträge an, ohne Berücksichtigung eines Mehraufwands für das Dateisystem. Der tatsächlich benötigte Speicherplatz hängt von den Eigenschaften des Dateisystems ab, wie z. B. der Größe des Festplattenblocks und der Anzahl der Cache-Einträge. Es wird empfohlen, doppelt so viel Festplattenspeicher für den HTTP-Datenträger-Cache zu reservieren, wie von `PS::cache.maxSize` angegeben. Es wird ein am wenigsten verwendeter Algorithmus verwendet, um die Menge der zwischengespeicherten Daten innerhalb der Grenze zu halten.

Zusätzlich zu `PS::cache.maxSize` wird der Antwort-Cache auch verwaltet, indem die maximale Anzahl von Cache-Einträgen mit `PS::cache.maxEntries` begrenzt wird. Unter Linux muss diese Einstellung einen Wert angeben, der nicht größer ist als die Anzahl der verfügbaren Inodes auf der Cache-Partition.

>[!NOTE]
>
>Der Platform Server verwaltet einen Index für Arbeitsspeichercache. Die Größe dieses Index beträgt das 32-fache des Wertes von `PS::cache.maxEntries`. Möglicherweise müssen Sie die Heap-Größe des Platform-Servers erhöhen, um größere Caches aufzunehmen.

Das System verwendet eine Cacheindexdatei, die auf der Festplatte gespeichert wird, wenn der Server ordnungsgemäß heruntergefahren wird. Bei unerwarteten Ereignissen wie einem Stromausfall kann diese Datei nicht gespeichert werden. Außerdem kann es mehrere Minuten dauern, bis der Platform Server fertig ist.
