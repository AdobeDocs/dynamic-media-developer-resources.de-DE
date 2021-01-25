---
description: Enthält Plattformservereinstellungen.
seo-description: Enthält Plattformservereinstellungen.
seo-title: server.xml
solution: Experience Manager
title: server.xml
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 6f8b7047-6de6-4a56-96b7-58c481150e32
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '89'
ht-degree: 0%

---


# server.xml{#server-xml}

Enthält Plattformservereinstellungen.

Beim Ändern dieser XML-Datei muss darauf geachtet werden, dass die gültige XML-Syntax beibehalten wird, da andernfalls der Plattformserver möglicherweise nicht Beginn werden kann.

Damit Änderungen wirksam werden, muss der Plattformserver nach der Bearbeitung dieser Datei neu gestartet werden.

Das folgende Diagramm zeigt, welche Einstellungen in dieser Datei geändert werden können. Eine Beschreibung dieser Einstellungen finden Sie in den entsprechenden Abschnitten weiter oben in diesem Dokument. Beachten Sie, dass dieses Diagramm keine vollständige Darstellung von [!DNL server.xml] ist.

```
<Server>
   <Service name="Catalina">
     <Connector port="TC::PsPort" />
     <Connector port="TC::SslPort"
        keystoreFile="TC::keystoreFile"
        keystoreType="TC::keystoreType"
        keystorePass="TC::keystorePass" 
        scheme="https" secure="true" URIEncoding="UTF-8" />
     <Engine>
        <Valve directory="TC::directory" 
           maxDays="TC::maxDays" 
           prefix="TC::prefix" 
           pattern="TC::pattern" 
     </Engine>  
   </Service>
</Server>
```

