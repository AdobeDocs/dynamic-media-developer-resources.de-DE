---
description: Die Position der Schaltfläche wird vollständig über das Menü Favoriten verwaltet.
solution: Experience Manager
title: Schaltfläche "Alle Favoriten anzeigen"
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: e07da96d-e6ad-4257-afdb-f6967fb83f52
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '198'
ht-degree: 1%

---

# Schaltfläche &quot;Alle Favoriten anzeigen&quot;{#view-all-favorites-button}

Die Position der Schaltfläche wird vollständig über das Menü Favoriten verwaltet.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

Das Erscheinungsbild der Schaltfläche Alle Favoriten anzeigen wird mit der folgenden CSS-Klassenauswahl gesteuert:

```
.s7ecatalogviewer .s7viewallfavoritebutton
```

**CSS-Eigenschaften der Schaltfläche &quot;Favorit entfernen&quot;**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image  </span> </p> </td> 
   <td colname="col2"> <p> Das Bild, das für einen bestimmten Schaltflächenstatus angezeigt wird. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position  </span> </p> </td> 
   <td colname="col2"> <p> Position innerhalb des Bildsprites, wenn CSS-Sprites verwendet werden. </p> <p>Siehe auch <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-customizingviewer/c-html5-20-ecatalog-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> CSS-Sprites </a>. </p> </td> 
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
>Diese Schaltfläche unterstützt die Attributselektoren `state` und `selected`, die verwendet werden können, um verschiedene Skins auf unterschiedliche Schaltflächenzustände anzuwenden. Insbesondere `selected='true'` entspricht dem Status, in dem ein Benutzer durch Klicken oder Tippen ein neues Favoritensymbol hinzufügen kann. `selected='false'` entspricht dem normalen Betriebsmodus, in dem ein Benutzer Seiten zoomen, schwenken und austauschen kann.

Die QuickInfo der Schaltfläche kann lokalisiert werden. Weitere Informationen finden Sie unter [Lokalisierung von Benutzeroberflächenelementen](../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74).

Beispiel: Zum Einrichten einer Schaltfläche Alle Favoriten anzeigen , die 28 x 28 Pixel groß ist und für jeden der vier verschiedenen Schaltflächenstatus ein anderes Bild anzeigt, wenn diese ausgewählt sind oder nicht.

```
.s7ecatalogviewer .s7viewallfavoritebutton { 
 width:28px; 
 height:28px; 
} 
.s7ecatalogviewer .s7viewallfavoritebutton[selected='false'][state='up'] { 
background-image:url(images/v2/ViewAllFavoritesButton_dark_up.png); 
} 
.s7ecatalogviewer .s7viewallfavoritebutton[selected='false'][state='over'] { 
background-image:url(images/v2/ViewAllFavoritesButton_dark_over.png); 
} 
.s7ecatalogviewer .s7viewallfavoritebutton[selected='false'][state='down'] { 
background-image:url(images/v2/ViewAllFavoritesButton_dark_down.png); 
} 
.s7ecatalogviewer .s7viewallfavoritebutton[selected='false'][state='disabled'] { 
background-image:url(images/v2/ViewAllFavoritesButton_dark_disabled.png); 
} 
.s7ecatalogviewer .s7viewallfavoritebutton[selected='true'][state='up'] { 
background-image:url(images/v2/ViewAllFavoritesButton_dark_over.png); 
} 
.s7ecatalogviewer .s7viewallfavoritebutton[selected='true'][state='over'] { 
background-image:url(images/v2/ViewAllFavoritesButton_dark_over.png); 
} 
.s7ecatalogviewer .s7viewallfavoritebutton[selected='true'][state='down'] { 
background-image:url(images/v2/ViewAllFavoritesButton_dark_over.png); 
} 
.s7ecatalogviewer .s7viewallfavoritebutton[selected='true'][state='disabled'] { 
background-image:url(images/v2/ViewAllFavoritesButton_dark_disabled.png); 
}
```
