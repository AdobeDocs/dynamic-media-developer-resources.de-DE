---
title: setContainerId
description: JavaScript-API-Referenz für Inline-Zoom-Viewer.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Inline Zoom
role: Developer,User
exl-id: ab3359f0-0c58-4984-815a-e0246728100e
source-git-commit: 50dddf148345d2ca5243d5d7108fefa56d23dad6
workflow-type: tm+mt
source-wordcount: '86'
ht-degree: 2%

---

# setContainerId{#setcontainerid}

JavaScript-API-Referenz für Inline-Zoom-Viewer.

` setContainerId( *`containerId`*)`

Legt die Kennung des DOM-Containers fest (normalerweise ist ein `DIV`), in die der Viewer eingefügt wird. Es ist nicht erforderlich, dass das Containerelement zum Zeitpunkt des Aufrufs dieser Methode erstellt wird. Der Container muss jedoch vorhanden sein, wenn `init()` ausgeführt wird. Sie muss zuvor aufgerufen werden `init()`. Diese Methode ist optional, wenn Informationen zur Viewer-Konfiguration mit `config` JSON-Objekt an den Konstruktor.

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
