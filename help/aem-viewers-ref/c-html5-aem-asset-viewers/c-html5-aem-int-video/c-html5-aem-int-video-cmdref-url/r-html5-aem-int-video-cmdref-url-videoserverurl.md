---
title: videoServerUrl
description: URL-Befehl für Video-Viewer.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: 2bcbe117-14a3-42c8-bdd3-790b32bb757c
source-git-commit: 6aaf4eccf51a05d200c6cc780e342be646d104d8
workflow-type: tm+mt
source-wordcount: '44'
ht-degree: 9%

---

# videoServerUrl{#videoserverurl}

URL-Befehl für Video-Viewer.

` videoServerUrl= *`videoRootPath`*`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> videoRootPath</span> </span> </p> </td> 
   <td colname="col2"> <p> Der Stammpfad des Videoservers. Wenn keine Domäne angegeben ist, wird stattdessen die Domäne angewendet, von der die Seite bereitgestellt wird. Es gilt die standardmäßige URI-Pfadauflösung. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschaften {#section-f42369774e2740dcb399626a0e4e930e}

Optional.

## Standard {#section-d016470e92a74f98a18c4ab3489410a5}

`/is/content/`

## Beispiel {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

```
videoServerUrl=https://gateway-na.assetsadobe.com/DMGateway/public/aodmarketingna
```
