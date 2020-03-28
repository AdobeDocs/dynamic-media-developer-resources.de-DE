---
description: Das Bedienfeld für interaktive Muster wird neben dem Videoinhalt angezeigt, wenn interaktive Daten in der Konfiguration an den Viewer weitergeleitet wurden. Es besteht aus einem Banner am oberen Rand, mit dem Text wie "Zur Ansicht klicken", einer oder mehreren interaktiven Farbfeldern und zwei Bildlaufschaltflächen (nur auf Desktop-Systemen verfügbar) gerendert werden.
seo-description: Das Bedienfeld für interaktive Muster wird neben dem Videoinhalt angezeigt, wenn interaktive Daten in der Konfiguration an den Viewer weitergeleitet wurden. Es besteht aus einem Banner am oberen Rand, mit dem Text wie "Zur Ansicht klicken", einer oder mehreren interaktiven Farbfeldern und zwei Bildlaufschaltflächen (nur auf Desktop-Systemen verfügbar) gerendert werden.
seo-title: Interaktive Muster
solution: Experience Manager
title: Interaktive Muster
topic: Dynamic media
uuid: 9f9df764-3dd0-414e-a0db-4287f0019313
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef

---


# Interaktive Muster{#interactive-swatches}

Das Bedienfeld für interaktive Muster wird neben dem Videoinhalt angezeigt, wenn interaktive Daten in der Konfiguration an den Viewer weitergeleitet wurden. Es besteht aus einem Banner am oberen Rand, mit dem Text wie &quot;Zur Ansicht klicken&quot;, einer oder mehreren interaktiven Farbfeldern und zwei Bildlaufschaltflächen (nur auf Desktop-Systemen verfügbar) gerendert werden.

<!--<a id="section_235621A1533A49AAADB64A7C3191F735"></a>-->

Auf Desktop-Systemen und Touch-Geräten werden interaktive Muster im Querformat vertikal rechts neben dem Videoinhalt gerendert. Auf Touch-Geräten im Hochformat werden sie am unteren Rand des Viewers als horizontale Zeile mit Farbfeldern angezeigt.

Der folgende CSS-Klassenselektor steuert die Position und Ausrichtung des interaktiven Farbfelderbedienfelds:

```
.s7interactivevideoviewer .s7interactiveswatches
```

## CSS-Eigenschaften der interaktiven Muster {#css-properties-of-the-interactive-swatches}

<table id="table_352DAD495AE742E39B4F12629C43F712"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Breite des Bedienfelds für interaktive Muster </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Höhe des interaktiven Farbfelderbedienfelds. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Anfang </span> </p> </td> 
   <td colname="col2"> <p>Position des Bedienfelds für interaktive Muster am Anfang. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> unten </span> </p> </td> 
   <td colname="col2"> <p>Unterste Position des interaktiven Farbfelderbedienfelds. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> links </span> </p> </td> 
   <td colname="col2"> <p>Linke Position des interaktiven Farbfelderbedienfelds. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> rechts </span> </p> </td> 
   <td colname="col2"> <p>Die rechte Position des interaktiven Farbfelderbedienfelds. </p> </td> 
  </tr> 
 </tbody> 
</table>

Die Laufzeitposition und Ausrichtung des interaktiven Farbfelderbedienfelds wird durch eine Kombination der oben genannten CSS-Eigenschaften wie folgt definiert:

* Um interaktive Muster horizontal am unteren Rand des Viewers zu rendern, legen Sie die Höhe auf einen absoluten Pixelwert fest. links und unten bis 0px; width, right und top to auto.
* Um interaktive Muster vertikal rechts neben dem Videoinhalt zu rendern, legen Sie die Breite auf ein absolutes Pixel fest. rechts und oben bis 0px; Höhe, links und unten nach Auto.

Es ist möglich, CSS-Markierungen in Verbindung mit dieser Formatierung zu verwenden, um eine adaptive Platzierung des interaktiven Farbfelderbedienfelds zu erreichen.

## Beispiel {#example}

So richten Sie ein interaktives Farbfeldbedienfeld ein, das am unteren Rand des Viewers auf Touch-Geräten im Querformat horizontal dargestellt und in allen anderen Fällen vertikal rechts neben dem Videoinhalt angezeigt wird:

```
.s7interactivevideoviewer.s7touchinput.s7device_landscape .s7interactiveswatches, 
.s7interactivevideoviewer.s7mouseinput .s7interactiveswatches { 
 width:120px; 
 height:auto; 
 right:0px; 
 top:0px; 
 left:auto; 
 bottom:auto; 
} 
.s7interactivevideoviewer.s7touchinput.s7device_portrait .s7interactiveswatches { 
 width:auto; 
 height:136px; 
 right:auto; 
 top:auto; 
 left:0px; 
 bottom:0px; 
}
```

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

