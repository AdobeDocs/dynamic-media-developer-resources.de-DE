---
title: Interaktive Farbfelder
description: Das Bedienfeld Interaktive Farbfelder wird neben dem Videoinhalt angezeigt, wenn in der -Konfiguration interaktive Daten an den Viewer übergeben wurden. Es besteht aus einem Banner oben, das Text rendert, z. B. „Click to View“, eine Spalte mit einem oder mehreren interaktiven Farbfeldern und zwei Bildlaufschaltflächen (nur auf Desktop-Systemen verfügbar).
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: c9ef02eb-f5db-474b-b234-c49508e2af35
source-git-commit: 6aaf4eccf51a05d200c6cc780e342be646d104d8
workflow-type: tm+mt
source-wordcount: '888'
ht-degree: 0%

---

# Interaktive Farbfelder{#interactive-swatches}

Das Bedienfeld Interaktive Farbfelder wird neben dem Videoinhalt angezeigt, wenn in der -Konfiguration interaktive Daten an den Viewer übergeben wurden. Es besteht aus einem Banner oben, das Text rendert, z. B. „Click to View“, eine Spalte mit einem oder mehreren interaktiven Farbfeldern und zwei Bildlaufschaltflächen (nur auf Desktop-Systemen verfügbar).

<!--<a id="section_235621A1533A49AAADB64A7C3191F735"></a>-->

Auf Desktop-Systemen und auf Touch-Geräten werden interaktive Farbfelder in Querformat vertikal rechts neben dem Videoinhalt gerendert. Auf Touch-Geräten in Hochformat werden sie am unteren Rand des Viewers als horizontale Reihe von Farbfeldern angezeigt.

Der folgende CSS-Klassenselektor steuert die Position und Ausrichtung des interaktiven Farbfeld-Bedienfelds:

```
.s7interactivevideoviewer .s7interactiveswatches
```

## CSS-Eigenschaften der interaktiven Farbfelder {#css-properties-of-the-interactive-swatches}

<table id="table_352DAD495AE742E39B4F12629C43F712"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Breite </span> </p> </td> 
   <td colname="col2"> <p>Breite des interaktiven Farbfeld-Panels </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Höhe </span> </p> </td> 
   <td colname="col2"> <p>Höhe des interaktiven Farbfeld-Panels. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Top-</span> </p> </td> 
   <td colname="col2"> <p>Obere Position des interaktiven Farbfeld-Bedienfelds. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> untere </span> </p> </td> 
   <td colname="col2"> <p>Untere Position des interaktiven Farbfeld-Bedienfelds. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> linker </span> </p> </td> 
   <td colname="col2"> <p>Linke Position des interaktiven Farbfeld-Bedienfelds. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> rechte </span> </p> </td> 
   <td colname="col2"> <p>Rechte Position des interaktiven Farbfeld-Panels. </p> </td> 
  </tr> 
 </tbody> 
</table>

Die Laufzeitposition und -ausrichtung des interaktiven Farbfeld-Bedienfelds wird durch eine Kombination der oben genannten CSS-Eigenschaften wie folgt definiert:

* Um interaktive Farbfelder horizontal am unteren Rand des Viewers zu rendern, setzen Sie die Höhe auf einen absoluten Pixelwert, links und unten auf 0px, Breite, rechts und oben auf auto.
* Um interaktive Farbfelder vertikal rechts neben dem Videoinhalt zu rendern, legen Sie die Breite auf ein absolutes Pixel fest; rechts und oben auf 0px; Höhe, links und unten auf auto.

Es ist möglich, CSS-Markierungen mit diesem Stil zu verwenden, um eine adaptive Platzierung des interaktiven Farbfeldbedienfelds zu erzielen.

## Beispiel {#example}

So richten Sie ein interaktives Farbfeld ein, das auf Touch-Geräten im Querformat horizontal am unteren Rand des Viewers gerendert wird. Und , um sie in allen anderen Fällen vertikal rechts neben dem Videoinhalt anzuzeigen:

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

Die Größe und Position des Banners werden von der interaktiven Farbfeld-Komponente auf der Grundlage anderer Stile verwaltet, die mit CSS angewendet werden, und können nicht explizit festgelegt werden.

