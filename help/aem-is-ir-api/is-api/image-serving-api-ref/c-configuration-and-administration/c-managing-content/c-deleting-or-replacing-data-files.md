---
description: Das Hinzufügen neuer Datendateien ist einfach und unkompliziert, es muss jedoch besondere Sorgfalt walten lassen, wenn bestehende Datendateien ersetzt werden, die aktiv vom Server verwendet werden. Anstatt diese Dateien einfach zu ersetzen, wird empfohlen, der Ersatzdatei einen neuen Namen zu geben (z. B. ein Versionssuffix an den Dateinamen anhängen). Nachdem die neue Datei live geschaltet wurde, kann die alte Version gelöscht werden.
solution: Experience Manager
title: Datendateien löschen oder ersetzen
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 1624e1b5-ba79-45db-8309-457a44fddab8
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '319'
ht-degree: 0%

---

# Datendateien löschen oder ersetzen{#deleting-or-replacing-data-files}

Das Hinzufügen neuer Datendateien ist einfach und unkompliziert, es muss jedoch besondere Sorgfalt walten lassen, wenn bestehende Datendateien ersetzt werden, die aktiv vom Server verwendet werden. Anstatt diese Dateien einfach zu ersetzen, wird empfohlen, der Ersatzdatei einen neuen Namen zu geben (z. B. ein Versionssuffix an den Dateinamen anhängen). Nachdem die neue Datei live geschaltet wurde, kann die alte Version gelöscht werden.

>[!NOTE]
>
>Datendateien sollten während der aktiven Verwendung durch Image Serving nie ersetzt oder gelöscht werden. Andernfalls kann es zu Fehlern oder sogar zum Absturz des Servers kommen.

Beachten Sie in allen Fällen, dass die Variable [!DNL Platform Server] Cache- und Client-Cache-Einträge müssen veraltet sein, bevor die aktualisierten Daten vom Client angezeigt werden. Bestimmte Cache-Einträge können sofort mit der `cache=validate` Befehl.

Änderungen an Schriftartendateien und ICC-Profildateien werden vom Cache-Manager nicht direkt verfolgt. Wenn eine solche Ressource geändert wird, ohne ihre ID zu ändern, weiß der Server-Cache nichts über die Änderung und `cache=validate` führt nicht dazu, dass der Cache-Eintrag aktualisiert wird. `cache=update` kann verwendet werden, um die Neuerstellung solcher Cache-Einträge zu erzwingen.

Um das Ersetzen von Dateien zu vermeiden, wird empfohlen, einer Ersatzdatei einen neuen Namen zu geben und die entsprechenden Katalogeinträge zu aktualisieren. Dadurch können Datendateien ersetzt werden, während der Server aktiv ist, und Server-Cache-Einträge werden sofort ohne zusätzliche Intervention veraltet. Dieser Ansatz kann für ICC-Profile, Schriftarten und alle Bilder verwendet werden, die von Bildkatalogen verwaltet werden.
