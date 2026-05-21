---
title: Installieren mehrerer Dynamic Media-Viewer auf demselben Server
description: Anweisungen zur Installation der Dynamic Media Viewers-API.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API
role: Developer,User
exl-id: 7a8d7205-d3bf-4ca8-b80a-9072436a3df5
TQID: 'https://experienceleague.adobe.com/Zz0BTc333AIELPKRWFeIxhNvTyOJZH1RHLYNvZpt-ZY'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 160
ht-degree: 0%

---

# Installieren mehrerer Viewer auf demselben Server{#installing-multiple-viewers-on-the-same-server}

<!-- Updated April 06, 2021 from https://wiki.corp.adobe.com/pages/viewpage.action?spaceKey=scene7qa&title=s7Viewers%2C+S7SDK%2C+S7OnDemand+Release+Notes - Contact is Sasha -->

Anweisungen zur Installation der Dynamic Media-Viewer-API.

Installieren und testen Sie Image-Serving, bevor Sie die Image-Serving-Viewer installieren.

Kopieren Sie die IMS-Viewer-Dateien auf Ihre Festplatte und stellen Sie dann die `s7viewers.war`-Datei im `../ImageServing/webapps` bereit. In der Image-Serving-Dokumentation finden Sie Anweisungen zum Bereitstellen, Starten, Beenden und Verwalten des Image-Servers.

>[!NOTE]
>
>Es gibt keine Upgrade-Installation für die Image-Serving-Viewer. Adobe empfiehlt, ein vorhandenes Dynamic Media-Viewer-Verzeichnis (s7viewers) zu sichern, bevor Sie mit der Installation fortfahren.

**So installieren Sie mehrere Viewer auf demselben Server:**

1. Benennen Sie die Viewer-Datei .war in den gewünschten Kontext um und stellen Sie die Datei an dem gewünschten Speicherort bereit.
1. `this.isViewerRoot` Parameter in `config.js` festlegen.
1. Öffnen Sie `config.js` im Stammverzeichnis des neu erstellten Viewer-Ordners.
1. Setzen Sie Parameter `this.isViewerRoot = "/s7viewers"` auf den Kontext der `s7viewers.war`. Beispiel: `"/s7viewers-4.0"`.
1. Speichern und schließen Sie die Datei.
