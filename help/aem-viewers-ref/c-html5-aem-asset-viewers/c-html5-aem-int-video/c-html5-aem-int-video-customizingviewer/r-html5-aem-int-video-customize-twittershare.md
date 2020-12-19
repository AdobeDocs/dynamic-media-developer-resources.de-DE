---
description: Das Twitter-Freigeben-Tool besteht aus einer Schaltfläche, die dem Social Sharing-Bedienfeld hinzugefügt wird. Wenn auf die Schaltfläche geklickt wird, wird der Benutzer zu einem Freigabedialogfeld umgeleitet, das von einem Social-Dienst bereitgestellt wird. Die Position der Schaltfläche wird vollständig vom Social Sharing-Tool verwaltet.
seo-description: Das Twitter-Freigeben-Tool besteht aus einer Schaltfläche, die dem Social Sharing-Bedienfeld hinzugefügt wird. Wenn auf die Schaltfläche geklickt wird, wird der Benutzer zu einem Freigabedialogfeld umgeleitet, das von einem Social-Dienst bereitgestellt wird. Die Position der Schaltfläche wird vollständig vom Social Sharing-Tool verwaltet.
seo-title: Twitter-Freigabe
solution: Experience Manager
title: Twitter-Freigabe
topic: Dynamic media
uuid: f5f1182f-f95c-43c4-b39f-1b50ed4a5458
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef
workflow-type: tm+mt
source-wordcount: '275'
ht-degree: 1%

---


# Twitter-Freigabe{#twitter-share}

Das Twitter-Freigeben-Tool besteht aus einer Schaltfläche, die dem Social Sharing-Bedienfeld hinzugefügt wird. Wenn auf die Schaltfläche geklickt wird, wird der Benutzer zu einem Freigabedialogfeld umgeleitet, das von einem Social-Dienst bereitgestellt wird. Die Position der Schaltfläche wird vollständig vom Social Sharing-Tool verwaltet.

<!--<a id="section_ADDF98E91AF24F618289D1682A5FB13A"></a>-->

Das Erscheinungsbild der Twitter-Schaltfläche &quot;Freigeben&quot;wird mit der folgenden CSS-Klassenauswahl gesteuert:

```
.s7interactivevideoviewer .s7twittershare
```

**CSS-Eigenschaften des Twitter-Freigabe-Tools**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Schaltflächenbreite. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Schaltflächenhöhe. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image  </span> </p> </td> 
   <td colname="col2"> <p> Das Bild, das für einen bestimmten Schaltflächenstatus angezeigt wird. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position  </span> </p> </td> 
   <td colname="col2"> <p> Position innerhalb des Bildausschnitt, wenn CSS-Sprites verwendet werden. </p> <p>Siehe <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-customizingviewer/c-html5-aem-int-video-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> CSS-Sprites </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Diese Schaltfläche unterstützt die Attributauswahl `state`, mit der verschiedene Skins auf verschiedene Schaltflächenzustände angewendet werden können.

Sie können die Schaltfläche aus dem Social Sharing-Bedienfeld entfernen, indem Sie die CSS-Eigenschaft für `display:none` in der CSS-Klasse festlegen.

Die QuickInfo für Schaltflächen kann lokalisiert werden. Siehe [Lokale Anpassung der Elemente der Benutzeroberfläche](../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74).

## Beispiel {#section-5a8837ea208e48ed8dfa6a3c1a514492}

So richten Sie eine Twitter-Schaltfläche für die Freigabe ein, die 28 x 28 Pixel groß ist und für jeden der vier Schaltflächenzustände ein anderes Bild anzeigt:

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

