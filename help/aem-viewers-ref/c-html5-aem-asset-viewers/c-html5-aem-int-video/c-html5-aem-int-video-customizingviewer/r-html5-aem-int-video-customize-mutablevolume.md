---
title: Veränderliches Volumen
description: Die veränderliche Lautstärkeregelung wird zunächst als Schaltfläche angezeigt, mit der ein Benutzer den Video-Player-Ton stummschalten oder die Stummschaltung aufheben kann.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: ecef47c1-e659-4930-bfb1-cc5e7c059094
source-git-commit: 6aaf4eccf51a05d200c6cc780e342be646d104d8
workflow-type: tm+mt
source-wordcount: '475'
ht-degree: 0%

---

# Veränderliches Volumen{#mutable-volume}

Die veränderliche Lautstärkeregelung wird zunächst als Schaltfläche angezeigt, mit der ein Benutzer den Video-Player-Ton stummschalten oder die Stummschaltung aufheben kann.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

Wenn ein(e) Benutzende(r) auf die Schaltfläche klickt, wird ein Schieberegler angezeigt, mit dem der Benutzer die Lautstärke einstellen kann. Die veränderliche Lautstärkeregelung kann über CSS in der Größe, der Haut und der Position relativ zur Kontrollleiste, in der sie enthalten ist, angepasst werden.

Das Erscheinungsbild des veränderlichen Volumenbereichs wird mit dem folgenden CSS-Klassenselektor gesteuert:

```
.s7interactivevideoviewer .s7mutablevolume
```

**CSS-Eigenschaften des veränderlichen Volumes**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Top-</span> </p> </td> 
   <td colname="col2"> <p> Position ab dem oberen Rahmen, einschließlich Auffüllung. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> rechte </span> </p> </td> 
   <td colname="col2"> <p> Position vom rechten Rand aus, einschließlich Abstand. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Breite </span> </p> </td> 
   <td colname="col2"> <p> Die Breite des veränderlichen Lautstärkereglers. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Höhe </span> </p> </td> 
   <td colname="col2"> <p>Die Höhe der veränderlichen Lautstärkeregelung. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">-</span> </p> </td> 
   <td colname="col2"> <p> Die Farbe der veränderlichen Lautstärkeregelung. </p> </td> 
  </tr> 
 </tbody> 
</table>

Das Erscheinungsbild der Schaltfläche Stummschaltung/Stummschaltung aufheben wird mit dem folgenden CSS-Klassenselektor gesteuert:

```
.s7interactivevideoviewer .s7mutablevolume .s7mutebutton
```

Sie können das Hintergrundbild für jeden Schaltflächenstatus steuern. Die Größe der Schaltfläche wird von der Größe des Lautstärkereglers übernommen.

**CSS-Eigenschaften des Schaltflächenbilds**

<table id="table_46903DCACF314426B67783167ADF7715"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Hintergrundbild-</span> </p> </td> 
   <td colname="col2"> <p> Das für einen bestimmten Schaltflächenstatus angezeigte Bild. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Hintergrundposition </span> </p> </td> 
   <td colname="col2"> <p> Positionieren Sie sie innerhalb des Bildsets, wenn CSS-Sprites verwendet werden. </p> <p>Siehe <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-customizingviewer/c-html5-aem-int-video-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> von CSS-Sprites </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Diese Schaltfläche unterstützt sowohl den `state`- als auch den `selected`-Attributselektor, mit dem verschiedene Skins auf verschiedene Schaltflächenzustände angewendet werden können. Insbesondere entspricht `selected='true'` dem Zustand „Stummschaltung“ und `selected='false'` dem Zustand „Stummschaltung“.

Der vertikale Lautstärkebereich wird mit dem folgenden CSS-Klassenselektor gesteuert:

```
.s7interactivevideoviewer .s7mutablevolume .s7verticalvolume
```

**CSS-Eigenschaften des vertikalen Volumenleistenbereichs**

<table id="table_966826FB81114362A8D81D1EED38D512"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">-</span> </p> </td> 
   <td colname="col2"> <p> Die Hintergrundfarbe des vertikalen Volumens. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Breite </span> </p> </td> 
   <td colname="col2"> <p> Die Breite des vertikalen Volumens. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Höhe </span> </p> </td> 
   <td colname="col2"> <p> Die Höhe des vertikalen Volumens. </p> </td> 
  </tr> 
 </tbody> 
</table>

Die Spur innerhalb der vertikalen Lautstärkeregelung wird mit den folgenden CSS-Klassenselektoren gesteuert:

```
.s7interactivevideoviewer .s7mutablevolume .s7verticalvolume .s7track 
.s7interactivevideoviewer .s7mutablevolume .s7verticalvolume .s7filledtrack
```

**CSS-Eigenschaften der Spur innerhalb der vertikalen Lautstärkeregelung**

<table id="table_21E9AD3FBC8C4437BA02E5CD1BF7E831"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">-</span> </p> </td> 
   <td colname="col2"> <p> Die Hintergrundfarbe der vertikalen Lautstärkeregelung. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Breite </span> </p> </td> 
   <td colname="col2"> <p>Breite der vertikalen Lautstärkeregelung. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Höhe </span> </p> </td> 
   <td colname="col2"> <p>Höhe der vertikalen Lautstärkeregelung. </p> </td> 
  </tr> 
 </tbody> 
</table>

Der vertikale Lautstärkeregler wird mit der folgenden CSS-Klassenauswahl gesteuert:

```
.s7interactivevideoviewer .s7mutablevolume .s7verticalvolume .s7knob
```

**CSS-Eigenschaften des vertikalen Lautstärkereglers**

<table id="table_709D64AF815341A5B50ED72CCB350F2E"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Hintergrundbild-</span> </p> </td> 
   <td colname="col2"> <p> vertikale Lautstärkeregler-Grafik. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Hintergrundposition </span> </p> </td> 
   <td colname="col2"> <p> Positionieren Sie sie innerhalb des Bildsets, wenn CSS-Sprites verwendet werden. </p> <p>Siehe <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-customizingviewer/c-html5-aem-int-video-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> von CSS-Sprites </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Breite </span> </p> </td> 
   <td colname="col2"> <p>Breite des vertikalen Lautstärkereglers. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Höhe </span> </p> </td> 
   <td colname="col2"> <p>Höhe des vertikalen Lautstärkereglers. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> linker </span> </p> </td> 
   <td colname="col2"> <p>Horizontale Position des vertikalen Lautstärkereglers. </p> </td> 
  </tr> 
 </tbody> 
</table>

Die QuickInfo der Schaltfläche kann lokalisiert werden. Siehe [Lokalisierung von Benutzeroberflächenelementen](../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) für weitere Informationen.

## Beispiele {#section-e8caea0a303c425a8a637c2a47c06355}

So richten Sie eine Stummschaltfläche ein, die 32 x 32 Pixel groß und 6 Pixel vom oberen und 38 Pixel vom rechten Rand der Steuerleiste entfernt positioniert ist. Für jeden der vier verschiedenen Schaltflächenzustände wird ein anderes Bild angezeigt, wenn ausgewählt oder nicht ausgewählt.

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

Im Folgenden finden Sie ein Beispiel dafür, wie Sie den Lautstärkeregler im veränderlichen Lautstärkeregler gestalten können.

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
