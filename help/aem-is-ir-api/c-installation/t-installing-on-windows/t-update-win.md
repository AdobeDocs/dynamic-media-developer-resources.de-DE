---
description: Verwenden Sie dieses Verfahren beim Aktualisieren von Dynamic Media Image Serving.
solution: Experience Manager
title: Aktualisierung von IS 4.7.4 oder höher
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: e0781f19-4aa8-46f7-a586-4724ff8a2e68
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '216'
ht-degree: 0%

---

# Aktualisierung von IS 4.7.4 oder höher{#updating-from-is-or-later}

Verwenden Sie dieses Verfahren beim Aktualisieren von Dynamic Media Image Serving.

Wenn Sie ein Upgrade von einer älteren Version von Image Serving durchführen, wenden Sie sich an den Support, um den korrekten Prozess durchzuführen.

>[!NOTE]
>
>Der Ordner [!DNL webapps] kann bei der Aktualisierung gelöscht werden. Sichern Sie den Ordner [!DNL webapps] vor der Aktualisierung.

1. Melden Sie sich mit Administratorrechten bei Ihrem Serverhost an.
1. Extrahieren Sie den Inhalt der Zip-Datei für die Image Serving-Distribution.
1. Führen Sie setup/setup.exe aus, um den Installationsassistenten zu starten.
1. Klicken Sie auf **[!UICONTROL Weiter]**, um zur Endbenutzer-Lizenzvereinbarung (EULA) zu wechseln, lesen Sie die Lizenzvereinbarung und klicken Sie auf **[!UICONTROL Ja]**.

   Auf der nächsten Seite werden die vorherigen Konfigurationseinstellungen angezeigt.
1. Klicken Sie auf **[!UICONTROL Weiter]**, um die Aktualisierungsinstallation zu starten.

   >[!NOTE]
   >
   >Das Installationsprogramm sichert die alten Server-Konfigurationsdateien in den Ordner [!DNL BACKUP/].

1. Nachdem die Installation abgeschlossen ist, klicken Sie auf &quot;Fertigstellen&quot;, um den Installationsassistenten zu beenden.

   In einigen Fällen kann der Installationsassistent den Neustart des Systems anfordern.

Während einer Aktualisierung wird die Datei [!DNL ImageServing/conf/server.xml] auf die neuesten Einstellungen aktualisiert. Wenn Sie Werte geändert oder hinzugefügt haben, sollten Sie Ihre vorhandenen [!DNL server.xml] speichern und Ihre Änderungen nach der Aktualisierung neu implementieren.

Nach einer Aktualisierungsinstallation sollten Sie den HTTP-Antwort-Cache wärmen, bevor Sie den Server live schalten. Weitere Informationen finden Sie in der Beschreibung des Dienstprogramms `playlog` .
