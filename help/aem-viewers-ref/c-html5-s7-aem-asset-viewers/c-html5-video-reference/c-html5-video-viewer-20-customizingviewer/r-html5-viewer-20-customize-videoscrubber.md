---
title: Video-Scrubber
description: Der Video-Scrubber ist der horizontale Schieberegler, mit dem Benutzende dynamisch nach einer beliebigen Position innerhalb des aktuell wiedergegebenen Videos suchen können
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Video
role: Developer,User
exl-id: 404e39d4-565e-4dde-b2bd-fa83a895d001
source-git-commit: ceb9483f67a19d969ecbbd01cede11f3dae86467
workflow-type: tm+mt
source-wordcount: '1037'
ht-degree: 0%

---

# Video-Scrubber{#video-scrubber}

Der Video-Scrubber ist der horizontale Schieberegler, mit dem Benutzende dynamisch nach einer beliebigen Position innerhalb des aktuell wiedergegebenen Videos suchen können.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

Der Scrubber-Regler bewegt sich während der Videowiedergabe auch, um die aktuelle Zeitposition des Videos während der Wiedergabe anzuzeigen. Der Video-Scrubber nimmt immer die gesamte Breite der Steuerleiste ein. Es ist möglich, den Video-Scrubber mit Haut zu versehen und seine Höhe und vertikale Position mithilfe von CSS zu ändern.

Das allgemeine Erscheinungsbild des Video-Scrubbers wird mit dem folgenden CSS-Klassenselektor gesteuert:

```
.s7videoviewer .s7videoscrubber 
.s7videoviewer .s7videoscrubber .s7videotime 
.s7videoviewer .s7videoscrubber .s7knob
```

**CSS-Eigenschaften des Video-Scrubbers**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Top-</span> </p> </td> 
   <td colname="col2"> <p>Position ab dem oberen Rahmen, einschließlich Auffüllung. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> untere </span> </p> </td> 
   <td colname="col2"> <p> Position ab dem unteren Rand, einschließlich Abstand. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Höhe </span> </p> </td> 
   <td colname="col2"> <p>Höhe des Video-Scrubbers. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">-</span> </p> </td> 
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

**CSS-Eigenschaften der Spur**

<table id="table_46903DCACF314426B67783167ADF7715"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Höhe </span> </p> </td> 
   <td colname="col2"> <p>Höhe des entsprechenden Gleises. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">-</span> </p> </td> 
   <td colname="col2"> <p>Die Farbe der entsprechenden Spur. </p> </td> 
  </tr> 
 </tbody> 
</table>

Der folgende CSS-Klassenselektor steuert den Regler:

```
.s7videoviewer .s7videoscrubber .s7knob
```

**CSS-Eigenschaften des Reglers**

<table id="table_966826FB81114362A8D81D1EED38D512"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Top-</span> </p> </td> 
   <td colname="col2"> <p>Vertikaler Knopfversatz. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Breite </span> </p> </td> 
   <td colname="col2"> <p>Breite des Knopfes. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Höhe </span> </p> </td> 
   <td colname="col2"> <p>Höhe des Drehknopfs. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Hintergrundbild-</span> </p> </td> 
   <td colname="col2"> <p>Knopf-Bildmaterial. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Hintergrundposition </span> </p> </td> 
   <td colname="col2"> <p> Positionieren Sie sie innerhalb des Bildsets, wenn CSS-Sprites verwendet werden. </p> <p>Siehe <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-viewer-20-customizingviewer/c-html5-video-viewer-20-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> von CSS-Sprites </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

Der folgende CSS-Klassenselektor steuert die wiedergegebene Zeitblase:

```
.s7videoviewer .s7videoscrubber .s7videotime
```

**CSS-Eigenschaften der wiedergegebenen Zeitblase**

<table id="table_21E9AD3FBC8C4437BA02E5CD1BF7E831"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">-</span> </p> </td> 
   <td colname="col2"> <p> Die Schriftfamilie, die für die Zeitanzeige verwendet werden soll. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">-</span> </p> </td> 
   <td colname="col2"> <p> Die Schriftgröße, die für den Text der Zeitanzeige verwendet werden soll. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">-</span> </p> </td> 
   <td colname="col2"> <p> Die Schriftfarbe, die für die Zeitanzeige verwendet werden soll. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Breite </span> </p> </td> 
   <td colname="col2"> <p>Breite des Blasenbereichs. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Höhe </span> </p> </td> 
   <td colname="col2"> <p>Höhe des Blasenbereichs. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">-</span> </p> </td> 
   <td colname="col2"> <p>Auffüllung des Blasenbereichs. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Hintergrundbild-</span> </p> </td> 
   <td colname="col2"> <p>Bubble-Grafik. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Hintergrundposition </span> </p> </td> 
   <td colname="col2"> <p> Positionieren Sie sie innerhalb des Bildsets, wenn CSS-Sprites verwendet werden. </p> <p>Siehe <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-viewer-20-customizingviewer/c-html5-video-viewer-20-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> von CSS-Sprites </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> </span> zur Textausrichtung <span class="codeph"> </p> </td> 
   <td colname="col2"> <p>Ausrichtung des Textes am Blasenbereich. </p> </td> 
  </tr> 
 </tbody> 