Größe und Position des Banners werden von der Komponente für interaktive Muster verwaltet, die auf anderen Stilen basiert, die mit CSS angewendet werden, und können nicht explizit festgelegt werden.

Die folgende CSS-Klassenauswahl steuert das Erscheinungsbild des Bannerbedienfelds:

```
.s7interactivevideoviewer .s7interactiveswatches .s7banner
```

## CSS-Eigenschaften des Bannerbedienfelds {#css-properties-of-the-banner-panel}

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p>Hintergrundfarbe des Bannerbedienfelds. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> color </span> </p> </td> 
   <td colname="col2"> <p>Textfarbe im Bannerbedienfeld. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> rand </span> </p> </td> 
   <td colname="col2"> <p>Rand um das Bannerbedienfeld herum. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-Gewichtung </span> </p> </td> 
   <td colname="col2"> <p>Die Schriftart-Gewichtung, die für den Text im Bannerbedienfeld verwendet wird. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size </span> </p> </td> 
   <td colname="col2"> <p>Die Schriftgröße, die für den Text im Bannerbedienfeld verwendet wird. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family </span> </p> </td> 
   <td colname="col2"> <p>Die Schriftfamilie, die für den Text im Bannerbedienfeld verwendet wird. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-align </span> </p> </td> 
   <td colname="col2"> <p>Die Schriftausrichtung für den Text im Bannerbedienfeld. </p> </td> 
  </tr> 
 </tbody> 
</table>

Die QuickInfo für Banner kann lokalisiert werden. Weitere Informationen finden Sie unter [Lokale Anpassung der Elemente](../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) der Benutzeroberfläche.

## Beispiel {#section-e8caea0a303c425a8a637c2a47c06355}

Um ein Banner mit dunkelgrauem Hintergrund einzurichten, heller grauer Rand mit zwei Pixeln und weißer Text horizontal zentriert:

```
.s7interactivevideoviewer .s7interactiveswatches .s7banner { 
    background-color: #222222; 
    border-bottom: 2px solid #444444; 
    color: #ffffff; 
    text-align: center; 
}
```

Der folgende CSS-Klassenselektor steuert das Erscheinungsbild der Muster:

```
.s7interactivevideoviewer .s7interactiveswatches .s7swatches
```

## CSS-Eigenschaften des Farbfeldbereichs {#css-properties-of-the-swatches-area}

