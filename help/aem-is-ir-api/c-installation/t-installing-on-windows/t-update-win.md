---
description: Verwenden Sie dieses Verfahren, wenn Sie das Dynamic Media Image Serving aktualisieren.
solution: Experience Manager
title: Aktualisieren von IS 4.7.4 oder höher
feature: Dynamic Media Classic, SDK/API
role: Entwickler, Geschäftspraktiker
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '219'
ht-degree: 0%

---


# Aktualisieren von IS 4.7.4 oder höher{#updating-from-is-or-later}

Verwenden Sie dieses Verfahren, wenn Sie das Dynamic Media Image Serving aktualisieren.

Wenn Sie ein Upgrade von einer älteren Version von Image Serving durchführen, wenden Sie sich bitte an den Support, um den korrekten Prozess zu erhalten.

>[!NOTE]
>
>Der Ordner [!DNL webapps] kann bei der Aktualisierung gelöscht werden. Sichern Sie den Ordner [!DNL webapps] vor der Aktualisierung.

1. Melden Sie sich mit Administratorrechten beim Serverhost an.
1. Extrahieren Sie den Inhalt der ZIP-Datei für die Image Serving-Distribution.
1. Führen Sie setup/setup.exe aus, um den Installationsassistenten zu starten.
1. Klicken Sie auf **[!UICONTROL Weiter]**, um zur Endbenutzer-Lizenzvereinbarung (EULA) zu wechseln, lesen Sie die Lizenzvereinbarung und klicken Sie auf **[!UICONTROL Ja]**.

   Auf der nächsten Seite werden die vorherigen Konfigurationseinstellungen angezeigt.
1. Klicken Sie auf **[!UICONTROL Weiter]**, um die Updateinstallation Beginn.

   >[!NOTE]
   >
   >Das Installationsprogramm sichert die alten Serverkonfigurationsdateien im Ordner [!DNL BACKUP/].

1. Klicken Sie nach Abschluss der Installation auf &quot;Fertig stellen&quot;, um den Installationsassistenten zu beenden.

   In einigen Fällen kann der Installationsassistent den Neustart des Systems anfordern.

Während einer Aktualisierung wird die Datei [!DNL ImageServing/conf/server.xml] auf die neuesten Einstellungen aktualisiert. Wenn Sie Werte geändert oder hinzugefügt haben, sollten Sie Ihre vorhandenen [!DNL server.xml] speichern und Ihre Änderungen nach der Aktualisierung erneut implementieren.

Nach einer Updateinstallation sollten Sie den HTTP-Antwort-Cache erwärmen, bevor Sie den Server aktivieren. Weitere Informationen finden Sie in der Beschreibung des Dienstprogramms `playlog`.
