---
description: Das Social Sharing-Tool wird standardmäßig oben rechts angezeigt. Es besteht aus einer Schaltfläche und einem Bereich, der erweitert wird, wenn der Benutzer auf eine Schaltfläche klickt oder darauf tippt und einzelne Freigabewerkzeuge enthält.
solution: Experience Manager
title: Social Sharing
feature: Dynamic Media Classic,Viewer,SDK/API,360 VR Video
role: Entwickler, Geschäftspraktiker
exl-id: 4bc951ae-2b9a-4cbe-9288-170c576b3b7b
translation-type: tm+mt
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '330'
ht-degree: 1%

---

# Social Sharing{#social-share}

Das Social Sharing-Tool wird standardmäßig oben rechts angezeigt. Es besteht aus einer Schaltfläche und einem Bereich, der erweitert wird, wenn der Benutzer auf eine Schaltfläche klickt oder darauf tippt und einzelne Freigabewerkzeuge enthält.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

Die Position und Größe des Social Sharing-Tools in der Benutzeroberfläche des Viewers wird wie folgt gesteuert:

```
.s7video360viewer .s7socialshare
```

**CSS-Eigenschaften des Social Sharing-Tools**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Anfang </span> </p> </td> 
   <td colname="col2"> <p> Vertikale Position des Social Sharing-Tools im Verhältnis zum Viewer-Container. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> links </span> </p> </td> 
   <td colname="col2"> <p> Horizontale Position des Social Sharing-Werkzeugs relativ zum Viewer-Container. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p> Die Breite des Social Sharing-Tools. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Die Höhe des Social Sharing-Tools. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Beispiel** : Um ein Social Sharing-Tool einzurichten, das vier Pixel von oben und fünf Pixel von rechts vom Viewer-Container positioniert und 28 x 28 Pixel groß ist.

```
.s7interactivevideoviewer .s7socialshare { 
 top:4px; 
 right:5px; 
 width:28px; 
 height:28px; 
}
```

Das Erscheinungsbild der Schaltfläche für das Social Sharing-Tool wird mit der folgenden CSS-Klassenauswahl gesteuert:

```
.s7video360viewer .s7socialshare .s7socialbutton
```

**CSS-Eigenschaften der Schaltfläche &quot;Social Sharing&quot;**

<table id="table_A18B6978EC304C378F5FE92DD44D138D"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image  </span> </p> </td> 
   <td colname="col2"> <p> Das Bild, das für einen bestimmten Schaltflächenstatus angezeigt wird. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position  </span> </p> </td> 
   <td colname="col2"> <p> Position innerhalb des Bildausschnitt, wenn CSS-Sprites verwendet werden. </p> <p>Siehe <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-customizingviewer/c-html5-aem-video360-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> CSS-Sprites </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Diese Schaltfläche unterstützt die Attributauswahl `state`, mit der verschiedene Skins auf verschiedene Schaltflächenzustände angewendet werden können.

Die QuickInfo für Schaltflächen kann lokalisiert werden. Siehe [Lokale Anpassung der Elemente der Benutzeroberfläche](../../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-localization.md#concept-16262b8096474d6c9c018c3e99110dd1).

**Beispiel** : Um eine Schaltfläche für das Social Sharing-Tool einzurichten, mit der für jeden der vier Schaltflächenzustände ein anderes Bild angezeigt wird.

```
.s7video360viewer .s7socialshare .s7socialbutton[state='up'] { 
background-image:url(images/v2/SocialShare_video_dark_up.png); 
} 
.s7video360viewer .s7socialshare .s7socialbutton[state='over'] { 
background-image:url(images/v2/SocialShare_dark_over.png); 
} 
.s7video360viewer .s7socialshare .s7socialbutton[state='down'] { 
background-image:url(images/v2/SocialShare_dark_down.png); 
} 
.s7video360viewer .s7socialshare .s7socialbutton[state='disabled'] { 
background-image:url(images/v2/SocialShare_dark_disabled.png); 
}
```

Das Erscheinungsbild des Bedienfelds mit den einzelnen Social Sharing-Symbolen wird mithilfe der folgenden CSS-Klassenauswahl gesteuert:

```
.s7video360viewer .s7socialshare .s7socialsharepanel
```

**CSS-Eigenschaften des Social Sharing-Bedienfelds**

<table id="table_86E777A5851F47D6A49D966E24A9A6CD"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color  </span> </p> </td> 
   <td colname="col2"> <p>Die Hintergrundfarbe des Bedienfelds. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Beispiel** : So richten Sie einen Bereich mit transparenter Farbe ein:

```
.s7video360viewer .s7socialshare .s7socialsharepanel { 
 background-color: transparent; 
}
```
