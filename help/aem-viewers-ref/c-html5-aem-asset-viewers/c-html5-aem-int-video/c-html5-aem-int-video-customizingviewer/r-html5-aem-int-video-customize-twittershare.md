---
title: Twitter-Freigabe
description: Das twitter-Freigabetool besteht aus einer Schaltfläche, die dem Social-Sharing-Bedienfeld hinzugefügt wurde. Wenn die Schaltfläche ausgewählt ist, wird der Benutzer zu einem Freigabedialogfeld weitergeleitet, das von einem Social-Media-Service bereitgestellt wird. Die Position der Schaltfläche wird vollständig vom Tool Social Share verwaltet.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: 045ca718-b971-4437-a0bf-580eee83ff2d
source-git-commit: 6aaf4eccf51a05d200c6cc780e342be646d104d8
workflow-type: tm+mt
source-wordcount: '228'
ht-degree: 0%

---

# Twitter-Freigabe{#twitter-share}

Das twitter-Freigabetool besteht aus einer Schaltfläche, die dem Social-Sharing-Bedienfeld hinzugefügt wurde. Wenn die Schaltfläche ausgewählt ist, wird der Benutzer zu einem Freigabedialogfeld weitergeleitet, das von einem Social-Media-Service bereitgestellt wird. Die Position der Schaltfläche wird vollständig vom Tool Social Share verwaltet.

<!--<a id="section_ADDF98E91AF24F618289D1682A5FB13A"></a>-->

Das Erscheinungsbild der Twitter-Freigabeschaltfläche wird mit dem folgenden CSS-Klassenselektor gesteuert:

```
.s7interactivevideoviewer .s7twittershare
```

**CSS-Eigenschaften des Twitter-Freigabe-Tools**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Breite </span> </p> </td> 
   <td colname="col2"> <p>Breite der Schaltfläche. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Höhe </span> </p> </td> 
   <td colname="col2"> <p>Höhe der Schaltfläche. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Hintergrundbild-</span> </p> </td> 
   <td colname="col2"> <p> Das Bild, das für einen bestimmten Schaltflächenstatus angezeigt wird. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Hintergrundposition </span> </p> </td> 
   <td colname="col2"> <p> Positionieren Sie sie innerhalb des Bildsets, wenn CSS-Sprites verwendet werden. </p> <p>Siehe <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-customizingviewer/c-html5-aem-int-video-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> von CSS-Sprites </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Diese Schaltfläche unterstützt die `state`-Attributauswahl, mit der verschiedene Skins auf verschiedene Schaltflächenzustände angewendet werden können.

Sie können die Schaltfläche aus dem Bedienfeld Social-Freigabe entfernen, indem Sie `display:none` CSS-Eigenschaft für die CSS-Klasse festlegen.

Die QuickInfo der Schaltfläche kann lokalisiert werden. Siehe [Lokalisierung von Benutzeroberflächenelementen](../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74).

## Beispiel {#section-5a8837ea208e48ed8dfa6a3c1a514492}

So richten Sie eine Twitter-Freigabetaste ein, die 28 x 28 Pixel groß ist und für jeden der vier verschiedenen Tastenstatus ein anderes Bild anzeigt:

```
.s7interactivevideoviewer .s7twittershare { 
 width:28px; 
 height:28px; 
} 
.s7interactivevideoviewer .s7twittershare[state='up'] { 
background-image:url(images/v2/TwitterShare_dark_up.png); 
} 
.s7interactivevideoviewer .s7twittershare[state='over'] { 
background-image:url(images/v2/TwitterShare_dark_over.png); 
} 
.s7interactivevideoviewer .s7twittershare[state='down'] { 
background-image:url(images/v2/TwitterShare_dark_down.png); 
} 
.s7interactivevideoviewer .s7twittershare[state='disabled'] { 
background-image:url(images/v2/TwitterShare_dark_disabled.png); 
}
```
