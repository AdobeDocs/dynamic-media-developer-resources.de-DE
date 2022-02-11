---
title: Videobauber
description: Der Video-Scrubber ist das horizontale Regler-Steuerelement, mit dem ein Benutzer dynamisch an eine beliebige Zeitposition innerhalb des derzeit wiedergegebenen Videos suchen kann
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Video
role: Developer,User
exl-id: 404e39d4-565e-4dde-b2bd-fa83a895d001
source-git-commit: ceb9483f67a19d969ecbbd01cede11f3dae86467
workflow-type: tm+mt
source-wordcount: '1025'
ht-degree: 2%

---

# Videobauber{#video-scrubber}

Der Video-Scrubber ist das horizontale Regler-Steuerelement, mit dem ein Benutzer dynamisch an eine beliebige Zeitposition innerhalb des derzeit wiedergegebenen Videos suchen kann.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

Der Scrubber-Knopf bewegt sich auch, während das Video abgespielt wird, um die aktuelle Zeitposition des Videos während der Wiedergabe anzugeben. Der Video-Scrubber nimmt immer die gesamte Breite der Steuerleiste ein. Es ist möglich, den Video-Scrubber zu entlüften und seine Höhe und vertikale Position durch CSS zu ändern.

Das allgemeine Erscheinungsbild des Video-Scrubbers wird mit der folgenden CSS-Klassenauswahl gesteuert:

```
.s7videoviewer .s7videoscrubber 
.s7videoviewer .s7videoscrubber .s7videotime 
.s7videoviewer .s7videoscrubber .s7knob
```

**CSS-Eigenschaften des Video-Scrubbers**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Anfang </span> </p> </td> 
   <td colname="col2"> <p>Position vom oberen Rand, einschließlich Abstand. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> unten </span> </p> </td> 
   <td colname="col2"> <p> Position vom unteren Rand, einschließlich Abstand. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Höhe des Video-Scrubbers. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p>Die Farbe des Video-Scrubbers. </p> </td> 
  </tr> 
 </tbody> 
</table>

Die folgenden CSS-Klassenselektoren verfolgen Hintergrund-, Wiedergabe- und Lastindikatoren:

```
.s7videoviewer .s7videoscrubber .s7track 
.s7videoviewer .s7videoscrubber .s7trackloaded 
.s7videoviewer .s7videoscrubber .s7trackplayed
```

**CSS-Eigenschaften des Tracks**

<table id="table_46903DCACF314426B67783167ADF7715"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Höhe der entsprechenden Strecke. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p>Die Farbe der entsprechenden Strecke. </p> </td> 
  </tr> 
 </tbody> 
</table>

Der folgende CSS-Klassenselektor steuert den Knoten:

```
.s7videoviewer .s7videoscrubber .s7knob
```

**CSS-Eigenschaften des Knotens**

<table id="table_966826FB81114362A8D81D1EED38D512"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Anfang </span> </p> </td> 
   <td colname="col2"> <p>Vertikaler Drehversatz. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Breite des Knopfes. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Höhe des Knotens. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image </span> </p> </td> 
   <td colname="col2"> <p>Knob-Grafik. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p> Position innerhalb des Bildsprites, wenn CSS-Sprites verwendet werden. </p> <p>Siehe <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-viewer-20-customizingviewer/c-html5-video-viewer-20-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> CSS-Sprites </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

Der folgende CSS-Klassenselektor steuert die Wiedergabedauer:

```
.s7videoviewer .s7videoscrubber .s7videotime
```

**CSS-Eigenschaften der wiedergegebenen Blase**

