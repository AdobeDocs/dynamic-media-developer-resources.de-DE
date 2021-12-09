---
title: Favoriten, Menü
description: Die Dropdownliste Favoriten-Menü wird in der Symbolleiste angezeigt. Er besteht aus einer Schaltfläche und einem Bereich, der sich erweitert, wenn ein Benutzer auf eine Schaltfläche klickt oder tippt. Der Bereich enthält die einzelnen Favoriten-Tools.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: e3c90320-b6fc-4a43-b75f-d39234b1e73c
source-git-commit: edc127dc6e2ae2d9bd5feed08c8bc896c8c39747
workflow-type: tm+mt
source-wordcount: '326'
ht-degree: 0%

---

# Favoriten, Menü{#favorites-menu}

Die Dropdownliste Favoriten-Menü wird in der Symbolleiste angezeigt. Er besteht aus einer Schaltfläche und einem Bereich, der sich erweitert, wenn ein Benutzer auf eine Schaltfläche klickt oder tippt. Der Bereich enthält die einzelnen Favoriten-Tools.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

Die Position und Größe des Favoriten-Menüs in der Viewer-Benutzeroberfläche wird mit der folgenden CSS-Klassenauswahl gesteuert:

```
.s7ecatalogviewer .s7favoritesmenu
```

**CSS-Eigenschaften der Menüschaltfläche &quot;Favoriten&quot;**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margin-top </span> </p> </td> 
   <td colname="col2"> <p> Der Versatz am oberen Rand der Steuerleiste. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margin-left </span> </p> </td> 
   <td colname="col2"> <p> Der Abstand zur nächsten Schaltfläche auf der linken Seite oder zur linken Seite der Steuerleiste, wenn dies die erste Schaltfläche in einer Zeile ist. </p> </td> 
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

Beispiel: So richten Sie ein Favoritenmenü ein, das vier Pixel von der oberen Ecke der Steuerleiste und zehn Pixel von der nächsten Schaltfläche links und 28 x 28 Pixel groß ist:

```
.s7ecatalogviewer .s7favoritesmenu { 
margin-top: 4px; 
margin-left: 10px; 
 width:28px; 
 height:28px; 
}
```

Das Erscheinungsbild der Menüschaltfläche &quot;Favoriten&quot;wird mit der folgenden CSS-Klassenauswahl gesteuert:

```
.s7ecatalogviewer .s7favoritesmenu .s7favoritesbutton
```

**CSS-Eigenschaften der Schaltfläche &quot;Favoriten&quot;**

<table id="table_970D62A1413145E0A964FA9D9F108579"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image </span> </p> </td> 
   <td colname="col2"> <p> Das Bild, das für einen bestimmten Schaltflächenstatus angezeigt wird. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p> Position innerhalb des Bildsprites, wenn CSS-Sprites verwendet werden. </p> <p>Siehe auch <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-customizingviewer/c-html5-20-ecatalog-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> CSS-Sprites </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Diese Schaltfläche unterstützt `state` -Attributauswahl, die verwendet werden kann, um verschiedene Skins auf verschiedene Schaltflächenzustände anzuwenden.

Die QuickInfo der Schaltfläche kann lokalisiert werden. Siehe [Lokalisierung der Elemente der Benutzeroberfläche](../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) für weitere Informationen.

Beispiel - So richten Sie eine Favoriten-Menüschaltfläche ein, die für jeden der vier Schaltflächenstatus ein anderes Bild anzeigt:

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

Das Erscheinungsbild des Bedienfelds, das einzelne Favoritensymbole enthält, wird mit der folgenden CSS-Klassenauswahl gesteuert:

```
.s7ecatalogviewer .s7favoritesmenu .s7favoritesmenupanel
```

**CSS-Eigenschaften des Menübereichs &quot;Favoriten&quot;**

<table id="table_B57B44C561E94F86BB1B0EC1671F26DB"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p>Die Hintergrundfarbe des Bedienfelds. </p> </td> 
  </tr> 
 </tbody> 
</table>

Beispiel: So richten Sie ein Bedienfeld mit einer transparenten Farbe ein:

```
.s7ecatalogviewer .s7favoritesmenu .s7favoritesmenupanel { 
 background-color: transparent; 
}
```
