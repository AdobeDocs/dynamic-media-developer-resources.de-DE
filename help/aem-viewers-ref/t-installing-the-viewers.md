---
title: Installieren mehrerer Dynamic Media-Viewer auf demselben Server
description: Anleitung zur Installation der Dynamic Media Viewers-API.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API
role: Developer,User
exl-id: 7a8d7205-d3bf-4ca8-b80a-9072436a3df5
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '160'
ht-degree: 0%

---

# Installieren mehrerer Viewer auf demselben Server{#installing-multiple-viewers-on-the-same-server}

<!-- Updated April 06, 2021 from https://wiki.corp.adobe.com/pages/viewpage.action?spaceKey=scene7qa&title=s7Viewers%2C+S7SDK%2C+S7OnDemand+Release+Notes - Contact is Sasha -->

Anleitung zur Installation der Dynamic Media Viewers-API.

Installieren und testen Sie Image-Serving, bevor Sie die Image-Serving-Viewer installieren.

Kopieren Sie die IMS-Viewer-Dateien auf Ihre Festplatte und stellen Sie dann die `s7viewers.war`-Datei im `../ImageServing/webapps` bereit. In der Image-Serving-Dokumentation finden Sie Anweisungen zum Bereitstellen, Starten, Beenden und Verwalten des Image-Servers.

>[!NOTE]
>
>Es gibt keine Upgrade-Installation für die Image-Serving-Viewer. Adobe empfiehlt, ein vorhandenes Dynamic Media Viewer-Verzeichnis (s7viewers) zu sichern, bevor Sie mit der Installation fortfahren.

**So installieren Sie mehrere Viewer auf demselben Server:**

1. Benennen Sie die Viewer-Datei .war in den gewünschten Kontext um und stellen Sie die Datei an dem gewünschten Speicherort bereit.
1. `this.isViewerRoot` Parameter in `config.js` festlegen.
1. Öffnen Sie `config.js` im Stammverzeichnis des neu erstellten Viewer-Ordners.
1. Setzen Sie Parameter `this.isViewerRoot = "/s7viewers"` auf den Kontext der `s7viewers.war`. Beispiel: `"/s7viewers-4.0"`.
1. Speichern und schließen Sie die Datei.
