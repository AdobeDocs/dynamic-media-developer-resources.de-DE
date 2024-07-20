---
title: Schaltfläche "Favoriten entfernen"
description: Die Position der Schaltfläche "Favoriten entfernen"wird vollständig über das Menü "Favoriten"verwaltet.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: 4bf4b055-598c-41b9-bc98-c51926c4785f
source-git-commit: ec2a15e2e76bae5da4fbabc9b6912b12dc080f66
workflow-type: tm+mt
source-wordcount: '194'
ht-degree: 0%

---

# Schaltfläche &quot;Favoriten entfernen&quot;{#remove-favorite-button}

Die Position der Schaltfläche &quot;Favoriten entfernen&quot;wird vollständig über das Menü &quot;Favoriten&quot;verwaltet.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

Das Erscheinungsbild der Schaltfläche &quot;Favorit entfernen&quot;wird mit der folgenden CSS-Klassenauswahl gesteuert:

```
.s7ecatalogsearchviewer .s7removefavoritebutton
```

**CSS-Eigenschaften der Schaltfläche &quot;Favoriten entfernen&quot;**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image </span> </p> </td> 
   <td colname="col2"> <p> Das Bild, das für einen bestimmten Schaltflächenstatus angezeigt wird. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p> Position innerhalb des Bildsprites, wenn CSS-Sprites verwendet werden. </p> <p>Siehe auch <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-customizingviewer/c-html5-ecatsearch-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> CSS-Sprites </a>. </p> </td> 
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
>Diese Schaltfläche unterstützt sowohl die Attribute `state` als auch `selected`, die verwendet werden können, um verschiedene Skins auf verschiedene Schaltflächenzustände anzuwenden. Insbesondere entspricht `selected='true'` dem Status, in dem ein Benutzer durch Klicken oder Tippen ein neues Favoritensymbol hinzufügen kann. Und `selected='false'` entspricht dem normalen Betriebsmodus, in dem ein Benutzer Seiten zoomen, schwenken und tauschen kann.

Die QuickInfo der Schaltfläche kann lokalisiert werden. Weitere Informationen finden Sie unter [Lokalisierung von Benutzeroberflächenelementen](../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) .

Beispiel: Zum Einrichten einer Schaltfläche &quot;Favoriten entfernen&quot;, die 28 x 28 Pixel groß ist und für jeden der vier Schaltflächenstatus ein anderes Bild anzeigt, wenn diese ausgewählt sind oder nicht.

```
.s7ecatalogsearchviewer .s7removefavoritebutton { 
 width:28px; 
 height:28px; 
} 
.s7ecatalogsearchviewer .s7removefavoritebutton[selected='false'][state='up'] { 
background-image:url(images/v2/RemoveFavoriteButton_dark_up.png); 
} 
.s7ecatalogsearchviewer .s7removefavoritebutton[selected='false'][state='over'] { 
background-image:url(images/v2/RemoveFavoriteButton_dark_over.png); 
} 
.s7ecatalogsearchviewer .s7removefavoritebutton[selected='false'][state='down'] { 
background-image:url(images/v2/RemoveFavoriteButton_dark_down.png); 
} 
.s7ecatalogsearchviewer .s7removefavoritebutton[selected='false'][state='disabled'] { 
background-image:url(images/v2/RemoveFavoriteButton_dark_disabled.png); 
} 
.s7ecatalogsearchviewer .s7removefavoritebutton[selected='true'][state='up'] { 
background-image:url(images/v2/RemoveFavoriteButton_dark_over.png); 
} 
.s7ecatalogsearchviewer .s7removefavoritebutton[selected='true'][state='over'] { 
background-image:url(images/v2/RemoveFavoriteButton_dark_over.png); 
} 
.s7ecatalogsearchviewer .s7removefavoritebutton[selected='true'][state='down'] { 
background-image:url(images/v2/RemoveFavoriteButton_dark_over.png); 
} 
.s7ecatalogsearchviewer .s7removefavoritebutton[selected='true'][state='disabled'] { 
background-image:url(images/v2/RemoveFavoriteButton_dark_disabled.png); 
}
```
