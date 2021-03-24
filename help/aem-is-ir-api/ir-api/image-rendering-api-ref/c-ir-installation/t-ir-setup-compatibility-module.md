---
description: Sie müssen das IR 3.x-Kompatibilitätsmodul einrichten und konfigurieren.
solution: Experience Manager
title: IR 3.x-Kompatibilitätsmodul einrichten und konfigurieren
feature: Dynamic Media Classic, SDK/API
role: Entwickler, Geschäftspraktiker
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '111'
ht-degree: 0%

---


# Einrichten und Konfigurieren des IR 3.x-Kompatibilitätsmoduls{#setup-and-configure-ir-x-compatibility-module}

Sie müssen das IR 3.x-Kompatibilitätsmodul einrichten und konfigurieren.

1. Stopp `<cmdname class="+ topic/keyword sw-d/cmdname ">  PlatformServer</cmdname>`.
1. Wechseln Sie zum Ordner für ImageServer-Webapps.
1. Kopieren Sie den Inhalt des Ordners [!DNL ir] in den Ordner [!DNL ROOT].
1. Öffnen Sie [!DNL ROOT/WEB-INF/web.xml] in einem Texteditor.
1. Suchen Sie nach der Zeile `<!-- Uncomment this to enable the Image Rendering 3.x protocol emulation. Only do this when you unpack ir.war in the ROOT webapp. -->`
1. Heben Sie die Auskommentierung der Tags `<servlet>` und `<servlet-mapping>` auf.
1. Starten Sie `<cmdname class="+ topic/keyword sw-d/cmdname ">  PlatformServer</cmdname>` neu.

**Linux-Beispiel**

`cd /usr/local/scene7/ImageServing/webapps/ROOT`

`cp -r ../ir/* ./`

`cd WEB-INF`

Bearbeiten Sie dann [!DNL web.xml]mit Ihrem Lieblings-Editor, um die Auskommentierung der Tags `<servlet>` und `<servlet-mapping>` aufzuheben.

**Windows-Beispiel**

Öffnen Sie den Explorer und gehen Sie zu `C:\Program Files\Scene7\ImageServing\webapps\ir`.

Wählen Sie alle Dateien und Ordner aus und kopieren Sie sie in `C:\Program Files\Scene7\ImageServing\webapps\ROOT`.

Bearbeiten Sie dann die Datei `c:\Program Files\Scene7\ImageServing\webapps\ROOT\WEB-INF\web.xml` und heben Sie die Kommentierung der Tags `<servlet>` und `<servlet-mapping>` auf.
