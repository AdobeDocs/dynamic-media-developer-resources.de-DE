---
description: Das Steuerelement für veränderliche Lautstärke wird zunächst als Schaltfläche angezeigt, mit der ein Benutzer den Video-Player-Ton stummschalten oder deaktivieren kann.
solution: Experience Manager
title: Veränderliches Volumen
feature: Dynamic Media Classic,Viewer,SDK/API,interaktive Videos
role: Developer,User
exl-id: ecef47c1-e659-4930-bfb1-cc5e7c059094
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '479'
ht-degree: 2%

---

# Veränderliches Volumen{#mutable-volume}

Das Steuerelement für veränderliche Lautstärke wird zunächst als Schaltfläche angezeigt, mit der ein Benutzer den Video-Player-Ton stummschalten oder deaktivieren kann.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

Wenn ein Benutzer über die Schaltfläche blättert, wird ein Regler angezeigt, mit dem der Benutzer die Lautstärke einstellen kann. Die veränderliche Lautstärkeregelung kann durch CSS relativ zur sie enthaltenden Steuerleiste skaliert, gehärtet und positioniert werden.

Das Erscheinungsbild des veränderlichen Lautstärkeregments wird mit der folgenden CSS-Klassenauswahl gesteuert:

```
.s7interactivevideoviewer .s7mutablevolume
```

**CSS-Eigenschaften des veränderlichen Volumens**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Anfang </span> </p> </td> 
   <td colname="col2"> <p> Position vom oberen Rand, einschließlich Abstand. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> rechts </span> </p> </td> 
   <td colname="col2"> <p> Position vom rechten Rand, einschließlich Abstand. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p> Die Breite der Steuerung des veränderlichen Volumens. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Die Höhe der veränderlichen Lautstärkeregelung. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color  </span> </p> </td> 
   <td colname="col2"> <p> Die Farbe der veränderlichen Lautstärkeregelung. </p> </td> 
  </tr> 
 </tbody> 
</table>

Das Aussehen der Schaltfläche zum Stummschalten/Unmutieren wird mit der folgenden CSS-Klassenauswahl gesteuert:

```
.s7interactivevideoviewer .s7mutablevolume .s7mutebutton
```

Sie können das Hintergrundbild für jeden Schaltflächenstatus steuern. Die Größe der Schaltfläche wird von der Größe des Lautstärkereglers übernommen.

**CSS-Eigenschaften des Schaltflächenbilds**

<table id="table_46903DCACF314426B67783167ADF7715"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image  </span> </p> </td> 
   <td colname="col2"> <p> Das für einen bestimmten Schaltflächenstatus angezeigte Bild. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position  </span> </p> </td> 
   <td colname="col2"> <p> Position innerhalb des Bildsprites, wenn CSS-Sprites verwendet werden. </p> <p>Siehe <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-customizingviewer/c-html5-aem-int-video-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> CSS-Sprites </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Diese Schaltfläche unterstützt die Attributselektoren `state` und `selected`, die verwendet werden können, um verschiedene Skins auf unterschiedliche Schaltflächenzustände anzuwenden. Insbesondere entspricht `selected='true'` dem Status &quot;muted&quot;und `selected='false'` dem Status &quot;unmuted&quot;.

Der Bereich für den vertikalen Volumenbalken wird mit der folgenden CSS-Klassenauswahl gesteuert:

```
.s7interactivevideoviewer .s7mutablevolume .s7verticalvolume
```

**CSS-Eigenschaften des Bereichs mit der vertikalen Lautstärkenleiste**

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

Die Steuerung des Gleises innerhalb der vertikalen Lautstärke wird mit den folgenden CSS-Klassenselektoren gesteuert:

```
.s7interactivevideoviewer .s7mutablevolume .s7verticalvolume .s7track 
.s7interactivevideoviewer .s7mutablevolume .s7verticalvolume .s7filledtrack
```

