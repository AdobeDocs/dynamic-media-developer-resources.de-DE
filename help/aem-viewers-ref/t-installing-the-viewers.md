---
description: Anweisungen zum Installieren der Dynamic Media Viewer-API.
seo-description: Anweisungen zum Installieren der Dynamic Media Viewer-API.
seo-title: Mehrere Viewer auf demselben Server installieren
solution: Experience Manager
title: Mehrere Viewer auf demselben Server installieren
topic: Dynamic media
uuid: 91ae8eb5-1d23-4fa3-a0d6-a4a0ed0eb104
translation-type: tm+mt
source-git-commit: a0983053795cc119eb57386c005e1f8a7c2fa3e4
workflow-type: tm+mt
source-wordcount: '177'
ht-degree: 1%

---


# Mehrere Viewer auf demselben Server installieren{#installing-multiple-viewers-on-the-same-server}

<!-- Updated June 1, 2020 from https://wiki.corp.adobe.com/pages/viewpage.action?spaceKey=scene7qa&title=s7Viewers%2C+S7SDK%2C+S7OnDemand+Release+Notes - Contact is Sasha -->

Anweisungen zum Installieren der Dynamic Media Viewer-API.

Installieren und testen Sie Image Serving, bevor Sie die Image Serving-Viewer installieren.

Kopieren Sie die IS Viewers-Dateien auf Ihre Festplatte und stellen Sie dann die `s7viewers.war`-Datei im Ordner `../ImageServing/webapps` bereit. Anweisungen zum Bereitstellen, Beginn, Beenden und Verwalten des Image-Servers finden Sie in der Dokumentation zum Image-Server.

>[!NOTE]
>
>Für die Image Serving-Viewer gibt es keine Installation eines Upgrades. Adobe empfiehlt, dass Sie alle vorhandenen Dynamic Media Viewer-Ordner sichern, bevor Sie mit der Installation fortfahren.

**So installieren Sie die Viewer auf demselben Server**

1. Benennen Sie die Viewer-Datei &quot;.war&quot;in den gewünschten Kontext um und stellen Sie die Datei an dem gewünschten Speicherort bereit.
1. Legen Sie den Parameter `this.isViewerRoot` in `config.js` fest.
1. Öffnen Sie `config.js` im Stammordner des neu erstellten Viewers.
1. Setzen Sie den Parameter `this.isViewerRoot = "/s7viewers"` auf den Kontext der `s7viewers.war`-Datei. Beispiel, `"/s7viewers-4.0"`. Datei speichern und schließen.
1. Speichern Sie die Datei und schließen Sie sie.
