---
title: serverUrl
description: Parameter, die allen Viewern gemeinsam sind.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API
role: Developer,User
exl-id: c9da3d5b-492d-4e1f-8fdc-3255b2b40fc6
source-git-commit: c99aac44711852d8ac661878e11ce0b19d3dbf60
workflow-type: tm+mt
source-wordcount: '100'
ht-degree: 4%

---

# serverUrl{#serverurl}

Parameter, die allen Viewern gemeinsam sind.

` serverUrl= *`isRootPath`*`

<table id="table_9B98C97485DD4DEB8A6ECBCE8DF6B886"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> isRootPath</span> </span> </p> </td> 
   <td colname="col2"> <p>Relativer oder absoluter Image Serving-Stammpfad. </p> <p> Gibt einen relativen oder absoluten Pfad zum Image Serving an, von dem aus der Viewer Bilder abruft. Wenn der Pfad keinen führenden <span class="filepath"> /</span>-Pfad aufweist, ist er relativ zum Speicherort der HTML-Seite des Viewers. Wenn der Pfad einen vorangestellten <span class="filepath"> /</span>-Pfad aufweist, gibt er einen absoluten Pfad auf demselben Server an. </p> <p> Verwenden Sie nur einen absoluten Pfad, wenn das Modul E-Mail-Freigabe im Viewer aktiviert ist. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschaften {#section-10ee45d637134e0fbcd943c62578cb78}

Optional. Nicht erforderlich für die standardmäßige Nutzung von SaaS (Software as a Service).

## Standard {#section-d411e450028c460392cb8508f8ccc5d9}

`/is/image/`

## Beispiele {#section-a8afbf76f8384aa0a83ed1feeccd5b9a}

```
serverUrl=http://s7d9.scene7.com/is/image/
```

```
serverUrl=http://aodmarketingna.assetsadobe.com/is/image
```

```
serverUrl=https://adobedemo62-h.assetsadobe.com/is/image
```
