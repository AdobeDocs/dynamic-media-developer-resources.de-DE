---
description: Der Viewer zeigt Favoritensymbole über der Haupt-Ansicht an den Stellen an, an denen sie ursprünglich vom Benutzer hinzugefügt wurden.
seo-description: Der Viewer zeigt Favoritensymbole über der Haupt-Ansicht an den Stellen an, an denen sie ursprünglich vom Benutzer hinzugefügt wurden.
seo-title: Favoriten, Effekt
solution: Experience Manager
title: Favoriten, Effekt
topic: Dynamic media
uuid: b660b9fd-592b-4072-83c9-f70330ee19ab
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef
workflow-type: tm+mt
source-wordcount: '202'
ht-degree: 0%

---


# Favoriteneffekt{#favorites-effect}

Der Viewer zeigt Favoritensymbole über der Haupt-Ansicht an den Stellen an, an denen sie ursprünglich vom Benutzer hinzugefügt wurden.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

Das Erscheinungsbild des Favoritensymbols wird mit der folgenden CSS-Klassenauswahl gesteuert:

```
.s7ecatalogviewer .s7favoriteseffect .s7icon
```

**CSS-Eigenschaften des Favoritensymbols**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image  </span> </p> </td> 
   <td colname="col2"> <p> Das für das Symbol angezeigte Bild. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position  </span> </p> </td> 
   <td colname="col2"> <p> Position innerhalb des Bildausschnitt, wenn CSS-Sprites verwendet werden. </p> <p>Siehe auch <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-customizingviewer/c-html5-20-ecatalog-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> CSS-Sprites </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Breite des Symbols. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Höhe des Symbols. </p> </td> 
  </tr> 
 </tbody> 
</table>

Beispiel: Richten Sie ein Favoritensymbol mit 36 x 36 Pixeln ein.

```
.s7ecatalogviewer .s7favoriteseffect .s7icon { 
 height: 36px; 
 width: 36px;  
 background-image: url(images/v2/FavoriteEffect_dark_up.png); 
}
```

Auf Desktop-Systemen unterstützt die Komponente die Attributauswahl `cursortype`, die Sie auf die Klasse `.s7favoriteseffect` anwenden können, und steuert den Cursortyp basierend auf der ausgewählten Benutzeraktion. Die folgenden `cursortype`-Werte werden unterstützt:

<table id="table_71F8F333909247E4ACFEBDE3A1370EAB"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> mode_add  </span> </p> </td> 
   <td colname="col2"> <p>Der angezeigte Benutzer fügt ein neues Favoritensymbol hinzu. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> mode_remove  </span> </p> </td> 
   <td colname="col2"> <p>Der angezeigte Benutzer entfernt ein vorhandenes Favoritensymbol. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> mode_Ansicht  </span> </p> </td> 
   <td colname="col2"> <p>Wird im normalen Betriebsmodus angezeigt, wenn die Bearbeitung der Favoriten nicht aktiv ist. </p> </td> 
  </tr> 
 </tbody> 
</table>

Beispiel: Sie haben unterschiedliche Mauszeiger für jeden Typ des Komponentenstatus.

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

