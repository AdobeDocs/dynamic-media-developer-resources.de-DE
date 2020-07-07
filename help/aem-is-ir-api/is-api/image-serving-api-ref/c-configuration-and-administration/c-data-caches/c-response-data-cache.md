---
description: Der Platform Server speichert alle Antwortbilder und bestimmte Textdaten auf dem Datenträger zwischen, es sei denn, eine Anforderung ist als nicht zwischenspeicherbar gekennzeichnet.
seo-description: Der Platform Server speichert alle Antwortbilder und bestimmte Textdaten auf dem Datenträger zwischen, es sei denn, eine Anforderung ist als nicht zwischenspeicherbar gekennzeichnet.
seo-title: Antwortdatencache
solution: Experience Manager
title: Antwortdatencache
topic: Scene7 Image Serving - Image Rendering API
uuid: dbfda210-3b50-4e8c-8d77-7263ae4e80a2
translation-type: tm+mt
source-git-commit: e8e5b07329bde3e23ee095d5022da62d67e9478c
workflow-type: tm+mt
source-wordcount: '316'
ht-degree: 0%

---


# Antwortdatencache{#response-data-cache}

Der Platform Server speichert alle Antwortbilder und bestimmte Textdaten auf dem Datenträger zwischen, es sei denn, eine Anforderung ist als nicht zwischenspeicherbar gekennzeichnet.

Der Speicherort des Datenträgercache des Platform-Servers wird mit festgelegt `PS::cache.rootPaths`.

Bei Anwendungen mit hohen Cache-Trefferraten können Sie die Serverleistung und -kapazität erhöhen, indem Sie den Antwortdaten-Cache auf mehrere Festplattengeräte verteilen. Erstellen Sie dazu auf jeder Festplatte einen Cache-Stammordner und registrieren Sie ihn `PS::cache.rootPaths`.

`PS::cache.maxSize` gibt die Gesamtgröße aller Cache-Einträge an, wobei kein Dateisystem-Overhead berücksichtigt wird. Der tatsächlich benötigte Speicherplatz hängt von den Eigenschaften des Dateisystems ab, wie z. B. der Blockgröße des Datenträgers und der Anzahl der Cacheeinträge. Es wird empfohlen, doppelt so viel Speicherplatz für den HTTP-Datenträger-Cache zu reservieren, wie von `PS::cache.maxSize`Ihnen angegeben. Es wird ein Algorithmus verwendet, der am wenigsten zuletzt verwendet wird, um die Menge der zwischengespeicherten Daten innerhalb der Grenze zu halten.

Darüber hinaus wird `PS::cache.maxSize`der Antwortcache auch verwaltet, indem die maximale Anzahl von Cache-Einträgen mit begrenzt wird `PS::cache.maxEntries`. Unter Linux muss diese Einstellung einen Wert angeben, der nicht größer ist als die Anzahl der verfügbaren Inodes auf der Cache-Partition.

>[!NOTE]
>
>Der Platform Server verwaltet einen Cache-Index im Arbeitsspeicher. Die Größe dieses Indexes beträgt das 32-fache des Werts `PS::cache.maxEntries`. Möglicherweise müssen Sie die Heap-Größe des Platform-Servers erhöhen, um größere Caches aufzunehmen.

Das System verwendet eine Cache-Indexdatei, die auf dem Datenträger gespeichert wird, wenn der Server ordnungsgemäß heruntergefahren wird. Bei unerwarteten Ereignissen wie einem Stromausfall wird diese Datei möglicherweise nicht gespeichert. Außerdem kann es mehrere Minuten dauern, bis der Platform-Server fertig ist.
