---
title: Schaltfläche "Favoriten hinzufügen"
description: Die Position der Schaltfläche "Favoriten hinzufügen"wird vollständig über das Menü "Favoriten"verwaltet.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: 3602fa7b-d654-4976-a62d-d959898cb530
source-git-commit: edc127dc6e2ae2d9bd5feed08c8bc896c8c39747
workflow-type: tm+mt
source-wordcount: '196'
ht-degree: 0%

---

# Schaltfläche &quot;Favoriten hinzufügen&quot;{#add-favorite-button}

Die Position der Schaltfläche &quot;Favoriten hinzufügen&quot;wird vollständig über das Menü &quot;Favoriten&quot;verwaltet.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

Das Erscheinungsbild der Schaltfläche &quot;Favorit hinzufügen&quot;wird mit der folgenden CSS-Klassenauswahl gesteuert:

```
.s7ecatalogviewer .s7addfavoritebutton
```

**CSS-Eigenschaften der Schaltfläche &quot;Favorit hinzufügen&quot;**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image </span> </p> </td> 
   <td colname="col2"> <p> Das Bild, das für einen bestimmten Schaltflächenstatus angezeigt wird. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p> Position innerhalb des Bildsprites, wenn CSS-Sprites verwendet werden. </p> <p>Siehe auch <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-customizingviewer/c-html5-20-ecatalog-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> CSS-Sprites </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Breite der Schaltfläche. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Höhe </span> </p> </td> 
   <td colname="col2"> <p>Höhe der Schaltfläche. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Diese Schaltfläche unterstützt sowohl die Attribute `state` als auch `selected`, die verwendet werden können, um verschiedene Skins auf verschiedene Schaltflächenzustände anzuwenden. Insbesondere entspricht `selected='true'` dem Status, in dem ein Benutzer durch Auswählen oder Tippen ein neues Favoritensymbol hinzufügen kann. Das Attribut `selected='false'` entspricht dem normalen Betriebsmodus, in dem ein Benutzer Seiten zoomen, schwenken und tauschen kann.

Die QuickInfo der Schaltfläche kann lokalisiert werden. Weitere Informationen finden Sie unter [Lokalisierung von Benutzeroberflächenelementen](../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) .

Beispiel: Um eine Schaltfläche &quot;Favoriten hinzufügen&quot;mit 28 x 28 Pixel einzurichten. Außerdem wird für jeden der vier Schaltflächenstatus ein anderes Bild angezeigt, wenn er ausgewählt oder nicht ausgewählt ist.

```
.s7ecatalogviewer .s7addfavoritebutton { 
 width:28px; 
 height:28px; 
} 
.s7ecatalogviewer .s7addfavoritebutton[selected='false'][state='up'] { 
background-image:url(images/v2/AddFavoriteButton_dark_up.png); 
} 
.s7ecatalogviewer .s7addfavoritebutton[selected='false'][state='over'] { 
background-image:url(images/v2/AddFavoriteButton_dark_over.png); 
} 
.s7ecatalogviewer .s7addfavoritebutton[selected='false'][state='down'] { 
background-image:url(images/v2/AddFavoriteButton_dark_down.png); 
} 
.s7ecatalogviewer .s7addfavoritebutton[selected='false'][state='disabled'] { 
background-image:url(images/v2/AddFavoriteButton_dark_disabled.png); 
} 
.s7ecatalogviewer .s7addfavoritebutton[selected='true'][state='up'] { 
background-image:url(images/v2/AddFavoriteButton_dark_over.png); 
} 
.s7ecatalogviewer .s7addfavoritebutton[selected='true'][state='over'] { 
background-image:url(images/v2/AddFavoriteButton_dark_over.png); 
} 
.s7ecatalogviewer .s7addfavoritebutton[selected='true'][state='down'] { 
background-image:url(images/v2/AddFavoriteButton_dark_over.png); 
} 
.s7ecatalogviewer .s7addfavoritebutton[selected='true'][state='disabled'] { 
background-image:url(images/v2/AddFavoriteButton_dark_disabled.png); 
}
```
