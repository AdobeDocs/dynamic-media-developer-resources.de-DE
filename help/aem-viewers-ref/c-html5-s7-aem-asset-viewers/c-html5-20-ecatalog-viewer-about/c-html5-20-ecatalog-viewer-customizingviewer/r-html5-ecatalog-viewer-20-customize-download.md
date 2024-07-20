---
title: Download
description: Download
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: fb01371b-0aa6-4591-8523-120c217cf45d
source-git-commit: edc127dc6e2ae2d9bd5feed08c8bc896c8c39747
workflow-type: tm+mt
source-wordcount: '155'
ht-degree: 1%

---

# Download{#download}

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

Das Erscheinungsbild der Schaltfläche &quot;Herunterladen&quot;wird mit der folgenden CSS-Klassenauswahl gesteuert:

```
.s7ecatalogviewer .s7download
```

**CSS-Eigenschaften der Schaltfläche &quot;Herunterladen&quot;**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margin-top </span> </p> </td> 
   <td colname="col2"> <p> Der Versatz am oberen Rand der Steuerleiste. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margin-left </span> </p> </td> 
   <td colname="col2"> <p> Der Abstand zur nächsten Schaltfläche auf der linken Seite oder zur linken Seite der Steuerleiste, wenn es sich um die erste Schaltfläche in einer Zeile handelt. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Breite der Schaltfläche. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Höhe </span> </p> </td> 
   <td colname="col2"> <p>Höhe der Schaltfläche. </p> </td> 
  </tr> 
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
>Diese Schaltfläche unterstützt die &quot;`state`&quot;-Attributauswahl, mit der verschiedene Skins auf unterschiedliche Schaltflächenzustände angewendet werden können.

Die QuickInfo der Schaltfläche kann lokalisiert werden. Weitere Informationen finden Sie unter [Lokalisierung von Benutzeroberflächenelementen](../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) .

Beispiel: Zum Einrichten einer Download-Schaltfläche mit 28 x 28 Pixel und einem anderen Bild für jeden der vier verschiedenen Schaltflächenstatus:

```
.s7ecatalogviewer .s7download { 
 margin-top: 4px; 
margin-left: 10px; 
 width:28px; 
 height:28px; 
} 
.s7ecatalogviewer .s7download[state='up'] { 
background-image:url(images/v2/Dowmload_dark_up.png); 
} 
.s7ecatalogviewer .s7download[state='over'] { 
background-image:url(images/v2/Dowmload_dark_over.png); 
} 
.s7ecatalogviewer .s7download[state='down'] { 
background-image:url(images/v2/Dowmload_dark_down.png); 
} 
.s7ecatalogviewer .s7download[state='disabled'] { 
background-image:url(images/v2/Dowmload_dark_disabled.png); 
}
```
