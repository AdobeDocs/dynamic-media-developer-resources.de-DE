---
description: Parameter, die allen Viewern gemein sind.
seo-description: Parameter, die allen Viewern gemein sind.
seo-title: videoServerUrl
solution: Experience Manager
title: videoServerUrl
topic: Dynamic media
uuid: ef9870f9-599b-449d-b713-66abafb80311
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '69'
ht-degree: 5%

---


# videoServerUrl{#videoserverurl}

Parameter, die allen Viewern gemein sind.

>[!NOTE]
>
>Dieser Befehl gilt nicht für den Video-Bild-Viewer.

` videoServerUrl= *`videoRootPath`*`

<table id="table_9B98C97485DD4DEB8A6ECBCE8DF6B886"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> videoRootPath</span> </span> </p> </td> 
   <td colname="col2"> <p> Der Stammpfad des Videoservers. Wenn keine Domäne angegeben ist, wird stattdessen die Domäne angewendet, von der die Seite bereitgestellt wird. Es gilt die Standardauflösung für URI-Pfade. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschaften {#section-10ee45d637134e0fbcd943c62578cb78}

Optional. Nicht erforderlich für Standard-Software als Service-Nutzung.

## Standard {#section-d411e450028c460392cb8508f8ccc5d9}

`/is/content/`

## Beispiel {#section-a8afbf76f8384aa0a83ed1feeccd5b9a}

```
videoServerUrl=http://s7d1.scene7.com/is/content/
```

