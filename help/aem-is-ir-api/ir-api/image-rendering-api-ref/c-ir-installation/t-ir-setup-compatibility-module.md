---
title: Einrichten und Konfigurieren des Kompatibilitätsmoduls IR 3.x
description: Richten Sie das IR 3.x-Kompatibilitätsmodul ein und konfigurieren Sie es.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 44fbc6be-7681-402a-936a-0511e138365c
source-git-commit: 8454991568374ecd1c4babdd3210250ea7988c4c
workflow-type: tm+mt
source-wordcount: '92'
ht-degree: 0%

---

# Einrichten und Konfigurieren des Kompatibilitätsmoduls IR 3.x{#setup-and-configure-ir-x-compatibility-module}

1. Stopp `<cmdname class="+ topic/keyword sw-d/cmdname ">  PlatformServer</cmdname>`.
1. Wechseln Sie zum Verzeichnis &quot;ImageServer webapps&quot;.
1. Kopieren Sie den Inhalt des Verzeichnisses [!DNL ir] in das Verzeichnis [!DNL `ROOT`] .
1. Öffnen Sie [!DNL `ROOT/WEB-INF/web.xml`] in einem Texteditor.
1. Suchen Sie nach der Zeile `<!-- Uncomment this to enable the Image Rendering 3.x protocol emulation. Only do this when you unpack ir.war in the ROOT webapp. -->`
1. Heben Sie den Kommentar für die Tags `<servlet>` und `<servlet-mapping>` auf.
1. Starten Sie `<cmdname class="+ topic/keyword sw-d/cmdname ">  PlatformServer</cmdname>` neu.

**Linux®-Beispiel**

`cd /usr/local/scene7/ImageServing/webapps/ROOT`

`cp -r ../ir/* ./`

`cd WEB-INF`

Bearbeiten Sie dann [!DNL `web.xml`] mit Ihrem Lieblings-Editor, um die Auskommentierung der `<servlet>` - und `<servlet-mapping>` -Tags aufzuheben.

**Windows-Beispiel**

Öffnen Sie den Explorer und gehen Sie zu &quot;`C:\Program Files\Scene7\ImageServing\webapps\ir`&quot;.

Wählen Sie alle Dateien und Ordner aus und kopieren Sie sie in `C:\Program Files\Scene7\ImageServing\webapps\ROOT`.

Bearbeiten Sie dann die Datei &quot;`c:\Program Files\Scene7\ImageServing\webapps\ROOT\WEB-INF\web.xml`&quot;, und heben Sie die Kommentierung der `<servlet>` - und `<servlet-mapping>` -Tags auf.
