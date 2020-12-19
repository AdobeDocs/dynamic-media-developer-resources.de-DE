---
description: Die Steuerleiste ist der rechteckige Bereich, der alle für den Video-Viewer verfügbaren Steuerelemente der Benutzeroberfläche enthält und darunter liegt, wie z. B. die Schaltfläche zum Abspielen/Anhalten, Lautstärkeregler usw.
seo-description: Die Steuerleiste ist der rechteckige Bereich, der alle für den Video-Viewer verfügbaren Steuerelemente der Benutzeroberfläche enthält und darunter liegt, wie z. B. die Schaltfläche zum Abspielen/Anhalten, Lautstärkeregler usw.
seo-title: Steuerungsleiste
solution: Experience Manager
title: Steuerungsleiste
topic: Dynamic media
uuid: 7b7dccb3-6c64-4342-aac7-82c769561902
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef
workflow-type: tm+mt
source-wordcount: '182'
ht-degree: 1%

---


# Steuerungsleiste{#control-bar}

Die Steuerleiste ist der rechteckige Bereich, der alle für den Video-Viewer verfügbaren Steuerelemente der Benutzeroberfläche enthält und darunter liegt, wie z. B. die Schaltfläche zum Abspielen/Anhalten, Lautstärkeregler usw.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

Die Steuerungsleiste nimmt immer die gesamte verfügbare Viewer-Breite ein. Sie können die Farbe, Höhe und vertikale Position mit CSS relativ zum Video-Viewer-Container ändern.

Der folgende CSS-Klassenselektor steuert das Erscheinungsbild der Steuerleiste:

```
.s7mixedmediaviewer .s7controlbar
```

## CSS-Eigenschaften der Steuerleiste {#css-properties-of-the-control-bar}

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
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

Um einen Viewer für gemischte Medien mit einer grauen Steuerungsleiste einzurichten, die 30 Pixel hoch ist.

```
.s7mixedmediaviewer .s7controlbar {  
height: 30px; 
background-color: rgb(51, 51, 51); 
}
```

