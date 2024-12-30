---
title: IR 3.x-Kompatibilitätsmodul einrichten und konfigurieren
description: Einrichten und Konfigurieren des IR 3.x-Kompatibilitätsmoduls.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 44fbc6be-7681-402a-936a-0511e138365c
source-git-commit: 8454991568374ecd1c4babdd3210250ea7988c4c
workflow-type: tm+mt
source-wordcount: '92'
ht-degree: 0%

---

# IR 3.x-Kompatibilitätsmodul einrichten und konfigurieren{#setup-and-configure-ir-x-compatibility-module}

1. `<cmdname class="+ topic/keyword sw-d/cmdname ">  PlatformServer</cmdname>` anhalten.
1. Wechseln Sie in das Verzeichnis ImageServer WebApps .
1. Kopieren Sie den Inhalt des [!DNL ir] in das [!DNL `ROOT`].
1. Öffnen Sie [!DNL `ROOT/WEB-INF/web.xml`] in einem Texteditor.
1. Nach der `<!-- Uncomment this to enable the Image Rendering 3.x protocol emulation. Only do this when you unpack ir.war in the ROOT webapp. -->` suchen
1. Entfernen Sie den Kommentar für die Tags `<servlet>` und `<servlet-mapping>` .
1. `<cmdname class="+ topic/keyword sw-d/cmdname ">  PlatformServer</cmdname>` neu starten.

**Linux®-Beispiel**

`cd /usr/local/scene7/ImageServing/webapps/ROOT`

`cp -r ../ir/* ./`

`cd WEB-INF`

Bearbeiten Sie dann [!DNL `web.xml`] mit Ihrem bevorzugten Editor, um die Auskommentierung der `<servlet>`- und `<servlet-mapping>`-Tags aufzuheben.

**Windows-Beispiel**

Öffnen Sie den Explorer und navigieren Sie zu `C:\Program Files\Scene7\ImageServing\webapps\ir`.

Wählen Sie alle Dateien und Ordner aus und kopieren Sie diese in `C:\Program Files\Scene7\ImageServing\webapps\ROOT`.

Bearbeiten Sie dann die Datei `c:\Program Files\Scene7\ImageServing\webapps\ROOT\WEB-INF\web.xml`, indem Sie die `<servlet>`- und `<servlet-mapping>`-Tags aus dem Kommentar entfernen.
