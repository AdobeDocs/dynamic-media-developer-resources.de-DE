---
description: Parameter, die allen Viewern gemein sind.
solution: Experience Manager
title: contentUrl
feature: Dynamic Media Classic,Viewer,SDK/API
role: Entwickler, Geschäftspraktiker
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '94'
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

