---
description: Der Plattformserver speichert alle Antwortbilder und bestimmte Textdaten auf dem Datenträger zwischen, es sei denn, eine Anforderung ist als nicht zwischenspeicherbar gekennzeichnet.
solution: Experience Manager
title: Antwortdatencache
feature: Dynamic Media Classic, SDK/API
role: Entwickler, Administrator, Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '302'
ht-degree: 0%

---


# Cache für Antwortdaten{#response-data-cache}

Der Plattformserver speichert alle Antwortbilder und bestimmte Textdaten auf dem Datenträger zwischen, es sei denn, eine Anforderung ist als nicht zwischenspeicherbar gekennzeichnet.

Der Speicherort des Datenträgercache des Plattformservers wird mit `PS::cache.rootPaths` festgelegt.

Bei Anwendungen mit hohen Cache-Trefferraten können Sie die Serverleistung und -kapazität erhöhen, indem Sie den Antwortdaten-Cache auf mehrere Festplattengeräte verteilen. Dazu erstellen Sie auf jeder Festplatte einen Cache-Stammordner und registrieren diese in `PS::cache.rootPaths`.

`PS::cache.maxSize` gibt die Gesamtgröße aller Cache-Einträge an, wobei kein Dateisystem-Overhead berücksichtigt wird. Der tatsächlich benötigte Speicherplatz hängt von den Eigenschaften des Dateisystems ab, wie z. B. der Blockgröße des Datenträgers und der Anzahl der Cacheeinträge. Es wird empfohlen, doppelt so viel Speicherplatz für den HTTP-Datenträger-Cache zu reservieren wie der von `PS::cache.maxSize` angegebene Betrag. Es wird ein Algorithmus verwendet, der am wenigsten zuletzt verwendet wird, um die Menge der zwischengespeicherten Daten innerhalb der Grenze zu halten.

Zusätzlich zu `PS::cache.maxSize` wird der Antwort-Cache auch verwaltet, indem die maximale Anzahl von Cache-Einträgen mit `PS::cache.maxEntries` begrenzt wird. Unter Linux muss diese Einstellung einen Wert angeben, der nicht größer ist als die Anzahl der verfügbaren Inodes auf der Cache-Partition.

>[!NOTE]
>
>Der Plattformserver verwaltet einen Cache-Index im Arbeitsspeicher. Die Größe dieses Indexes beträgt das 32-fache des Werts von `PS::cache.maxEntries`. Möglicherweise müssen Sie die Heap-Größe des Plattformservers erhöhen, um größere Caches aufzunehmen.

Das System verwendet eine Cache-Indexdatei, die auf dem Datenträger gespeichert wird, wenn der Server ordnungsgemäß heruntergefahren wird. Bei unerwarteten Ereignissen wie einem Stromausfall wird diese Datei möglicherweise nicht gespeichert. Außerdem kann es mehrere Minuten dauern, bis der Plattformserver fertig ist.
