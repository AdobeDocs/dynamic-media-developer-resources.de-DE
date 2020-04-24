---
description: Sie müssen das IR 3.x-Kompatibilitätsmodul einrichten und konfigurieren.
seo-description: Sie müssen das IR 3.x-Kompatibilitätsmodul einrichten und konfigurieren.
seo-title: IR 3.x-Kompatibilitätsmodul einrichten und konfigurieren
solution: Experience Manager
title: IR 3.x-Kompatibilitätsmodul einrichten und konfigurieren
topic: Scene7 Image Serving - Image Rendering API
uuid: 609a6ac9-1a4e-4cca-ab08-aa0f957b0e31
translation-type: tm+mt
source-git-commit: a47f2b4ef8ebef0c8218dafa4678443aa61241f5

---


# IR 3.x-Kompatibilitätsmodul einrichten und konfigurieren{#setup-and-configure-ir-x-compatibility-module}

Sie müssen das IR 3.x-Kompatibilitätsmodul einrichten und konfigurieren.

1. Stopp `<cmdname class="+ topic/keyword sw-d/cmdname ">  PlatformServer</cmdname>`.
1. Wechseln Sie zum Ordner für ImageServer-Webapps.
1. Kopieren Sie den Inhalt des [!DNL ir] Ordners in den [!DNL ROOT] Ordner.
1. Öffnen Sie [!DNL ROOT/WEB-INF/web.xml] in einem Texteditor.
1. Nach der Zeile suchen `<!-- Uncomment this to enable the Image Rendering 3.x protocol emulation. Only do this when you unpack ir.war in the ROOT webapp. -->`
1. Heben Sie die Auskommentierung der Tags `<servlet>` und `<servlet-mapping>` auf.
1. Restart `<cmdname class="+ topic/keyword sw-d/cmdname ">  PlatformServer</cmdname>`.

**Linux-Beispiel**

`cd /usr/local/scene7/ImageServing/webapps/ROOT`

`cp -r ../ir/* ./`

`cd WEB-INF`

Bearbeiten Sie dann [!DNL web.xml]mit Ihrem Lieblings-Editor, um die Kommentare `<servlet>` und `<servlet-mapping>` -Tags aufzuheben.

**Windows-Beispiel**

Öffnen Sie den Explorer und gehen Sie zu `C:\Program Files\Scene7\ImageServing\webapps\ir`.

Wählen Sie alle Dateien und Ordner aus und kopieren Sie sie `C:\Program Files\Scene7\ImageServing\webapps\ROOT`.

Bearbeiten Sie dann die Datei `c:\Program Files\Scene7\ImageServing\webapps\ROOT\WEB-INF\web.xml`und heben Sie die Kommentierung `<servlet>` und `<servlet-mapping>` -Tags auf.
