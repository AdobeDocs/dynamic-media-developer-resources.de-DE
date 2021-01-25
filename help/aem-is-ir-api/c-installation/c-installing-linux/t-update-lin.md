---
description: Verwenden Sie dieses Verfahren, wenn Sie Dynamic Media Image Serving unter Linux aktualisieren.
seo-description: Verwenden Sie dieses Verfahren, wenn Sie Dynamic Media Image Serving unter Linux aktualisieren.
seo-title: Aktualisieren von IS 4.7.4 oder höher
solution: Experience Manager
title: Aktualisieren von IS 4.7.4 oder höher
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 70beb1a3-71b9-4bd0-b048-13d88446a9d3
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '223'
ht-degree: 0%

---


# Aktualisieren von IS 4.7.4 oder höher{#updating-from-is-or-later}

Verwenden Sie dieses Verfahren, wenn Sie Dynamic Media Image Serving unter Linux aktualisieren.

Wenn Sie ein Upgrade von einer älteren Version von Image Serving durchführen, wenden Sie sich bitte an den Support, um den korrekten Prozess zu erhalten.

Der Ordner [!DNL webapps] kann bei der Aktualisierung gelöscht werden. Sichern Sie den Ordner [!DNL webapps] vor der Aktualisierung.

1. Melden Sie sich mit Root-Berechtigungen beim Serverhost an.
1. Dekomprimieren Sie die Image Serving-Distribution-Tar-Datei und entfernen Sie sie.
1. Führen Sie [!DNL ./install-is] aus, um den Installationsassistenten zu starten, der sich im Ordner [!DNL setup] befindet.

   Das Updateinstallationsprogramm überprüft die Integrität und Version des installierten Pakets. Bei erfolgreichem Abschluss wird der Endbenutzer-Lizenzvertrag (&quot;EULA&quot;) angezeigt.
1. Lesen Sie die Lizenzvereinbarung und geben Sie dann &quot;**[!UICONTROL y]**&quot;ein, um mit der Installation fortzufahren.

   Das Installationsprogramm sichert die alten Serverkonfigurationsdateien im Ordner [!DNL BACKUP/].

   Nach Abschluss der Installation wird folgende Meldung angezeigt:

   `Image Server was started successfully`

Während einer Aktualisierung wird die Datei [!DNL ImageServing/conf/server.xml] auf die neuesten Einstellungen aktualisiert. Wenn Sie Werte geändert oder hinzugefügt haben, sollten Sie Ihre vorhandenen [!DNL server.xml] speichern und Ihre Änderungen nach der Aktualisierung erneut implementieren.

Nach einer Updateinstallation sollten Sie den HTTP-Antwort-Cache erwärmen, bevor Sie den Server aktivieren. Weitere Informationen finden Sie in der Beschreibung des Dienstprogramms [!DNL playlog].
