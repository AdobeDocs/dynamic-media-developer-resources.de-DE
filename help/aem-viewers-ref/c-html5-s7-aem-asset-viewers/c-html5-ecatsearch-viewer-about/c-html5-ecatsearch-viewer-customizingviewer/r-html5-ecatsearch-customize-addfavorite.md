---
description: Die Position der Schaltfläche "Hinzufügen Favoriten"wird vollständig über das Menü "Favoriten"verwaltet.
seo-description: Die Position der Schaltfläche "Hinzufügen Favoriten"wird vollständig über das Menü "Favoriten"verwaltet.
seo-title: Schaltfläche "Hinzufügen Favoriten"
solution: Experience Manager
title: Schaltfläche "Hinzufügen Favoriten"
topic: Dynamic media
uuid: decde7d1-d7d1-4056-815c-2b6571110d9f
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef

---


# Schaltfläche &quot;Hinzufügen Favoriten&quot;{#add-favorite-button}

Die Position der Schaltfläche &quot;Hinzufügen Favoriten&quot;wird vollständig über das Menü &quot;Favoriten&quot;verwaltet.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

Die Darstellung der Schaltfläche &quot;Hinzufügen Favorite&quot;wird mit der folgenden CSS-Klassenauswahl gesteuert:

```
.s7ecatalogsearchviewer .s7addfavoritebutton
```

**CSS-Eigenschaften der Schaltfläche &quot;Hinzufügen Favorit&quot;**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image </span> </p> </td> 
   <td colname="col2"> <p> Das Bild, das für einen bestimmten Schaltflächenstatus angezeigt wird. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p> Position innerhalb des Bildausschnitt, wenn CSS-Sprites verwendet werden. </p> <p>Siehe auch <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-customizingviewer/c-html5-ecatsearch-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> CSS-Sprites </a>. </p> </td> 
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

>[!NOTE]
>
>Diese Schaltfläche unterstützt sowohl die `state` als auch die `selected` Attributselektoren, die verwendet werden können, um verschiedene Skins auf verschiedene Schaltflächenzustände anzuwenden. Dies `selected='true'` entspricht insbesondere dem Status, in dem ein Benutzer durch Klicken oder Tippen ein neues Favoritensymbol hinzufügen kann. `selected='false'` entspricht dem normalen Betriebsmodus, wenn ein Benutzer Seiten heranzoomen, schwenken und austauschen kann.

Die QuickInfo für Schaltflächen kann lokalisiert werden. Weitere Informationen finden Sie unter [Lokale Anpassung der Elemente](../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) der Benutzeroberfläche.

Beispiel: Zum Einrichten einer Hinzufügen Favoritenschaltfläche mit 28 x 28 Pixel und zum Anzeigen eines anderen Bilds für jeden der vier verschiedenen Schaltflächenzustände, wenn diese ausgewählt oder nicht ausgewählt sind.

```
.s7ecatalogsearchviewer .s7addfavoritebutton { 
 width:28px; 
 height:28px; 
} 
.s7ecatalogsearchviewer .s7addfavoritebutton[selected='false'][state='up'] { 
background-image:url(images/v2/AddFavoriteButton_dark_up.png); 
} 
.s7ecatalogsearchviewer .s7addfavoritebutton[selected='false'][state='over'] { 
background-image:url(images/v2/AddFavoriteButton_dark_over.png); 
} 
.s7ecatalogsearchviewer .s7addfavoritebutton[selected='false'][state='down'] { 
background-image:url(images/v2/AddFavoriteButton_dark_down.png); 
} 
.s7ecatalogsearchviewer .s7addfavoritebutton[selected='false'][state='disabled'] { 
background-image:url(images/v2/AddFavoriteButton_dark_disabled.png); 
} 
.s7ecatalogsearchviewer .s7addfavoritebutton[selected='true'][state='up'] { 
background-image:url(images/v2/AddFavoriteButton_dark_over.png); 
} 
.s7ecatalogsearchviewer .s7addfavoritebutton[selected='true'][state='over'] { 
background-image:url(images/v2/AddFavoriteButton_dark_over.png); 
} 
.s7ecatalogsearchviewer .s7addfavoritebutton[selected='true'][state='down'] { 
background-image:url(images/v2/AddFavoriteButton_dark_over.png); 
} 
.s7ecatalogsearchviewer .s7addfavoritebutton[selected='true'][state='disabled'] { 
background-image:url(images/v2/AddFavoriteButton_dark_disabled.png); 
}
```

