---
title: InitialFrame
description: InitialFrame
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: 28b6b981-94f6-4136-b322-992e18d154db
source-git-commit: a919130f0940d81a221b79563b6b3e41533ba788
workflow-type: tm+mt
source-wordcount: '58'
ht-degree: 5%

---

# InitialFrame{#initialframe}

` initialFrame= *`frame`*`

<table id="table_06B5F795889E402FB6BCEA4D882E1422"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> frame</span></span> </p> </td> 
   <td colname="col2"> <p> Gibt einen nullbasierten Spread-Index an, der beim Laden des Viewers angezeigt werden soll. Der Index entspricht dem Index des Streams im Querformat. Wenn der Viewer in ein Hochformat gedreht wird, zeigt der Viewer die am weitesten links liegende Seite des Streams an, auf die durch <span class="codeph"> frameIdx</span> verwiesen wird. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschaften {#section-fc7c012c91d1419b8a5bb60d28e17327}

Optional.

## Standard {#section-bbc6ebad3af54fd79837515c270e6ddf}

`0`

## Beispiel {#section-cbc6684eb22e4d0883edc4b3d5742336}

Wenn in der Viewer-URL angegeben.

```
initialFrame=2
```