</table>

Die QuickInfo des Video-Scrubbers kann lokalisiert werden. Siehe [Lokalisierung von Benutzeroberflächenelementen](../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/r-html5-video-viewer-20-localization.md#concept-1d5ca2d8480f4064a51eddba13940aad) für weitere Informationen.

**Beispiel** - Zum Einrichten eines Video-Viewers mit einem Video-Scrubber mit benutzerdefinierten Spurfarben. Der Scrubber muss zehn Pixel hoch sein und zehn Pixel und 35 Pixel vom oberen und linken Rand der Steuerleiste entfernt positioniert sein.

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

Wenn die Videokapitelung mit dem Parameter &quot;`navigation`&quot; aktiviert ist, werden Kapitelpositionen als Markierungen über der Video-Scrubber-Spur angezeigt.

Die Videokapitelmarkierung wird durch den folgenden CSS-Klassenselektor gesteuert:

```
 .s7videoviewer .s7videoscrubber .s7navigation
```

**CSS-Eigenschaften der Videokapitelmarkierung**

<table id="table_51F16E47BEF3430B919ABEEDBE543973"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Breite </span> </p> </td> 
   <td colname="col2"> <p>Videokapitelmarkierungsbreite. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Höhe </span> </p> </td> 
   <td colname="col2"> <p>Videokapitelmarkenhöhe </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Hintergrundbild-</span> </p> </td> 
   <td colname="col2"> <p>Videokapitelmarkierung </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Hintergrundposition </span> </p> </td> 
   <td colname="col2"> <p> Positionieren Sie sie innerhalb des Bildsets, wenn CSS-Sprites verwendet werden. </p> <p>Siehe <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-viewer-20-customizingviewer/c-html5-video-viewer-20-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> von CSS-Sprites </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Diese Schaltfläche unterstützt sowohl die `state` Attributauswahl, mit der Sie verschiedene Skins auf verschiedene Schaltflächenzustände anwenden können. Insbesondere entspricht `selected='default'` dem standardmäßigen Videokapitelmarkierungsstatus und `selected='over'` wird verwendet, wenn die Videokapitelmarkierung durch eine Maus-über- oder Touch-Geste aktiviert wird.

**Beispiel** - Zum Einrichten einer Videokapitelmarkierung, die 5 x 8 Pixel groß ist und unterschiedliche Grafiken für den Status „Standard“ und „Über“ verwendet.

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

Die Videokapitelblase wird über der Videokapitelmarkierung positioniert und zeigt den Titel, die Startzeit und die Beschreibung für ein bestimmtes Kapitel an. Es ist möglich, die maximale Blasenbreite und den vertikalen Versatz relativ zur Video-Scrubber-Spur zu steuern. Der Rest wird automatisch von der Komponente berechnet.

Die Videokapitelblase wird durch den folgenden CSS-Klassenselektor gesteuert:

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
   <td colname="col1"> <p> <span class="codeph"> untere </span> </p> </td> 
   <td colname="col2"> <p>Vertikaler Versatz zur Video-Scrubber-Spur. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Beispiel** - Zum Einrichten einer Videokapitelblase, die 235 Pixel breit ist und acht Pixel vom unteren Rand der Video-Scrubber-Spur nach oben zeigt.

```
.s7videoviewer .s7videoscrubber .s7chapter { 
max-width:235px; 
bottom:8px; 
}
```

Die Videokapitelblase besteht aus einer optionalen Kopfzeile und einem optionalen Inhalt. Die Kopfzeile hat die optionale Kapitelstartzeit und den Kapiteltitel.

Der Header wird durch den folgenden CSS-Klassenselektor gesteuert:

```
.s7videoviewer .s7videoscrubber .s7chapter .s7header
```

**CSS-Eigenschaften der Bubble-Kopfzeile des Videokapitels**

<table id="table_56FBC3BADDEA4E15924DD750CADC474F"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Höhe </span> </p> </td> 
   <td colname="col2"> <p>Bubble-Header-Höhe des Videokapitels. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">-</span> </p> </td> 
   <td colname="col2"> <p>Innerer Abstand für den Text der Videokapitelblase. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">-</span> </p> </td> 
   <td colname="col2"> <p>Hintergrundfarbe des Videokapitels für die Sprechblase. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> </span> mit <span class="codeph"> Zeilenhöhe </p> </td> 
   <td colname="col2"> <p>Bubble-Header-Text der Videokapitelhöhe </p> </td> 
  </tr> 
 </tbody> 
</table>

**Beispiel** - Zum Einrichten einer Videokapitel-Bubble-Kopfzeile, die 22 Pixel hoch ist, eine Zeilenhöhe von 22 Pixel, einen horizontalen Rand von 12 Pixel und einen grauen Hintergrund.

```
.s7videoviewer .s7videoscrubber .s7chapter .s7header { 
height:22px; 
padding:0 12px; 
line-height:22px; 
background-color: rgba(51, 51, 51, 0.8); 
}
```

Die Startzeit des Videokapitels wird durch den folgenden CSS-Klassenselektor gesteuert:

```
 .s7videoviewer .s7videoscrubber .s7chapter .s7header .s7starttime
```

**CSS-Eigenschaften der Startzeit des Videokapitels**

<table id="table_D58D6B22BAEE4E26BAAB34783AE5A044"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">-</span> </p> </td> 
   <td colname="col2"> <p>Textfarbe. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">-</span> </p> </td> 
   <td colname="col2"> <p>Schriftstärke. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">-</span> </p> </td> 
   <td colname="col2"> <p>Schriftgröße. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">-</span> </p> </td> 
   <td colname="col2"> <p>Schriftfamilie. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Abstand rechts </span> </p> </td> 
   <td colname="col2"> <p> Auffüllung zwischen der Startzeit und dem Kapiteltitel. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Beispiel** - Zum Einrichten der Kapitelstartzeit mit der Schriftart Verdana (grau, zehn Pixel) und dem Abstand auf der rechten Seite.

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
   <td colname="col1"> <p> <span class="codeph">-</span> </p> </td> 
   <td colname="col2"> <p>Textfarbe des Videokapitels. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">-</span> </p> </td> 
   <td colname="col2"> <p>Schriftstärke des Videokapiteltitels. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">-</span> </p> </td> 
   <td colname="col2"> <p>Schriftgröße des Videokapiteltitels. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">-</span> </p> </td> 
   <td colname="col2"> <p>Schriftfamilie für Videokapiteltitel. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Beispiel** - Zum Einrichten eines Videokapiteltitels, der eine weiße, fette, zehn Pixel große Verdana-Schriftart verwendet.

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
   <td colname="col1"> <p> <span class="codeph">-</span> </p> </td> 
   <td colname="col2"> <p>Textfarbe der Videokapitelbeschreibung. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">-</span> </p> </td> 
   <td colname="col2"> <p>Hintergrundfarbe der Videokapitelbeschreibung. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">-</span> </p> </td> 
   <td colname="col2"> <p>Schriftstärke der Videokapitelbeschreibung. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">-</span> </p> </td> 
   <td colname="col2"> <p>Schriftgröße der Videokapitelbeschreibung. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">-</span> </p> </td> 
   <td colname="col2"> <p>Schriftfamilie der Videokapitelbeschreibung. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> </span> mit <span class="codeph"> Zeilenhöhe </p> </td> 
   <td colname="col2"> <p>Zeilenhöhe der Videokapitelbeschreibung </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">-</span> </p> </td> 
   <td colname="col2"> <p>Beschreibung des Videokapitels, innerer Abstand. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Beispiel** - Zum Einrichten einer Videokapitelbeschreibung mit einer dunkelgrauen, 11 Pixel großen Verdana-Schriftart und einem hellgrauen Hintergrund. Und schließlich verwendet fünf Pixel Zeilenhöhe, 12 Pixel horizontaler Abstand, 12 Pixel oberer Abstand und neun Pixel unterer Abstand.

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

Der Keil-Connector im unteren Bereich der Kapitelblase wird von der folgenden CSS-Klassenauswahl gesteuert:

```
 .s7videoviewer .s7videoscrubber .s7chapter .s7tail
```

**CSS-Eigenschaften des Keil-Connectors**

<table id="table_BC6AFB57D9404A84A3AE657448C0EB06"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">-</span> </p> </td> 
   <td colname="col2"> <p>Farbe des Keilverbinders. </p> <p>Wird als <span class="codeph"> &lt;color&gt; transparente </span> definiert, sodass nur die Farbe des oberen Rahmens definiert wird und die verbleibenden Rahmen transparent bleiben. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> border-width </span> </p> </td> 
   <td colname="col2"> <p> Breite des Keilverbinders. </p> <p>Definiert als <span class="codeph"> &lt;width&gt; &lt;width&gt; 0 </span>, sodass dieselbe Breite nur für den oberen und horizontalen Rahmen definiert ist und die Breite des unteren Rahmens <span class="codeph"> 0 </span> beträgt. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">-</span> </p> </td> 
   <td colname="col2"> <p> Definiert nur einen negativen unteren Rand. Sie sollte denselben Wert wie <span class="codeph"> border-width-</span> haben. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Beispiel** - So richten Sie einen grauen, sechs Pixel großen Keilverbinder ein:

```
.s7videoviewer .s7videoscrubber .s7chapter .s7tail { 
border-color: rgba(221, 221, 221, 0.9) transparent transparent; 
border-width: 6px 6px 0; 
margin: 0 0 0 -6px; 
}
```
