---
title: Favoriten-Effekt
description: Der Viewer zeigt an den Stellen, an denen er ursprünglich vom Benutzer hinzugefügt wurde, die Favoritensymbole über der Hauptansicht an.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: e87226cf-56bf-4d54-8df5-91295eae90a8
source-git-commit: edc127dc6e2ae2d9bd5feed08c8bc896c8c39747
workflow-type: tm+mt
source-wordcount: '181'
ht-degree: 0%

---

# Favoriten-Effekt{#favorites-effect}

Der Viewer zeigt an den Stellen, an denen er ursprünglich vom Benutzer hinzugefügt wurde, die Favoritensymbole über der Hauptansicht an.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

Das Erscheinungsbild des Favoritensymbols wird mit dem folgenden CSS-Klassenselektor gesteuert:

```
.s7ecatalogviewer .s7favoriteseffect .s7icon
```

**CSS-Eigenschaften des Favoritensymbols**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Hintergrundbild-</span> </p> </td> 
   <td colname="col2"> <p> Das Bild, das für das Symbol angezeigt wird. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Hintergrundposition </span> </p> </td> 
   <td colname="col2"> <p> Positionieren Sie sie innerhalb des Bildsets, wenn CSS-Sprites verwendet werden. </p> <p>Siehe auch <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-customizingviewer/c-html5-20-ecatalog-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> CSS Sprites-</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Breite </span> </p> </td> 
   <td colname="col2"> <p>Breite des Symbols. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Höhe </span> </p> </td> 
   <td colname="col2"> <p>Höhe des Symbols. </p> </td> 
  </tr> 
 </tbody> 
</table>

Beispiel - Ein Favoritensymbol mit 36 x 36 Pixeln einrichten.

```
.s7ecatalogviewer .s7favoriteseffect .s7icon { 
 height: 36px; 
 width: 36px;  
 background-image: url(images/v2/FavoriteEffect_dark_up.png); 
}
```

Auf Desktop-Systemen unterstützt die Komponente den `cursortype`-Attributselektor , den Sie auf die `.s7favoriteseffect`-Klasse anwenden können, und steuert den Cursortyp anhand der ausgewählten Benutzeraktion. Die folgenden `cursortype` werden unterstützt:

<table id="table_71F8F333909247E4ACFEBDE3A1370EAB"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> mode_add </span> </p> </td> 
   <td colname="col2"> <p>Angezeigter Benutzer fügt ein neues Favoritensymbol hinzu. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> mode_remove </span> </p> </td> 
   <td colname="col2"> <p>Angezeigter Benutzer entfernt ein vorhandenes Favoritensymbol. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> mode_view </span> </p> </td> 
   <td colname="col2"> <p>Wird im normalen Betriebsmodus angezeigt, wenn die Bearbeitung der Favoriten nicht aktiv ist. </p> </td> 
  </tr> 
 </tbody> 
</table>

Beispiel: Für unterschiedliche Mauszeiger für die einzelnen Arten von Komponentenstatus.

```
.s7ecatalogviewer .s7favoriteseffect[cursortype="mode_add"] { 
cursor: crosshair; 
} 
.s7ecatalogviewer .s7favoriteseffect[cursortype="mode_remove"] { 
cursor: not-allowed; 
} 
.s7ecatalogviewer .s7favoriteseffect[cursortype="mode_view"] { 
cursor: auto; 
}
```
