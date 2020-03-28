---
description: Anweisungen zum Installieren der Scene7 Viewer-API.
seo-description: Anweisungen zum Installieren der Scene7 Viewer-API.
seo-title: Mehrere Viewer auf demselben Server installieren
solution: Experience Manager
title: Mehrere Viewer auf demselben Server installieren
topic: Dynamic media
uuid: 91ae8eb5-1d23-4fa3-a0d6-a4a0ed0eb104
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Mehrere Viewer auf demselben Server installieren{#installing-multiple-viewers-on-the-same-server}

Anweisungen zum Installieren der Scene7 Viewer-API.

Installieren und testen Sie Image Serving, bevor Sie die Image Serving-Viewer installieren.

Kopieren Sie die IS Viewer-Dateien auf Ihre Festplatte und stellen Sie die `s7viewers.war` Datei dann im `../ImageServing/webapps` Ordner bereit. Anweisungen zum Bereitstellen, Beginn, Beenden und Verwalten des Image-Servers finden Sie in der Dokumentation zum Image-Server.

>[!NOTE]
>
>Für die Image Serving-Viewer gibt es keine Installation eines Upgrades. Adobe empfiehlt, dass Sie alle vorhandenen Scene7-Viewer-Ordner sichern, bevor Sie mit der Installation fortfahren.

**So installieren Sie die Viewer auf demselben Server**

1. Benennen Sie die Viewer-Datei &quot;.war&quot;in den gewünschten Kontext um und stellen Sie die Datei an dem gewünschten Speicherort bereit.
1. Legen Sie `this.isViewerRoot` den Parameter in fest `config.js`.
1. Öffnen Sie `config.js` den Ordner im Stammordner des neu erstellten Viewers.
1. Legen Sie Parameter `this.isViewerRoot = "/s7viewers"` auf den Kontext der `s7viewers.war` Datei fest. Beispiel, `"/s7viewers-4.0"`. Datei speichern und schließen.
1. Speichern Sie die Datei und schließen Sie sie.
