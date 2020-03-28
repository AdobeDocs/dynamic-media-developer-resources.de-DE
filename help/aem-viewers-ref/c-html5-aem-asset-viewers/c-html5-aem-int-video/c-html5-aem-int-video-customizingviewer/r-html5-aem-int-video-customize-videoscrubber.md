---
description: Der Video-Scrubber ist der horizontale Regler, mit dem ein Benutzer dynamisch nach einer beliebigen Zeitposition innerhalb des derzeit wiedergegebenen Videos suchen kann.
seo-description: Der Video-Scrubber ist der horizontale Regler, mit dem ein Benutzer dynamisch nach einer beliebigen Zeitposition innerhalb des derzeit wiedergegebenen Videos suchen kann.
seo-title: Video-Scrubber
solution: Experience Manager
title: Video-Scrubber
topic: Dynamic media
uuid: cfd1055b-c4d6-42e4-ad24-a897e923e8e9
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef

---


# Video scrubber{#video-scrubber}

Der Video-Scrubber ist der horizontale Regler, mit dem ein Benutzer dynamisch nach einer beliebigen Zeitposition innerhalb des derzeit wiedergegebenen Videos suchen kann.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

Der Navigationsleisten-Knopf bewegt sich auch, während das Video abgespielt wird, um die aktuelle Zeitposition des Videos während der Wiedergabe anzugeben. Der Video-Scrubber nimmt immer die gesamte Breite der Steuerleiste ein. Es ist möglich, den Video-Scrubber in die Haut zu stecken. ihre Höhe und ihre vertikale Position durch CSS ändern.

Das allgemeine Erscheinungsbild des Video-Scrubbers wird mit der folgenden CSS-Klassenauswahl gesteuert:

```
.s7interactivevideoviewer .s7videoscrubber 
.s7interactivevideoviewer .s7videoscrubber .s7videotime 
.s7interactivevideoviewer .s7videoscrubber .s7knob
```

**CSS-Eigenschaften des Videobildschirms**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Anfang </span> </p> </td> 
   <td colname="col2"> <p>Position vom oberen Rand, einschließlich Auffüllung. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> unten </span> </p> </td> 
   <td colname="col2"> <p> Position vom unteren Rand, einschließlich Auffüllung. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Höhe des Videobildschirms. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p>Die Farbe des Videobildschirms. </p> </td> 
  </tr> 
 </tbody> 
</table>

Die folgenden CSS-Klassenselektoren verfolgen Hintergrund-, Wiedergabe- und Load-Indikatoren:

```
.s7interactivevideoviewer .s7videoscrubber .s7track 
.s7interactivevideoviewer .s7videoscrubber .s7trackloaded 
.s7interactivevideoviewer .s7videoscrubber .s7trackplayed
```

**CSS-Eigenschaften der Verfolgung**

<table id="table_46903DCACF314426B67783167ADF7715"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Höhe der entsprechenden Spur. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p>Die Farbe der entsprechenden Spur. </p> </td> 
  </tr> 
 </tbody> 
</table>

Der folgende CSS-Klassenselektor steuert den Knoten:

```
.s7interactivevideoviewer .s7videoscrubber .s7knob
```

**CSS-Eigenschaften des Knotens**

<table id="table_966826FB81114362A8D81D1EED38D512"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Anfang </span> </p> </td> 
   <td colname="col2"> <p>Vertikaler Knopfversatz. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Breite des Knopfes. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Höhe des Knopfes. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image </span> </p> </td> 
   <td colname="col2"> <p>Knob-Grafik. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p> Position innerhalb des Bildausschnitt, wenn CSS-Sprites verwendet werden. </p> <p>Siehe <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-customizingviewer/c-html5-aem-int-video-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> CSS-Sprites </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

Mit dem folgenden CSS-Klassenselektor wird die Wiedergabedauer gesteuert:

```
.s7interactivevideoviewer .s7videoscrubber .s7videotime
```

**CSS-Eigenschaften der Wiedergabepause**

