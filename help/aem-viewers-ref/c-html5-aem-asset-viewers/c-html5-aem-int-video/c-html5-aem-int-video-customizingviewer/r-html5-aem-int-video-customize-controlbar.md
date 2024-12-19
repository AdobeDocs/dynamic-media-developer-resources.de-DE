---
title: Steuerleiste
description: Die Steuerleiste ist der rechteckige Bereich, der alle Steuerelemente der Benutzeroberfläche enthält, die für den Video-Viewer verfügbar sind, z. B. die Steuerelemente Wiedergabe/Pause und Lautstärke, und sich hinter diesen befindet.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: 685fad5a-a75a-4c0c-9038-de99d814f4be
source-git-commit: 67e12fae514341137e4218ea950f34da0d9997f3
workflow-type: tm+mt
source-wordcount: '173'
ht-degree: 0%

---

# Steuerleiste{#control-bar}

Die Steuerleiste ist der rechteckige Bereich, der alle Steuerelemente der Benutzeroberfläche enthält, die für den Video-Viewer verfügbar sind, z. B. die Steuerelemente Wiedergabe/Pause und Lautstärke, und sich hinter diesen befindet.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

Die Steuerleiste nimmt immer die gesamte verfügbare Viewer-Breite ein. Es ist möglich, Farbe, Höhe und vertikale Position durch CSS relativ zum Video-Viewer-Container zu ändern.

Der folgende CSS-Klassenselektor steuert das Erscheinungsbild der Steuerleiste:

```
.s7interactivevideoviewer .s7controlbar
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

So richten Sie einen Video-Viewer mit einer grauen Steuerleiste ein, die 30 Pixel hoch ist und sich oben im Video-Viewer-Container befindet.

```
.s7interactivevideoviewer .s7controlbar {  
position: absolute; 
top: 0px; 
height: 30px; 
background-color: rgb(51, 51, 51); 
}
```
