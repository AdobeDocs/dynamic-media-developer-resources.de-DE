---
description: Das Steuerelement für veränderliche Lautstärke wird zunächst als Schaltfläche angezeigt, mit der der Benutzer den Videoplayer-Sound stummschalten oder deaktivieren kann.
solution: Experience Manager
title: Wechselbares Volumen
feature: Dynamic Media Classic, Viewer, SDK/API, Video
role: Entwickler, Geschäftspraktiker
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '536'
ht-degree: 2%

---


# Mutables Volume{#mutable-volume}

Das Steuerelement für veränderliche Lautstärke wird zunächst als Schaltfläche angezeigt, mit der der Benutzer den Videoplayer-Sound stummschalten oder deaktivieren kann.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

Wenn ein Benutzer den Mauszeiger über die Schaltfläche bewegt, wird ein Schieberegler angezeigt, mit dem der Benutzer die Lautstärke einstellen kann. Das veränderliche Lautstärkeregler kann relativ zur zugehörigen Steuerleiste durch CSS skaliert, geschliffen und positioniert werden.

Das Aussehen des Bereichs für veränderbare Lautstärke wird mit der folgenden CSS-Klassenauswahl gesteuert:

```
.s7videoviewer .s7mutablevolume
```

**CSS-Eigenschaften des veränderlichen Volumens**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Anfang </span> </p> </td> 
   <td colname="col2"> <p> Position vom oberen Rand, einschließlich Auffüllung. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> rechts </span> </p> </td> 
   <td colname="col2"> <p> Position vom rechten Rand, einschließlich Auffüllung. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p> Die Breite der Steuerung des veränderlichen Volumens. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Die Höhe der Steuerung des veränderlichen Volumens. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color  </span> </p> </td> 
   <td colname="col2"> <p> Die Farbe der Lautstärkeregelung. </p> </td> 
  </tr> 
 </tbody> 
</table>

Die Darstellung der Schaltflächen &quot;Stummschalten/Unmutieren&quot;wird mit der folgenden CSS-Klassenauswahl gesteuert:

```
.s7videoviewer .s7mutablevolume .s7mutebutton
```

Sie können das Hintergrundbild für jeden Schaltflächenstatus steuern. Die Größe der Schaltfläche wird von der Größe der Lautstärkeregelung übernommen.

**CSS-Eigenschaften des Schaltflächenbilds**

<table id="table_46903DCACF314426B67783167ADF7715"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image  </span> </p> </td> 
   <td colname="col2"> <p> Das für einen Schaltflächenstatus angezeigte Bild. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position  </span> </p> </td> 
   <td colname="col2"> <p> Position innerhalb des Bildausschnitt, wenn CSS-Sprites verwendet werden. </p> <p>Siehe <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-viewer-20-customizingviewer/c-html5-video-viewer-20-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> CSS-Sprites </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Diese Schaltfläche unterstützt sowohl die Attributselektoren `state` als auch `selected`, die verwendet werden können, um verschiedene Skins auf verschiedene Schaltflächenzustände anzuwenden. Insbesondere entspricht `selected='true'` dem Status &quot;muted&quot;und `selected='false'` dem Status &quot;unmuted&quot;.

Der Bereich für die vertikale Lautstärkenleiste wird mit der folgenden CSS-Klassenauswahl gesteuert:

```
.s7videoviewer .s7mutablevolume .s7verticalvolume
```

**CSS-Eigenschaften des Bereichs der vertikalen Lautstärkenleiste**

<table id="table_966826FB81114362A8D81D1EED38D512"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color  </span> </p> </td> 
   <td colname="col2"> <p> Die Hintergrundfarbe des vertikalen Volumens. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width  </span> </p> </td> 
   <td colname="col2"> <p> Die Breite des vertikalen Volumens. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height  </span> </p> </td> 
   <td colname="col2"> <p> Die Höhe des vertikalen Volumens. </p> </td> 
  </tr> 
 </tbody> 
</table>

Die Gleise innerhalb der vertikalen Lautstärkeregelung wird mit den folgenden CSS-Klassenselektoren gesteuert:

```
.s7videoviewer .s7mutablevolume .s7verticalvolume .s7track 
.s7videoviewer .s7mutablevolume .s7verticalvolume .s7filledtrack
```

**CSS-Eigenschaften der Steuerung des vertikalen Volumens**

<table id="table_21E9AD3FBC8C4437BA02E5CD1BF7E831"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color  </span> </p> </td> 
   <td colname="col2"> <p> Die Hintergrundfarbe der Steuerung des vertikalen Volumens. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width  </span> </p> </td> 
   <td colname="col2"> <p>Breite der Steuerung des vertikalen Volumens. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height  </span> </p> </td> 
   <td colname="col2"> <p>Höhe der vertikalen Lautstärkeregelung. </p> </td> 
  </tr> 
 </tbody> 
