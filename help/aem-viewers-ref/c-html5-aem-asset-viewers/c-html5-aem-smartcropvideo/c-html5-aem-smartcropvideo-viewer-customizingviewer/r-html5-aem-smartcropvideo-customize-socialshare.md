---
title: Social Share
description: Das Social-Sharing-Tool wird standardmäßig in der oberen rechten Ecke angezeigt. Er besteht aus einer Schaltfläche und einem Bereich, der sich erweitert, wenn der Benutzer auf eine Schaltfläche klickt oder tippt, und einzelne Tools zur Freigabe enthält.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop Video
role: Developer,User
exl-id: 82b482f9-b117-4529-a422-cdb0eead0031
source-git-commit: b6ebc938f55117c4144ff921bed7f8742cf3a8a7
workflow-type: tm+mt
source-wordcount: '314'
ht-degree: 1%

---

# Social Share{#social-share}

Das Social-Sharing-Tool wird standardmäßig in der oberen rechten Ecke angezeigt. Er besteht aus einer Schaltfläche und einem Bereich, der sich erweitert, wenn der Benutzer auf eine Schaltfläche klickt oder tippt, und einzelne Tools zur Freigabe enthält.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

Die Position und Größe des Tools für die Freigabe in sozialen Netzwerken in der Viewer-Benutzeroberfläche wird wie folgt gesteuert:

```
.s7smartcropvideoviewer .s7socialshare
```

**CSS-Eigenschaften des Tools für die Freigabe in sozialen Netzwerken**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Anfang </span> </p> </td> 
   <td colname="col2"> <p> Vertikale Position des Tools für die Freigabe in sozialen Netzwerken relativ zum Viewer-Container. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> links </span> </p> </td> 
   <td colname="col2"> <p> Horizontale Position des Tools für die Freigabe in sozialen Netzwerken im Verhältnis zum Viewer-Container. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p> Die Breite des Social-Sharing-Tools. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Die Höhe des Social-Sharing-Tools. </p> </td> 
  </tr> 
 </tbody> 
</table>

Beispiel: Richten Sie ein Social-Sharing-Tool ein, das vier Pixel von der Oberseite und fünf Pixel von der rechten Seite des Viewer-Containers positioniert und auf 28 x 28 Pixel skaliert ist.

```
.s7smartcropvideoviewer .s7socialshare { 
 top:4px; 
 right:5px; 
 width:28px; 
 height:28px; 
}
```

Das Erscheinungsbild der Schaltfläche für das Social-Sharing-Tool wird mit der folgenden CSS-Klassenauswahl gesteuert:

```
.s7smartcropvideoviewer .s7socialshare .s7socialbutton
```

**CSS-Eigenschaften der Social-Schaltfläche**

<table id="table_A18B6978EC304C378F5FE92DD44D138D"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image </span> </p> </td> 
   <td colname="col2"> <p> Das Bild, das für einen bestimmten Schaltflächenstatus angezeigt wird. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p> Position innerhalb des Bildsprites, wenn CSS-Sprites verwendet werden. </p> <p>Siehe <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-smartcropvideo/c-html5-aem-smartcropvideo-viewer-customizingviewer/c-html5-aem-smartcropvideo-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> CSS-Sprites </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Diese Schaltfläche unterstützt `state` -Attributauswahl, die verwendet werden kann, um verschiedene Skins auf verschiedene Schaltflächenzustände anzuwenden.

Die QuickInfo der Schaltfläche kann lokalisiert werden. Siehe [Lokalisierung der Elemente der Benutzeroberfläche](../../../c-html5-aem-asset-viewers/c-html5-aem-smartcropvideo/r-html5-aem-smartcropvideo-viewer-localization.md#concept-1d5ca2d8480f4064a51eddba13940aad) für weitere Informationen.

Beispiel: Richten Sie eine Schaltfläche für das Social-Sharing-Tool ein, die für jeden der vier verschiedenen Schaltflächenstatus ein anderes Bild anzeigt.

```
.s7smartcropvideoviewer .s7socialshare .s7socialbutton[state='up'] { 
background-image:url(images/v2/SocialShare_video_dark_up.png); 
} 
.s7smartcropvideoviewer .s7socialshare .s7socialbutton[state='over'] { 
background-image:url(images/v2/SocialShare_dark_over.png); 
} 
.s7smartcropvideoviewer .s7socialshare .s7socialbutton[state='down'] { 
background-image:url(images/v2/SocialShare_dark_down.png); 
} 
.s7smartcropvideoviewer .s7socialshare .s7socialbutton[state='disabled'] { 
background-image:url(images/v2/SocialShare_dark_disabled.png); 
}
```

Das Erscheinungsbild des Bedienfelds, das die einzelnen Symbole für die Freigabe in sozialen Netzwerken enthält, wird mit der folgenden CSS-Klassenauswahl gesteuert:

```
.s7smartcropvideoviewer .s7socialshare .s7socialsharepanel
```

**CSS-Eigenschaften des Bedienfelds &quot;Social Share&quot;**

<table id="table_86E777A5851F47D6A49D966E24A9A6CD"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p>Die Hintergrundfarbe des Bedienfelds. </p> </td> 
  </tr> 
 </tbody> 
</table>

Beispiel: Richten Sie ein Bedienfeld ein, das eine transparente Farbe hat:

```
.s7smartcropvideoviewer .s7socialshare .s7socialsharepanel { 
 background-color: transparent; 
}
```
