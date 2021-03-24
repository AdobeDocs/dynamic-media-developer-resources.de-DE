---
description: URL-Befehl für Video360-Viewer.
solution: Experience Manager
title: videoServerUrl
feature: Dynamic Media Classic,Viewer,SDK/API,360 VR Video
role: Entwickler, Geschäftspraktiker
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '62'
ht-degree: 6%

---


# videoServerUrl{#videoserverurl}

URL-Befehl für Video360-Viewer.

` videoServerUrl= *`videoRootPath`*`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> videoRootPath</span> </span> </p> </td> 
   <td colname="col2"> <p> Der Stammpfad des Videoservers. Wenn keine Domäne angegeben ist, wird stattdessen die Domäne angewendet, von der die Seite bereitgestellt wird. Es gilt die Standardauflösung für URI-Pfade. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschaften {#section-f42369774e2740dcb399626a0e4e930e}

Optional. Für die standardmäßige SaaS-Nutzung nicht erforderlich.

## Standard {#section-d016470e92a74f98a18c4ab3489410a5}

`/is/content/`

## Beispiel {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

```
videoServerUrl=http://s7d9.scene7.com/is/content/
```

