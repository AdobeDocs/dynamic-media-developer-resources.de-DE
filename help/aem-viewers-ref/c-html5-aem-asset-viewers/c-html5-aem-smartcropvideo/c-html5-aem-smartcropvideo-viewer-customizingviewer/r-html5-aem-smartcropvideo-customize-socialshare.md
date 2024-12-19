---
title: Gesellschaftsanteil
description: Das Social-Sharing-Tool wird standardmäßig oben rechts angezeigt. Es besteht aus einer Schaltfläche und einem Bedienfeld, das sich erweitert, wenn Benutzende auf eine Schaltfläche klicken oder tippen, und individuelle Freigabetools enthält.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop,Video
role: Developer,User
exl-id: 650e1a57-9b0e-4132-a9b0-42c33cacdc04
source-git-commit: 1aa8be858b0ba8ec9b99753d43c202b35ed58c30
workflow-type: tm+mt
source-wordcount: '316'
ht-degree: 0%

---

# Gesellschaftsanteil{#social-share}

Das Social-Sharing-Tool wird standardmäßig oben rechts angezeigt. Es besteht aus einer Schaltfläche und einem Bedienfeld, das sich erweitert, wenn Benutzende auf eine Schaltfläche klicken oder tippen, und individuelle Freigabetools enthält.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

Position und Größe des Tools für die Freigabe in der Viewer-Benutzeroberfläche werden wie folgt gesteuert:

```
.s7smartcropvideoviewer .s7socialshare
```

**CSS-Eigenschaften des Social-Share-Tools**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Top-</span> </p> </td> 
   <td colname="col2"> <p> Vertikale Position des Tools zur gemeinsamen Nutzung in sozialen Netzwerken relativ zum Viewer-Container. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> linker </span> </p> </td> 
   <td colname="col2"> <p> Horizontale Position des Tools zur gemeinsamen Nutzung in sozialen Netzwerken relativ zum Viewer-Container. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Breite </span> </p> </td> 
   <td colname="col2"> <p> Die Breite des Social-Sharing-Tools. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Höhe </span> </p> </td> 
   <td colname="col2"> <p>Die Höhe des Social-Sharing-Tools. </p> </td> 
  </tr> 
 </tbody> 
</table>

Beispiel - Richten Sie ein Tool zur gemeinsamen Nutzung sozialer Daten ein, das vier Pixel vom oberen und fünf Pixel vom rechten Rand des Viewer-Containers entfernt platziert und eine Größe von 28 x 28 Pixel hat.

```
.s7smartcropvideoviewer .s7socialshare { 
 top:4px; 
 right:5px; 
 width:28px; 
 height:28px; 
}
```

Das Erscheinungsbild der Schaltfläche Social Share Tool wird mit dem folgenden CSS-Klassenselektor gesteuert:

```
.s7smartcropvideoviewer .s7socialshare .s7socialbutton
```

**CSS-Eigenschaften der sozialen Schaltfläche**

<table id="table_A18B6978EC304C378F5FE92DD44D138D"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Hintergrundbild-</span> </p> </td> 
   <td colname="col2"> <p> Das Bild, das für einen bestimmten Schaltflächenstatus angezeigt wird. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Hintergrundposition </span> </p> </td> 
   <td colname="col2"> <p> Positionieren Sie sie innerhalb des Bildsets, wenn CSS-Sprites verwendet werden. </p> <p>Siehe <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-smartcropvideo/c-html5-aem-smartcropvideo-viewer-customizingviewer/c-html5-aem-smartcropvideo-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> von CSS-Sprites </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Diese Schaltfläche unterstützt die `state`-Attributauswahl, mit der verschiedene Skins auf verschiedene Schaltflächenzustände angewendet werden können.

Die QuickInfo der Schaltfläche kann lokalisiert werden. Siehe [Lokalisierung von Benutzeroberflächenelementen](../../../c-html5-aem-asset-viewers/c-html5-aem-smartcropvideo/r-html5-aem-smartcropvideo-viewer-localization.md#concept-1d5ca2d8480f4064a51eddba13940aad) für weitere Informationen.

Beispiel: Richten Sie eine Schaltfläche für ein Social-Sharing-Tool ein, die für jeden der vier verschiedenen Schaltflächenstatus ein anderes Bild anzeigt.

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

Das Erscheinungsbild des Bedienfelds, das die einzelnen Social-Sharing-Symbole enthält, wird mit dem folgenden CSS-Klassenselektor gesteuert:

```
.s7smartcropvideoviewer .s7socialshare .s7socialsharepanel
```

**CSS-Eigenschaften des Social-Share-Bedienfelds**

<table id="table_86E777A5851F47D6A49D966E24A9A6CD"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">-</span> </p> </td> 
   <td colname="col2"> <p>Die Hintergrundfarbe des Bedienfelds. </p> </td> 
  </tr> 
 </tbody> 
</table>

Beispiel: Richten Sie ein Bedienfeld so ein, dass es eine transparente Farbe hat:

```
.s7smartcropvideoviewer .s7socialshare .s7socialsharepanel { 
 background-color: transparent; 
}
```
