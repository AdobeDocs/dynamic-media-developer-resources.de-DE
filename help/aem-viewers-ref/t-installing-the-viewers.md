---
title: Mehrere Dynamic Media-Viewer auf demselben Server installieren
description: Anweisungen zum Installieren der Dynamic Media Viewer-API.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API
role: Developer,Business Practitioner
exl-id: 7a8d7205-d3bf-4ca8-b80a-9072436a3df5
translation-type: tm+mt
source-git-commit: 8207cba7e75c6bff878ef7f11f74b19bb88f1d61
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# Mehrere Viewer auf demselben Server installieren{#installing-multiple-viewers-on-the-same-server}

<!-- Updated April 06, 2021 from https://wiki.corp.adobe.com/pages/viewpage.action?spaceKey=scene7qa&title=s7Viewers%2C+S7SDK%2C+S7OnDemand+Release+Notes - Contact is Sasha -->

Anweisungen zum Installieren der Dynamic Media Viewer-API.

Installieren und testen Sie Image Serving, bevor Sie die Image Serving-Viewer installieren.

Kopieren Sie die IS Viewers-Dateien auf Ihre Festplatte und stellen Sie dann die `s7viewers.war`-Datei im Ordner `../ImageServing/webapps` bereit. Anweisungen zum Bereitstellen, Beginn, Beenden und Verwalten des Image-Servers finden Sie in der Dokumentation zum Image-Server.

>[!NOTE]
>
>Für die Image Serving-Viewer gibt es keine Installation eines Upgrades. Adobe empfiehlt, dass Sie den vorhandenen Dynamic Media Viewer-Ordner (s7viewers) sichern, bevor Sie mit der Installation fortfahren.

**So installieren Sie mehrere Viewer auf demselben Server:**

1. Benennen Sie die Viewer-Datei &quot;.war&quot;in den gewünschten Kontext um und stellen Sie die Datei an dem gewünschten Speicherort bereit.
1. Legen Sie den Parameter `this.isViewerRoot` in `config.js` fest.
1. Öffnen Sie `config.js` im Stammordner des neu erstellten Viewer-Ordners.
1. Setzen Sie den Parameter `this.isViewerRoot = "/s7viewers"` auf den Kontext der `s7viewers.war`-Datei. Beispiel, `"/s7viewers-4.0"`.
1. Speichern Sie die Datei und schließen Sie sie.
