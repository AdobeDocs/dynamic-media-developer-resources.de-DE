---
description: Die Steuerleiste ist der rechteckige Bereich, der alle für den Video-Viewer verfügbaren Steuerelemente der Benutzeroberfläche enthält und darunter liegt, wie z. B. die Schaltfläche zum Abspielen/Anhalten, Lautstärkeregler usw.
seo-description: Die Steuerleiste ist der rechteckige Bereich, der alle für den Video-Viewer verfügbaren Steuerelemente der Benutzeroberfläche enthält und darunter liegt, wie z. B. die Schaltfläche zum Abspielen/Anhalten, Lautstärkeregler usw.
seo-title: Steuerungsleiste
solution: Experience Manager
title: Steuerungsleiste
uuid: 1fa90f7d-6b26-499d-8e6c-1cd80405aec0
feature: Dynamic Media Classic, Viewer, SDK/API, Interaktive Videos
role: Entwickler, Geschäftspraktiker
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '215'
ht-degree: 1%

---


# Steuerungsleiste{#control-bar}

Die Steuerleiste ist der rechteckige Bereich, der alle für den Video-Viewer verfügbaren Steuerelemente der Benutzeroberfläche enthält und darunter liegt, wie z. B. die Schaltfläche zum Abspielen/Anhalten, Lautstärkeregler usw.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

Die Steuerungsleiste nimmt immer die gesamte verfügbare Viewer-Breite ein. Sie können die Farbe, Höhe und vertikale Position mit CSS relativ zum Video-Viewer-Container ändern.

Der folgende CSS-Klassenselektor steuert das Erscheinungsbild der Steuerleiste:

```
.s7interactivevideoviewer .s7controlbar
```

## CSS-Eigenschaften der Steuerleiste {#css-properties-of-the-control-bar}

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Anfang </span> </p> </td> 
   <td colname="col2"> <p>Position vom oberen Rand, einschließlich Auffüllung. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> unten </span> </p> </td> 
   <td colname="col2"> <p> Position vom unteren Rand, einschließlich Auffüllung. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Höhe der Steuerleiste. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color  </span> </p> </td> 
   <td colname="col2"> <p>Hintergrundfarbe der Steuerleiste. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Beispiel {#section-e8caea0a303c425a8a637c2a47c06355}

So richten Sie einen Video-Viewer mit einer grauen Steuerungsleiste ein, die 30 Pixel hoch ist und sich oben im Video-Viewer-Container befindet.

```
.s7interactivevideoviewer .s7controlbar {  
position: absolute; 
top: 0px; 
height: 30px; 
background-color: rgb(51, 51, 51); 
}
```

