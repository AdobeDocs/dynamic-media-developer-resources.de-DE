---
description: Die Steuerleiste ist der rechteckige Bereich, der alle für den Video-Viewer verfügbaren Steuerelemente der Benutzeroberfläche enthält und darunter liegt, wie z. B. die Schaltfläche zum Abspielen/Anhalten, Lautstärkeregler usw.
seo-description: Die Steuerleiste ist der rechteckige Bereich, der alle für den Video-Viewer verfügbaren Steuerelemente der Benutzeroberfläche enthält und darunter liegt, wie z. B. die Schaltfläche zum Abspielen/Anhalten, Lautstärkeregler usw.
seo-title: Steuerungsleiste
solution: Experience Manager
title: Steuerungsleiste
topic: Dynamic media
uuid: 328e34f1-9e60-4056-9a8a-e9292fb65605
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef
workflow-type: tm+mt
source-wordcount: '207'
ht-degree: 1%

---


# Steuerungsleiste{#control-bar}

Die Steuerleiste ist der rechteckige Bereich, der alle für den Video-Viewer verfügbaren Steuerelemente der Benutzeroberfläche enthält und darunter liegt, wie z. B. die Schaltfläche zum Abspielen/Anhalten, Lautstärkeregler usw.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

Die Steuerungsleiste nimmt immer die gesamte verfügbare Viewer-Breite ein. Sie können die Farbe, Höhe und vertikale Position mit CSS relativ zum Video-Viewer-Container ändern.

Der folgende CSS-Klassenselektor steuert das Erscheinungsbild der Steuerleiste:

```
.s7video360viewer .s7controlbar
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

**Beispiel** : Zum Einrichten eines Video-Viewers mit einer grauen Steuerungsleiste, die 30 Pixel hoch und oben im Video-Viewer-Container liegt.

```
.s7video360viewer .s7controlbar {  
position: absolute; 
top: 0px; 
height: 30px; 
background-color: rgb(51, 51, 51); 
}
```

