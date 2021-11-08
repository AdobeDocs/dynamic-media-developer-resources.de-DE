---
title: Kontrollleiste
description: Die Steuerleiste ist der rechteckige Bereich, der alle für den Smart Crop Video-Viewer verfügbaren UI-Steuerelemente enthält und sich darunter befindet, wie z. B. die Wiedergabe-/Pause-Schaltfläche und die Lautstärkeregler.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop,Video
role: Developer,User
exl-id: null
source-git-commit: 254d1ef05c73e19618b7ad4743c6a242fa177929
workflow-type: tm+mt
source-wordcount: '176'
ht-degree: 2%

---

# Kontrollleiste{#control-bar}

Die Steuerleiste ist der rechteckige Bereich, der alle für den Smart Crop Video-Viewer verfügbaren UI-Steuerelemente enthält und sich darunter befindet, wie z. B. die Wiedergabe-/Pause-Schaltfläche und die Lautstärkeregler.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

Die Steuerleiste nimmt immer die gesamte verfügbare Viewer-Breite ein. Es ist möglich, die Farbe, Höhe und vertikale Position durch CSS in Bezug auf den Viewer-Container für Smart Crop-Video zu ändern.

Der folgende CSS-Klassenselektor steuert das Erscheinungsbild der Steuerleiste:

```
.s7smartcropvideoviewer .s7controlbar
```

## CSS-Eigenschaften der Steuerleiste {#css-properties-of-the-control-bar}

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Anfang </span> </p> </td> 
   <td colname="col2"> <p>Position vom oberen Rand, einschließlich Abstand. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> unten </span> </p> </td> 
   <td colname="col2"> <p> Position vom unteren Rand, einschließlich Abstand. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Höhe der Steuerleiste. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p>Hintergrundfarbe der Steuerleiste. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Beispiel {#section-e8caea0a303c425a8a637c2a47c06355}

Um einen Viewer für smartes Zuschneiden von Videos mit einer grauen Steuerleiste einzurichten, die 30 Pixel groß ist und sich oben im Viewer-Container für Smart Crop-Video befindet.

```
.s7smartcropvideoviewer .s7controlbar {  
position: absolute; 
top: 0px; 
height: 30px; 
background-color: rgb(51, 51, 51); 
}
```
