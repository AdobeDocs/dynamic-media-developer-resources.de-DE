---
title: Installieren mehrerer Dynamic Media-Viewer auf demselben Server
description: Anweisungen zur Installation der Dynamic Media Viewer-API.
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

Anweisungen zur Installation der Dynamic Media Viewer-API.

Installieren und testen Sie Image Serving, bevor Sie die Image Serving-Viewer installieren.

Kopieren Sie die IS-Viewer-Dateien auf Ihre Festplatte und stellen Sie dann die Datei &quot;`s7viewers.war`&quot;im Verzeichnis &quot;`../ImageServing/webapps`&quot;bereit. Anweisungen zum Bereitstellen, Starten, Anhalten und Verwalten des Image-Servers finden Sie in der Dokumentation zum Image Serving .

>[!NOTE]
>
>Für die Image Serving-Viewer gibt es keine Upgrade-Installation. Adobe empfiehlt, dass Sie den vorhandenen Ordner der Dynamic Media-Viewer (s7viewers) sichern, bevor Sie mit der Installation fortfahren.

**So installieren Sie mehrere Viewer auf demselben Server:**

1. Benennen Sie die Viewer-Datei &quot;.war&quot;in den gewünschten Kontext um und stellen Sie die Datei an dem gewünschten Speicherort bereit.
1. Legen Sie den Parameter `this.isViewerRoot` in `config.js` fest.
1. Öffnen Sie `config.js` im Stammverzeichnis des neu erstellten Viewer-Ordners.
1. Setzen Sie den Parameter `this.isViewerRoot = "/s7viewers"` auf den Kontext der Datei `s7viewers.war` . Beispiel: `"/s7viewers-4.0"`.
1. Speichern Sie die Datei und schließen Sie sie.
