---
title: Aktualisierung von IS 4.7.4 oder höher
description: Verwenden Sie dieses Verfahren bei der Aktualisierung von Dynamic Media Image Serving unter Linux®.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 54733fcc-c4e3-4501-8a3d-000778678bdb
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '206'
ht-degree: 0%

---

# Aktualisierung von IS 4.7.4 oder höher{#updating-from-is-or-later}

Verwenden Sie dieses Verfahren bei der Aktualisierung von Dynamic Media Image Serving unter Linux®.

Wenn Sie ein Upgrade von einer älteren Version von Image Serving durchführen, wenden Sie sich an den Support, um den korrekten Prozess durchzuführen.

Der Ordner &quot;[!DNL webapps]&quot; kann bei der Aktualisierung gelöscht werden. Sichern Sie den Ordner &quot;[!DNL webapps]&quot; vor dem Upgrade.

1. Melden Sie sich mit Root-Berechtigungen bei Ihrem Serverhost an.
1. Dekomprimieren Sie die Tar-Datei Image Serving und entpacken Sie sie.
1. Führen Sie im Ordner [!DNL setup] den Befehl [!DNL `./install-is`] aus, um den Installationsassistenten zu starten.

   Das Aktualisierungs-Installationsprogramm überprüft die Integrität und Version des installierten Pakets. Bei Erfolg wird der Endbenutzer-Lizenzvertrag (&quot;EULA&quot;) angezeigt.
1. Lesen Sie die Lizenzvereinbarung und geben Sie dann **[!UICONTROL y]** ein, um mit der Installation fortzufahren.

   Das Installationsprogramm sichert die alten Server-Konfigurationsdateien in den Ordner &quot;[!DNL BACKUP/]&quot;.

   Nach Abschluss der Installation wird die folgende Meldung angezeigt:

   `Image Server was started successfully`

Bei einer Aktualisierung wird die Datei [!DNL ImageServing/conf/server.xml] auf die neuesten Einstellungen aktualisiert. Wenn Sie Werte geändert oder hinzugefügt haben, speichern Sie die vorhandene [!DNL server.xml] und implementieren Sie Ihre Änderungen nach dem Upgrade erneut.

Nach einer Aktualisierungsinstallation sollten Sie den HTTP-Antwort-Cache wärmen, bevor Sie den Server live schalten. Weitere Informationen finden Sie in der Beschreibung des Dienstprogramms [!DNL playlog] .
