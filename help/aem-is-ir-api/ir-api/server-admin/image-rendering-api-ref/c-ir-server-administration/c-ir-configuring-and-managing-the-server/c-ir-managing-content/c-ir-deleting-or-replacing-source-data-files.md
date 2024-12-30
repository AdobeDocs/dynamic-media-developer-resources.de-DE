---
description: Vignettendateien können bei laufendem Server durch den Befehl req=release direkt vor dem Überschreiben ersetzt oder gelöscht werden.
solution: Experience Manager
title: Quelldatendateien löschen oder ersetzen
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 9daf8534-a844-4f4a-8e99-8dc751acd550
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '207'
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
