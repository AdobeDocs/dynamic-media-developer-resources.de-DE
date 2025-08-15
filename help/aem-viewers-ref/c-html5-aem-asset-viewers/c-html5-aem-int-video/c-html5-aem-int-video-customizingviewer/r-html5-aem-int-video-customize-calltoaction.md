---
title: Aktionsaufruf
description: Das Call to action-Bedienfeld wird angezeigt, wenn das Video beendet wird, und zeigt alle interaktiven Farbfelder an, die mit dem jeweiligen Video verknüpft sind.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: 43e0ffb3-d650-4b79-ab48-2f32b313b832
source-git-commit: 6aaf4eccf51a05d200c6cc780e342be646d104d8
workflow-type: tm+mt
source-wordcount: '1299'
ht-degree: 1%

---

# Aktionsaufruf{#call-to-action}

Das Call to action-Bedienfeld wird angezeigt, wenn das Video beendet wird, und zeigt alle interaktiven Farbfelder an, die mit dem jeweiligen Video verknüpft sind.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

Das Bedienfeld besteht aus einem Kopfzeilenbereich mit dem Videotitel, einer Wiederholungsschaltfläche in der oberen rechten Ecke und tatsächlichen interaktiven Farbfeldern, die als scrollbares Raster angezeigt werden. Sie können den Bereich mithilfe des Konfigurationsattributs [callToActionRecap](../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/r-html5-aem-int-video-config-attrib/r-html5-aem-int-video-config-attrib-calltoactionrecap.md#reference-3720b68800684ddabf523e9d81644ce6) deaktivieren.

Das call to action-Bedienfeld nimmt immer den gesamten verfügbaren Viewer-Bereich ein.

<!--<a id="section_3A619BE925C04AFA87A6B7846C5C7E2B"></a>-->

Der folgende CSS-Klassenselektor steuert das Erscheinungsbild der Hintergrundfarbe im call to action-Bedienfeld:

```
.s7interactivevideoviewer .s7calltoaction
```

## CSS-Eigenschaften der Hintergrundfarbe des call to action-Bedienfelds {#css-properties-of-the-background-color-of-the-call-to-action-panel}

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">-</span> </p> </td> 
   <td colname="col2"> <p> Hintergrundfarbe des call to action-Bedienfelds. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Beispiel {#example}

So richten Sie ein call to action-Bedienfeld mit dunkelgrauem Hintergrund ein:

```
.s7interactivevideoviewer .s7calltoaction { 
    background-color: #222222; 
}
```

<!--<a id="section_AD18C770788B49989BEDAA608ECA804C"></a>-->

Der folgende CSS-Klassenselektor steuert die Darstellung der Kopfzeile im call to action-Bedienfeld:

```
.s7interactivevideoviewer .s7calltoaction .s7header
```

## CSS-Eigenschaften der Kopfzeile des call to action-Bedienfelds {#css-properties-of-the-call-to-action-panel-header}

<table id="table_DAA1770AB3074845B5E1B700CD6FC18A"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">-</span> </p> </td> 
   <td colname="col2"> <p>Hintergrundfarbe des Headers. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Höhe </span> </p> </td> 
   <td colname="col2"> <p>Höhe der Kopfzeile. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Rahmen - untere </span> </p> </td> 
   <td colname="col2"> <p>Unterer Rand der Kopfzeile. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Beispiel {#example-1}

So richten Sie eine Kopfzeile ein, die 70 Pixel hoch ist, einen dunkelgrauen Hintergrund und einen etwas helleren grauen Rahmen mit zwei Pixeln am unteren Rand aufweist:

```
.s7interactivevideoviewer .s7calltoaction .s7header { 
    height: 70px; 
    border-bottom: 2px solid #444444; 
    background-color: #222222; 
}
```

<!--<a id="section_B0333FC1A2CC4E089C68D34B839E5156"></a>-->

Der folgende CSS-Klassenselektor steuert die Darstellung des Kopfzeilentitels im call to action-Bedienfeld:

```
.s7interactivevideoviewer .s7calltoaction .s7header .s7title
```

## CSS-Eigenschaften des Kopfzeilentitels im call to action-Bedienfeld:  {#css-properties-of-the-header-title-in-the-call-to-action-panel}

<table id="table_A5E36A5C4C664346B6DAE9A02B36C3D2"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">-</span> </p> </td> 
   <td colname="col2"> <p> Textfarbe im Banner. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">-</span> </p> </td> 
   <td colname="col2"> <p>Schriftgröße. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> mit </span> Zeilenhöhe </p> </td> 
   <td colname="col2"> <p>Zeilenhöhe. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">-</span> </p> </td> 
   <td colname="col2"> <p> Schriftfamilie. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> zur Textausrichtung </span> </p> </td> 
   <td colname="col2"> <p>Ausrichtung des Texts im Banner. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Abstand - </span> </p> </td> 
   <td colname="col2"> <p>Linker Abstand. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Abstand rechts </span> </p> </td> 
   <td colname="col2"> <p> Rechter Abstand, um Platz für die Schaltfläche „Wiederholen“ zu lassen. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Beispiel {#example-2}

So richten Sie einen Videotitel mit einer Zeilenhöhe von 70 Pixel, einer Schriftgröße von 25 Pixel, einer weißen Farbe und einer linksbündigen Ausrichtung ein:

```
.s7interactivevideoviewer .s7calltoaction .s7header .s7title { 
    line-height: 70px; 
    font-size: 25px; 
    color: #ffffff; 
    text-align: left; 
}
```

<!--<a id="section_D23A6D4BA0614286A060982B359E3C08"></a>-->

Der folgende CSS-Klassenselektor steuert das Erscheinungsbild der Schaltfläche „Schließen“ im call to action-Bedienfeld:

```
.s7interactivevideoviewer .s7calltoaction .s7closebutton
```

## CSS-Eigenschaften der Schließen-Schaltfläche im call to action-Bedienfeld: {#css-properties-of-the-close-button-in-the-call-to-action-panel}

<table id="table_CB0BCBE70DB447BC8D31034A96308924"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Top-</span> </p> </td> 
   <td colname="col2"> <p>Position oben in der Kopfzeile, einschließlich Auffüllung. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> rechte </span> </p> </td> 
   <td colname="col2"> <p>Position rechts von der Kopfzeile, einschließlich Auffüllung. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Breite </span> </p> </td> 
   <td colname="col2"> <p>Breite der Schaltfläche. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Höhe </span> </p> </td> 
   <td colname="col2"> <p> Höhe der Schaltfläche. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Hintergrundbild-</span> </p> </td> 
   <td colname="col2"> <p>Bild, das für einen bestimmten Schaltflächenstatus angezeigt wird. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Hintergrundposition </span> </p> </td> 
   <td colname="col2"> <p>Positionieren Sie sie innerhalb des Bildsets, wenn CSS-Sprites verwendet werden. </p> <p>Siehe <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-customizingviewer/c-html5-aem-int-video-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> von CSS-Sprites </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Diese Schaltfläche unterstützt die `state`-Attributauswahl, mit der verschiedene Skins auf verschiedene Schaltflächenzustände angewendet werden können.

## Beispiel {#example-3}

So richten Sie eine Wiedergabeschaltfläche ein, die 28 x 28 Pixel groß ist. Die Schaltfläche muss 20 Pixel vom oberen und rechten Rand der Kopfzeile entfernt positioniert werden. Außerdem muss für jeden der vier verschiedenen Schaltflächenzustände ein anderes Bild angezeigt werden. Nimmt das Bildmaterial aus dem Sprite-Bild der Komponente:

```
.s7interactivevideoviewer .s7calltoaction .s7closebutton { 
 top: 20px; 
 right: 20px; 
 background-size: 336px; 
 width: 28px; 
 height: 28px;  
} 
.s7interactivevideoviewer .s7calltoaction .s7closebutton[state] { 
 background-image: url(images/v2/PlayPauseButton_sprite.png); 
} 
.s7interactivevideoviewer .s7calltoaction .s7closebutton[state='up'] { 
 background-position: -28px -1260px; 
} 
.s7interactivevideoviewer .s7calltoaction .s7closebutton[state='over'] { 
 background-position: -0px -1260px; 
} 
.s7interactivevideoviewer .s7calltoaction .s7closebutton[state='down'] { 
 background-position: -28px -1232px; 
} 
.s7interactivevideoviewer .s7calltoaction .s7closebutton[state='disabled'] { 
 background-position: -0px -1232px; 
}
```

<!--<a id="section_3975B58E78DE4E81B469372FB8A3A348"></a>-->

Der folgende CSS-Klassenselektor steuert das Erscheinungsbild der Miniaturansicht-Rasteransicht im call to action-Bedienfeld:

```
.s7interactivevideoviewer .s7calltoaction .s7thumbnailgridview
```

## CSS-Eigenschaften der Rasteransicht für Miniaturansichten im call to action-Bedienfeld:  {#css-properties-of-the-thumbnail-grid-view-in-the-call-to-action-panel}

<table id="table_A0DDD21C84944D48A639F51FCC8DF065"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">-</span> </p> </td> 
   <td colname="col2"> <p>Hintergrundfarbe des Bereichs „Miniaturen“. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Beispiel {#example-4}

So richten Sie einen Bereich für Miniaturen mit dunkelgrauem Hintergrund ein:

```
.s7interactivevideoviewer .s7calltoaction .s7thumbnailgridview { 
    background-color: #222222; 
}
```

<!--<a id="section_D2E5AADFCE0345468DC0D2977E2765D2"></a>-->

Der folgende CSS-Klassenselektor steuert das Erscheinungsbild der Miniaturzelle im call to action-Bedienfeld:

```
.s7interactivevideoviewer .s7calltoaction .s7thumbcell
```

## CSS-Eigenschaften der Faustzelle im call to action-Bedienfeld: {#css-properties-of-the-thumbcell-in-the-call-to-action-panel}

<table id="table_9CEBEF6FC7024F02840A581AEEF612B4"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">-</span> </p> </td> 
   <td colname="col2"> <p> Größe des horizontalen und vertikalen Rands um jede Miniaturansicht. </p> <p>Der tatsächliche Abstand zwischen horizontalen Miniaturen entspricht der Summe aus dem linken und rechten Randsatz für <span class="codeph"> s7thumbcell-</span>. Die gleiche Regel gilt auch für den vertikalen Abstand. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Beispiel {#example-5}

So legen Sie einen horizontalen Abstand von 24 Pixel und einen vertikalen Abstand von 18 Pixel fest:

```
.s7interactivevideoviewer .s7calltoaction .s7thumbcell { 
 margin-top: 9px; 
 margin-bottom: 9px; 
 margin-left: 12px; 
 margin-right: 12px; 
}
```

<!--<a id="section_D06CF9F709A3447F83DC6E1CE7CA58B5"></a>-->

Der folgende CSS-Klassenselektor steuert die Darstellung der Miniaturansicht im call to action-Bedienfeld:

```
.s7interactivevideoviewer .s7calltoaction .s7thumb
```

## CSS-Eigenschaften der Miniaturansicht im call to action-Bedienfeld: {#css-properties-of-the-thumbnail-in-the-call-to-action-panel}

<table id="table_ECD7477F4BE94BA8943210FA8B6B8D01"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Breite </span> </p> </td> 
   <td colname="col2"> <p>Breite der Miniaturansicht. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Höhe </span> </p> </td> 
   <td colname="col2"> <p>Höhe der Miniatur. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">-</span> </p> </td> 
   <td colname="col2"> <p>Rahmen der Miniatur. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>„Miniaturansicht“ unterstützt die `state`-Attributauswahl, mit der verschiedene Skins auf verschiedene Miniaturansichtszustände angewendet werden können. Insbesondere entspricht `state="selected"` der Miniatur für das aktuell ausgewählte Bild; `state="default"` entspricht dem Rest der Miniaturen; `state="over"` wird beim Bewegen des Mauszeigers verwendet.

## Beispiel {#example-6}

So richten Sie Miniaturen mit 94 x 100 Pixel ein:

```
.s7interactivevideoviewer .s7calltoaction .s7thumb { 
 width:94px; 
 height:100px; 
}
```

<!--<a id="section_F1B7E3FA3ABD4D71848586A3B308F9E2"></a>-->

Der folgende CSS-Klassenselektor steuert die Darstellung der Miniaturbildbeschriftung im call to action-Bedienfeld:

```
.s7interactivevideoviewer .s7calltoaction .s7label
```

## CSS-Eigenschaften der Miniaturbildbeschriftung im call to action-Bedienfeld: {#css-properties-of-the-thumbnail-label-in-the-call-to-action-panel}

<table id="table_E2C9F21EBD9140FD9D20A4BBAD117E2F"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">-</span> </p> </td> 
   <td colname="col2"> <p> Textfarbe des Titels. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> zur Textausrichtung </span> </p> </td> 
   <td colname="col2"> <p>Horizontale Ausrichtung des Titels. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">-</span> </p> </td> 
   <td colname="col2"> <p>Schriftart. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">-</span> </p> </td> 
   <td colname="col2"> <p>Schriftfamilie. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Beispiel {#example-7}

Um Bezeichnungen einzurichten, die eine weiße Farbe verwenden, richten Sie sie um 15 Pixel zentriert aus und verwenden Sie eine Arial®-Schriftart:

```
.s7interactivevideoviewer .s7calltoaction .s7label { 
 text-align: center; 
 color: #ffffff; 
  font-family: Arial,Helvetica,sans-serif; 
  font-size: 15px; 
}
```

<!--<a id="section_2C011101EB804513B942EFB4CBD38E62"></a>-->

Wenn mehr Miniaturen vorhanden sind, als vertikal in die Ansicht passen, wird für die Miniaturen eine vertikale Bildlaufleiste auf der rechten Seite gerendert. Standardmäßig rendert das call to action-Bedienfeld einen winzigen vertikalen Balken ohne die Schaltflächen „Daumen“ und „Bildlauf“. Es ist jedoch möglich, die Leiste anzupassen, indem die Viewer-CSS geändert wird.

Der folgende CSS-Klassenselektor steuert die Darstellung des Bildlaufleistenbereichs im call to action-Bedienfeld:

```
.s7interactivevideoviewer .s7calltoaction .s7thumbnailgridview .s7scrollbar
```

## CSS-Eigenschaften des Bildlaufleistenbereichs im call to action-Bedienfeld: {#css-properties-of-the-scroll-bar-area-in-the-call-to-action-panel}

<table id="table_6D3A4A68BFDB44259A6E2E632B9195F3"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Breite </span> </p> </td> 
   <td colname="col2"> <p> Breite der Bildlaufleiste. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Top-</span> </p> </td> 
   <td colname="col2"> <p>Vertikaler Bildlaufbalken, der vom oberen Rand des Bereichs „Miniaturen“ versetzt ist. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> untere </span> </p> </td> 
   <td colname="col2"> <p>Vertikaler Bildlaufbalken, der vom unteren Rand des Bereichs „Miniaturen“ versetzt ist. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> rechte </span> </p> </td> 
   <td colname="col2"> <p> Horizontaler Bildlaufbalken versetzt vom rechten Rand des Bereichs Miniaturen. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Beispiel {#example-8}

So richten Sie eine Bildlaufleiste ein, die 22 Pixel breit ist und keinen Rand vom oberen, rechten oder unteren Rand des Bereichs „Miniaturen“ hat:

```
.s7interactivevideoviewer .s7calltoaction .s7thumbnailgridview .s7scrollbar { 
 top:0px; 
 bottom:0px; 
 right:0px; 
 width:22px; 
}
```

<!--<a id="section_E27B7253441543278E1081D70BA46122"></a>-->

Die Bildlaufleistenspur ist der Bereich zwischen den Schaltflächen der oberen und unteren Bildlaufleiste. Die Komponente legt automatisch die Position und Höhe der Spur fest.

Der folgende CSS-Klassenselektor steuert die Darstellung der Bildlaufleisten-Spur im call to action-Bedienfeld:

```
.s7interactivevideoviewer .s7calltoaction .s7thumbnailgridview .s7scrollbar .s7scrolltrack
```

## CSS-Eigenschaften der Bildlaufspurleiste {#css-properties-of-the-scroll-track-bar}

<table id="table_7A7D40C332F4461FAAC623196C00D5A8"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Breite </span> </p> </td> 
   <td colname="col2"> <p>Breite der Bildlaufspurleiste. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">-</span> </p> </td> 
   <td colname="col2"> <p>Hintergrundfarbe der Trackleiste. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Beispiel {#example-9}

So richten Sie eine Bildlaufleistenspur ein, die 22 Pixel breit ist und eine graue Farbe aufweist:

```
.s7interactivevideoviewer .s7calltoaction .s7thumbnailgridview .s7scrollbar .s7scrolltrack { 
 width:22px; 
 background-color:#222222; 
}
```

<!--<a id="section_4A5D8C1A9C9D4E7B8AC0CD5BC6F3772D"></a>-->

Der Daumen der Bildlaufleiste bewegt sich vertikal innerhalb des Bereichs der Bildlaufspur. Die vertikale Position wird vollständig von der Komponentenlogik gesteuert. Die Höhe des Daumens ändert sich jedoch je nach Inhaltsmenge nicht dynamisch.

Der folgende CSS-Klassenselektor steuert das Erscheinungsbild der Daumenhöhe und anderer Aspekte:

```
.s7interactivevideoviewer .s7calltoaction .s7thumbnailgridview .s7scrollbar .s7scrollthumb
```

## CSS-Eigenschaften der Daumenhöhe im call to action-Bedienfeld: {#css-properties-of-the-thumb-height-in-the-call-to-action-panel}

<table id="table_1F39948FC3924FA4B7F851B65B2D860B"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Breite </span> </p> </td> 
   <td colname="col2"> <p>Breite des Daumens. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Höhe </span> </p> </td> 
   <td colname="col2"> <p>Daumenhöhe. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">-</span> </p> </td> 
   <td colname="col2"> <p>Vertikaler Abstand zwischen dem oberen Ende der Spur. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">-</span> </p> </td> 
   <td colname="col2"> <p>Vertikaler Abstand zwischen dem unteren Ende der Spur. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">-</span> </p> </td> 
   <td colname="col2"> <p>Radius des Rahmens. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">-</span> </p> </td> 
   <td colname="col2"> <p>Daumenfarbe. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Hintergrundbild-</span> </p> </td> 
   <td colname="col2"> <p> Bild, das für einen bestimmten Daumenstatus angezeigt wird. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Hintergrundposition </span> </p> </td> 
   <td colname="col2"> <p> Positionieren Sie sie innerhalb des Bildsets, wenn CSS-Sprites verwendet werden. </p> <p>Siehe <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-customizingviewer/c-html5-aem-int-video-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> von CSS-Sprites </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Thumb unterstützt den `state`-Attributselektor , mit dem verschiedene Skins auf die folgenden verschiedenen Thumb-Status angewendet werden können: `"up"`, `"down"`, `"over"` und `"disabled"`.

## Beispiel {#example-10}

So richten Sie einen Bildlaufleisten-Daumen mit 6 x 167 Pixeln ein, hat drei abgerundete Pixel und eine graue Farbe:

```
.s7interactivevideoviewer .s7calltoaction .s7thumbnailgridview .s7scrollbar .s7scrollthumb[state] { 
 width:6px; 
 height:167px; 
 background-color:#666666; 
 background-image:none; 
 border-radius:3px 3px 3px 3px; 
}
```

<!--<a id="section_C393B59763344E70A3BBD0601110F8DD"></a>-->

Der folgende CSS-Klassenselektor steuert die Darstellung der oberen und unteren Bildlaufschaltflächen:

```
.s7interactivevideoviewer .s7calltoaction .s7thumbnailgridview .s7scrollbar .s7scrollupbutton 
 
.s7interactivevideoviewer .s7calltoaction .s7thumbnailgridview .s7scrollbar .s7scrolldownbutton
```

Scroll-Schaltflächen können nicht mit den CSS-Eigenschaften „oben“, „links“, „unten“ oder „rechts“ positioniert werden. Die Viewer-Logik positioniert sie automatisch. Das call to action-Bedienfeld im interaktiven Video-Viewer verwendet diese Schaltflächen nicht in der Bildlaufleiste, sodass ihre Größe in der Standard-CSS auf 0 Pixel festgelegt ist.

## CSS-Eigenschaften der oberen und unteren Bildlaufschaltflächen im call to action-Bedienfeld:  {#css-properties-of-the-top-and-bottom-scroll-buttons-in-the-call-to-action-panel}

<table id="table_FE17D19E0545424EADB0256524361359"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Breite </span> </p> </td> 
   <td colname="col2"> <p> Breite der Schaltfläche. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Höhe </span> </p> </td> 
   <td colname="col2"> <p>Höhe der Schaltfläche. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Hintergrundbild-</span> </p> </td> 
   <td colname="col2"> <p>Bild, das für einen bestimmten Schaltflächenstatus angezeigt wird. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Hintergrundposition </span> </p> </td> 
   <td colname="col2"> <p> Positionieren Sie sie innerhalb des Bildsets, wenn CSS-Sprites verwendet werden. </p> <p>Siehe <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-customizingviewer/c-html5-aem-int-video-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> von CSS-Sprites </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Diese Schaltflächen unterstützen die `state` Attributauswahl, mit der Sie verschiedene Skins auf die folgenden verschiedenen Miniaturansichten anwenden können: `"up"`, `"down"`, `"over"` und `"disabled"`.

Die QuickInfos für die Schaltfläche können lokalisiert werden. Siehe [Lokalisierung von Benutzeroberflächenelementen](../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74).

## Beispiel {#example-11}

Deaktivieren Sie Bildlaufschaltflächen, indem Sie ihre Größe auf 0 setzen und sie ausblenden:

```
.s7interactivevideoviewer .s7calltoaction .s7thumbnailgridview .s7scrollbar .s7scrollupbutton { 
 visibility: hidden; 
 width: 0px; 
 height: 0px; 
} 
.s7interactivevideoviewer .s7calltoaction .s7thumbnailgridview .s7scrollbar .s7scrolldownbutton { 
 visibility: hidden; 
 width: 0px; 
 height: 0px; 
}
```
