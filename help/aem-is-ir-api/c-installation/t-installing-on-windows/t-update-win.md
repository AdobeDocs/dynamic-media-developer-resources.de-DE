---
title: Aktualisierung von IS 4.7.4 oder höher
description: Verwenden Sie dieses Verfahren beim Aktualisieren von Dynamic Media Image Serving.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: e0781f19-4aa8-46f7-a586-4724ff8a2e68
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '211'
ht-degree: 0%

---

# Aktualisierung von IS 4.7.4 oder höher{#updating-from-is-or-later}

Verwenden Sie dieses Verfahren beim Aktualisieren von Dynamic Media Image Serving.

Wenn Sie ein Upgrade von einer älteren Version von Image Serving durchführen, wenden Sie sich an den Support, um den korrekten Prozess durchzuführen.

>[!NOTE]
>
>Der Ordner &quot;[!DNL webapps]&quot; kann bei der Aktualisierung gelöscht werden. Sichern Sie den Ordner &quot;[!DNL webapps]&quot;vor dem Upgrade.

1. Melden Sie sich mit Administratorrechten bei Ihrem Serverhost an.
1. Extrahieren Sie den Inhalt der Zip-Datei für die Image Serving-Distribution.
1. Starten Sie den Installationsassistenten, indem Sie `setup/setup.exe` ausführen.
1. Wählen Sie **[!UICONTROL Weiter]** aus, um zur Endbenutzer-Lizenzvereinbarung (EULA) zu wechseln, lesen Sie die Lizenzvereinbarung und wählen Sie **[!UICONTROL Ja]** aus.

   Auf der nächsten Seite werden die vorherigen Konfigurationseinstellungen angezeigt.
1. Klicken Sie auf **[!UICONTROL Weiter]** , um die Aktualisierungsinstallation zu starten.

   >[!NOTE]
   >
   >Das Installationsprogramm sichert die alten Server-Konfigurationsdateien in den Ordner &quot;[!DNL BACKUP/]&quot;.

1. Wählen Sie nach Abschluss der Installation **[!UICONTROL Beenden]** aus, um den Installationsassistenten zu beenden.

   Manchmal werden Sie vom Installationsassistenten aufgefordert, das System neu zu starten.

Bei einer Aktualisierung wird die Datei [!DNL ImageServing/conf/server.xml] auf die neuesten Einstellungen aktualisiert. Wenn Sie Werte geändert oder hinzugefügt haben, sollten Sie Ihre vorhandene [!DNL server.xml] speichern und Ihre Änderungen nach dem Upgrade neu implementieren.

Nach einer Aktualisierungsinstallation sollten Sie den HTTP-Antwort-Cache wärmen, bevor Sie den Server live schalten. Weitere Informationen finden Sie in der Beschreibung des Dienstprogramms `playlog` .
