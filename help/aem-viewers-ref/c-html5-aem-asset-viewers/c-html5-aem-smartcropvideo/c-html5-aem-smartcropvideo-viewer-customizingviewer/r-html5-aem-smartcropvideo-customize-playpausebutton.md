---
title: Schaltfläche "Wiedergabe/Pause"
description: Durch die Schaltfläche "Wiedergabe/Pause"wird der Videoplayer für das smarte Zuschneiden wiedergegeben oder angehalten, wenn ein Benutzer darauf klickt.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop,Video
role: Developer,User
source-git-commit: 2dc7b92da6c73a328a82c50dc5a052a3351ee2dc
workflow-type: tm+mt
source-wordcount: '267'
ht-degree: 2%

---

# Schaltfläche &quot;Wiedergabe/Pause&quot;{#play-pause-button}

Durch die Schaltfläche &quot;Wiedergabe/Pause&quot;wird der Videoinhalt vom Videoplayer wiedergegeben oder angehalten, wenn ein Benutzer darauf klickt.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

Sie können die Schaltfläche durch CSS in der Größe, der Haut und der Position relativ zur sie enthaltenden Steuerleiste anpassen.

Der folgende CSS-Klassenselektor steuert das Erscheinungsbild der Schaltfläche:

```
.s7smartcropvideoviewer .s7playpausebutton
```

## CSS-Eigenschaften der Wiedergabe/Pause-Schaltfläche {#css-properties-of-the-play-pause-button}

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Anfang </span> </p> </td> 
   <td colname="col2"> <p>Position vom oberen Rand, einschließlich Abstand. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> rechts </span> </p> </td> 
   <td colname="col2"> <p>Position vom rechten Rand, einschließlich Abstand. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> links </span> </p> </td> 
   <td colname="col2"> <p>Position vom linken Rand, einschließlich Abstand. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> unten </span> </p> </td> 
   <td colname="col2"> <p> Position vom unteren Rand, einschließlich Abstand. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Breite der Schaltfläche. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Höhe der Schaltfläche. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image </span> </p> </td> 
   <td colname="col2"> <p>Das Bild, das für einen bestimmten Schaltflächenstatus angezeigt wird. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p> Position innerhalb des Bildsprites, wenn CSS-Sprites verwendet werden. </p> <p>Siehe <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-smartcropvideo/c-html5-aem-smartcropvideo-viewer-customizingviewer/c-html5-aem-smartcropvideo-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> CSS-Sprites </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Diese Schaltfläche unterstützt beide `state`, `selected`und `replay` -Attributselektoren, die verwendet werden können, um verschiedene Skins auf unterschiedliche Schaltflächenzustände anzuwenden. Insbesondere `selected='true'` entspricht dem Status &quot;play&quot;und `selected='false'` entspricht dem Status &quot;pause&quot;;
>
>Die Attributauswahl `replay='true'` festgelegt ist, wenn das Video das Ende erreicht hat und die Auswahl der Schaltfläche die Wiedergabe von Anfang an neu startet.

Die QuickInfo der Schaltfläche kann lokalisiert werden. Siehe [Lokalisierung der Elemente der Benutzeroberfläche](../../../c-html5-aem-asset-viewers/c-html5-aem-smartcropvideo/r-html5-aem-smartcropvideo-viewer-localization.md#concept-1d5ca2d8480f4064a51eddba13940aad) für weitere Informationen.

## Beispiel {#section-e8caea0a303c425a8a637c2a47c06355}

So richten Sie eine Wiedergabe-/Pause-Schaltfläche mit einer Größe von 32 x 32 Pixel ein. Lassen Sie sie sechs Pixel von der oberen und linken Kante der Steuerleiste entfernt. Zeigen Sie schließlich ein anderes Bild für jeden der vier Schaltflächenstatus an, wenn diese ausgewählt sind oder nicht ausgewählt sind.

```
.s7smartcropvideoviewer .s7playpausebutton { 
top:6px; 
left:6px; 
width:32px; 
height:32px; 
} 
.s7smartcropvideoviewer .s7playpausebutton[selected='true'][state='up'] { 
background-image:url(images/playBtn_up.png); 
} 
.s7smartcropvideoviewer .s7playpausebutton[selected='true'][state='over'] {  
background-image:url(images/playBtn_over.png); 
} 
.s7smartcropvideoviewer .s7playpausebutton[selected='true'][state='down'] {  
background-image:url(images/playBtn_down.png); 
} 
.s7smartcropvideoviewer .s7playpausebutton[selected='true'][state='disabled'] { 
background-image:url(images/playBtn_disabled.png); 
} 
.s7smartcropvideoviewer .s7playpausebutton[selected='false'][state='up'] {  
background-image:url(images/pauseBtn_up.png); 
} 
.s7smartcropvideoviewer .s7playpausebutton[selected='false'][state='over'] {  
background-image:url(images/pauseBtn_over.png); 
} 
.s7smartcropvideoviewer .s7playpausebutton[selected='false'][state='down'] {  
background-image:url(images/pauseBtn_down.png); 
} 
.s7smartcropvideoviewer .s7playpausebutton[selected='false'][state='disabled'] {  
background-image:url(images/pauseBtn_disabled.png); } 
} 
.s7smartcropvideoviewer .s7playpausebutton[selected='true'][replay='true'][state='up'] { 
background-image:url(images/replayBtn_up.png); 
} 
.s7smartcropvideoviewer .s7playpausebutton[selected='true'][replay='true'][state='over'] {  
background-image:url(images/replayBtn_over.png); 
} 
.s7smartcropvideoviewer .s7playpausebutton[selected='true'][replay='true'][state='down'] {  
background-image:url(images/replayBtn_down.png); 
} 
.s7smartcropvideoviewer .s7playpausebutton[selected='true'][replay='true'][state='disabled'] { 
background-image:url(images/replayBtn_disabled.png); 
}
```
