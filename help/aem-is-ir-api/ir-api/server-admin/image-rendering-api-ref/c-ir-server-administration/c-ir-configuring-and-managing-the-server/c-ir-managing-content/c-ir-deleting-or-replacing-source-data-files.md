---
description: Vignettendateien können bei laufendem Server durch den Befehl req=release direkt vor dem Überschreiben ersetzt oder gelöscht werden.
solution: Experience Manager
title: Quelldatendateien löschen oder ersetzen
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 9daf8534-a844-4f4a-8e99-8dc751acd550
TQID: 'https://experienceleague.adobe.com/clXDwtsKfD4WkpgNvoJoXG19WvFkcOhdjtTGmoArpv4'
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
source-git-commit: 49c3ac586f6fb17608838f8dcf2c637822314fc7
workflow-type: tm+mt
source-wordcount: 207
ht-degree: 0%

---

# Quelldatendateien löschen oder ersetzen{#deleting-or-replacing-source-data-files}

Vignettendateien können bei laufendem Server durch den Befehl req=release direkt vor dem Überschreiben ersetzt oder gelöscht werden.

>[!NOTE]
>
>Eine Datendatei darf nicht ersetzt oder gelöscht werden, während der Render-Server darauf zugreift.

Beachten Sie, dass durch Löschen oder Ersetzen einer Quelldatendatei die Datei nur bis zur nächsten Anforderung, die auf diese Vignette zugreift, vom Render-Server geschlossen wird. Wenn eine Datei häufig verwendet wird, sind möglicherweise mehrere weitere Zustellversuche erforderlich.

Der Render-Server muss angehalten werden, um andere Datendateien zu ersetzen.

[!DNL Platform Server] Cache-Einträge werden automatisch ungültig, wenn Materialdateien oder Vignetten ersetzt werden. Durch Ersetzen von ICC-Profildateien werden Caches nicht ungültig gemacht.

Um die Komplikationen beim Ersetzen von Dateien zu vermeiden, wird empfohlen, einer Ersatzdatei einen neuen Namen zu geben und die entsprechenden Katalogeinträge zu aktualisieren. Dadurch können alle Datendateien ersetzt werden, während der Server live ist, und die Cache-Einträge des Servers werden automatisch veraltet, ohne dass ein zusätzlicher Eingriff erforderlich ist. Dieser Ansatz kann für alle Datendateien verwendet werden, die von Bildkatalogen verwaltet werden.

