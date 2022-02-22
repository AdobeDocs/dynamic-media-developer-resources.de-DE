---
title: Aktualisierung von IS 4.7.4 oder höher
description: Verwenden Sie dieses Verfahren beim Aktualisieren von Dynamic Media Image Serving.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: e0781f19-4aa8-46f7-a586-4724ff8a2e68
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '207'
ht-degree: 0%

---

# Aktualisierung von IS 4.7.4 oder höher{#updating-from-is-or-later}

Verwenden Sie dieses Verfahren beim Aktualisieren von Dynamic Media Image Serving.

Wenn Sie ein Upgrade von einer älteren Version von Image Serving durchführen, wenden Sie sich an den Support, um den korrekten Prozess durchzuführen.

>[!NOTE]
>
>Die [!DNL webapps] -Ordner bei der Aktualisierung gelöscht werden. Sichern Sie die [!DNL webapps] Ordner vor der Aktualisierung.

1. Melden Sie sich mit Administratorrechten bei Ihrem Serverhost an.
1. Extrahieren Sie den Inhalt der Zip-Datei für die Image Serving-Distribution.
1. Starten Sie den Installationsassistenten, indem Sie `setup/setup.exe`.
1. Auswählen **[!UICONTROL Nächste]** , um zur Endbenutzer-Lizenzvereinbarung (EULA) zu wechseln, lesen Sie die Lizenzvereinbarung und wählen Sie **[!UICONTROL Ja]**.

   Auf der nächsten Seite werden die vorherigen Konfigurationseinstellungen angezeigt.
1. Klicken **[!UICONTROL Nächste]** um die Installation der Aktualisierung zu starten.

   >[!NOTE]
   >
   >Das Installationsprogramm sichert die alten Server-Konfigurationsdateien in der [!DNL BACKUP/] Ordner.

1. Nachdem die Installation abgeschlossen ist, wählen Sie **[!UICONTROL Beenden]** um den Installationsassistenten zu beenden.

   Manchmal werden Sie vom Installationsassistenten aufgefordert, das System neu zu starten.

Während einer Aktualisierung wird die [!DNL ImageServing/conf/server.xml] -Datei auf die neuesten Einstellungen aktualisiert. Wenn Sie Werte geändert oder hinzugefügt haben, sollten Sie Ihre vorhandenen speichern [!DNL server.xml] und implementieren Sie Ihre Änderungen nach der Aktualisierung erneut.

Nach einer Aktualisierungsinstallation sollten Sie den HTTP-Antwort-Cache wärmen, bevor Sie den Server live schalten. Siehe Beschreibung der `playlog` -Dienstprogramm für Details.
