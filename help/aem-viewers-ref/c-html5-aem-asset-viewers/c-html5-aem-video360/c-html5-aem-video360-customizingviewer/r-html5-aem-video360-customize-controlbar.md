---
title: Kontrollleiste
description: Die Steuerleiste ist der rechteckige Bereich, der alle für den Video-Viewer verfügbaren Steuerelemente der Benutzeroberfläche enthält und sich darunter befindet, wie z. B. die Wiedergabe-/Pause-Schaltfläche und Lautstärkeregler.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,360 VR Video
role: Developer,User
exl-id: 06078310-8aeb-449f-919a-ce88ddc8c4b3
source-git-commit: 24667a5ebab54ba22c4a3f6b52d19d7a31a93576
workflow-type: tm+mt
source-wordcount: '169'
ht-degree: 0%

---

# Kontrollleiste{#control-bar}

Die Steuerleiste ist der rechteckige Bereich, der alle für den Video-Viewer verfügbaren Steuerelemente der Benutzeroberfläche enthält und sich darunter befindet, wie z. B. die Wiedergabe-/Pause-Schaltfläche und Lautstärkeregler.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

Die Steuerleiste nimmt immer die gesamte verfügbare Viewer-Breite ein. Es ist möglich, die Farbe, Höhe und vertikale Position durch CSS in Bezug auf den Video-Viewer-Container zu ändern.

Der folgende CSS-Klassenselektor steuert das Erscheinungsbild der Steuerleiste:

```
.s7video360viewer .s7controlbar
```

## CSS-Eigenschaften der Steuerleiste {#css-properties-of-the-control-bar}

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> top </span> </p> </td> 
   <td colname="col2"> <p>Position vom oberen Rand, einschließlich Abstand. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> unten </span> </p> </td> 
   <td colname="col2"> <p> Position vom unteren Rand, einschließlich Abstand. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Höhe </span> </p> </td> 
   <td colname="col2"> <p>Höhe der Steuerleiste. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p>Hintergrundfarbe der Steuerleiste. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Beispiel** - Um einen Video-Viewer mit einer grauen Steuerleiste einzurichten, die 30 Pixel groß ist und sich oben im Video-Viewer-Container befindet.

```
.s7video360viewer .s7controlbar {  
position: absolute; 
top: 0px; 
height: 30px; 
background-color: rgb(51, 51, 51); 
}
```
