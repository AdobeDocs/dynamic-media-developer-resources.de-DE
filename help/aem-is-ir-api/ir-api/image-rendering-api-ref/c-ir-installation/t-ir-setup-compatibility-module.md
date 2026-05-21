---
title: IR 3.x-Kompatibilitätsmodul einrichten und konfigurieren
description: Einrichten und Konfigurieren des IR 3.x-Kompatibilitätsmoduls.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 44fbc6be-7681-402a-936a-0511e138365c
TQID: 'https://experienceleague.adobe.com/ce7CdClFrrIFb7fhZRKQ7XBpsNm4BTgwVFHPXy3BXhw'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 95
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
