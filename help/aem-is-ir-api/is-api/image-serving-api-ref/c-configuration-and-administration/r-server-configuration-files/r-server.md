---
description: Enthält Plattformservereinstellungen.
solution: Experience Manager
title: server.xml
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator,User
exl-id: 72b343ba-0d4b-405a-ace3-d44c4d4c44b0
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '89'
ht-degree: 0%

---

# server.xml{#server-xml}

Enthält Plattformservereinstellungen.

Beim Ändern dieser XML-Datei muss darauf geachtet werden, dass die gültige XML-Syntax beibehalten wird. Andernfalls kann der Platform Server möglicherweise nicht gestartet werden.

Damit Änderungen wirksam werden, muss der Platform Server nach der Bearbeitung dieser Datei neu gestartet werden.

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