Der folgende CSS-Klassenselektor steuert die Darstellung des Bannerbereichs:

```
.s7interactivevideoviewer .s7interactiveswatches .s7banner
```

## CSS-Eigenschaften des Bannerbedienfelds {#css-properties-of-the-banner-panel}

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">-</span> </p> </td> 
   <td colname="col2"> <p>Hintergrundfarbe des Bannerbedienfelds. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">-</span> </p> </td> 
   <td colname="col2"> <p>Textfarbe im Bannerbedienfeld. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">-</span> </p> </td> 
   <td colname="col2"> <p>Rahmen um das Bannerbedienfeld. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">-</span> </p> </td> 
   <td colname="col2"> <p>Die Schriftstärke, die für den Text im Bannerbereich verwendet werden soll. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">-</span> </p> </td> 
   <td colname="col2"> <p>Die Schriftgröße, die für den Text im Bannerbereich verwendet werden soll. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">-</span> </p> </td> 
   <td colname="col2"> <p>Die Schriftfamilie, die für den Text im Bannerbereich verwendet werden soll. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> </span> für die <span class="codeph">-Ausrichtung </p> </td> 
   <td colname="col2"> <p>Die Schriftausrichtung, die für den Text im Bannerbereich verwendet werden soll. </p> </td> 
  </tr> 
 </tbody> 
</table>

Die QuickInfo des Banners kann lokalisiert werden. Siehe [Lokalisierung von Benutzeroberflächenelementen](../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) für weitere Informationen.

## Beispiel {#section-e8caea0a303c425a8a637c2a47c06355}

So richten Sie ein Banner mit dunkelgrauem Hintergrund, einem hellgrauen Rahmen mit zwei Pixeln und einem horizontal zentrierten weißen Text ein:

```
.s7interactivevideoviewer .s7interactiveswatches .s7banner { 
    background-color: #222222; 
    border-bottom: 2px solid #444444; 
    color: #ffffff; 
    text-align: center; 
}
```

Der folgende CSS-Klassenselektor steuert die Darstellung der Farbfelder:

```
.s7interactivevideoviewer .s7interactiveswatches .s7swatches
```

## CSS-Eigenschaften des Farbfeldbereichs {#css-properties-of-the-swatches-area}

<table id="table_45E98E96B07246CAA5D3076FAF62A0B3"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">-</span> </p> </td> 
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

Der folgende CSS-Klassenselektor steuert den Abstand zwischen Musterminiaturen:

`.s7interactivevideoviewer .s7interactiveswatches .s7swatches .s7thumbcell`

## CSS-Eigenschaften der Miniaturansichten des Farbfelds {#css-properties-of-the-swatches-thumbnail-spacing}

