---
description: Parameter, die allen Viewern gemein sind.
seo-description: Parameter, die allen Viewern gemein sind.
seo-title: contentUrl
solution: Experience Manager
title: contentUrl
topic: Dynamic media
uuid: 85b00c4e-b382-4970-b780-e4ef59108cb7
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '91'
ht-degree: 4%

---


# contentUrl{#contenturl}

Parameter, die allen Viewern gemein sind.

` contentUrl= *`contentUrlPath`*`

<table id="table_9B98C97485DD4DEB8A6ECBCE8DF6B886"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> contentUrlPath</span> </span> </p> </td> 
   <td colname="col2"> <p>Gibt den Basispfad für benutzerdefinierte CSS-Dateien, Untertitelinhalte oder Navigationsinhalte an. </p> <p>Wenn der Pfad keinen führenden <span class="filepath"> /</span>-Pfad hat, ist er relativ zum Speicherort der Viewer-HTML-Seite. Wenn der Pfad einen führenden <span class="filepath"> /</span>-Pfad hat, gibt er einen absoluten Pfad auf demselben Server an. </p> <p> Das Laden der Standard-CSS-Datei wird nicht beeinträchtigt, wenn Sie keinen Stilbefehl angeben. </p> </td> 
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

