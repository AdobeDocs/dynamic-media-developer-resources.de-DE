---
title: Taste PLAY/PAUSE
description: Durch Klicken auf die Schaltfläche „Wiedergabe/Pause“ wird der Video-Player wiedergegeben oder der Videoinhalt angehalten, wenn ein Benutzer darauf klickt.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Video
role: Developer,User
exl-id: 174ddf15-e6be-4a65-8c82-5c9edf061a6c
source-git-commit: ceb9483f67a19d969ecbbd01cede11f3dae86467
workflow-type: tm+mt
source-wordcount: '265'
ht-degree: 0%

---

# Taste PLAY/PAUSE{#play-pause-button}

Durch Klicken auf die Schaltfläche „Wiedergabe/Pause“ wird der Video-Player wiedergegeben oder der Videoinhalt angehalten, wenn ein Benutzer darauf klickt.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

Sie können die Größe, das Design und die Position der Schaltfläche in Bezug auf die Steuerleiste, die sie enthält, per CSS festlegen.

Der folgende CSS-Klassenselektor steuert das Erscheinungsbild der Schaltfläche:

```
.s7videoviewer .s7playpausebutton
```

## CSS-Eigenschaften der Wiedergabe-/Pause-Schaltfläche {#css-properties-of-the-play-pause-button}

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Top-</span> </p> </td> 
   <td colname="col2"> <p>Position ab dem oberen Rahmen, einschließlich Auffüllung. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> rechte </span> </p> </td> 
   <td colname="col2"> <p>Position vom rechten Rand aus, einschließlich Abstand. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> linker </span> </p> </td> 
   <td colname="col2"> <p>Position vom linken Rand aus, einschließlich Auffüllung. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> untere </span> </p> </td> 
   <td colname="col2"> <p> Position ab dem unteren Rand, einschließlich Abstand. </p> </td> 
  </tr> 
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
   <td colname="col2"> <p>Das Bild, das für einen bestimmten Schaltflächenstatus angezeigt wird. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Hintergrundposition </span> </p> </td> 
   <td colname="col2"> <p> Positionieren Sie sie innerhalb des Bildsets, wenn CSS-Sprites verwendet werden. </p> <p>Siehe <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-viewer-20-customizingviewer/c-html5-video-viewer-20-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> von CSS-Sprites </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Diese Schaltfläche unterstützt sowohl die `state`-, `selected`- als auch `replay`-Attributauswahl, mit der verschiedene Skins auf verschiedene Schaltflächenzustände angewendet werden können. Insbesondere entspricht `selected='true'` dem „Play“-Zustand und `selected='false'` dem „Pause“-Zustand;
>
>Der Attributauswahl-`replay='true'` wird festgelegt, wenn das Video das Ende erreicht hat und wenn Sie auf die Schaltfläche klicken, wird die Wiedergabe von vorne gestartet.

Die QuickInfo der Schaltfläche kann lokalisiert werden. Siehe [Lokalisierung von Benutzeroberflächenelementen](../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/r-html5-video-viewer-20-localization.md#concept-1d5ca2d8480f4064a51eddba13940aad) für weitere Informationen.

## Beispiel {#section-e8caea0a303c425a8a637c2a47c06355}

So richten Sie eine Wiedergabe-/Pause-Schaltfläche ein, die 32 x 32 Pixel groß ist und sechs Pixel vom oberen und linken Rand der Steuerleiste entfernt positioniert ist. Und schließlich zeigt ein anderes Bild für jeden der vier verschiedenen Schaltflächenstatus an, wenn ausgewählt oder nicht ausgewählt.

```
.s7videoviewer .s7playpausebutton { 
top:6px; 
left:6px; 
width:32px; 
height:32px; 
} 
.s7videoviewer .s7playpausebutton[selected='true'][state='up'] { 
background-image:url(images/playBtn_up.png); 
} 
.s7videoviewer .s7playpausebutton[selected='true'][state='over'] {  
background-image:url(images/playBtn_over.png); 
} 
.s7videoviewer .s7playpausebutton[selected='true'][state='down'] {  
background-image:url(images/playBtn_down.png); 
} 
.s7videoviewer .s7playpausebutton[selected='true'][state='disabled'] { 
background-image:url(images/playBtn_disabled.png); 
} 
.s7videoviewer .s7playpausebutton[selected='false'][state='up'] {  
background-image:url(images/pauseBtn_up.png); 
} 
.s7videoviewer .s7playpausebutton[selected='false'][state='over'] {  
background-image:url(images/pauseBtn_over.png); 
} 
.s7videoviewer .s7playpausebutton[selected='false'][state='down'] {  
background-image:url(images/pauseBtn_down.png); 
} 
.s7videoviewer .s7playpausebutton[selected='false'][state='disabled'] {  
background-image:url(images/pauseBtn_disabled.png); } 
} 
.s7videoviewer .s7playpausebutton[selected='true'][replay='true'][state='up'] { 
background-image:url(images/replayBtn_up.png); 
} 
.s7videoviewer .s7playpausebutton[selected='true'][replay='true'][state='over'] {  
background-image:url(images/replayBtn_over.png); 
} 
.s7videoviewer .s7playpausebutton[selected='true'][replay='true'][state='down'] {  
background-image:url(images/replayBtn_down.png); 
} 
.s7videoviewer .s7playpausebutton[selected='true'][replay='true'][state='disabled'] { 
background-image:url(images/replayBtn_disabled.png); 
}
```
