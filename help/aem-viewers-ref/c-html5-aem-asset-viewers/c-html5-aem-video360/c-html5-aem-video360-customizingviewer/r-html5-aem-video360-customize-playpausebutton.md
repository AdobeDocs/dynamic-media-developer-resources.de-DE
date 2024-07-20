---
title: Schaltfläche "Wiedergabe/Pause"
description: Durch die Schaltfläche "Wiedergabe/Pause"wird der Videoinhalt vom Videoplayer wiedergegeben oder angehalten, wenn ein Benutzer darauf klickt.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,360 VR Video
role: Developer,User
exl-id: 5f8741a4-d286-4b2d-8a11-23bce119209a
source-git-commit: 14b9f6d3a01d47ca60710b19abfe11df1e927978
workflow-type: tm+mt
source-wordcount: '266'
ht-degree: 0%

---

# Schaltfläche &quot;Wiedergabe/Pause&quot;{#play-pause-button}

Durch die Schaltfläche &quot;Wiedergabe/Pause&quot;wird der Videoinhalt vom Videoplayer wiedergegeben oder angehalten, wenn ein Benutzer darauf klickt.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

Sie können die Schaltfläche durch CSS in der Größe, der Haut und der Position relativ zur sie enthaltenden Steuerleiste anpassen.

Der folgende CSS-Klassenselektor steuert das Erscheinungsbild der Schaltfläche:

```
.s7video360viewer .s7playpausebutton
```

## CSS-Eigenschaften der Wiedergabe/Pause-Schaltfläche {#css-properties-of-the-play-pause-button}

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> top </span> </p> </td> 
   <td colname="col2"> <p>Position vom oberen Rand, einschließlich Abstand. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> rechts </span> </p> </td> 
   <td colname="col2"> <p>Position vom rechten Rand, einschließlich Abstand. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> left </span> </p> </td> 
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
   <td colname="col1"> <p> <span class="codeph"> Höhe </span> </p> </td> 
   <td colname="col2"> <p>Höhe der Schaltfläche. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image </span> </p> </td> 
   <td colname="col2"> <p>Das Bild, das für einen bestimmten Schaltflächenstatus angezeigt wird. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p> Position innerhalb des Bildsprites, wenn CSS-Sprites verwendet werden. </p> <p>Siehe <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-customizingviewer/c-html5-aem-video360-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> CSS-Sprites </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Diese Schaltfläche unterstützt die Attributselektoren `state`, `selected` und `replay`, die verwendet werden können, um verschiedene Skins auf verschiedene Schaltflächenzustände anzuwenden. Insbesondere entspricht `selected='true'` dem Status &quot;play&quot;und `selected='false'` dem Status &quot;pause&quot;.
>
>Der Attributselektor &quot;`replay='true'`&quot; wird festgelegt, wenn das Video das Ende erreicht hat und die Auswahl der Schaltfläche die Wiedergabe von Anfang an neu startet.

Die QuickInfo der Schaltfläche kann lokalisiert werden. Weitere Informationen finden Sie unter [Lokalisierung von Benutzeroberflächenelementen](../../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-localization.md#concept-16262b8096474d6c9c018c3e99110dd1) .

**Beispiel** - Zum Einrichten einer Wiedergabe-/Pausenschaltfläche von 32 x 32 Pixel. Lassen Sie ihn sechs Pixel von der oberen und linken Kante der Steuerleiste platzieren. Schließlich zeigt ein anderes Bild für jeden der vier verschiedenen Schaltflächenstatus an, wenn diese ausgewählt sind oder nicht ausgewählt sind.

```
.s7video360viewer .s7playpausebutton { 
top:6px; 
left:6px; 
width:32px; 
height:32px; 
} 
.s7video360viewer .s7playpausebutton[selected='true'][state='up'] { 
background-image:url(images/playBtn_up.png); 
} 
.s7video360viewer .s7playpausebutton[selected='true'][state='over'] {  
background-image:url(images/playBtn_over.png); 
} 
.s7video360viewer .s7playpausebutton[selected='true'][state='down'] {  
background-image:url(images/playBtn_down.png); 
} 
.s7video360viewer .s7playpausebutton[selected='true'][state='disabled'] { 
background-image:url(images/playBtn_disabled.png); 
} 
.s7video360viewer .s7playpausebutton[selected='false'][state='up'] {  
background-image:url(images/pauseBtn_up.png); 
} 
.s7video360viewer .s7playpausebutton[selected='false'][state='over'] {  
background-image:url(images/pauseBtn_over.png); 
} 
.s7video360viewer .s7playpausebutton[selected='false'][state='down'] {  
background-image:url(images/pauseBtn_down.png); 
} 
.s7video360viewer .s7playpausebutton[selected='false'][state='disabled'] {  
background-image:url(images/pauseBtn_disabled.png); } 
} 
.s7video360viewer .s7playpausebutton[selected='true'][replay='true'][state='up'] { 
background-image:url(images/replayBtn_up.png); 
} 
.s7video360viewer .s7playpausebutton[selected='true'][replay='true'][state='over'] {  
background-image:url(images/replayBtn_over.png); 
} 
.s7video360viewer .s7playpausebutton[selected='true'][replay='true'][state='down'] {  
background-image:url(images/replayBtn_down.png); 
} 
.s7video360viewer .s7playpausebutton[selected='true'][replay='true'][state='disabled'] { 
background-image:url(images/replayBtn_disabled.png); 
}
```
