---
description: Parameter, die allen Viewern gemein sind.
seo-description: Parameter, die allen Viewern gemein sind.
seo-title: serverUrl
solution: Experience Manager
title: serverUrl
uuid: a079a223-7478-4b6a-bc99-284e3366fb30
feature: Dynamic Media Classic,Viewer,SDK/API
role: Entwickler, Geschäftspraktiker
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '115'
ht-degree: 3%

---


# serverUrl{#serverurl}

Parameter, die allen Viewern gemein sind.

` serverUrl= *`isRootPath`*`

<table id="table_9B98C97485DD4DEB8A6ECBCE8DF6B886"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> isRootPath</span> </span> </p> </td> 
   <td colname="col2"> <p>Relativer oder absoluter Image Serving-Stammpfad. </p> <p> Gibt einen relativen oder absoluten Pfad zum Image-Server an, von dem aus der Viewer Bilder abruft. Wenn der Pfad keinen führenden <span class="filepath"> /</span>-Pfad hat, ist er relativ zum Speicherort der Viewer-HTML-Seite. Wenn der Pfad einen führenden <span class="filepath"> /</span>-Pfad hat, gibt er einen absoluten Pfad auf demselben Server an. </p> <p> Verwenden Sie nur einen absoluten Pfad, wenn das Modul E-Mail-Freigabe im Viewer aktiviert ist. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschaften {#section-10ee45d637134e0fbcd943c62578cb78}

Optional. Nicht erforderlich für Standard-SaaS (Software als Service).

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

