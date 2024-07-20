---
title: Interaktive Muster
description: Das interaktive Bedienfeld "Muster"wird neben dem Videoinhalt angezeigt, wenn interaktive Daten in der Konfiguration an den Viewer übergeben wurden. Es besteht aus einem Banner oben, das Text wie "Click to View", eine Spalte mit mindestens einem interaktiven Farbfeld und zwei Bildlauftasten (nur auf Desktop-Systemen verfügbar) rendert.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: c9ef02eb-f5db-474b-b234-c49508e2af35
source-git-commit: 6aaf4eccf51a05d200c6cc780e342be646d104d8
workflow-type: tm+mt
source-wordcount: '888'
ht-degree: 0%

---

# Interaktive Muster{#interactive-swatches}

Das interaktive Bedienfeld &quot;Muster&quot;wird neben dem Videoinhalt angezeigt, wenn interaktive Daten in der Konfiguration an den Viewer übergeben wurden. Es besteht aus einem Banner oben, das Text wie &quot;Click to View&quot;, eine Spalte mit mindestens einem interaktiven Farbfeld und zwei Bildlauftasten (nur auf Desktop-Systemen verfügbar) rendert.

<!--<a id="section_235621A1533A49AAADB64A7C3191F735"></a>-->

Auf Desktop-Systemen und Touch-Geräten werden interaktive Muster im Querformat vertikal rechts neben dem Videoinhalt gerendert. Auf Touch-Geräten mit Hochformatausrichtung werden sie unten im Viewer als horizontale Zeile mit Farbfeldern angezeigt.

Der folgende CSS-Klassenselektor steuert die Position und Ausrichtung des interaktiven Bedienfelds &quot;Muster&quot;:

```
.s7interactivevideoviewer .s7interactiveswatches
```

## CSS-Eigenschaften der interaktiven Muster {#css-properties-of-the-interactive-swatches}

<table id="table_352DAD495AE742E39B4F12629C43F712"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Breite des interaktiven Farbfeldbedienfelds </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Höhe </span> </p> </td> 
   <td colname="col2"> <p>Höhe des interaktiven Farbfeldbedienfelds. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> top </span> </p> </td> 
   <td colname="col2"> <p>Position am oberen Rand des interaktiven Bedienfelds "Muster". </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> unten </span> </p> </td> 
   <td colname="col2"> <p>Untere Position des interaktiven Bedienfelds "Farbfelder". </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> left </span> </p> </td> 
   <td colname="col2"> <p>Linke Position des interaktiven Bedienfelds "Muster". </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> rechts </span> </p> </td> 
   <td colname="col2"> <p>Die rechte Position des interaktiven Bedienfelds "Muster". </p> </td> 
  </tr> 
 </tbody> 
</table>

Die Laufzeitposition und -ausrichtung des interaktiven Bedienfelds wird durch eine Kombination der oben genannten CSS-Eigenschaften wie folgt definiert:

* Um interaktive Muster horizontal am unteren Rand des Viewers zu rendern, legen Sie die Höhe auf einen absoluten Pixelwert fest, setzen Sie die Höhe auf &quot;Auto&quot;von links und von unten auf &quot;0px&quot;, &quot;Breite&quot;, &quot;Rechts&quot;und &quot;Oben&quot;auf &quot;Auto&quot;.
* Um interaktive Muster vertikal rechts neben dem Videoinhalt zu rendern, legen Sie die Breite auf ein absolutes Pixel fest, rechts und oben auf 0px, Höhe, links und unten auf auto.

Es ist möglich, CSS-Markierungen mit diesem Stil zu verwenden, um eine adaptive Platzierung des interaktiven Bedienfelds &quot;Muster&quot;zu erreichen.

## Beispiel {#example}

So richten Sie ein interaktives Bedienfeld für Muster ein, das am unteren Rand des Viewers auf Touch-Geräten horizontal im Querformat dargestellt wird. Und um ihn in allen anderen Fällen vertikal rechts neben dem Videoinhalt anzuzeigen:

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

Größe und Position des Banners werden von der interaktiven Farbfeldkomponente verwaltet, die auf anderen Stilen basiert, die mit CSS angewendet werden, und können nicht explizit festgelegt werden.

Der folgende CSS-Klassenselektor steuert das Erscheinungsbild des Bannerbereichs:

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
   <td colname="col2"> <p>Textfarbe im Bannerbereich. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> border </span> </p> </td> 
   <td colname="col2"> <p>Rand um das Bannerbedienfeld herum. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-weight </span> </p> </td> 
   <td colname="col2"> <p>Die Schriftstärke für den Text im Bannerbereich. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size </span> </p> </td> 
   <td colname="col2"> <p>Die Schriftgröße für den Text im Bannerbereich. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Schriftfamilie </span> </p> </td> 
   <td colname="col2"> <p>Die Schriftfamilie für den Text im Bannerbereich. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-align </span> </p> </td> 
   <td colname="col2"> <p>Die Schriftausrichtung für den Text im Bannerbereich. </p> </td> 
  </tr> 
 </tbody> 
</table>

Die Banner-QuickInfo kann lokalisiert werden. Weitere Informationen finden Sie unter [Lokalisierung von Benutzeroberflächenelementen](../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) .

## Beispiel {#section-e8caea0a303c425a8a637c2a47c06355}

Um ein Banner mit dunkelgrauem Hintergrund einzurichten, verwenden Sie einen helleren, zwei Pixel langen Rahmen und den horizontal zentrierten weißen Text:

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

Der folgende CSS-Klassenselektor steuert den Abstand zwischen Musterminiaturansichten:

`.s7interactivevideoviewer .s7interactiveswatches .s7swatches .s7thumbcell`