<table id="table_21E9AD3FBC8C4437BA02E5CD1BF7E831"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family </span> </p> </td> 
   <td colname="col2"> <p> Die Schriftfamilie, die für die Zeitanzeige verwendet wird. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size </span> </p> </td> 
   <td colname="col2"> <p> Die Schriftgröße, die für die Zeitanzeige verwendet wird. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> color </span> </p> </td> 
   <td colname="col2"> <p> Die Schriftfarbe, die für die Zeitanzeige verwendet wird. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Punktflächenbreite. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Punktflächenhöhe. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Padding </span> </p> </td> 
   <td colname="col2"> <p>Punktflächenfüllung. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image </span> </p> </td> 
   <td colname="col2"> <p>Blasengrafik. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p> Position innerhalb des Bildausschnitt, wenn CSS-Sprites verwendet werden. </p> <p>Siehe <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-customizingviewer/c-html5-aem-int-video-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> CSS-Sprites </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> text-align </span> </p> </td> 
   <td colname="col2"> <p>Ausrichtung des Textes am Blasenbereich </p> </td> 
  </tr> 
 </tbody> 
</table>

Die QuickInfo zum Video-Scrubber kann lokalisiert werden. Weitere Informationen finden Sie unter [Lokale Anpassung der Elemente](../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) der Benutzeroberfläche.

**Beispiel** : Zum Einrichten eines Video-Viewers mit einem Video-Scrubber mit benutzerdefinierten Trackfarben, die 10 Pixel hoch und 10 Pixel und 35 Pixel von der oberen und linken Kante der Steuerleiste entfernt sind.

```
.s7interactivevideoviewer .s7videoscrubber  { 
top:10px; 
left:35px; 
height:10px; 
background-color:#AAAAAA; 
} 
.s7interactivevideoviewer .s7videoscrubber .s7track { 
height:10px; 
background-color:#444444; 
} 
.s7interactivevideoviewer .s7videoscrubber .s7trackloaded { 
height:10px; 
background-color:#666666; 
} 
.s7interactivevideoviewer .s7videoscrubber .s7trackplayed { 
height:10px; 
background-color:#888888; 
}
```

Wenn das Videochaptern mit dem `navigation` Parameter aktiviert ist, werden die Kapitelpositionen als Markierungen auf der Video-Navigationsleiste angezeigt.

Die Videokapitelmarke wird von der folgenden CSS-Klassenauswahl gesteuert:

```
.s7interactivevideoviewer .s7videoscrubber .s7navigation
```

**CSS-Eigenschaften der Videokapitelmarke**

<table id="table_51F16E47BEF3430B919ABEEDBE543973"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Breite der Videokapitelmarke. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Höhe der Videokapitelmarke. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image </span> </p> </td> 
   <td colname="col2"> <p>Grafik zur Videokapitelmarke. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p> Position innerhalb des Bildausschnitt, wenn CSS-Sprites verwendet werden. </p> <p>Siehe <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-customizingviewer/c-html5-aem-int-video-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> CSS-Sprites </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Diese Schaltfläche unterstützt die `state` Attributauswahl, mit der Sie verschiedene Skins auf verschiedene Schaltflächenzustände anwenden können. Insbesondere `selected='default'` entspricht dies dem Standard-Videokapitelmarkierungsstatus und `selected='over'` wird verwendet, wenn die Videokapitelmarke durch eine Maus- oder Berührungsgeste aktiviert wird.

**Beispiel** : Um eine Kapitelmarke für Videos mit 5 x 8 Pixeln einzurichten, die für den Status &quot;Standard&quot;und &quot;Over&quot;unterschiedliche Grafiken verwendet.

```
.s7interactivevideoviewer .s7videoscrubber .s7navigation { 
width:5px; 
height:8px; 
} 
.s7interactivevideoviewer .s7videoscrubber .s7navigation[state="default"] { 
background-image: url("images/v2/VideoScrubberDiamond.png"); 
} 
.s7interactivevideoviewer .s7videoscrubber .s7navigation[state="over"] { 
background-image: url("images/v2/VideoScrubberDiamond_over.png"); 
}
```

Die Kapitelblase für Videos wird über der Videokapitelmarke platziert und zeigt den Beginn, die Uhrzeit und die Beschreibung für ein bestimmtes Kapitel an. Es ist möglich, die maximale Blasenbreite und den vertikalen Versatz relativ zur Videobildspur zu steuern. Der Rest wird automatisch von der Komponente berechnet.

