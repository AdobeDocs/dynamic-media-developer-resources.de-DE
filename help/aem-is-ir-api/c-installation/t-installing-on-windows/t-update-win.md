---
title: Aktualisierung von IS 4.7.4 oder höher
description: Gehen Sie beim Upgrade von Dynamic Media Image Serving wie folgt vor.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: e0781f19-4aa8-46f7-a586-4724ff8a2e68
TQID: 'https://experienceleague.adobe.com/ibeLWHpA-Lk2wiXkSgGL02uMEYH4t8l0xjjXuN9ooiE'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 209
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