## CSS-Eigenschaften des Farbfeldminiaturenabstands {#css-properties-of-the-swatches-thumbnail-spacing}

<table id="table_FE6A749EA3894956998D50EA4AB6497B"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margin </span> </p> </td> 
   <td colname="col2"> <p> Die Größe des horizontalen und vertikalen Rands um jede Miniaturansicht. Der tatsächliche Abstand der Miniaturansichten entspricht der Summe des linken und rechten Rands, der für <span class="codeph"> .s7thumbcell </span> festgelegt wurde. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Beispiel {#section-39fb270b7e494a9d99e6e8f6890ec53c}

So legen Sie einen vertikalen Abstand von zehn Pixeln fest:

```
.s7interactivevideoviewer .s7interactiveswatches .s7swatches .s7thumbcell { 
 margin: 5px; 
}
```

Der folgende CSS-Klassenselektor steuert das Erscheinungsbild einzelner Miniaturansichten:

`.s7interactivevideoviewer .s7interactiveswatches .s7swatches .s7thumb`

## CSS-Eigenschaften des Erscheinungsbilds einzelner Miniaturen {#css-properties-of-the-appearance-of-individual-thumbnails}

<table id="table_FB760FE6BEA44E129C07DD912C86DE57"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Breite der Miniaturansicht. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Höhe </span> </p> </td> 
   <td colname="col2"> <p>Höhe der Miniaturansicht. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> border </span> </p> </td> 
   <td colname="col2"> <p>Rand der Miniaturansicht. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Miniaturansicht unterstützt die &quot;`state`&quot;-Attributauswahl, mit der Sie verschiedene Skins auf verschiedene Miniaturansichten anwenden können. Insbesondere entspricht `state="selected"` der Miniaturansicht des aktuell ausgewählten Bildes; `state="default"` der restlichen Miniaturansicht; `state="over"` wird beim Bewegen des Mauszeigers verwendet.

## Beispiel {#section-69fec189ffaa440b97b6b846c320b75b}

So richten Sie Miniaturansichten mit einer Größe von 100 x 75 Pixel ein:

```
.s7interactivevideoviewer .s7interactiveswatches .s7swatches .s7thumb { 
 width:100px; 
 height:75px; 
}
```

Der folgende CSS-Klassenselektor steuert das Erscheinungsbild der Miniaturansichtsbeschriftung:

`.s7interactivevideoviewer .s7interactiveswatches .s7swatches .s7label`

## CSS-Eigenschaften des Erscheinungsbilds der Bezeichnung der Miniaturansicht {#css-properties-of-the-appearance-of-the-thumbnail-label}

<table id="table_81B3209FB8124FFA9DB81FD35717900D"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> color </span> </p> </td> 
   <td colname="col2"> <p>Textfarbe. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> border </span> </p> </td> 
   <td colname="col2"> <p>Beschriftungsrahmen </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> text-align </span> </p> </td> 
   <td colname="col2"> <p>Horizontale Textausrichtung. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Schriftfamilie </span> </p> </td> 
   <td colname="col2"> <p>Schriftname. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Beispiel {#section-eb141eb6c1154183baa69796edb90536}

So richten Sie Beschriftungen für linksbündig, weiß, 12 Pixel in der Helvetica®-Schriftart und einen unteren Rand ein:

```
.s7interactivevideoviewer .s7interactiveswatches .s7swatches .s7label { 
 border-bottom: 1px solid #e9e9e9; 
 text-align: left; 
color: #ffffff; 
font-family: Helvetica,sans-serif; 
font-size: 12px; 
}
```

Der folgende CSS-Klassenselektor steuert das Erscheinungsbild der Bildlaufschaltflächen nach oben und unten:

`.s7interactivevideoviewer .s7interactiveswatches .s7scrollupbutton`

`.s7interactivevideoviewer .s7interactiveswatches .s7scrolldownbutton`

Es ist nicht möglich, die Bildlaufschaltflächen mit den Eigenschaften CSS `top`, `left`, `bottom` und `right` zu positionieren. Stattdessen werden sie von der Viewer-Logik automatisch positioniert.

## CSS-Eigenschaften des Erscheinungsbilds der Bildlaufschaltflächen nach oben und unten {#css-properties-of-the-appearance-of-the-up-and-down-scroll-buttons}

<table id="table_48AF27AFBB1543288D45449D6900675C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Breite der Bildlaufschaltfläche. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Höhe </span> </p> </td> 
   <td colname="col2"> <p>Höhe der Bildlaufschaltfläche. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image </span> </p> </td> 
   <td colname="col2"> <p>Das Bild, das für einen bestimmten Schaltflächenstatus angezeigt wird. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p>Die Position innerhalb des Bildsprites, wenn CSS-Sprites verwendet werden. </p> <p>Siehe auch <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-customizingviewer/c-html5-aem-int-video-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> CSS-Sprites </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Diese Schaltfläche unterstützt den Attributselektor `state` , mit dem Sie verschiedene Skins auf die Schaltflächenstatus anwenden können: &quot; `up`&quot;, &quot; `down`&quot;, &quot;`over`&quot;und &quot;`disabled`&quot;.

Die QuickInfos für Schaltflächen können lokalisiert werden. Weitere Informationen finden Sie unter [Lokalisierung von Benutzeroberflächenelementen](../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) .

## Beispiel {#section-e6ce4fa084b84288bc7583342b2c510c}

Um eine Bildlaufschaltfläche von 60 x 36 Pixel einzurichten, verwenden Sie für jeden Status ein anderes Bildmaterial und nehmen dieses Bildmaterial aus dem Sprite-Bild der Komponente:

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
