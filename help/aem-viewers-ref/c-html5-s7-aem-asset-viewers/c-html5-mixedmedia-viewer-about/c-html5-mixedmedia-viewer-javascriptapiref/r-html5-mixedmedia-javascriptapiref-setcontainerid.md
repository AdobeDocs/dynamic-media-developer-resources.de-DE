---
description: JavaScript-API-Referenz für gemischte Medien-Viewer.
seo-description: JavaScript-API-Referenz für gemischte Medien-Viewer.
seo-title: setContainerId
solution: Experience Manager
title: setContainerId
topic: Dynamic Media
uuid: 56d82392-1c6f-422a-ab5b-2e407d78ba74
translation-type: tm+mt
source-git-commit: e4695cc4e882351ec3f2c55fd8a3cfca455bd79d
workflow-type: tm+mt
source-wordcount: '95'
ht-degree: 2%

---


# setContainerId{#setcontainerid}

JavaScript-API-Referenz für gemischte Medien-Viewer.

` setContainerId( *`containerId`*)`

Legt die ID des DOM-Containers (normalerweise ein DIV) fest, in den der Viewer eingefügt wird. Es ist nicht erforderlich, dass das Container-Element zum Zeitpunkt des Aufrufs dieser Methode erstellt wird. Der Container muss jedoch vorhanden sein, wenn `init()` ausgeführt wird. Es muss vor `init()` aufgerufen werden. Diese Methode ist optional, wenn Viewer-Konfigurationsinformationen mit dem JSON-Objekt `config` an den Konstruktor übergeben werden.

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> containerId  </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {string}  </span> ID des Containers. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Gibt {#section-1d3cf85bc7cc4dfe9670e038d02b9101} zurück

Keine.

## Beispiel {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setContainerId("s7viewer");
```

