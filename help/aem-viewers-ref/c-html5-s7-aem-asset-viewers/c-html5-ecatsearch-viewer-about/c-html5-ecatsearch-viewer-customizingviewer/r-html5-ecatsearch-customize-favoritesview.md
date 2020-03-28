---
description: Die Ansicht "Favoriten"besteht aus einer Spalte mit Miniaturbildern.
seo-description: Die Ansicht "Favoriten"besteht aus einer Spalte mit Miniaturbildern.
seo-title: Favoriten-Ansicht
solution: Experience Manager
title: Favoriten-Ansicht
topic: Dynamic media
uuid: e9d0380e-3b08-45e4-8419-447df2e8de37
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef

---


# Favoriten-Ansicht{#favorites-view}

Die Ansicht &quot;Favoriten&quot;besteht aus einer Spalte mit Miniaturbildern.

<!--<a id="section_B6EFCCADB5A5495DAE6BBE42F7F405CB"></a>-->

Das Erscheinungsbild des Containers der Favoriten-Ansicht wird mit der folgenden CSS-Klassenauswahl gesteuert:

```
.s7ecatalogsearchviewer .s7favoritesview
```

Die Position und Höhe der Favoriten-Ansicht wird von der Ansicht verwaltet; in CSS ist es nur möglich, die Breite zu definieren.

**CSS-Eigenschaften der Favoriten-Ansicht**

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

Beispiel: Zum Einrichten einer Favoriten-Ansicht mit einer Breite von 100 Pixeln und einem halbtransparenten grauen Hintergrund.

```
.s7ecatalogsearchviewer .s7favoritesview { 
 width: 100px; 
 background-color: rgba(221, 221, 221, 0.5); 
}
```

Der Abstand zwischen den Favoriten-Miniaturbildern wird mit der folgenden CSS-Klassenauswahl gesteuert:

```
.s7ecatalogsearchviewer .s7favoritesview .s7thumbcell
```

**CSS-Eigenschaften der Favoriten-Miniaturansichten**

<table id="table_EED8CE63D805458196DE0E87C7E9945F"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margin </span> </p> </td> 
   <td colname="col2"> <p> Die Größe des vertikalen Randes um die einzelnen Miniaturansichten. Der tatsächliche Abstand der Miniaturansichten entspricht der Summe der oberen und unteren Ränder, die für <span class="codeph"> .s7thumbcell festgelegt wurde </span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

Beispiel: Zum Einrichten eines 10-Pixel-Abstands.

```
.s7ecatalogsearchviewer .s7favoritesview .s7thumbcell { 
 margin: 5px; 
}
```

Das Erscheinungsbild der einzelnen Miniaturansichten wird mit der folgenden CSS-Klassenauswahl gesteuert:

```
.s7ecatalogsearchviewer .s7favoritesview .s7thumb
```

**CSS-Eigenschaften der Favoriten-Miniaturansichten**

<table id="table_6F5B1438CAFA49E9B33400C6970ABDA1"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Breite der Miniaturansicht. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Höhe der Miniaturansicht. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> rand </span> </p> </td> 
   <td colname="col2"> <p>Rand der Miniaturansicht. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Miniaturansicht unterstützt die `state` Attributauswahl, mit der verschiedene Skins auf verschiedene Miniaturansichten angewendet werden können. Dies entspricht insbesondere `state="selected"` der Miniaturansicht, die der Benutzer kürzlich ausgewählt hat. `state="default"` entspricht dem Rest der Miniaturansichten. Und `state="over"` wird beim Bewegen der Maus verwendet.

Beispiel: Zum Einrichten von Miniaturbildern mit 75 x 75 Pixel, einem hellgrauen Standardrand und einem dunkelgrauen ausgewählten Rand.

```
.s7ecatalogsearchviewer .s7favoritesview .s7thumb { 
 width: 75px; 
 height: 75px;  
} 
.s7ecatalogsearchviewer .s7favoritesview .s7thumb[state="default"] { 
 border: 1px solid #dddddd; 
} 
.s7ecatalogsearchviewer .s7favoritesview .s7thumb[state="selected"] { 
 border: 1px solid #666666; 
}
```

Die Darstellung der Miniaturansichtsbeschriftung wird mit der folgenden CSS-Klassenauswahl gesteuert:

```
.s7ecatalogsearchviewer .s7favoritesview .s7label
```

**CSS-Eigenschaften der Favoritenbeschriftung**

<table id="table_B41339A16ACB46CB87D3EB1FD05FA2CD"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-famiy </span> </p> </td> 
   <td colname="col2"> <p>Schriftname. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size </span> </p> </td> 
   <td colname="col2"> <p>Schriftgröße. </p> </td> 
  </tr> 
 </tbody> 
</table>

Beispiel: Zum Einrichten von Beschriftungen mit einer Helvetica-Schrift von 14 Pixel.

```
.s7ecatalogsearchviewer .s7favoritesview .s7label { 
 font-family: Helvetica,sans-serif; 
 font-size: 14px; 
}
```

