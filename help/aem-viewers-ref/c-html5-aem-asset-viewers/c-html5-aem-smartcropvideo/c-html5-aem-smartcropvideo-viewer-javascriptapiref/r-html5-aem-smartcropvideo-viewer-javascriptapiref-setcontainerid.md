---
title: setContainerId
description: JavaScript-API-Referenz für Smart Crop Video Viewer.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop Video
role: Developer,User
exl-id: 9f2857a4-108d-4689-9c39-cb2635405d0d
source-git-commit: b6ebc938f55117c4144ff921bed7f8742cf3a8a7
workflow-type: tm+mt
source-wordcount: '89'
ht-degree: 2%

---

# setContainerId{#setcontainerid}

JavaScript-API-Referenz für Smart Crop Video Viewer.

` setContainerId( *`containerId`*)`

Legt die Kennung des DOM-Containers fest (normalerweise ist ein `DIV`), in den der Viewer eingefügt wird. Es ist nicht erforderlich, dass das Containerelement zum Zeitpunkt des Aufrufs dieser Methode erstellt wird. Der Container muss jedoch vorhanden sein, wenn `init()` ausgeführt wird. Dieser Parameter wird vor aufgerufen. `init()`. Diese Methode ist optional, wenn die Viewer-Konfigurationsinformationen mit `config` JSON-Objekt an den Konstruktor.

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
