---
description: Parameter, die allen Viewern gemein sind.
solution: Experience Manager
title: videoServerUrl
feature: Dynamic Media Classic,Viewer,SDK/API
role: Entwickler, Geschäftspraktiker
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '72'
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

