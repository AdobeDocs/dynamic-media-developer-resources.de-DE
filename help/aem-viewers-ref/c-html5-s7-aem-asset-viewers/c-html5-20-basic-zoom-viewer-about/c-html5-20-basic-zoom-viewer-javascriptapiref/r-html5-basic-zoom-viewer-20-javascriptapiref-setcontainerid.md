---
title: setContainerId
description: JavaScript-API-Referenz für einfachen Zoom-Viewer.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: dae07170-24bb-4e8c-86d6-5313db33736f
source-git-commit: 7eddc50fb9803eacdd1f513c6132380793b6f88d
workflow-type: tm+mt
source-wordcount: '87'
ht-degree: 2%

---

# setContainerId{#setcontainerid}

JavaScript-API-Referenz für einfachen Zoom-Viewer.

` setContainerId( *`containerId`*)`

Legt die ID des DOM-Containers (normalerweise ein DIV) fest, in den der Viewer eingefügt wird. Es ist nicht erforderlich, dass das Containerelement zum Zeitpunkt des Aufrufs dieser Methode erstellt wird. Der Container muss jedoch vorhanden sein, wenn `init()` ausgeführt wird. Sie muss zuvor aufgerufen werden `init()`.

Diese Methode ist optional, wenn die Konfigurationsinformationen des Viewers mit `config` JSON-Objekt zum Konstruktor.

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> containerId </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {string} </span> Kennung des Containers. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Rückgabe {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Keine.

## Beispiel {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setContainerId("s7viewer");
```