Die Kapitelblase für Videos wird durch den folgenden CSS-Klassenselektor gesteuert:

```
.s7interactivevideoviewer .s7videoscrubber .s7chapter
```

**CSS-Eigenschaften der Videokapitelblase**

<table id="table_7F33738422F84978B9132495F67C2156"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> max-width </span> </p> </td> 
   <td colname="col2"> <p>Maximale Breite des Videokapitels. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> unten </span> </p> </td> 
   <td colname="col2"> <p>Vertikaler Versatz zur Videobildspur. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Beispiel** : Um eine Videokapitelblase einzurichten, die 235 Pixel breit und 8 Pixel hoch vom unteren Rand der Videokassettenspur entfernt ist.

```
.s7interactivevideoviewer .s7videoscrubber .s7chapter { 
max-width:235px; 
bottom:8px; 
}
```

Die Kapitelblase für Videos besteht aus einer optionalen Kopfzeile und einem optionalen Inhalt. Die Kopfzeile verfügt über die optionale Kapitelzeit und den Beginn des Kapitels.

Die Kopfzeile wird von der folgenden CSS-Klassenauswahl gesteuert:

```
.s7interactivevideoviewer .s7videoscrubber .s7chapter .s7header
```

**CSS-Eigenschaften der Kopfzeile des Videokapitels**

<table id="table_56FBC3BADDEA4E15924DD750CADC474F"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Höhe der Kopfzeile des Videokapitels. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Padding </span> </p> </td> 
   <td colname="col2"> <p>Innenabstand für Videokapitelblasen-Kopfzeilentext. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p>Hintergrundfarbe für Videokapitelblase-Kopfzeile. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> line-height </span> </p> </td> 
   <td colname="col2"> <p>Höhe der Kopfzeile des Videokapitels </p> </td> 
  </tr> 
 </tbody> 
</table>

**Beispiel** : Zum Einrichten eines Videokapitelblasen-Headers mit einer Höhe von 22 Pixel, einer Zeilenhöhe von 22 Pixel, einem horizontalen Rand von 12 Pixel und einem grauen Hintergrund.

```
.s7interactivevideoviewer .s7videoscrubber .s7chapter .s7header { 
height:22px; 
padding:0 12px; 
line-height:22px; 
background-color: rgba(51, 51, 51, 0.8); 
}
```

Die Beginn-Zeit des Videokapitels wird durch die folgende CSS-Klassenauswahl gesteuert:

```
.s7interactivevideoviewer .s7videoscrubber .s7chapter .s7header .s7starttime
```

**CSS-Eigenschaften der Videokapitel-Beginn-Zeit**

<table id="table_D58D6B22BAEE4E26BAAB34783AE5A044"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> color </span> </p> </td> 
   <td colname="col2"> <p>Textfarbe. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-Gewichtung </span> </p> </td> 
   <td colname="col2"> <p>Schriftart-Gewichtung. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size </span> </p> </td> 
   <td colname="col2"> <p>Schriftgröße. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family </span> </p> </td> 
   <td colname="col2"> <p>Schriftfamilie. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> padding-right </span> </p> </td> 
   <td colname="col2"> <p> Auffüllung zwischen der Beginn- und Kapitelzeit. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Beispiel** : Zum Einrichten der Kapitelzeit mit einer grauen 10 Pixel hohen Verdana-Schrift und einer 10 Pixel langen Auffüllung rechts.

```
.s7interactivevideoviewer .s7videoscrubber .s7chapter .s7header .s7starttime { 
color: #dddddd; 
font-family: Verdana,Arial,Helvetica,sans-serif; 
font-size: 10px; 
padding-right: 10px; 
}
```

Der Titel des Videokapitels wird von der folgenden CSS-Klassenauswahl gesteuert:

```
.s7interactivevideoviewer .s7videoscrubber .s7chapter .s7header .s7title
```

**CSS-Eigenschaften des Videokapiteltitels**

