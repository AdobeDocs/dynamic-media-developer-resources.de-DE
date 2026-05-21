---
title: Cache für Antwortdaten
description: Die  [!DNL Platform Server]  alle Antwortbilder und bestimmte Textdaten auf der Festplatte zwischenspeichern, es sei denn, eine Anfrage wird als nicht zwischenspeicherbar markiert.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: f09e596d-2b85-4950-8515-d54a2c2e86ae
TQID: 'https://experienceleague.adobe.com/zxZqRHFCMKKDxOBb35IEZWEhTFhknDgCKcYatA6lqGs'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 282
ht-degree: 0%

---

# Cache für Antwortdaten{#response-data-cache}

Der [!DNL Platform Server] speichert alle Antwortbilder und bestimmte Textdaten zwischen, es sei denn, eine Anfrage wird als nicht zwischenspeicherbar markiert.

Der Speicherort des Festplatten-Cache des [!DNL Platform Server] wird mit `PS::cache.rootPaths` festgelegt.

Bei Anwendungen mit hohen Cache-Trefferraten können Sie die Serverleistung und -kapazität erhöhen, indem Sie den Cache für Antwortdaten auf mehrere Festplattengeräte verteilen. Erstellen Sie dazu einen Cache-Stammordner auf jeder Festplatte und registrieren Sie sie in `PS::cache.rootPaths`.

Die `PS::cache.maxSize` gibt die Gesamtgröße aller Cache-Einträge an, ohne Berücksichtigung eines Dateisystem-Overheads. Der erforderliche Speicherplatz hängt von den Dateisystemeigenschaften ab, z. B. der Größe des Festplattenblocks und der Anzahl der Cache-Einträge. Reservieren Sie doppelt so viel Speicherplatz für den HTTP-Datenträger-Cache wie in `PS::cache.maxSize` angegeben. Ein Algorithmus, der zuletzt verwendet wurde, wird verwendet, um die Menge der zwischengespeicherten Daten im Rahmen des Limits zu halten.

Zusätzlich zur `PS::cache.maxSize` wird der Antwort-Cache auch verwaltet, indem die maximale Anzahl von Cache-Einträgen mit `PS::cache.maxEntries` begrenzt wird. Unter Linux® muss diese Einstellung einen Wert angeben, der nicht größer ist als die Anzahl der verfügbaren Knoten auf der Cache-Partition.

>[!NOTE]
>
>Der [!DNL Platform Server] verwaltet einen Cache-Index im Arbeitsspeicher. Die Größe dieses Index ist 32-Byte-mal der Wert von `PS::cache.maxEntries`. Erhöhen Sie bei Bedarf die [!DNL Platform Server] Heap-Größe, um größere Caches aufzunehmen.

Das System verwendet eine Cache-Indexdatei, die auf der Festplatte gespeichert wird, wenn der Server ordnungsgemäß heruntergefahren wird. Wenn unerwartete Ereignisse wie ein Stromausfall auftreten, wird diese Datei möglicherweise nicht gespeichert. Es kann auch mehrere Minuten dauern, bis die [!DNL Platform Server] bereit ist.
