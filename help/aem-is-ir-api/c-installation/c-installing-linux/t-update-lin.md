---
description: Verwenden Sie dieses Verfahren bei der Aktualisierung von Dynamic Media Image Serving unter Linux.
solution: Experience Manager
title: Aktualisierung von IS 4.7.4 oder höher
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 54733fcc-c4e3-4501-8a3d-000778678bdb
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '212'
ht-degree: 0%

---

# Aktualisierung von IS 4.7.4 oder höher{#updating-from-is-or-later}

Verwenden Sie dieses Verfahren bei der Aktualisierung von Dynamic Media Image Serving unter Linux.

Wenn Sie ein Upgrade von einer älteren Version von Image Serving durchführen, wenden Sie sich an den Support, um den korrekten Prozess durchzuführen.

Der Ordner [!DNL webapps] kann bei der Aktualisierung gelöscht werden. Bitte sichern Sie den Ordner [!DNL webapps] vor der Aktualisierung.

1. Melden Sie sich mit Root-Berechtigungen bei Ihrem Serverhost an.
1. Dekomprimieren Sie die Tar-Datei Image Serving und entpacken Sie sie.
1. Führen Sie [!DNL ./install-is] aus, um den Installationsassistenten zu starten, der sich im Ordner [!DNL setup] befindet.

   Das Aktualisierungs-Installationsprogramm überprüft die Integrität und Version des installierten Pakets. Bei Erfolg wird der Endbenutzer-Lizenzvertrag (&quot;EULA&quot;) angezeigt.
1. Lesen Sie die Lizenzvereinbarung und geben Sie &quot;**[!UICONTROL y]**&quot;ein, um mit der Installation fortzufahren.

   Das Installationsprogramm sichert die alten Server-Konfigurationsdateien in den Ordner [!DNL BACKUP/].

   Nach Abschluss der Installation wird die folgende Meldung angezeigt:

   `Image Server was started successfully`

Während einer Aktualisierung wird die Datei [!DNL ImageServing/conf/server.xml] auf die neuesten Einstellungen aktualisiert. Wenn Sie Werte geändert oder hinzugefügt haben, sollten Sie Ihre vorhandenen [!DNL server.xml] speichern und Ihre Änderungen nach der Aktualisierung neu implementieren.

Nach einer Aktualisierungsinstallation sollten Sie den HTTP-Antwort-Cache wärmen, bevor Sie den Server live schalten. Weitere Informationen finden Sie in der Beschreibung des Dienstprogramms [!DNL playlog] .
