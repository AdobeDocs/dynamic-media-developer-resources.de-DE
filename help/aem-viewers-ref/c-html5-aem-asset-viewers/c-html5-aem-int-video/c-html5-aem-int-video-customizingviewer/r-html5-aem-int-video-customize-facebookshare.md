---
title: Facebook Share
description: Das facebook-Freigebungs-Tool besteht aus einer Schaltfläche, die dem Social-Freigabe-Bedienfeld hinzugefügt wird. Wenn die Schaltfläche ausgewählt ist, wird der Benutzer zu einem Freigabedialogfeld umgeleitet, das von einem Social-Dienst bereitgestellt wird. Die Position der Schaltfläche wird vollständig vom Social-Freigabe-Tool verwaltet.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: 209dfe87-ca9d-405f-ba78-4e88f6ebe1d2
source-git-commit: 6aaf4eccf51a05d200c6cc780e342be646d104d8
workflow-type: tm+mt
source-wordcount: '228'
ht-degree: 0%

---

# Facebook Share{#facebook-share}

Das facebook-Freigebungs-Tool besteht aus einer Schaltfläche, die dem Social-Freigabe-Bedienfeld hinzugefügt wird. Wenn die Schaltfläche ausgewählt ist, wird der Benutzer zu einem Freigabedialogfeld umgeleitet, das von einem Social-Dienst bereitgestellt wird. Die Position der Schaltfläche wird vollständig vom Social-Freigabe-Tool verwaltet.

<!--<a id="section_ADDF98E91AF24F618289D1682A5FB13A"></a>-->

Das Erscheinungsbild der Facebook-Freigabe-Schaltfläche wird mit der folgenden CSS-Klassenauswahl gesteuert:

```
.s7interactivevideoviewer .s7facebookshare
```

**CSS-Eigenschaften des Facebook-Freigabe-Tools**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Schaltflächenbreite. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Höhe </span> </p> </td> 
   <td colname="col2"> <p>Schaltflächenhöhe. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image </span> </p> </td> 
   <td colname="col2"> <p> Das Bild, das für einen bestimmten Schaltflächenstatus angezeigt wird. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p> Position innerhalb des Bildsprites, wenn CSS-Sprites verwendet werden. </p> <p>Siehe <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-viewer-20-customizingviewer/c-html5-video-viewer-20-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> CSS-Sprites </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Diese Schaltfläche unterstützt die &quot;`state`&quot;-Attributauswahl, mit der verschiedene Skins auf unterschiedliche Schaltflächenzustände angewendet werden können.

Sie können die Schaltfläche aus dem Social-Freigabebereich entfernen, indem Sie die CSS-Eigenschaft `display:none` in der CSS-Klasse festlegen.

Die QuickInfo der Schaltfläche kann lokalisiert werden. Siehe [Lokalisierung von Elementen der Benutzeroberfläche](../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74).

## Beispiel {#section-01cbe0096b1443e0a7d91956bd264465}

So richten Sie eine Facebook-Freigabeschaltfläche ein, die 28 x 28 Pixel groß ist und für jeden der vier Schaltflächenstatus ein anderes Bild anzeigt:

```
.s7interactivevideoviewer .s7facebookshare { 
 width:28px; 
 height:28px; 
} 
.s7interactivevideoviewer .s7facebookshare[state='up'] { 
background-image:url(images/v2/FacebookShare_dark_up.png); 
} 
.s7interactivevideoviewer .s7facebookshare[state='over'] { 
background-image:url(images/v2/FacebookShare_dark_over.png); 
} 
.s7interactivevideoviewer .s7facebookshare[state='down'] { 
background-image:url(images/v2/FacebookShare_dark_down.png); 
} 
.s7interactivevideoviewer .s7facebookshare[state='disabled'] { 
background-image:url(images/v2/FacebookShare_dark_disabled.png); 
}
```
