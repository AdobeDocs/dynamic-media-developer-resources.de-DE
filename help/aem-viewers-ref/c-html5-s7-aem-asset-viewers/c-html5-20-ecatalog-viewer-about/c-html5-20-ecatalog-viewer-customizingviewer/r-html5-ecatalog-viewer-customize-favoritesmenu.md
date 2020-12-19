---
description: Die Dropdown-Liste "Favoriten"wird in der Steuerungsleiste angezeigt. Es besteht aus einer Schaltfläche und einem Bereich, der erweitert wird, wenn ein Benutzer auf eine Schaltfläche klickt oder darauf tippt. Das Bedienfeld enthält einzelne Favoriten-Werkzeuge.
seo-description: Die Dropdown-Liste "Favoriten"wird in der Steuerungsleiste angezeigt. Es besteht aus einer Schaltfläche und einem Bereich, der erweitert wird, wenn ein Benutzer auf eine Schaltfläche klickt oder darauf tippt. Das Bedienfeld enthält einzelne Favoriten-Werkzeuge.
seo-title: Favoriten, Menü
solution: Experience Manager
title: Favoriten, Menü
topic: Dynamic media
uuid: 816e614d-8253-49a8-b57e-0b57b44db535
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef
workflow-type: tm+mt
source-wordcount: '360'
ht-degree: 0%

---


# Favoriten-Menü{#favorites-menu}

Die Dropdown-Liste &quot;Favoriten&quot;wird in der Steuerungsleiste angezeigt. Es besteht aus einer Schaltfläche und einem Bereich, der erweitert wird, wenn ein Benutzer auf eine Schaltfläche klickt oder darauf tippt. Das Bedienfeld enthält einzelne Favoriten-Werkzeuge.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

Die Position und Größe des Menüs &quot;Favoriten&quot;in der Benutzeroberfläche des Viewers werden mit der folgenden CSS-Klassenauswahl gesteuert:

```
.s7ecatalogviewer .s7favoritesmenu
```

**CSS-Eigenschaften der Menüschaltfläche &quot;Favoriten&quot;**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margin-top  </span> </p> </td> 
   <td colname="col2"> <p> Der Offset vom oberen Rand der Steuerleiste. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margin-left  </span> </p> </td> 
   <td colname="col2"> <p> Der Abstand zur nächsten Schaltfläche links oder zur linken Seite der Steuerungsleiste, wenn dies die erste Schaltfläche in einer Zeile ist. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Breite der Schaltfläche. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Höhe der Schaltfläche. </p> </td> 
  </tr> 
 </tbody> 
</table>

Beispiel: Richten Sie ein Favoritenmenü ein, das vier Pixel von oben in der Steuerungsleiste und zehn Pixel von der nächsten Schaltfläche links und 28 x 28 Pixel in der Größe positioniert wird.

```
.s7ecatalogviewer .s7favoritesmenu { 
margin-top: 4px; 
margin-left: 10px; 
 width:28px; 
 height:28px; 
}
```

Die Darstellung der Menüschaltfläche &quot;Favoriten&quot;wird mit der folgenden CSS-Klassenauswahl gesteuert:

```
.s7ecatalogviewer .s7favoritesmenu .s7favoritesbutton
```

**CSS-Eigenschaften der Schaltfläche &quot;Favoriten&quot;**

<table id="table_970D62A1413145E0A964FA9D9F108579"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image  </span> </p> </td> 
   <td colname="col2"> <p> Das Bild, das für einen bestimmten Schaltflächenstatus angezeigt wird. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position  </span> </p> </td> 
   <td colname="col2"> <p> Position innerhalb des Bildausschnitt, wenn CSS-Sprites verwendet werden. </p> <p>Siehe auch <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-customizingviewer/c-html5-20-ecatalog-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> CSS-Sprites </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Diese Schaltfläche unterstützt die Attributauswahl `state`, mit der verschiedene Skins auf verschiedene Schaltflächenzustände angewendet werden können.

Die QuickInfo für Schaltflächen kann lokalisiert werden. Weitere Informationen finden Sie unter [Lokale Anpassung der Elemente der Benutzeroberfläche](../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74).

Beispiel: Richten Sie eine Menüschaltfläche &quot;Favoriten&quot;ein, mit der für jeden der vier Schaltflächenzustände ein anderes Bild angezeigt wird.

```
.s7ecatalogviewer .s7favoritesmenu .s7favoritesbutton[state='up'] { 
background-image:url(images/v2/FavoritesMenu dark_up.png); 
} 
.s7ecatalogviewer .s7favoritesmenu .s7favoritesbutton[state='over'] { 
background-image:url(images/v2/FavoritesMenu_dark_over.png); 
} 
.s7ecatalogviewer .s7favoritesmenu .s7favoritesbutton[state='down'] { 
background-image:url(images/v2/FavoritesMenu_dark_down.png); 
} 
.s7ecatalogviewer .s7favoritesmenu .s7favoritesbutton[state='disabled'] { 
background-image:url(images/v2/FavoritesMenu_dark_disabled.png); 
}
```

Das Erscheinungsbild des Bedienfelds, das einzelne Favoritensymbole enthält, wird mithilfe der folgenden CSS-Klassenauswahl gesteuert:

```
.s7ecatalogviewer .s7favoritesmenu .s7favoritesmenupanel
```

**CSS-Eigenschaften des Menüfelds &quot;Favoriten&quot;**

<table id="table_B57B44C561E94F86BB1B0EC1671F26DB"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color  </span> </p> </td> 
   <td colname="col2"> <p>Die Hintergrundfarbe des Bedienfelds. </p> </td> 
  </tr> 
 </tbody> 
</table>

Beispiel: Richten Sie ein Bedienfeld ein, das eine transparente Farbe hat.

```
.s7ecatalogviewer .s7favoritesmenu .s7favoritesmenupanel { 
 background-color: transparent; 
}
```

