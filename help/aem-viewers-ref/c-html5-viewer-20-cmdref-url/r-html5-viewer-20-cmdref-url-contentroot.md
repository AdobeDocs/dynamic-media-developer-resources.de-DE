---
description: Parameter, die allen Viewern gemeinsam sind.
solution: Experience Manager
title: contentUrl
feature: Dynamic Media Classic,Viewers,SDK/API
role: Developer,User
exl-id: cab3c3fe-1a64-4a50-8559-57cadb31f689
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '91'
ht-degree: 4%

---

# contentUrl{#contenturl}

Parameter, die allen Viewern gemeinsam sind.

` contentUrl= *`contentUrlPath`*`

<table id="table_9B98C97485DD4DEB8A6ECBCE8DF6B886"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> contentUrlPath</span> </span> </p> </td> 
   <td colname="col2"> <p>Gibt den Basispfad für benutzerdefinierte CSS-Dateien, geschlossene Untertitelinhalte oder Navigationsinhalte an. </p> <p>Wenn der Pfad keinen führenden <span class="filepath"> /</span>-Pfad aufweist, ist er relativ zum Speicherort der HTML-Seite des Viewers. Wenn der Pfad einen vorangestellten <span class="filepath"> /</span>-Pfad aufweist, gibt er einen absoluten Pfad auf demselben Server an. </p> <p> Das Laden der Standard-CSS-Datei ist davon nicht betroffen, wenn Sie keinen Stilbefehl angeben. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschaften {#section-10ee45d637134e0fbcd943c62578cb78}

Optional.

## Standard {#section-d411e450028c460392cb8508f8ccc5d9}

`/is/content/`

## Beispiele {#section-a8afbf76f8384aa0a83ed1feeccd5b9a}

```
contentUrl=/skins/
```

```
contentUrl=http://aodmarketingna.assetsadobe.com/
```

```
contentUrl=https://demos-pub.assetsadobe.com/
```