<table id="table_21E9AD3FBC8C4437BA02E5CD1BF7E831"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Schriftfamilie </span> </p> </td> 
   <td colname="col2"> <p> Die Schriftfamilie, die für die Zeitanzeige verwendet werden soll. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Schriftgröße </span> </p> </td> 
   <td colname="col2"> <p> Die Schriftgröße, die für die Zeitanzeige verwendet werden soll. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> color </span> </p> </td> 
   <td colname="col2"> <p> Die Schriftfarbe für die Zeitanzeige. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Blasenbereichbreite. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Blasenbereichshöhe. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Padding </span> </p> </td> 
   <td colname="col2"> <p>Blasenflächen-Umrandung. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image </span> </p> </td> 
   <td colname="col2"> <p>Blasengrafik. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p> Position innerhalb des Bildsprites, wenn CSS-Sprites verwendet werden. </p> <p>Siehe <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-viewer-20-customizingviewer/c-html5-video-viewer-20-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> CSS-Sprites </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> text-align </span> </p> </td> 
   <td colname="col2"> <p>Ausrichtung des Texts am Blasenbereich </p> </td> 
  </tr> 
 </tbody> 
</table>

Die QuickInfo für Video-Scrubber kann lokalisiert werden. Siehe [Lokalisierung der Elemente der Benutzeroberfläche](../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/r-html5-video-viewer-20-localization.md#concept-1d5ca2d8480f4064a51eddba13940aad) für weitere Informationen.

**Beispiel** - Um einen Video-Viewer mit einem Video-Scrubber mit benutzerdefinierten Track-Farben einzurichten. Der Scrubber muss zehn Pixel groß sein und zehn Pixel und 35 Pixel von den oberen und linken Kanten der Steuerleiste positioniert werden.

```
.s7videoviewer .s7videoscrubber  { 
top:10px; 
left:35px; 
height:10px; 
background-color:#AAAAAA; 
} 
.s7videoviewer .s7videoscrubber .s7track { 
height:10px; 
background-color:#444444; 
} 
.s7videoviewer .s7videoscrubber .s7trackloaded { 
height:10px; 
background-color:#666666; 
} 
.s7videoviewer .s7videoscrubber .s7trackplayed { 
height:10px; 
background-color:#888888; 
}
```

Wenn die Videokapzeichnung mit der Funktion `navigation` -Parameter werden Kapitelspeicherorte als Markierungen auf der Video-Scrubber-Spur angezeigt.

Die Videokapitelmarke wird durch den folgenden CSS-Klassenselektor gesteuert:

```
 .s7videoviewer .s7videoscrubber .s7navigation
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
   <td colname="col2"> <p>Grafik zur Videokapitelmarkierung. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p> Position innerhalb des Bildsprites, wenn CSS-Sprites verwendet werden. </p> <p>Siehe <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-viewer-20-customizingviewer/c-html5-video-viewer-20-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> CSS-Sprites </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Diese Schaltfläche unterstützt beide `state` -Attributauswahl, mit der Sie verschiedene Skins auf unterschiedliche Schaltflächenzustände anwenden können. Insbesondere `selected='default'` entspricht dem standardmäßigen Videokapitelmarkierungsstatus und `selected='over'` wird verwendet, wenn die Videokapitelmarke von einer Maus- oder Berührungsgeste aktiviert wird.

**Beispiel** - Um eine Videokapitelmarke einzurichten, die 5 x 8 Pixel groß ist und unterschiedliche Grafiken für den Status &quot;Standard&quot;und &quot;Over&quot;verwendet.

```
.s7videoviewer .s7videoscrubber .s7navigation { 
width:5px; 
height:8px; 
} 
.s7videoviewer .s7videoscrubber .s7navigation[state="default"] { 
background-image: url("images/v2/VideoScrubberDiamond.png"); 
} 
.s7videoviewer .s7videoscrubber .s7navigation[state="over"] { 
background-image: url("images/v2/VideoScrubberDiamond_over.png"); 
}
```

Die Kapitelblase für Videos wird über der Videokapitelmarke positioniert und zeigt den Titel, die Startzeit und die Beschreibung für ein bestimmtes Kapitel an. Es ist möglich, die maximale Blasenbreite und den vertikalen Versatz relativ zum Video-Scrubber-Track zu steuern. Der Rest wird automatisch von der Komponente berechnet.

Die Kapitelblase für Videos wird durch den folgenden CSS-Klassenselektor gesteuert:

```
.s7videoviewer .s7videoscrubber .s7chapter
```

**CSS-Eigenschaften der Videokapitelblase**

<table id="table_7F33738422F84978B9132495F67C2156"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> max-width </span> </p> </td> 
   <td colname="col2"> <p>Maximale Breite der Videokapitelblase. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> unten </span> </p> </td> 
   <td colname="col2"> <p>Vertikaler Versatz der Video-Scrubber-Spur. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Beispiel** - Um eine Kapitelblase für Videos einzurichten, die 235 Pixel breit und 8 Pixel nach oben vom unteren Rand des Video-Scrubber-Spur ist.

```
.s7videoviewer .s7videoscrubber .s7chapter { 
max-width:235px; 
bottom:8px; 
}
```

Die Kapitelblase für Videos besteht aus einer optionalen Kopfzeile und einem optionalen Inhalt. Die Kopfzeile verfügt über die optionale Kapitelstartzeit und den Kapiteltitel.

Die Kopfzeile wird durch den folgenden CSS-Klassenselektor gesteuert:

```
.s7videoviewer .s7videoscrubber .s7chapter .s7header
```

**CSS-Eigenschaften des Kapitelblasen-Headers des Videos**

<table id="table_56FBC3BADDEA4E15924DD750CADC474F"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Höhe der Kopfzeile des Videokapitels. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Padding </span> </p> </td> 
   <td colname="col2"> <p>Innerer Abstand für Kopfzeilentext von Videokapiteln. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p>Hintergrundfarbe der Videokapitelblase mit Kopfzeile. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> line-height </span> </p> </td> 
   <td colname="col2"> <p>Höhe der Textlinie der Videokapitelblase in der Kopfzeile. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Beispiel** - So richten Sie einen Video-Kapitelblasen-Header ein, der 22 Pixel hoch ist, eine 22-Pixel-Zeilenhöhe, einen 12-Pixel-horizontalen Rand und einen grauen Hintergrund.

```
.s7videoviewer .s7videoscrubber .s7chapter .s7header { 
height:22px; 
padding:0 12px; 
line-height:22px; 
background-color: rgba(51, 51, 51, 0.8); 
}
```

Die Startzeit des Videokapitels wird durch die folgende CSS-Klassenauswahl gesteuert:

```
 .s7videoviewer .s7videoscrubber .s7chapter .s7header .s7starttime
```

**CSS-Eigenschaften der Videokapitelstartzeit**

<table id="table_D58D6B22BAEE4E26BAAB34783AE5A044"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> color </span> </p> </td> 
   <td colname="col2"> <p>Textfarbe. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Schriftstärke </span> </p> </td> 
   <td colname="col2"> <p>Schriftstärke. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Schriftgröße </span> </p> </td> 
   <td colname="col2"> <p>Schriftgröße. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Schriftfamilie </span> </p> </td> 
   <td colname="col2"> <p>Schriftfamilie. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> padding-right </span> </p> </td> 
   <td colname="col2"> <p> Abstand zwischen der Startzeit und dem Kapiteltitel. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Beispiel** - Um die Startzeit des Kapitels mit grauen zehn Pixel Verdana-Schriftart einzurichten und hat zehn Pixel Abstand auf der rechten Seite.

```
.s7videoviewer .s7videoscrubber .s7chapter .s7header .s7starttime { 
color: #dddddd; 
font-family: Verdana,Arial,Helvetica,sans-serif; 
font-size: 10px; 
padding-right: 10px; 
}
```

Der Videokapiteltitel wird durch den folgenden CSS-Klassenselektor gesteuert:

```
.s7videoviewer .s7videoscrubber .s7chapter .s7header .s7title
```

**CSS-Eigenschaften des Videokapiteltitels**

<table id="table_240DD3E119584DCC95FF480B60266603"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> color </span> </p> </td> 
   <td colname="col2"> <p>Textfarbe für Videokapiteltitel. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Schriftstärke </span> </p> </td> 
   <td colname="col2"> <p>Schriftgröße für Videokapiteltitel </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Schriftgröße </span> </p> </td> 
   <td colname="col2"> <p>Schriftgröße für Videokapiteltitel. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Schriftfamilie </span> </p> </td> 
   <td colname="col2"> <p>Schriftfamilie der Videokapiteltitel. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Beispiel** - Um einen Videokapiteltitel einzurichten, der eine weiße, fette, zehn Pixel große Verdana-Schriftart verwendet.

```
.s7videoviewer .s7videoscrubber .s7chapter .s7header .s7title { 
color: #ffffff; 
font-family: Verdana,Arial,Helvetica,sans-serif; 
font-size: 10px; 
font-weight: bold; 
}
```

Die Beschreibung des Videokapitels wird durch den folgenden CSS-Klassenselektor gesteuert:

```
 .s7videoviewer .s7videoscrubber .s7chapter .s7description
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
   <td colname="col1"> <p> <span class="codeph"> Schriftstärke </span> </p> </td> 
   <td colname="col2"> <p>Schriftstärke der Videokapitelbeschreibung. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Schriftgröße </span> </p> </td> 
   <td colname="col2"> <p>Schriftgröße der Videokapitelbeschreibung. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Schriftfamilie </span> </p> </td> 
   <td colname="col2"> <p>Schriftfamilie der Videokapitelbeschreibung. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> line-height </span> </p> </td> 
   <td colname="col2"> <p>Zeilenhöhe der Videokapitelbeschreibung </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Padding </span> </p> </td> 
   <td colname="col2"> <p>Beschreibung des Videokapitels - innerer Abstand. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Beispiel** - Um eine Videokapitelbeschreibung mit einer dunkelgrauen, 11 Pixel großen Verdana-Schriftart mit hellgrauem Hintergrund einzurichten. Und schließlich verwendet fünf Pixelzeilenhöhe, 12-Pixel-horizontaler Abstand, 12-Pixel-Top-Abstand und neun Pixel-Bodenabstände.

```
.s7videoviewer .s7videoscrubber .s7chapter .s7description { 
color: #333333; 
background-color: rgba(221, 221, 221, 0.9); 
font-family: Verdana,Arial,Helvetica,sans-serif; 
font-size: 11px; 
line-height: 15px; 
padding: 12px 12px 9px; 
}
```

Der Keil-Connector am unteren Rand der Kapitelblase wird durch den folgenden CSS-Klassenselektor gesteuert:

```
 .s7videoviewer .s7videoscrubber .s7chapter .s7tail
```

**CSS-Eigenschaften des Keil-Connectors**

<table id="table_BC6AFB57D9404A84A3AE657448C0EB06"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> border-color </span> </p> </td> 
   <td colname="col2"> <p>Farbe des Wedge-Connectors. </p> <p>Definiert als <span class="codeph"> &lt;color&gt; transparent </span> sodass nur die Farbe des oberen Rands definiert und die verbleibenden Ränder transparent bleiben. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> border-width </span> </p> </td> 
   <td colname="col2"> <p> Breite des Wedge-Connectors. </p> <p>Definiert als <span class="codeph"> &lt;width&gt; &lt;width&gt; 0 </span> sodass dieselbe Breite nur für die oberen und horizontalen Ränder und die untere Rahmenbreite definiert ist <span class="codeph"> 0 </span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margin </span> </p> </td> 
   <td colname="col2"> <p> Definiert nur eine negative untere Marge. Sie sollte denselben Wert haben wie <span class="codeph"> border-width </span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Beispiel** - So richten Sie einen grauen, sechs Pixel großen Keil-Connector ein:

```
.s7videoviewer .s7videoscrubber .s7chapter .s7tail { 
border-color: rgba(221, 221, 221, 0.9) transparent transparent; 
border-width: 6px 6px 0; 
margin: 0 0 0 -6px; 
}
```
