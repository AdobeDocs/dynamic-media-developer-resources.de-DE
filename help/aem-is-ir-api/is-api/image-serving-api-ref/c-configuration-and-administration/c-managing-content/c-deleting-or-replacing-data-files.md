---
description: Während das Hinzufügen neuer Datendateien einfach und unkompliziert ist, muss beim Ersetzen vorhandener Datendateien, die aktiv vom Server verwendet werden, besondere Vorsicht angewendet werden. Anstatt solche Dateien einfach zu ersetzen, wird empfohlen, der Ersatzdatei einen neuen Namen zu geben (hängen Sie beispielsweise ein Versionssuffix an den Dateinamen an). Nachdem die neue Datei live geschaltet wurde, kann die alte Version gelöscht werden.
solution: Experience Manager
title: Datendateien löschen oder ersetzen
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 1624e1b5-ba79-45db-8309-457a44fddab8
TQID: 'https://experienceleague.adobe.com/RLwRWtyvlbeSlQy4woV6-a-nrq3Sz1q7gviUsTrL2Q4'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 322
ht-degree: 0%

---

# Datendateien löschen oder ersetzen{#deleting-or-replacing-data-files}

Während das Hinzufügen neuer Datendateien einfach und unkompliziert ist, muss beim Ersetzen vorhandener Datendateien, die aktiv vom Server verwendet werden, besondere Vorsicht angewendet werden. Anstatt solche Dateien einfach zu ersetzen, wird empfohlen, der Ersatzdatei einen neuen Namen zu geben (hängen Sie beispielsweise ein Versionssuffix an den Dateinamen an). Nachdem die neue Datei live geschaltet wurde, kann die alte Version gelöscht werden.

>[!NOTE]
>
>Datendateien sollten während der aktiven Verwendung von Image Serving niemals ersetzt oder gelöscht werden. Fehler oder sogar ein Serverabsturz können andernfalls auftreten.

Denken Sie in allen Fällen daran, dass der [!DNL Platform Server]-Cache und die Client-Cache-Einträge veraltet sein müssen, bevor die aktualisierten Daten vom Client angezeigt werden. Bestimmte Cache-Einträge können mit dem Befehl `cache=validate` sofort aktualisiert werden.

Änderungen an Schriftarten und ICC-Profildateien werden nicht direkt vom Cache-Manager verfolgt. Wenn eine solche Ressource geändert wird, ohne ihre ID zu ändern, weiß der Server-Cache nicht über die Änderung und `cache=validate` bewirkt nicht, dass der Cache-Eintrag aktualisiert wird. `cache=update` kann verwendet werden, um die Neuerstellung solcher Cache-Einträge zu erzwingen.

Um die Komplikationen beim Ersetzen von Dateien zu vermeiden, wird empfohlen, einer Ersatzdatei einen neuen Namen zu geben und die entsprechenden Katalogeinträge zu aktualisieren. Dies ermöglicht den Austausch jeder Datendatei, während der Server live ist, und führt dazu, dass die Cache-Einträge des Servers sofort veralten, ohne dass ein zusätzlicher Eingriff erforderlich ist. Dieser Ansatz kann für ICC-Profile, Schriftarten und alle Bilder verwendet werden, die von Bildkatalogen verwaltet werden.