**CSS-Eigenschaften des Gleises innerhalb der Steuerung der vertikalen Lautstärke**

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

Der Regler für das vertikale Volumen wird mit der folgenden CSS-Klassenauswahl gesteuert:

```
.s7interactivevideoviewer .s7mutablevolume .s7verticalvolume .s7knob
```

**CSS-Eigenschaften des Reglers für die vertikale Lautstärkeregelung**

<table id="table_709D64AF815341A5B50ED72CCB350F2E"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image  </span> </p> </td> 
   <td colname="col2"> <p> Vertikale Lautstärkeregler-Grafik. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position  </span> </p> </td> 
   <td colname="col2"> <p> Position innerhalb des Bildsprites, wenn CSS-Sprites verwendet werden. </p> <p>Siehe <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-customizingviewer/c-html5-aem-int-video-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> CSS-Sprites </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width  </span> </p> </td> 
   <td colname="col2"> <p>Breite des vertikalen Lautstärkereglers. </p> </td> 
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

Die QuickInfo der Schaltfläche kann lokalisiert werden. Weitere Informationen finden Sie unter [Lokalisierung von Benutzeroberflächenelementen](../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74).

## Beispiele {#section-e8caea0a303c425a8a637c2a47c06355}

So richten Sie eine Stummschaltfläche ein, die 32 x 32 Pixel groß und 6 Pixel von der oberen Seite und 38 Pixel von der rechten Kante der Steuerleiste positioniert ist. Zeigen Sie für jeden der vier Schaltflächenstatus ein anderes Bild an, wenn diese ausgewählt sind oder nicht ausgewählt sind.

```
.s7interactivevideoviewer .s7mutablevolume { 
top:6px; 
right:38px; 
width:32px; 
height:32px; 
} 
.s7interactivevideoviewer .s7mutablevolume .s7mutebutton[selected='true'][state='up'] { 
background-image:url(images/mute_up.png); 
} 
.s7interactivevideoviewer .s7mutablevolume .s7mutebutton[selected='true'][state='over'] { 
background-image:url(images/mute_over.png); 
} 
.s7interactivevideoviewer .s7mutablevolume .s7mutebutton[selected='true'][state='down'] { 
background-image:url(images/mute_down.png); 
} 
.s7interactivevideoviewer .s7mutablevolume .s7mutebutton[selected='true'][state='disabled'] { 
background-image:url(images/mute_disabled.png); 
} 
.s7interactivevideoviewer .s7mutablevolume .s7mutebutton[selected='false'][state='up'] { 
background-image:url(images/unmute_up.png); 
} 
.s7interactivevideoviewer .s7mutablevolume .s7mutebutton[selected='false'][state='over'] { 
background-image:url(images/unmute_over.png); 
} 
.s7interactivevideoviewer .s7mutablevolume .s7mutebutton[selected='false'][state='down'] { 
background-image:url(images/unmute_down.png); 
} 
.s7interactivevideoviewer .s7mutablevolume .s7mutebutton[selected='false'][state='disabled'] { 
background-image:url(images/unmute_disabled.png); 
}
```

Im Folgenden finden Sie ein Beispiel dafür, wie Sie den Lautstärkeregler innerhalb des veränderlichen Lautstärkereglers formatieren können.

```
.s7interactivevideoviewer .s7mutablevolume .s7verticalvolume { 
width:36px; 
height:83px; 
left:0px; 
background-color:#dddddd; 
} 
.s7interactivevideoviewer .s7mutablevolume .s7verticalvolume .s7track { 
top:11px; 
left:14px; 
width:10px; 
height:63px; 
background-color:#666666; 
} 
.s7interactivevideoviewer .s7mutablevolume .s7verticalvolume .s7filledtrack { 
width:10px; 
background-color:#ababab; 
} 
.s7interactivevideoviewer .s7mutablevolume .s7verticalvolume .s7knob { 
width:18px; 
height:10px; 
left:9px; 
background-image:url(images/volumeKnob.png); 
}
```
