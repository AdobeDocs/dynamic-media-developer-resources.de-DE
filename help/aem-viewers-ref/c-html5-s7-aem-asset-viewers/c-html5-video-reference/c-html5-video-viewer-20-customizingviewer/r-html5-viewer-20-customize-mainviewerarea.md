---
title: Hauptanzeige-Bereich
description: Der Hauptansichtsbereich wird durch das Video belegt. Normalerweise wird sie an den verfügbaren Gerätebildschirm angepasst, wenn keine Größe angegeben ist.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Video
role: Developer,User
exl-id: 7d1379c1-7746-4f61-92df-e8ac4ab7d506
source-git-commit: ceb9483f67a19d969ecbbd01cede11f3dae86467
workflow-type: tm+mt
source-wordcount: '103'
ht-degree: 0%

---

# Hauptanzeige-Bereich{#main-viewer-area}

Der Hauptansichtsbereich wird durch das Video belegt. Normalerweise wird sie an den verfügbaren Gerätebildschirm angepasst, wenn keine Größe angegeben ist.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

Der folgende CSS-Klassenselektor steuert das Erscheinungsbild des Anzeigebereichs:

```
.s7videoviewer 
```

## CSS-Eigenschaften des Haupt-Viewer-Bereichs {#css-properties-of-the-main-viewer-area}

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Viewer-Breite. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Höhe </span> </p> </td> 
   <td colname="col2"> <p>Viewer-Höhe. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p> Hintergrundfarbe im hexadezimalen Format. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Beispiel {#section-e8caea0a303c425a8a637c2a47c06355}

So richten Sie einen Video-Viewer mit weißem Hintergrund (#FFFFFF) ein und machen seine Größe 512 x 288 Pixel groß:

```
.s7videoviewer { 
 background-color: #FFFFFF; 
 width: 512px; 
 height: 288px;  
}
```
