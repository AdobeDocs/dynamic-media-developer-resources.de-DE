---
description: Suchschaltfläche
solution: Experience Manager
title: Suchschaltfläche
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: ede7d887-526b-4e00-9885-166dc37627aa
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '193'
ht-degree: 1%

---

# Suchschaltfläche{#search-button}

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**CSS-Eigenschaften des Haupt-Viewer-Bereichs**

Das Erscheinungsbild der Schaltfläche wird mit der folgenden CSS-Klassenauswahl gesteuert:

`.s7ecatalogsearchviewer .s7searchbutton`

<table id="table_94EE3F5BBE4547C0B4943471CEE7EDE4"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS-Eigenschaft </p> </th> 
   <th colname="col2" class="entry"> <p>Beschreibung </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Breite der Schaltfläche. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Höhe der Schaltfläche. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margin-top  </span> </p> </td> 
   <td colname="col2"> <p> Der Versatz am oberen Rand der Steuerleiste. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margin-left  </span> </p> </td> 
   <td colname="col2"> <p> Der Abstand zur nächsten Schaltfläche auf der linken Seite oder zur linken Seite der Steuerleiste, wenn dies die erste Schaltfläche in einer Zeile ist. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image  </span> </p> </td> 
   <td colname="col2"> <p>Das Bild, das für einen bestimmten Schaltflächenstatus angezeigt wird. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position  </span> </p> </td> 
   <td colname="col2"> <p> Position innerhalb des Bildsprites, wenn CSS-Sprites verwendet werden. </p> <p>Siehe auch <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-customizingviewer/c-html5-ecatsearch-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> CSS-Sprites </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Diese Schaltfläche unterstützt die Attributselektoren `state` und `selected`, die verwendet werden können, um verschiedene Skins auf unterschiedliche Schaltflächenzustände anzuwenden.
>
>Insbesondere entspricht `selected='false'` dem Status der ersten Bildlaufschaltfläche und `selected='true'` dem Status, in dem das Suchfeld aktiv ist.

Die QuickInfo der Schaltfläche kann lokalisiert werden. Weitere Informationen finden Sie unter [Lokalisierung von Benutzeroberflächenelementen](../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74).

Beispiel: Zum Einrichten einer Suchschaltfläche mit 28 x 28 Pixel und einem anderen Bild für jeden der vier verschiedenen Schaltflächenstatus, wenn ausgewählt oder nicht ausgewählt.

```
.s7ecatalogsearchviewer .s7searchbutton{ 
 margin-top: 4px; 
 margin-left: 10px; 
 width:28px; 
 height:28px;  
 display: inline-block; 
 background-size:contain; 
} 
 
.s7ecatalogsearchviewer.s7mouseinput .s7searchbutton[selected='false'][state='up'] { 
 background-image:url(images/v2/Search_dark_up.png); 
} 
.s7ecatalogsearchviewer.s7mouseinput .s7searchbutton[selected='false'][state='over'] { 
 background-image:url(images/v2/Search_dark_over.png);  
} 
.s7ecatalogsearchviewer.s7mouseinput .s7searchbutton[selected='false'][state='down'] { 
 background-image:url(images/v2/Search_dark_down.png); 
} 
.s7ecatalogsearchviewer.s7mouseinput .s7searchbutton[selected='false'][state='disabled'] { 
 background-image:url(images/v2/Search_dark_disabled.png); 
} 
.s7ecatalogsearchviewer.s7mouseinput .s7searchbutton[selected='true'][state='up'] { 
 background-image:url(images/v2/Search_dark_over.png); 
} 
.s7ecatalogsearchviewer.s7mouseinput .s7searchbutton[selected='true'][state='over'] { 
 background-image:url(images/v2/Search_dark_over.png);  
} 
.s7ecatalogsearchviewer.s7mouseinput .s7searchbutton[selected='true'][state='down'] { 
 background-image:url(images/v2/Search_dark_over.png);  
} 
.s7ecatalogsearchviewer.s7mouseinput .s7searchbutton[selected='true'][state='disabled'] { 
 background-image:url(images/v2/Search_dark_disabled.png);  
}
```
