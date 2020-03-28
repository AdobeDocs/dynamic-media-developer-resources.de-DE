---
description: Durch die Schaltfläche "Abspielen/Anhalten"wird der Videoinhalt vom Videoplayer abgespielt oder angehalten, wenn der Benutzer darauf klickt.
seo-description: Durch die Schaltfläche "Abspielen/Anhalten"wird der Videoinhalt vom Videoplayer abgespielt oder angehalten, wenn der Benutzer darauf klickt.
seo-title: Schaltfläche "Abspielen/Anhalten"
solution: Experience Manager
title: Schaltfläche "Abspielen/Anhalten"
topic: Dynamic media
uuid: d6dd795d-f608-4304-8221-251d0a082421
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef

---


# Schaltfläche &quot;Abspielen/Anhalten&quot;{#play-pause-button}

Durch die Schaltfläche &quot;Abspielen/Anhalten&quot;wird der Videoinhalt vom Videoplayer abgespielt oder angehalten, wenn der Benutzer darauf klickt.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

Sie können die Größe, Skin und Position der Schaltfläche relativ zur Steuerungsleiste, in der sie enthalten ist, mithilfe von CSS festlegen.

Der folgende CSS-Klassenselektor steuert das Aussehen der Schaltfläche:

```
.s7interactivevideoviewer .s7playpausebutton
```

## CSS-Eigenschaften der Schaltfläche &quot;Abspielen/Anhalten&quot; {#css-properties-of-the-play-pause-button}

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Anfang </span> </p> </td> 
   <td colname="col2"> <p>Position vom oberen Rand, einschließlich Auffüllung. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> rechts </span> </p> </td> 
   <td colname="col2"> <p>Position vom rechten Rand, einschließlich Auffüllung. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> links </span> </p> </td> 
   <td colname="col2"> <p>Position vom linken Rand, einschließlich Auffüllung. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> unten </span> </p> </td> 
   <td colname="col2"> <p> Position vom unteren Rand, einschließlich Auffüllung. </p> </td> 
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
   <td colname="col2"> <p> Position innerhalb des Bildausschnitt, wenn CSS-Sprites verwendet werden. </p> <p>Siehe <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-customizingviewer/c-html5-aem-int-video-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> CSS-Sprites </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Diese Schaltfläche unterstützt sowohl die `state`-, `selected`- als auch die `replay` Attributauswahl, mit der verschiedene Skins auf verschiedene Schaltflächenzustände angewendet werden können. Dies `selected='true'` entspricht insbesondere dem Status &quot;play&quot;und `selected='false'` dem Status &quot;pause&quot;;
>
>`replay='true'` eingestellt ist, wenn das Video das Ende erreicht hat und wenn auf die Schaltfläche geklickt wird, beginnt die Wiedergabe von Anfang an.

Die QuickInfo für Schaltflächen kann lokalisiert werden. Weitere Informationen finden Sie unter [Lokale Anpassung der Elemente](../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) der Benutzeroberfläche.

## Beispiel {#section-e8caea0a303c425a8a637c2a47c06355}

So richten Sie eine Wiedergabe-/Pause-Schaltfläche mit 32 x 32 Pixeln ein Es wird sechs Pixel von der oberen und linken Kante der Steuerleiste entfernt und zeigt ein anderes Bild für jeden der vier verschiedenen Schaltflächenzustände an, wenn diese ausgewählt sind oder nicht.

```
.s7interactivevideoviewer .s7playpausebutton { 
top:6px; 
left:6px; 
width:32px; 
height:32px; 
} 
.s7interactivevideoviewer .s7playpausebutton[selected='true'][state='up'] { 
background-image:url(images/playBtn_up.png); 
} 
.s7interactivevideoviewer .s7playpausebutton[selected='true'][state='over'] {  
background-image:url(images/playBtn_over.png); 
} 
.s7interactivevideoviewer .s7playpausebutton[selected='true'][state='down'] {  
background-image:url(images/playBtn_down.png); 
} 
.s7interactivevideoviewer .s7playpausebutton[selected='true'][state='disabled'] { 
background-image:url(images/playBtn_disabled.png); 
} 
.s7interactivevideoviewer .s7playpausebutton[selected='false'][state='up'] {  
background-image:url(images/pauseBtn_up.png); 
} 
.s7interactivevideoviewer .s7playpausebutton[selected='false'][state='over'] {  
background-image:url(images/pauseBtn_over.png); 
} 
.s7interactivevideoviewer .s7playpausebutton[selected='false'][state='down'] {  
background-image:url(images/pauseBtn_down.png); 
} 
.s7interactivevideoviewer .s7playpausebutton[selected='false'][state='disabled'] {  
background-image:url(images/pauseBtn_disabled.png); } 
} 
.s7interactivevideoviewer .s7playpausebutton[selected='true'][replay='true'][state='up'] { 
background-image:url(images/replayBtn_up.png); 
} 
.s7interactivevideoviewer .s7playpausebutton[selected='true'][replay='true'][state='over'] {  
background-image:url(images/replayBtn_over.png); 
} 
.s7interactivevideoviewer .s7playpausebutton[selected='true'][replay='true'][state='down'] {  
background-image:url(images/replayBtn_down.png); 
} 
.s7interactivevideoviewer .s7playpausebutton[selected='true'][replay='true'][state='disabled'] { 
background-image:url(images/replayBtn_disabled.png); 
}
```