<table id="table_45E98E96B07246CAA5D3076FAF62A0B3"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p>Hintergrundfarbe des Farbfeldbereichs. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Beispiel {#section-9cadd62a09fd44a280f55ff42437e416}

So richten Sie einen Farbfeldbereich mit dunkelgrauem Hintergrund ein:

```
.s7interactivevideoviewer .s7interactiveswatches .s7swatches { 
    background-color: #222222; 
}
```

Der folgende CSS-Klassenselektor steuert den Abstand zwischen den Musterminiaturen:

`.s7interactivevideoviewer .s7interactiveswatches .s7swatches .s7thumbcell`

## CSS-Eigenschaften des Farbfeldminiaturenabstands {#css-properties-of-the-swatches-thumbnail-spacing}

<table id="table_FE6A749EA3894956998D50EA4AB6497B"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margin </span> </p> </td> 
   <td colname="col2"> <p> Die Größe des horizontalen und vertikalen Randes um die einzelnen Miniaturansichten. Der tatsächliche Abstand der Miniaturansichten entspricht der Summe des linken und rechten Randes, der für <span class="codeph"> .s7thumbcell festgelegt wurde </span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Beispiel {#section-39fb270b7e494a9d99e6e8f6890ec53c}

So legen Sie einen vertikalen Abstand von 10 Pixel fest:

```
.s7interactivevideoviewer .s7interactiveswatches .s7swatches .s7thumbcell { 
 margin: 5px; 
}
```

Der folgende CSS-Klassenselektor steuert das Erscheinungsbild der einzelnen Miniaturansichten:

`.s7interactivevideoviewer .s7interactiveswatches .s7swatches .s7thumb`

## CSS-Eigenschaften des Erscheinungsbilds einzelner Miniaturansichten {#css-properties-of-the-appearance-of-individual-thumbnails}

<table id="table_FB760FE6BEA44E129C07DD912C86DE57"> 
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
>Miniaturansicht unterstützt die `state` Attributauswahl, mit der Sie verschiedene Skins auf verschiedene Miniaturansichten anwenden können. entspricht insbesondere `state="selected"` der Miniaturansicht des derzeit ausgewählten Bildes; entspricht `state="default"` dem Rest der Miniaturansichten; wird `state="over"` beim Bewegen der Maus verwendet.

## Beispiel {#section-69fec189ffaa440b97b6b846c320b75b}

So richten Sie Miniaturansichten mit 100 x 75 Pixeln ein:

```
.s7interactivevideoviewer .s7interactiveswatches .s7swatches .s7thumb { 
 width:100px; 
 height:75px; 
}
```

Der folgende CSS-Klassenselektor steuert das Erscheinungsbild der Miniaturansichtsbeschriftung:

`.s7interactivevideoviewer .s7interactiveswatches .s7swatches .s7label`

## CSS-Eigenschaften des Erscheinungsbilds der Miniaturansichten-Beschriftung {#css-properties-of-the-appearance-of-the-thumbnail-label}

<table id="table_81B3209FB8124FFA9DB81FD35717900D"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> color </span> </p> </td> 
   <td colname="col2"> <p>Textfarbe. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> rand </span> </p> </td> 
   <td colname="col2"> <p>Beschriftungsrand. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> text-align </span> </p> </td> 
   <td colname="col2"> <p>Horizontale Textausrichtung. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family </span> </p> </td> 
   <td colname="col2"> <p>Schriftname. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Beispiel {#section-eb141eb6c1154183baa69796edb90536}

So richten Sie Beschriftungen so ein, dass sie linksbündig, weiß, 12 Pixel in Helvetica-Schrift und einen unteren Rand verwenden:

```
.s7interactivevideoviewer .s7interactiveswatches .s7swatches .s7label { 
 border-bottom: 1px solid #e9e9e9; 
 text-align: left; 
color: #ffffff; 
font-family: Helvetica,sans-serif; 
font-size: 12px; 
}
```

Der folgende CSS-Klassenselektor steuert das Erscheinungsbild der Schaltflächen für den Bildlauf nach oben und nach unten:

`.s7interactivevideoviewer .s7interactiveswatches .s7scrollupbutton`

`.s7interactivevideoviewer .s7interactiveswatches .s7scrolldownbutton`

Es ist nicht möglich, die Bildlaufschaltflächen mithilfe von CSS `top`, `left`, `bottom`und `right` -Eigenschaften zu positionieren. Stattdessen werden sie von der Viewer-Logik automatisch positioniert.

## CSS-Eigenschaften des Erscheinungsbilds der Schaltflächen für den Bildlauf nach oben und unten {#css-properties-of-the-appearance-of-the-up-and-down-scroll-buttons}

<table id="table_48AF27AFBB1543288D45449D6900675C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Breite der Bildlaufschaltfläche. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Höhe der Bildlauftaste. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image </span> </p> </td> 
   <td colname="col2"> <p>Das Bild, das für einen bestimmten Schaltflächenstatus angezeigt wird. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p>Die Position innerhalb des Grafik-Sprites, wenn CSS-Sprites verwendet werden. </p> <p>Siehe auch <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-customizingviewer/c-html5-aem-int-video-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> CSS-Sprites </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Diese Schaltfläche unterstützt die `state` Attributauswahl, mit der Sie verschiedene Skins auf die Schaltflächenzustände anwenden können: &quot; `up`&quot;, &quot; `down`&quot;, &quot; `over`&quot;und &quot; `disabled`&quot;.

Die QuickInfos für Schaltflächen können lokalisiert werden. Weitere Informationen finden Sie unter [Lokale Anpassung der Elemente](../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) der Benutzeroberfläche.

## Beispiel {#section-e6ce4fa084b84288bc7583342b2c510c}

Um eine Bildlaufschaltfläche von 60 x 36 Pixel einzurichten, müssen Sie für jeden Status ein anderes Bildmaterial verwenden, das aus dem Sprite-Bild der Komponente stammt:

```
.s7interactivevideoviewer .s7interactiveswatches .s7scrollupbutton { 
 background-size: 120px; 
 width: 60px; 
 height: 36px;  
} 
.s7interactivevideoviewer .s7interactiveswatches .s7scrollupbutton[state] { 
 background-image: url(images/v2/InteractiveSwatches_light_sprite.png); 
} 
.s7interactivevideoviewer .s7interactiveswatches .s7scrollupbutton[state='up'] { background-position: -60px -684px; } 
.s7interactivevideoviewer .s7interactiveswatches .s7scrollupbutton[state='over'] { background-position: -0px -684px; } 
.s7interactivevideoviewer .s7interactiveswatches .s7scrollupbutton[state='down'] { background-position: -60px -648px; } 
.s7interactivevideoviewer .s7interactiveswatches .s7scrollupbutton[state='disabled'] { background-position: -0px -648px; }
```

