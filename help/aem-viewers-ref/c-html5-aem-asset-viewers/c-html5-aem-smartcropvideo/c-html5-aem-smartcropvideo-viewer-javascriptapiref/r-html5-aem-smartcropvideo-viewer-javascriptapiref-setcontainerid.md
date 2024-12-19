---
title: setContainerId
description: JavaScript-API-Referenz für den Smart Crop Video Viewer.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop,Video
role: Developer,User
exl-id: 1c7a7494-e872-4e78-9518-ea30af46303c
source-git-commit: 67e12fae514341137e4218ea950f34da0d9997f3
workflow-type: tm+mt
source-wordcount: '89'
ht-degree: 2%

---

# setContainerId{#setcontainerid}

JavaScript-API-Referenz für den Smart Crop Video Viewer.

` setContainerId( *`containerId`*)`

Legt die ID des DOM-Containers (normalerweise ein `DIV`) fest, in den der Viewer eingefügt wird. Es ist nicht erforderlich, dass das Container-Element zum Zeitpunkt des Aufrufs dieser Methode erstellt wird. Der Container muss jedoch vorhanden sein, wenn `init()` ausgeführt wird. Dieser Parameter wird vor dem `init()` aufgerufen. Diese Methode ist optional, wenn die Viewer-Konfigurationsinformationen mit `config` JSON-Objekt an den Konstruktor übergeben werden.

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> containerId </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {string} </span> ID des Containers. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Rückgabe {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Keine.

## Beispiel {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setContainerId("s7viewer");
```
