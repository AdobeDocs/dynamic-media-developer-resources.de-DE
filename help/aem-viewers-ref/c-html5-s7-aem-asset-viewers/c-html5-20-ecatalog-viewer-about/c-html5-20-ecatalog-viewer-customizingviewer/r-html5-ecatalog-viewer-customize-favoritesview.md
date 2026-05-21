---
title: Favoritenansicht
description: Die Favoritenansicht besteht aus einer Spalte mit Miniaturbildern.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: 10536242-1015-49ff-ae27-59671f30d886
TQID: 'https://experienceleague.adobe.com/jOrrq3rLoXwGWAKAcafCkv2twn-N-PE5jbEqQpZI9WQ'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: null
workflow-type: tm+mt
source-wordcount: 295
ht-degree: 0%

---

# Favoritenansicht{#favorites-view}

Die Favoritenansicht besteht aus einer Spalte mit Miniaturbildern.

<!--<a id="section_B6EFCCADB5A5495DAE6BBE42F7F405CB"></a>-->

Das Erscheinungsbild des Ansichts-Containers Favoriten wird mit dem folgenden CSS-Klassenselektor gesteuert:

```
.s7ecatalogviewer .s7favoritesview
```

Position und Höhe der Favoritenansicht werden von der Ansicht verwaltet. In CSS kann nur die Breite definiert werden.

**CSS-Eigenschaften der Favoritenansicht**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">-</span> </p> </td> 
   <td colname="col2"> <p> Hintergrundfarbe der Favoritenansicht. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Breite </span> </p> </td> 
   <td colname="col2"> <p>Breite der Ansicht. </p> </td> 
  </tr> 
 </tbody> 
</table>

Beispiel: So richten Sie eine Favoritenansicht mit einer Breite von 100 Pixel und einem halbtransparenten grauen Hintergrund ein:

```
.s7ecatalogviewer .s7favoritesview { 
 width: 100px; 
 background-color: rgba(221, 221, 221, 0.5); 
}
```

Der Abstand zwischen Favoritenminiaturen wird mit dem folgenden CSS-Klassenselektor gesteuert:

```
.s7ecatalogviewer .s7favoritesview .s7thumbcell
```

**CSS-Eigenschaften der Favoriten-Miniaturansichten**

<table id="table_EED8CE63D805458196DE0E87C7E9945F"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">-</span> </p> </td> 
   <td colname="col2"> <p> Die Größe des vertikalen Rands um jede Miniaturansicht. Der tatsächliche Abstand zwischen den Miniaturen entspricht der Summe des oberen und unteren Rands, der für <span class="codeph"> s7thumbcell-</span> festgelegt ist. </p> </td> 
  </tr> 
 </tbody> 
</table>

Beispiel - So richten Sie einen Zehn-Pixel-Abstand ein:

```
.s7ecatalogviewer .s7favoritesview .s7thumbcell { 
 margin: 5px; 
}
```

Das Erscheinungsbild einzelner Miniaturansichten wird mit dem folgenden CSS-Klassenselektor gesteuert:

```
.s7ecatalogviewer .s7favoritesview .s7thumb
```

**CSS-Eigenschaften der Favoriten-Miniaturansichten**

<table id="table_6F5B1438CAFA49E9B33400C6970ABDA1"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Breite </span> </p> </td> 
   <td colname="col2"> <p>Breite der Miniaturansicht. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Höhe </span> </p> </td> 
   <td colname="col2"> <p>Höhe der Miniatur. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">-</span> </p> </td> 
   <td colname="col2"> <p>Rahmen der Miniatur. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>„Miniaturansicht“ unterstützt die `state`-Attributauswahl, mit der verschiedene Skins auf verschiedene Miniaturansichtszustände angewendet werden können. Insbesondere entspricht `state="selected"` der Miniaturansicht, die der Benutzer kürzlich ausgewählt hat. Das Attribut `state="default"` entspricht dem Rest der Miniaturen. Außerdem wird das Attribut `state="over"` beim Bewegen der Maus verwendet.

Beispiel: Für Miniaturen mit einer Größe von 75 x 75 Pixel wird ein hellgrauer Standardrahmen und ein dunkelgrauer Rahmen ausgewählt:

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

Das Erscheinungsbild der Miniaturbildbeschriftung wird mit dem folgenden CSS-Klassenselektor gesteuert:

```
.s7ecatalogviewer .s7favoritesview .s7label
```

**CSS-Eigenschaften der Favoritenbeschriftung**

<table id="table_B41339A16ACB46CB87D3EB1FD05FA2CD"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> </span> der Schriftfamilie <span class="codeph"> </p> </td> 
   <td colname="col2"> <p>Schriftart. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">-</span> </p> </td> 
   <td colname="col2"> <p>Schriftgröße. </p> </td> 
  </tr> 
 </tbody> 
</table>

Beispiel - So richten Sie Beschriftungen mit einer Helvetica®-Schriftart mit 14 Pixeln ein:

```
.s7ecatalogviewer .s7favoritesview .s7label { 
 font-family: Helvetica,sans-serif; 
 font-size: 14px; 
}
```
