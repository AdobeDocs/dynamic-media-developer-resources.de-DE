---
description: Das Hinzufügen neuer Datendateien ist einfach und unkompliziert, aber beim Ersetzen vorhandener Datendateien, die vom Server aktiv verwendet werden, muss besondere Vorsicht geboten werden. Anstatt diese Dateien einfach zu ersetzen, wird empfohlen, der Ersatzdatei einen neuen Namen zu geben (z. B. ein Versionssuffix an den Dateinamen anhängen). Nachdem die neue Datei live geschaltet wurde, kann die alte Version gelöscht werden.
seo-description: Das Hinzufügen neuer Datendateien ist einfach und unkompliziert, aber beim Ersetzen vorhandener Datendateien, die vom Server aktiv verwendet werden, muss besondere Vorsicht geboten werden. Anstatt diese Dateien einfach zu ersetzen, wird empfohlen, der Ersatzdatei einen neuen Namen zu geben (z. B. ein Versionssuffix an den Dateinamen anhängen). Nachdem die neue Datei live geschaltet wurde, kann die alte Version gelöscht werden.
seo-title: Löschen oder Ersetzen von Datendateien
solution: Experience Manager
title: Löschen oder Ersetzen von Datendateien
uuid: 7b446144-48f6-4b50-93ec-0287425d932a
feature: Dynamic Media Classic, SDK/API
role: Entwickler, Administrator, Business Practitioner
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '402'
ht-degree: 0%

---


# Löschen oder Ersetzen von Datendateien{#deleting-or-replacing-data-files}

Das Hinzufügen neuer Datendateien ist einfach und unkompliziert, aber beim Ersetzen vorhandener Datendateien, die vom Server aktiv verwendet werden, muss besondere Vorsicht geboten werden. Anstatt diese Dateien einfach zu ersetzen, wird empfohlen, der Ersatzdatei einen neuen Namen zu geben (z. B. ein Versionssuffix an den Dateinamen anhängen). Nachdem die neue Datei live geschaltet wurde, kann die alte Version gelöscht werden.

>[!NOTE]
>
>Datendateien sollten während der aktiven Verwendung durch Image Serving nie ersetzt oder gelöscht werden. Andernfalls kann es zu Fehlern oder sogar zu einem Serverabsturz kommen.

Beachten Sie in allen Fällen, dass der Platform Server-Cache und die Clientcache-Einträge statisch sein müssen, bevor die aktualisierten Daten vom Client angezeigt werden. Spezifische Cache-Einträge können sofort mit dem Befehl `cache=validate` aktualisiert werden.

Änderungen an Schriftartdateien und ICC-Profil-Dateien werden nicht direkt vom Cache-Manager verfolgt. Wenn eine solche Ressource ohne Änderung der ID geändert wird, wird der Server-Cache nicht über die Änderung informiert und `cache=validate` führt nicht dazu, dass der Cache-Eintrag aktualisiert wird. `cache=update` kann verwendet werden, um die Wiederherstellung solcher Cache-Einträge zu erzwingen.

Um die Komplikationen beim Ersetzen von Dateien zu vermeiden, wird empfohlen, einer Ersatzdatei einen neuen Namen zu geben und die entsprechenden Katalogeinträge zu aktualisieren. Dadurch kann eine Datendatei während der Live-Schaltung des Servers ersetzt werden, und die Einträge im Server-Cache werden ohne weitere Intervention sofort statisch. Dieser Ansatz kann für ICC-Profile, Schriftarten und alle Bilder verwendet werden, die von Bildkatalogen verwaltet werden.
