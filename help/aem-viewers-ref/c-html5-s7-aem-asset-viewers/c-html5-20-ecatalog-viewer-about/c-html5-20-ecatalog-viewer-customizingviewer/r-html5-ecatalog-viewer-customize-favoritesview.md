---
title: Favoritenansicht
description: Die Favoritenansicht besteht aus einer Spalte mit Miniaturbildern.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: 10536242-1015-49ff-ae27-59671f30d886
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '291'
ht-degree: 0%

---

# Favoritenansicht{#favorites-view}

Die Favoritenansicht besteht aus einer Spalte mit Miniaturbildern.

<!--<a id="section_B6EFCCADB5A5495DAE6BBE42F7F405CB"></a>-->

Das Erscheinungsbild des Favoriten-Ansichtscontainers wird mit der folgenden CSS-Klassenauswahl gesteuert:

```
.s7ecatalogviewer .s7favoritesview
```

Die Position und Höhe der Favoriten-Ansicht werden von der Ansicht verwaltet. In CSS ist es nur möglich, die Breite zu definieren.

**CSS-Eigenschaften der Favoritenansicht**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p> Hintergrundfarbe der Favoriten-Ansicht. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Breite der Ansicht. </p> </td> 
  </tr> 
 </tbody> 
</table>

Beispiel - So richten Sie eine Favoritenansicht ein, die 100 Pixel breit und einen halbtransparenten grauen Hintergrund aufweist:

```
.s7ecatalogviewer .s7favoritesview { 
 width: 100px; 
 background-color: rgba(221, 221, 221, 0.5); 
}
```

Der Abstand zwischen Favoriten-Miniaturansichten wird mit der folgenden CSS-Klassenauswahl gesteuert:

```
.s7ecatalogviewer .s7favoritesview .s7thumbcell
```

**CSS-Eigenschaften der Favoriten-Miniaturansichten**

<table id="table_EED8CE63D805458196DE0E87C7E9945F"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margin </span> </p> </td> 
   <td colname="col2"> <p> Die Größe des vertikalen Rands um jede Miniaturansicht. Der tatsächliche Abstand der Miniaturansichten entspricht der Summe des oberen und unteren Rands, der für <span class="codeph"> .s7thumbcell </span> festgelegt ist. </p> </td> 
  </tr> 
 </tbody> 
</table>

Beispiel - So richten Sie einen Abstand von zehn Pixeln ein:

```
.s7ecatalogviewer .s7favoritesview .s7thumbcell { 
 margin: 5px; 
}
```

Das Erscheinungsbild der einzelnen Miniaturansichten wird mit der folgenden CSS-Klassenauswahl gesteuert:

```
.s7ecatalogviewer .s7favoritesview .s7thumb
```

**CSS-Eigenschaften der Favoriten-Miniaturansichten**

<table id="table_6F5B1438CAFA49E9B33400C6970ABDA1"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Breite der Miniaturansicht. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Höhe </span> </p> </td> 
   <td colname="col2"> <p>Höhe der Miniaturansicht. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> border </span> </p> </td> 
   <td colname="col2"> <p>Rand der Miniaturansicht. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Miniaturansichten unterstützen die &quot;`state`&quot;-Attributauswahl, mit der verschiedene Skins auf verschiedene Miniaturansichten angewendet werden können. Insbesondere entspricht `state="selected"` der Miniaturansicht, die der Benutzer kürzlich ausgewählt hat. Das Attribut `state="default"` entspricht dem Rest der Miniaturansichten. Und das Attribut `state="over"` wird beim Bewegen der Maus verwendet.

Beispiel: Um Miniaturansichten mit einer Größe von 75 x 75 Pixel einzurichten, haben Sie einen hellgrauen Standardrahmen und einen dunkelgrauen ausgewählten Rahmen:

```
.s7ecatalogviewer .s7favoritesview .s7thumb { 
 width: 75px; 
 height: 75px;  
} 
.s7ecatalogviewer .s7favoritesview .s7thumb[state="default"] { 
 border: 1px solid #dddddd; 
} 
.s7ecatalogviewer .s7favoritesview .s7thumb[state="selected"] { 
 border: 1px solid #666666; 
}
```

Das Erscheinungsbild der Miniaturansichtsbeschriftung wird mit der folgenden CSS-Klassenauswahl gesteuert:

```
.s7ecatalogviewer .s7favoritesview .s7label
```

**CSS-Eigenschaften der Favoritenbeschriftung**

<table id="table_B41339A16ACB46CB87D3EB1FD05FA2CD"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Schriftfamilie </span> </p> </td> 
   <td colname="col2"> <p>Schriftname. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size </span> </p> </td> 
   <td colname="col2"> <p>Schriftgröße. </p> </td> 
  </tr> 
 </tbody> 
</table>

Beispiel - So richten Sie Beschriftungen mit einer Helvetica®-Schrift von 14 Pixel ein:

```
.s7ecatalogviewer .s7favoritesview .s7label { 
 font-family: Helvetica,sans-serif; 
 font-size: 14px; 
}
```