<table id="table_FE6A749EA3894956998D50EA4AB6497B"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">-</span> </p> </td> 
   <td colname="col2"> <p> Die Größe des horizontalen und vertikalen Rands um jede Miniaturansicht. Der tatsächliche Abstand zwischen den Miniaturen entspricht der Summe des linken und rechten Rands, die für <span class="codeph"> s7thumbcell-</span> festgelegt wurden. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Beispiel {#section-39fb270b7e494a9d99e6e8f6890ec53c}

So legen Sie einen vertikalen Abstand von 10 Pixeln fest:

```
.s7interactivevideoviewer .s7interactiveswatches .s7swatches .s7thumbcell { 
 margin: 5px; 
}
```

Der folgende CSS-Klassenselektor steuert die Darstellung einzelner Miniaturen:

`.s7interactivevideoviewer .s7interactiveswatches .s7swatches .s7thumb`

## CSS-Eigenschaften der Darstellung einzelner Miniaturen {#css-properties-of-the-appearance-of-individual-thumbnails}

<table id="table_FB760FE6BEA44E129C07DD912C86DE57"> 
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
>Miniaturansicht unterstützt die `state` Attributauswahl , mit der Sie verschiedene Skins auf verschiedene Miniaturansichtszustände anwenden können. Insbesondere entspricht `state="selected"` der Miniatur für das aktuell ausgewählte Bild; `state="default"` entspricht dem Rest der Miniaturen; `state="over"` wird beim Bewegen des Mauszeigers verwendet.

## Beispiel {#section-69fec189ffaa440b97b6b846c320b75b}

So richten Sie Miniaturen mit einer Größe von 100 x 75 Pixel ein:

```
.s7interactivevideoviewer .s7interactiveswatches .s7swatches .s7thumb { 
 width:100px; 
 height:75px; 
}
```

Der folgende CSS-Klassenselektor steuert die Darstellung der Miniaturbildbeschriftung:

`.s7interactivevideoviewer .s7interactiveswatches .s7swatches .s7label`

## CSS-Eigenschaften der Darstellung der Miniaturbildbeschriftung {#css-properties-of-the-appearance-of-the-thumbnail-label}

<table id="table_81B3209FB8124FFA9DB81FD35717900D"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">-</span> </p> </td> 
   <td colname="col2"> <p>Textfarbe. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">-</span> </p> </td> 
   <td colname="col2"> <p>Rahmen kennzeichnen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> </span> zur Textausrichtung <span class="codeph"> </p> </td> 
   <td colname="col2"> <p>Horizontale Textausrichtung. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">-</span> </p> </td> 
   <td colname="col2"> <p>Schriftart. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Beispiel {#section-eb141eb6c1154183baa69796edb90536}

So richten Sie Beschriftungen für die Verwendung von linksbündig, weiß, 12 Pixel, in der Helvetica®-Schriftart und mit einem unteren Rahmen ein:

```
.s7interactivevideoviewer .s7interactiveswatches .s7swatches .s7label { 
 border-bottom: 1px solid #e9e9e9; 
 text-align: left; 
color: #ffffff; 
font-family: Helvetica,sans-serif; 
font-size: 12px; 
}
```

Der folgende CSS-Klassenselektor steuert die Darstellung der Schaltflächen für den Bildlauf nach oben und unten:

`.s7interactivevideoviewer .s7interactiveswatches .s7scrollupbutton`

`.s7interactivevideoviewer .s7interactiveswatches .s7scrolldownbutton`

Es ist nicht möglich, die Bildlaufschaltflächen mit den Eigenschaften CSS `top`, `left`, `bottom` und `right` zu positionieren. Stattdessen werden sie von der Viewer-Logik automatisch positioniert.

## CSS-Eigenschaften der Darstellung der Bildlaufschaltflächen nach oben und unten {#css-properties-of-the-appearance-of-the-up-and-down-scroll-buttons}

<table id="table_48AF27AFBB1543288D45449D6900675C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Breite </span> </p> </td> 
   <td colname="col2"> <p>Breite der Bildlaufschaltfläche. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Höhe </span> </p> </td> 
   <td colname="col2"> <p>Höhe der Bildlaufschaltfläche. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Hintergrundbild-</span> </p> </td> 
   <td colname="col2"> <p>Das Bild, das für einen bestimmten Schaltflächenstatus angezeigt wird. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Hintergrundposition </span> </p> </td> 
   <td colname="col2"> <p>Die Position innerhalb des Bildsets, wenn CSS-Sprites verwendet werden. </p> <p>Siehe auch <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-customizingviewer/c-html5-aem-int-video-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> CSS Sprites-</a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Diese Schaltfläche unterstützt die `state` Attributauswahl, mit der Sie verschiedene Skins auf die Schaltflächenzustände &quot;`up`&quot;, &quot;`down`&quot;, &quot;`over`&quot; und &quot;`disabled`&quot; anwenden können.

Die QuickInfos für die Schaltfläche können lokalisiert werden. Siehe [Lokalisierung von Benutzeroberflächenelementen](../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) für weitere Informationen.

## Beispiel {#section-e6ce4fa084b84288bc7583342b2c510c}

Um eine Bildlaufschaltfläche einzurichten, die 60 x 36 Pixel groß ist, weisen für jeden Status unterschiedliche Grafiken auf und nehmen diese Grafiken aus dem Sprite-Bild der Komponente:

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
