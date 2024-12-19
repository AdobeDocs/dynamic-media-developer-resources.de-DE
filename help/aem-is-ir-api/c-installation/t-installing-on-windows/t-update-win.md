---
title: Aktualisierung von IS 4.7.4 oder höher
description: Gehen Sie beim Upgrade von Dynamic Media Image Serving wie folgt vor.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: e0781f19-4aa8-46f7-a586-4724ff8a2e68
source-git-commit: 67e12fae514341137e4218ea950f34da0d9997f3
workflow-type: tm+mt
source-wordcount: '211'
ht-degree: 0%

---

# Aktualisierung von IS 4.7.4 oder höher{#updating-from-is-or-later}

Gehen Sie beim Upgrade von Dynamic Media Image Serving wie folgt vor.

Wenn Sie von einer älteren Version von Image Serving aktualisieren, wenden Sie sich für den richtigen Prozess an den Support.

>[!NOTE]
>
>Der [!DNL webapps] Ordner wird beim Upgrade möglicherweise gelöscht. Sichern Sie den [!DNL webapps] vor dem Upgrade.

1. Melden Sie sich bei Ihrem Serverhost mit Administratorrechten an.
1. Extrahieren Sie den Inhalt der ZIP-Datei der Image-Serving-Verteilung.
1. Starten Sie den Installationsassistenten, indem Sie `setup/setup.exe` ausführen.
1. Wählen Sie **[!UICONTROL Weiter]**, um zum Endbenutzer-Lizenzvertrag (EULA) zu gelangen, lesen Sie die Lizenzvereinbarung und wählen Sie **[!UICONTROL Ja]**.

   Auf der nächsten Seite werden die vorherigen Konfigurationseinstellungen angezeigt.
1. Klicken Sie **[!UICONTROL Weiter]**, um die Update-Installation zu starten.

   >[!NOTE]
   >
   >Das Installationsprogramm sichert die alten Server-Konfigurationsdateien im Ordner [!DNL BACKUP/] .

1. Klicken Sie nach Abschluss der Installation auf **[!UICONTROL Beenden]**, um den Installationsassistenten zu beenden.

   Manchmal werden Sie vom Installationsassistenten aufgefordert, das System neu zu starten.

Während eines Updates wird die [!DNL ImageServing/conf/server.xml] auf die neuesten Einstellungen aktualisiert. Wenn Sie Werte geändert oder hinzugefügt haben, sollten Sie Ihre vorhandenen [!DNL server.xml] speichern und Ihre Änderungen nach dem Upgrade erneut implementieren.

Nach einer Update-Installation sollten Sie den HTTP-Antwort-Cache aufwärmen, bevor Sie den Server live schalten. Weitere Informationen finden Sie in der Beschreibung des `playlog`.