</table>

Der vertikale Lautstärkeregler wird mit der folgenden CSS-Klassenauswahl gesteuert:

```
.s7videoviewer .s7mutablevolume .s7verticalvolume .s7knob
```

**CSS-Eigenschaften des Reglers für die Steuerung der vertikalen Lautstärke**

<table id="table_709D64AF815341A5B50ED72CCB350F2E"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image  </span> </p> </td> 
   <td colname="col2"> <p> Grafik mit vertikalem Lautstärkeregler. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position  </span> </p> </td> 
   <td colname="col2"> <p> Position innerhalb des Bildausschnitt, wenn CSS-Sprites verwendet werden. </p> <p>Siehe <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-viewer-20-customizingviewer/c-html5-video-viewer-20-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> CSS-Sprites </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width  </span> </p> </td> 
   <td colname="col2"> <p>Breite des Reglers für die vertikale Lautstärke. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height  </span> </p> </td> 
   <td colname="col2"> <p>Höhe des vertikalen Lautstärkereglers. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> links </span> </p> </td> 
   <td colname="col2"> <p>Horizontale Position des vertikalen Lautstärkereglers. </p> </td> 
  </tr> 
 </tbody> 
</table>

Die QuickInfo für Schaltflächen kann lokalisiert werden. Weitere Informationen finden Sie unter [Lokale Anpassung der Elemente der Benutzeroberfläche](../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/r-html5-video-viewer-20-localization.md#concept-1d5ca2d8480f4064a51eddba13940aad).

## Beispiele {#section-e8caea0a303c425a8a637c2a47c06355}

Um eine Stummschaltfläche mit 32 x 32 Pixel und einer Position von 6 Pixel von oben und 38 Pixel von der rechten Kante der Steuerleiste einzurichten. Zeigt ein anderes Bild für jeden der vier verschiedenen Schaltflächenzustände an, wenn diese ausgewählt sind oder nicht.

```
.s7videoviewer .s7mutablevolume { 
top:6px; 
right:38px; 
width:32px; 
height:32px; 
} 
.s7videoviewer .s7mutablevolume .s7mutebutton[selected='true'][state='up'] { 
background-image:url(images/mute_up.png); 
} 
.s7videoviewer .s7mutablevolume .s7mutebutton[selected='true'][state='over'] { 
background-image:url(images/mute_over.png); 
} 
.s7videoviewer .s7mutablevolume .s7mutebutton[selected='true'][state='down'] { 
background-image:url(images/mute_down.png); 
} 
.s7videoviewer .s7mutablevolume .s7mutebutton[selected='true'][state='disabled'] { 
background-image:url(images/mute_disabled.png); 
} 
.s7videoviewer .s7mutablevolume .s7mutebutton[selected='false'][state='up'] { 
background-image:url(images/unmute_up.png); 
} 
.s7videoviewer .s7mutablevolume .s7mutebutton[selected='false'][state='over'] { 
background-image:url(images/unmute_over.png); 
} 
.s7videoviewer .s7mutablevolume .s7mutebutton[selected='false'][state='down'] { 
background-image:url(images/unmute_down.png); 
} 
.s7videoviewer .s7mutablevolume .s7mutebutton[selected='false'][state='disabled'] { 
background-image:url(images/unmute_disabled.png); 
}
```

Im Folgenden sehen Sie ein Beispiel dafür, wie Sie den Lautstärkeregler innerhalb der Steuerung für veränderliche Lautstärke gestalten können.

```
.s7videoviewer .s7mutablevolume .s7verticalvolume { 
width:36px; 
height:83px; 
left:0px; 
background-color:#dddddd; 
} 
.s7videoviewer .s7mutablevolume .s7verticalvolume .s7track { 
top:11px; 
left:14px; 
width:10px; 
height:63px; 
background-color:#666666; 
} 
.s7videoviewer .s7mutablevolume .s7verticalvolume .s7filledtrack { 
width:10px; 
background-color:#ababab; 
} 
.s7videoviewer .s7mutablevolume .s7verticalvolume .s7knob { 
width:18px; 
height:10px; 
left:9px; 
background-image:url(images/volumeKnob.png); 
}
```

Im Folgenden sehen Sie ein Beispiel dafür, wie Sie den Videoplayer so anpassen können, dass der Ton während der Wiedergabe deaktiviert wird. hinzufügen den folgenden Code in den Einbettungscode des Viewers:

```
                "handlers":{ 
                    "initComplete":function() { 
                        videoViewer.getComponent("mutableVolume").setPosition(0); 
                        videoViewer.getComponent("mutableVolume").deactivate(); 
                    } 
                }
```

Im obigen Codebeispiel wird die Lautstärke auf `0` für die `mutableVolume`-Komponente eingestellt. Dann wird dieselbe Komponente deaktiviert, sodass sie vom Endbenutzer nicht verwendet werden kann.