<table id="table_240DD3E119584DCC95FF480B60266603"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> color </span> </p> </td> 
   <td colname="col2"> <p>Textfarbe des Videokapitels </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-Gewichtung </span> </p> </td> 
   <td colname="col2"> <p>Gewichtung der Videokapitelschrift </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size </span> </p> </td> 
   <td colname="col2"> <p>Schriftgröße des Videokapitels </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family </span> </p> </td> 
   <td colname="col2"> <p>Schriftfamilie des Videokapitels </p> </td> 
  </tr> 
 </tbody> 
</table>

**Beispiel** : Zum Einrichten eines Videokapiteltitels mit einer weißen, fett gedruckten Verdana-Schrift mit zehn Pixeln.

```
.s7interactivevideoviewer .s7videoscrubber .s7chapter .s7header .s7title { 
color: #ffffff; 
font-family: Verdana,Arial,Helvetica,sans-serif; 
font-size: 10px; 
font-weight: bold; 
}
```

Die Beschreibung des Videokapitels wird von der folgenden CSS-Klassenauswahl gesteuert:

```
.s7interactivevideoviewer .s7videoscrubber .s7chapter .s7description
```

**CSS-Eigenschaften der Videokapitelbeschreibung**

<table id="table_780382ECB3D049118857DCA21D130326"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> color </span> </p> </td> 
   <td colname="col2"> <p>Textfarbe der Videokapitelbeschreibung. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p>Hintergrundfarbe der Videokapitelbeschreibung. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-Gewichtung </span> </p> </td> 
   <td colname="col2"> <p>Gewichtung der Videokapitelbeschreibung </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size </span> </p> </td> 
   <td colname="col2"> <p>Schriftgröße der Videokapitelbeschreibung. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family </span> </p> </td> 
   <td colname="col2"> <p>Schriftfamilie der Videokapitelbeschreibung. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> line-height </span> </p> </td> 
   <td colname="col2"> <p>Zeilenhöhe der Videokapitelbeschreibung. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Padding </span> </p> </td> 
   <td colname="col2"> <p>Beschreibung des Videokapitels nach innen. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Beispiel** : Zum Einrichten einer Videokapitelbeschreibung mit einer dunkelgrauen, 11 Pixel großen Verdana-Schrift mit einem hellgrauen Hintergrund; 5 Pixel Zeilenhöhe, 12 Pixel horizontale Auffüllung, 12 Pixel obere Auffüllung und 9 Pixel untere Auffüllung.

```
.s7interactivevideoviewer .s7videoscrubber .s7chapter .s7description { 
color: #333333; 
background-color: rgba(221, 221, 221, 0.9); 
font-family: Verdana,Arial,Helvetica,sans-serif; 
font-size: 11px; 
line-height: 15px; 
padding: 12px 12px 9px; 
}
```

Der Keil-Anschluss am unteren Rand der Kapitelblase wird durch den folgenden CSS-Klassenselektor gesteuert:

```
.s7interactivevideoviewer .s7videoscrubber .s7chapter .s7tail
```

**CSS-Eigenschaften des Keil-Connectors**

<table id="table_BC6AFB57D9404A84A3AE657448C0EB06"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> border-color </span> </p> </td> 
   <td colname="col2"> <p>Farbe des Wedge-Connectors. </p> <p>Wird als <span class="codeph"> &lt;color&gt; transparent definiert, </span> sodass nur die Farbe des oberen Randes definiert und die übrigen Ränder transparent bleiben. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> border-width </span> </p> </td> 
   <td colname="col2"> <p> Breite des Wedge-Anschlusses. </p> <p>Wird als <span class="codeph"> &lt;width&gt; &lt;width&gt; 0 definiert, </span> sodass dieselbe Breite nur für den oberen und den horizontalen Rahmen und die untere Rahmenbreite <span class="codeph"> 0 beträgt </span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margin </span> </p> </td> 
   <td colname="col2"> <p> Definiert nur einen negativen unteren Rand. Er sollte denselben Wert haben wie der Wert für <span class="codeph"> Rahmenbreite </span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Beispiel** : Zum Einrichten eines grauen, sechs Pixel großen Keil-Anschlusses:

```
.s7interactivevideoviewer .s7videoscrubber .s7chapter .s7tail { 
border-color: rgba(221, 221, 221, 0.9) transparent transparent; 
border-width: 6px 6px 0; 
margin: 0 0 0 -6px; 
}
```

