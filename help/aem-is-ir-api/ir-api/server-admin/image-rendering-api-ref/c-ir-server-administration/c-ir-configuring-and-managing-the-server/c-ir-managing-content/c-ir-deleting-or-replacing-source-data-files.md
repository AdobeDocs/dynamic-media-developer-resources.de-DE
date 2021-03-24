---
description: Vignettendateien können während der Live-Schaltung durch den Befehl req=release ersetzt oder gelöscht werden, bevor die Datei überschrieben wird.
solution: Experience Manager
title: Löschen oder Ersetzen von Quelldatendateien
feature: Dynamic Media Classic, SDK/API
role: Entwickler, Administrator, Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '218'
ht-degree: 0%

---


# Löschen oder Ersetzen von Quelldatendateien{#deleting-or-replacing-source-data-files}

Vignettendateien können während der Live-Schaltung durch den Befehl req=release ersetzt oder gelöscht werden, bevor die Datei überschrieben wird.

>[!NOTE]
>
>Eine Datendatei darf nicht ersetzt oder gelöscht werden, während der Render-Server darauf zugreift.

Beachten Sie, dass beim Löschen oder Ersetzen einer Quelldatendatei der Render-Server die Datei nur bis zur nächsten Anforderung schließt, die auf diese Vignette zugreift. Mehrere weitere Zustellversuche sind ggf. erforderlich, wenn eine Datei stark verwendet wird.

Der Render-Server muss beendet werden, um andere Datendateien zu ersetzen.

Plattformserver-Cache-Einträge werden automatisch ungültig, wenn Materialdateien oder Vignetten ersetzt werden. Durch das Ersetzen von ICC-Profil-Dateien werden keine Zwischenspeicher ungültig.

Um die Komplikationen beim Ersetzen von Dateien zu vermeiden, wird empfohlen, einer Ersatzdatei einen neuen Namen zu geben und die entsprechenden Katalogeinträge zu aktualisieren. Dadurch können Datendateien ersetzt werden, während der Server live ist, und Server-Cache-Einträge werden automatisch deaktiviert, ohne dass ein weiterer Eingriff erforderlich ist. Dieser Ansatz kann für alle Datendateien verwendet werden, die von Bildkatalogen verwaltet werden.
