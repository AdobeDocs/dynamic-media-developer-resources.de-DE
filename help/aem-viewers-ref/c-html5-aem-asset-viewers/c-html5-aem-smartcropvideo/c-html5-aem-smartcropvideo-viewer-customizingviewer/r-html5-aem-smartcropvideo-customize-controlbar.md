---
title: Steuerleiste
description: Die Steuerleiste ist der rechteckige Bereich, der alle für den Viewer für smartes Zuschneiden verfügbaren UI-Steuerelemente (z. B. die Steuerelemente Wiedergabe/Pause und Lautstärke) enthält und sich hinter diesen befindet.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop,Video
role: Developer,User
exl-id: 8ea06e0a-705d-436a-9393-75a36381cba6
source-git-commit: 1aa8be858b0ba8ec9b99753d43c202b35ed58c30
workflow-type: tm+mt
source-wordcount: '177'
ht-degree: 0%

---

# Steuerleiste{#control-bar}

Die Steuerleiste ist der rechteckige Bereich, der alle für den Viewer für smartes Zuschneiden verfügbaren UI-Steuerelemente (z. B. die Steuerelemente Wiedergabe/Pause und Lautstärke) enthält und sich hinter diesen befindet.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

Die Steuerleiste nimmt immer die gesamte verfügbare Viewer-Breite ein. Es ist möglich, Farbe, Höhe und vertikale Position durch CSS relativ zum Viewer-Container für das intelligente Zuschneiden-Video zu ändern.

Der folgende CSS-Klassenselektor steuert das Erscheinungsbild der Steuerleiste:

```
.s7smartcropvideoviewer .s7controlbar
```

## CSS-Eigenschaften der Steuerleiste {#css-properties-of-the-control-bar}

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Top-</span> </p> </td> 
   <td colname="col2"> <p>Position ab dem oberen Rahmen, einschließlich Auffüllung. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> untere </span> </p> </td> 
   <td colname="col2"> <p> Position ab dem unteren Rand, einschließlich Abstand. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Höhe </span> </p> </td> 
   <td colname="col2"> <p>Höhe des Steuerstabs. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">-</span> </p> </td> 
   <td colname="col2"> <p>Hintergrundfarbe der Steuerleiste. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Beispiel {#section-e8caea0a303c425a8a637c2a47c06355}

So richten Sie einen Smart Crop Video-Viewer mit einer grauen Steuerleiste ein, die 30 Pixel hoch ist und sich oben im Viewer-Container für Smart Crop-Videos befindet.

```
.s7smartcropvideoviewer .s7controlbar {  
position: absolute; 
top: 0px; 
height: 30px; 
background-color: rgb(51, 51, 51); 
}
```
