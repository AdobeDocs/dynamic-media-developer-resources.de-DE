---
description: JavaScript-API-Referenz für Karussell-Viewer.
seo-description: JavaScript-API-Referenz für Karussell-Viewer.
seo-title: setContainerId
solution: Experience Manager
title: setContainerId
topic: Dynamic media
uuid: 3e26c121-7493-49b5-af25-ebd76477a415
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# setContainerId{#setcontainerid}

JavaScript-API-Referenz für Karussell-Viewer.

` setContainerId( *`containerId`*)`

Legt die ID des DOM-Containers (normalerweise ein `DIV`) fest, in den der Viewer eingefügt wird. Es ist nicht erforderlich, dass das Container-Element zum Zeitpunkt des Aufrufs dieser Methode erstellt wird. Der Container muss jedoch vorhanden sein, wenn er ausgeführt `init()` wird. Es muss vorher aufgerufen werden `init()`.

Diese Methode ist optional, wenn die Viewer-Konfigurationsinformationen mit dem `config` JSON-Objekt an den Konstruktor übergeben werden.

## Parameter {#section-fa807db629ce43bab286b1e1dc96c492}

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> containerId </span></span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {string} </span> ID des Containers. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Returns {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Keine.

## Beispiel {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setContainerId("s7viewer");
```

