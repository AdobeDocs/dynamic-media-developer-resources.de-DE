---
description: Vignettendateien können während der Live-Schaltung des Servers ersetzt oder gelöscht werden, indem Sie den Befehl req=release verwenden, unmittelbar bevor die Datei überschrieben wird.
solution: Experience Manager
title: Quelldatendateien löschen oder ersetzen
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator,User
exl-id: 9daf8534-a844-4f4a-8e99-8dc751acd550
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '214'
ht-degree: 0%

---

# Quelldatendateien löschen oder ersetzen{#deleting-or-replacing-source-data-files}

Vignettendateien können während der Live-Schaltung des Servers ersetzt oder gelöscht werden, indem Sie den Befehl req=release verwenden, unmittelbar bevor die Datei überschrieben wird.

>[!NOTE]
>
>Eine Datendatei darf nicht ersetzt oder gelöscht werden, während der Render Server darauf zugreift.

Beachten Sie, dass das Löschen oder Ersetzen einer Quelldatendatei nur dazu führt, dass der Render Server die Datei schließt, bis die nächste Anforderung, die auf diese Vignette zugreift, ausgeführt wird. Wenn eine Datei häufig verwendet wird, können mehrere weitere Versuche erforderlich sein.

Der Render-Server muss angehalten werden, um andere Datendateien zu ersetzen.

Zwischenspeichereinträge des Platform-Servers werden automatisch invalidiert, wenn Materialdateien oder Vignetten ersetzt werden. Durch das Ersetzen von ICC-Profildateien werden Caches nicht invalidiert.

Um das Ersetzen von Dateien zu vermeiden, wird empfohlen, einer Ersatzdatei einen neuen Namen zu geben und die entsprechenden Katalogeinträge zu aktualisieren. Dies ermöglicht das Ersetzen von Datendateien, während der Server aktiv ist, und bewirkt, dass Server-Cache-Einträge automatisch ohne zusätzliche Intervention veraltet werden. Dieser Ansatz kann für alle Datendateien verwendet werden, die von Bildkatalogen verwaltet werden.
