---
description: Das Aktionsaufruf-Bedienfeld wird nach dem Ende des Videos angezeigt und zeigt alle interaktiven Muster an, die mit dem betreffenden Video verknüpft sind.
seo-description: Das Aktionsaufruf-Bedienfeld wird nach dem Ende des Videos angezeigt und zeigt alle interaktiven Muster an, die mit dem betreffenden Video verknüpft sind.
seo-title: Aktionsaufruf
solution: Experience Manager
title: Aktionsaufruf
topic: Dynamic media
uuid: 04a042d8-7329-4f1d-b3b9-312d620b1f29
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef

---


# Aktionsaufruf{#call-to-action}

Das Aktionsaufruf-Bedienfeld wird nach dem Ende des Videos angezeigt und zeigt alle interaktiven Muster an, die mit dem betreffenden Video verknüpft sind.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

Das Bedienfeld besteht aus einem Kopfzeilenbereich, der den Videotitel, eine Wiederholungsschaltfläche in der oberen rechten Ecke und tatsächliche interaktive Muster, die als durchlaufbares Raster angezeigt werden, anzeigt. Sie können das Bedienfeld mit dem [Konfigurationsattribut callToActionRecap](../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/r-html5-aem-int-video-config-attrib/r-html5-aem-int-video-config-attrib-calltoactionrecap.md#reference-3720b68800684ddabf523e9d81644ce6) deaktivieren.

Der Aktionsaufruf-Bereich nimmt immer den gesamten verfügbaren Viewer-Bereich ein.

<!--<a id="section_3A619BE925C04AFA87A6B7846C5C7E2B"></a>-->

Der folgende CSS-Klassenselektor steuert das Erscheinungsbild der Hintergrundfarbe im Aktionsaufruf-Bedienfeld:

```
.s7interactivevideoviewer .s7calltoaction
```

## CSS-Eigenschaften der Hintergrundfarbe des Aktionsaufrufs {#css-properties-of-the-background-color-of-the-call-to-action-panel}

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p> Hintergrundfarbe des Aktionsaufrufs. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Beispiel {#example}

So richten Sie einen Aktionsaufruf mit dunkelgrauem Hintergrund ein:

```
.s7interactivevideoviewer .s7calltoaction { 
    background-color: #222222; 
}
```

<!--<a id="section_AD18C770788B49989BEDAA608ECA804C"></a>-->

Der folgende CSS-Klassenselektor steuert das Aussehen der Kopfzeile im Aktionsaufruf-Bedienfeld:

```
.s7interactivevideoviewer .s7calltoaction .s7header
```

## CSS-Eigenschaften der Kopfzeile des Aktionsbedienfelds {#css-properties-of-the-call-to-action-panel-header}

<table id="table_DAA1770AB3074845B5E1B700CD6FC18A"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p>Hintergrundfarbe der Kopfzeile. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Höhe der Kopfzeile. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> border-bottom </span> </p> </td> 
   <td colname="col2"> <p>Unterer Rand der Kopfzeile. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Beispiel {#example-1}

So richten Sie eine 70 Pixel große Kopfzeile mit dunkelgrauem Hintergrund und einen etwas helleren, zwei Pixel breiten Rand am unteren Rand ein:

```
.s7interactivevideoviewer .s7calltoaction .s7header { 
    height: 70px; 
    border-bottom: 2px solid #444444; 
    background-color: #222222; 
}
```

<!--<a id="section_B0333FC1A2CC4E089C68D34B839E5156"></a>-->

Der folgende CSS-Klassenselektor steuert das Erscheinungsbild des Kopfzeiltitels im Aktionsaufruf-Bedienfeld:

```
.s7interactivevideoviewer .s7calltoaction .s7header .s7title
```

## CSS-Eigenschaften des Kopfzeilentitels im Aktionsaufruf-Bedienfeld:  {#css-properties-of-the-header-title-in-the-call-to-action-panel}

<table id="table_A5E36A5C4C664346B6DAE9A02B36C3D2"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> color </span> </p> </td> 
   <td colname="col2"> <p> Textfarbe im Banner. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size </span> </p> </td> 
   <td colname="col2"> <p>Schriftgröße. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> line-height </span> </p> </td> 
   <td colname="col2"> <p>Zeilenhöhe. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family </span> </p> </td> 
   <td colname="col2"> <p> Schriftfamilie. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> text-align </span> </p> </td> 
   <td colname="col2"> <p>Ausrichtung des Texts im Banner. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> padding-left </span> </p> </td> 
   <td colname="col2"> <p>Auffüllung links. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> padding-right </span> </p> </td> 
   <td colname="col2"> <p> Rechte Auffüllung, um Platz für die Schaltfläche "Wiedergabe"zu schaffen. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Beispiel {#example-2}

So richten Sie einen Videotitel mit einer Zeilenhöhe von 70 Pixel, einer Schriftgröße von 25 Pixel, einer weißen Farbe und einer Linksausrichtung ein:

```
.s7interactivevideoviewer .s7calltoaction .s7header .s7title { 
    line-height: 70px; 
    font-size: 25px; 
    color: #ffffff; 
    text-align: left; 
}
```

<!--<a id="section_D23A6D4BA0614286A060982B359E3C08"></a>-->

Der folgende CSS-Klassenselektor steuert das Erscheinungsbild der Schaltfläche zum Schließen im Aktionsaufruf-Bedienfeld:

```
.s7interactivevideoviewer .s7calltoaction .s7closebutton
```

## CSS-Eigenschaften der Schaltfläche &quot;Schließen&quot;im Aktionsaufruf-Bedienfeld: {#css-properties-of-the-close-button-in-the-call-to-action-panel}

<table id="table_CB0BCBE70DB447BC8D31034A96308924"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Anfang </span> </p> </td> 
   <td colname="col2"> <p>Position oben in der Kopfzeile, einschließlich Auffüllung. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> rechts </span> </p> </td> 
   <td colname="col2"> <p>Position rechts neben der Kopfzeile, einschließlich Auffüllung. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Schaltflächenbreite. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p> Schaltflächenhöhe. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image </span> </p> </td> 
   <td colname="col2"> <p>Bild, das für einen bestimmten Schaltflächenstatus angezeigt wird. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p>Position innerhalb des Grafik-Sprites, wenn CSS-Sprites verwendet werden. </p> <p>Siehe <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-customizingviewer/c-html5-aem-int-video-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> CSS-Sprites </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Diese Schaltfläche unterstützt die `state` Attributauswahl, mit der verschiedene Skins auf verschiedene Schaltflächenzustände angewendet werden können.

## Beispiel {#example-3}

So richten Sie eine Wiederholungsschaltfläche von 28 x 28 Pixeln ein. 20 Pixel von oben und von der rechten Kante der Kopfzeile entfernt; zeigt für jeden der vier Schaltflächenzustände ein anderes Bild an; nimmt das Bildmaterial aus dem Sprite-Bild der Komponente:

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

Mit dem folgenden CSS-Klassenselektor wird das Erscheinungsbild der Ansicht des Miniaturraster im Aktionsaufruf-Bedienfeld gesteuert:

```
.s7interactivevideoviewer .s7calltoaction .s7thumbnailgridview
```

## CSS-Eigenschaften der Ansicht des Miniaturrasters im Aktionsaufruf-Bedienfeld:  {#css-properties-of-the-thumbnail-grid-view-in-the-call-to-action-panel}

<table id="table_A0DDD21C84944D48A639F51FCC8DF065"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p>Hintergrundfarbe des Miniaturansichtsbereichs. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Beispiel {#example-4}

So richten Sie einen Bereich für Miniaturansichten mit dunkelgrauem Hintergrund ein:

```
.s7interactivevideoviewer .s7calltoaction .s7thumbnailgridview { 
    background-color: #222222; 
}
```

<!--<a id="section_D2E5AADFCE0345468DC0D2977E2765D2"></a>-->

Der folgende CSS-Klassenselektor steuert das Erscheinungsbild der Thumb-Zelle im Aktionsaufruf-Bedienfeld:

```
.s7interactivevideoviewer .s7calltoaction .s7thumbcell
```

## CSS-Eigenschaften der Thumbcell im Aktionsaufruf-Bedienfeld: {#css-properties-of-the-thumbcell-in-the-call-to-action-panel}

<table id="table_9CEBEF6FC7024F02840A581AEEF612B4"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margin </span> </p> </td> 
   <td colname="col2"> <p> Größe des horizontalen und vertikalen Randes um die einzelnen Miniaturansichten. </p> <p>Der tatsächliche horizontale Abstand der Miniaturansichten entspricht der Summe des linken und rechten Randes, der für <span class="codeph"> .s7thumbcell festgelegt wurde </span>. Dieselbe Regel gilt auch für den vertikalen Abstand. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Beispiel {#example-5}

So richten Sie einen horizontalen Abstand von 24 Pixel und einen vertikalen Abstand von 18 Pixeln ein:

```
.s7interactivevideoviewer .s7calltoaction .s7thumbcell { 
 margin-top: 9px; 
 margin-bottom: 9px; 
 margin-left: 12px; 
 margin-right: 12px; 
}
```

<!--<a id="section_D06CF9F709A3447F83DC6E1CE7CA58B5"></a>-->

Der folgende CSS-Klassenselektor steuert das Erscheinungsbild der Miniaturansicht im Aktionsaufruf-Bedienfeld:

```
.s7interactivevideoviewer .s7calltoaction .s7thumb
```

## CSS-Eigenschaften der Miniaturansicht im Aktionsaufruf-Bedienfeld: {#css-properties-of-the-thumbnail-in-the-call-to-action-panel}

<table id="table_ECD7477F4BE94BA8943210FA8B6B8D01"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Breite der Miniaturansicht. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Höhe der Miniaturansicht. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> rand </span> </p> </td> 
   <td colname="col2"> <p>Rand der Miniaturansicht. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Miniaturansicht unterstützt die `state` Attributauswahl, mit der verschiedene Skins auf verschiedene Miniaturansichten angewendet werden können. entspricht insbesondere `state="selected"` der Miniaturansicht des derzeit ausgewählten Bildes; entspricht `state="default"` dem Rest der Miniaturansichten; wird `state="over"` beim Bewegen der Maus verwendet.

## Beispiel {#example-6}

So richten Sie Miniaturansichten mit 94 x 100 Pixel ein:

```
.s7interactivevideoviewer .s7calltoaction .s7thumb { 
 width:94px; 
 height:100px; 
}
```

<!--<a id="section_F1B7E3FA3ABD4D71848586A3B308F9E2"></a>-->

Der folgende CSS-Klassenselektor steuert das Erscheinungsbild der Miniaturansichtsbeschriftung im Aktionsaufruf-Bedienfeld:

```
.s7interactivevideoviewer .s7calltoaction .s7label
```

## CSS-Eigenschaften der Miniaturansichtsbeschriftung im Aktionsaufruf-Bedienfeld: {#css-properties-of-the-thumbnail-label-in-the-call-to-action-panel}

<table id="table_E2C9F21EBD9140FD9D20A4BBAD117E2F"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> color </span> </p> </td> 
   <td colname="col2"> <p> Textfarbe der Beschriftung. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> text-align </span> </p> </td> 
   <td colname="col2"> <p>Horizontale Ausrichtung der Beschriftung. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family </span> </p> </td> 
   <td colname="col2"> <p>Schriftname. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size </span> </p> </td> 
   <td colname="col2"> <p>Schriftfamilie. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Beispiel {#example-7}

Um Beschriftungen mit einer weißen Farbe einzurichten, müssen Sie 15 Pixel zentriert ausrichten und eine Arial-Schrift verwenden:

```
.s7interactivevideoviewer .s7calltoaction .s7label { 
 text-align: center; 
 color: #ffffff; 
  font-family: Arial,Helvetica,sans-serif; 
  font-size: 15px; 
}
```

<!--<a id="section_2C011101EB804513B942EFB4CBD38E62"></a>-->

Wenn mehr Miniaturansichten vorhanden sind, als vertikal in die Ansicht passen können, wird durch Miniaturansichten eine vertikale Bildlaufleiste auf der rechten Seite gerendert. Der Aktionsaufruf rendert standardmäßig einen winzigen vertikalen Balken ohne Daumen- und Bildlaufschaltflächen. Sie können die Leiste jedoch anpassen, indem Sie die CSS des Viewers ändern.

Der folgende CSS-Klassenselektor steuert das Erscheinungsbild des Bildlaufleistenbereichs im Aktionsaufruf-Bedienfeld:

```
.s7interactivevideoviewer .s7calltoaction .s7thumbnailgridview .s7scrollbar
```

## CSS-Eigenschaften des Bildlaufleistenbereichs im Aktionsaufruf-Bedienfeld: {#css-properties-of-the-scroll-bar-area-in-the-call-to-action-panel}

<table id="table_6D3A4A68BFDB44259A6E2E632B9195F3"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p> Breite der Bildlaufleiste. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Anfang </span> </p> </td> 
   <td colname="col2"> <p>Versatz der vertikalen Bildlaufleiste vom oberen Rand des Bereichs der Miniaturansichten. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> unten </span> </p> </td> 
   <td colname="col2"> <p>Versatz der vertikalen Bildlaufleiste vom unteren Rand des Bereichs der Miniaturansichten. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> rechts </span> </p> </td> 
   <td colname="col2"> <p> Die horizontale Bildlaufleiste wird vom rechten Rand des Bereichs der Miniaturansichten versetzt. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Beispiel {#example-8}

So richten Sie eine Bildlaufleiste ein, die 22 Pixel breit ist und keinen Rand von oben, rechts oder unten im Bereich der Miniaturansichten hat:

```
.s7interactivevideoviewer .s7calltoaction .s7thumbnailgridview .s7scrollbar { 
 top:0px; 
 bottom:0px; 
 right:0px; 
 width:22px; 
}
```

<!--<a id="section_E27B7253441543278E1081D70BA46122"></a>-->

Die Bildlaufleistenspur ist der Bereich zwischen den Schaltflächen der oberen und unteren Bildlaufleiste. Die Komponente legt automatisch die Position und Höhe der Leiste fest.

Der folgende CSS-Klassenselektor steuert das Erscheinungsbild der Bildlaufleistenspur im Aktionsaufruf-Bedienfeld:

```
.s7interactivevideoviewer .s7calltoaction .s7thumbnailgridview .s7scrollbar .s7scrolltrack
```

## CSS-Eigenschaften der Bildlaufleiste {#css-properties-of-the-scroll-track-bar}

<table id="table_7A7D40C332F4461FAAC623196C00D5A8"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Breite der Bildlaufleiste. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p>Hintergrundfarbe der Leiste. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Beispiel {#example-9}

So richten Sie eine Bildlaufleistenspur mit einer Breite von 22 Pixel und einer grauen Farbe ein:

```
.s7interactivevideoviewer .s7calltoaction .s7thumbnailgridview .s7scrollbar .s7scrolltrack { 
 width:22px; 
 background-color:#222222; 
}
```

<!--<a id="section_4A5D8C1A9C9D4E7B8AC0CD5BC6F3772D"></a>-->

Der Bildlaufleistenminiaturbereich bewegt sich vertikal innerhalb des Bildlaufspurbereichs. Seine vertikale Position wird vollständig durch die Komponentenlogik gesteuert; Die Höhe des Daumens ändert sich jedoch nicht dynamisch je nach Inhaltsmenge.

Der folgende CSS-Klassenselektor steuert das Aussehen der Thumb-Höhe und anderer Aspekte:

```
.s7interactivevideoviewer .s7calltoaction .s7thumbnailgridview .s7scrollbar .s7scrollthumb
```

## CSS-Eigenschaften der Miniaturhöhe im Aktionsaufruf-Bedienfeld: {#css-properties-of-the-thumb-height-in-the-call-to-action-panel}

<table id="table_1F39948FC3924FA4B7F851B65B2D860B"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Breite des Daumens. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Höhe des Daumens. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> padding-top </span> </p> </td> 
   <td colname="col2"> <p>Vertikale Umrandung zwischen der Oberkante der Spur. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> padding-bottom </span> </p> </td> 
   <td colname="col2"> <p>Vertikale Umrandung zwischen dem unteren Ende der Leiste. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> border-radius </span> </p> </td> 
   <td colname="col2"> <p>Rahmenradius. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p>Farbe des Daumens. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image </span> </p> </td> 
   <td colname="col2"> <p> Bild, das für einen bestimmten Daumenstatus angezeigt wird. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p> Position innerhalb des Bildausschnitt, wenn CSS-Sprites verwendet werden. </p> <p>Siehe <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-customizingviewer/c-html5-aem-int-video-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> CSS-Sprites </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Thumb unterstützt die `state` Attributauswahl, mit der verschiedene Skins auf die folgenden verschiedenen Thumb-Status angewendet werden können: `"up"`, `"down"`, `"over"`und `"disabled"`.

## Beispiel {#example-10}

Um ein Bildlaufleistenminiaturbild mit 6 x 167 Pixeln einzurichten, das drei abgerundete Pixel und eine graue Farbe hat:

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

Der folgende CSS-Klassenselektor steuert das Erscheinungsbild der Schaltflächen für den oberen und unteren Bildlauf:

```
.s7interactivevideoviewer .s7calltoaction .s7thumbnailgridview .s7scrollbar .s7scrollupbutton 
 
.s7interactivevideoviewer .s7calltoaction .s7thumbnailgridview .s7scrollbar .s7scrolldownbutton
```

Es ist nicht möglich, Bildlaufschaltflächen mithilfe der CSS-Eigenschaften top, left, bottom oder right zu positionieren. Die Viewer-Logik positioniert sie automatisch. Im Bedienfeld &quot;Aktionsaufruf&quot;des interaktiven Video-Viewers werden diese Schaltflächen in der Bildlaufleiste nicht verwendet. Daher ist ihre Größe im Standard-CSS auf 0 Pixel eingestellt.

## CSS-Eigenschaften der Schaltflächen für den oberen und unteren Bildlauf im Aktionsaufruf-Bedienfeld:  {#css-properties-of-the-top-and-bottom-scroll-buttons-in-the-call-to-action-panel}

<table id="table_FE17D19E0545424EADB0256524361359"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p> Breite der Schaltfläche. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Höhe der Schaltfläche. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image </span> </p> </td> 
   <td colname="col2"> <p>Bild, das für einen bestimmten Schaltflächenstatus angezeigt wird. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p> Position innerhalb des Bildausschnitt, wenn CSS-Sprites verwendet werden. </p> <p>Siehe <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-customizingviewer/c-html5-aem-int-video-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> CSS-Sprites </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Diese Schaltflächen unterstützen die `state` Attributauswahl, mit der verschiedene Skins auf die folgenden verschiedenen Thumb-Status angewendet werden können: `"up"`, `"down"`, `"over"`und `"disabled"`.

Die QuickInfos für Schaltflächen können lokalisiert werden. Siehe [Lokale Anpassung der Elemente](../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74)der Benutzeroberfläche.

## Beispiel {#example-11}

Deaktivieren Sie die Bildlaufschaltflächen, indem Sie ihre Größe auf 0 einstellen und sie ausblenden:

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

