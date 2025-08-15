---
title: Aktualisierung von IS 4.7.4 oder höher
description: Gehen Sie wie folgt vor, wenn Sie Dynamic Media Image Serving unter Linux® aktualisieren.
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

Gehen Sie wie folgt vor, wenn Sie Dynamic Media Image Serving unter Linux® aktualisieren.

Wenn Sie von einer älteren Version von Image Serving aktualisieren, wenden Sie sich für den richtigen Prozess an den Support.

Der [!DNL webapps] kann beim Upgrade gelöscht werden. Sichern Sie den [!DNL webapps] vor dem Upgrade.

1. Melden Sie sich bei Ihrem Serverhost mit Root-Berechtigungen an.
1. Dekomprimieren und entpacken Sie die TAR-Datei der Image-Serving-Verteilung.
1. Führen Sie im [!DNL setup]-Ordner [!DNL `./install-is`] aus, um den Installationsassistenten zu starten.

   Das Update-Installationsprogramm überprüft die Integrität und Version des installierten Pakets. Bei erfolgreicher Ausführung wird der Endbenutzer-Lizenzvertrag („EULA„) angezeigt.
1. Lesen Sie die Lizenzvereinbarung und geben Sie **[!UICONTROL y]** ein, um mit der Installation fortzufahren.

   Das Installationsprogramm sichert die alten Server-Konfigurationsdateien im Ordner [!DNL BACKUP/] .

   Wenn die Installation abgeschlossen ist, wird die folgende Meldung angezeigt:

   `Image Server was started successfully`

Während eines Updates wird die [!DNL ImageServing/conf/server.xml] auf die neuesten Einstellungen aktualisiert. Wenn Sie Werte geändert oder hinzugefügt haben, speichern Sie die vorhandenen [!DNL server.xml] und implementieren Sie die Änderungen nach dem Upgrade erneut.

Nach einer Update-Installation sollten Sie den HTTP-Antwort-Cache aufwärmen, bevor Sie den Server live schalten. Weitere Informationen finden Sie in der Beschreibung des [!DNL playlog].
