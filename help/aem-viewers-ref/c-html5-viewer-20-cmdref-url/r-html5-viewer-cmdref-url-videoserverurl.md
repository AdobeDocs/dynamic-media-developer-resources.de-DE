---
title: videoServerUrl
description: Für alle Viewer gemeinsamer Parameter.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API
role: Developer,User
exl-id: db0ce8c4-3754-4fef-9430-44ee8e5c5e80
source-git-commit: c99aac44711852d8ac661878e11ce0b19d3dbf60
workflow-type: tm+mt
source-wordcount: '63'
ht-degree: 3%

---

# videoServerUrl{#videoserverurl}

Für alle Viewer gemeinsamer Parameter.

>[!NOTE]
>
>Dieser Befehl gilt nicht für den Videobild-Viewer.

` videoServerUrl= *`videoRootPath`*`

<table id="table_9B98C97485DD4DEB8A6ECBCE8DF6B886"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> videoRootPath</span> </span> </p> </td> 
   <td colname="col2"> <p> Den Stammverzeichnis des Videoservers. Wenn keine Domain angegeben ist, wird stattdessen die Domain angewendet, von der die Seite bereitgestellt wird. Es gilt die standardmäßige URI-Pfadauflösung. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschaften {#section-10ee45d637134e0fbcd943c62578cb78}

Optional. Wird für die Verwendung von Standardsoftware als Service nicht benötigt.

## Standard {#section-d411e450028c460392cb8508f8ccc5d9}

`/is/content/`

## Beispiel {#section-a8afbf76f8384aa0a83ed1feeccd5b9a}

```
videoServerUrl=http://s7d1.scene7.com/is/content/
```
