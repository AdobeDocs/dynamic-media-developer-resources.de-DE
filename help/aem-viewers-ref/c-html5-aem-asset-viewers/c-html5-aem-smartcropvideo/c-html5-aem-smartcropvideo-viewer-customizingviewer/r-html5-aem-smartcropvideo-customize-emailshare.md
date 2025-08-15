---
title: E-Mail-Freigabe
description: Das Tool zur E-Mail-Freigabe besteht aus einer Schaltfläche, die zum Bedienfeld Social-Media-Freigabe und zum modalen Dialogfeld hinzugefügt wird und angezeigt wird, wenn das Tool aktiviert wird. Die Position der Schaltfläche wird vollständig vom Tool Social Share verwaltet.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop,Video
role: Developer,User
exl-id: f2685d59-6b92-49cf-9359-dda602af4297
source-git-commit: 97fbf820590b53de5a1e6ce904e44d6b0ef9a214
workflow-type: tm+mt
source-wordcount: '3029'
ht-degree: 0%

---

# E-Mail-Freigabe{#email-share}

Das Tool zur E-Mail-Freigabe besteht aus einer Schaltfläche, die zum Bedienfeld Social-Media-Freigabe und zum modalen Dialogfeld hinzugefügt wird und angezeigt wird, wenn das Tool aktiviert wird. Die Position der Schaltfläche wird vollständig vom Tool Social Share verwaltet.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

Das Erscheinungsbild der Schaltfläche „E-Mail-Freigabe“ wird mit dem folgenden CSS-Klassenselektor gesteuert:

```
.s7smartcropvideoviewer .s7emailshare
```

**CSS-Eigenschaften des E-Mail-Freigaben-Tools**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Breite </span> </p> </td> 
   <td colname="col2"> <p>Breite der Schaltfläche. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Höhe </span> </p> </td> 
   <td colname="col2"> <p>Höhe der Schaltfläche. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Hintergrundbild-</span> </p> </td> 
   <td colname="col2"> <p> Das Bild, das für einen bestimmten Schaltflächenstatus angezeigt wird. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Hintergrundposition </span> </p> </td> 
   <td colname="col2"> <p> Positionieren Sie sie innerhalb des Bildsets, wenn CSS-Sprites verwendet werden. </p> <p>Siehe <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-smartcropvideo/c-html5-aem-smartcropvideo-viewer-customizingviewer/c-html5-aem-smartcropvideo-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> von CSS-Sprites </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

Diese Schaltfläche unterstützt die `state`-Attributauswahl, mit der verschiedene Skins auf verschiedene Schaltflächenzustände angewendet werden können.

Sie können die Schaltfläche aus dem Bedienfeld Social-Freigabe entfernen, indem Sie `display:none` CSS-Eigenschaft für die CSS-Klasse festlegen.

Die QuickInfo der Schaltfläche kann lokalisiert werden. Siehe [Lokalisierung von Benutzeroberflächenelementen](../../../c-html5-aem-asset-viewers/c-html5-aem-smartcropvideo/r-html5-aem-smartcropvideo-viewer-localization.md#concept-1d5ca2d8480f4064a51eddba13940aad) für weitere Informationen.

Beispiel: Einrichten einer E-Mail-Freigabeschaltfläche mit 28 x 28 Pixel, über die für jeden der vier verschiedenen Schaltflächenstatus ein anderes Bild angezeigt wird.

```
.s7smartcropvideoviewer .s7emailshare { 
 width:28px; 
 height:28px; 
} 
.s7smartcropvideoviewer .s7emailshare[state='up'] { 
background-image:url(images/v2/EmailShare_dark_up.png); 
} 
.s7smartcropvideoviewer .s7emailshare[state='over'] { 
background-image:url(images/v2/EmailShare_dark_over.png); 
} 
.s7smartcropvideoviewer .s7emailshare[state='down'] { 
background-image:url(images/v2/EmailShare_dark_down.png); 
} 
.s7smartcropvideoviewer .s7emailshare[state='disabled'] { 
background-image:url(images/v2/EmailShare_dark_disabled.png); 
}
```

Die Hintergrundüberlagerung, die eine Web-Seite abdeckt, wenn das Dialogfeld aktiv ist, wird mit der folgenden CSS-Klassenauswahl gesteuert:

```
.s7smartcropvideoviewer .s7emaildialog .s7backoverlay
```

**CSS-Eigenschaften der Backoverlay-**

<table id="table_1A0C28D8C81D413C83D73DEAC53057C5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">-</span> </p> </td> 
   <td colname="col2"> <p> Deckkraft der Hintergrundüberlagerung. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">-</span> </p> </td> 
   <td colname="col2"> <p>Hintergrundfarbe der Überlagerung. </p> </td> 
  </tr> 
 </tbody> 
</table>

Beispiel: So richten Sie eine Hintergrundüberlagerung ein, die mit einer Deckkraft von 70 % grau dargestellt wird:

```
.s7smartcropvideoviewer .s7emaildialog .s7backoverlay { 
 opacity:0.7; 
 background-color:#222222; 
}
```

Standardmäßig wird das modale Dialogfeld auf Desktop-Systemen zentriert auf dem Bildschirm angezeigt und nimmt auf Touch-Geräten den gesamten Web-Seitenbereich ein. In allen Fällen werden die Positionierung und Größe des Dialogfelds von der Komponente verwaltet. Das Dialogfeld wird mit dem folgenden CSS-Klassenselektor gesteuert:

```
.s7smartcropvideoviewer .s7emaildialog .s7dialog
```

**CSS-Eigenschaften des Dialogfelds**

<table id="table_5272BC8EF9124018B4290356B95B5559"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">-</span> </p> </td> 
   <td colname="col2"> <p> Rahmenradius des Dialogfelds (wenn im Dialogfeld nicht das gesamte Browser-Fenster angezeigt wird) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">-</span> </p> </td> 
   <td colname="col2"> <p> Hintergrundfarbe des Dialogfelds </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Breite </span> </p> </td> 
   <td colname="col2"> <p> Sollte entweder deaktiviert oder auf 100 % gesetzt sein. In diesem Fall nimmt das Dialogfeld das gesamte Browser-Fenster ein (dieser Modus wird auf Touch-Geräten bevorzugt). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Höhe </span> </p> </td> 
   <td colname="col2"> <p> Sollte entweder deaktiviert oder auf 100 % eingestellt sein. In diesem Fall nimmt das Dialogfeld das gesamte Browser-Fenster ein (dieser Modus wird auf Touch-Geräten bevorzugt). </p> </td> 
  </tr> 
 </tbody> 
</table>

Beispiel: So richten Sie ein Dialogfeld ein, um das gesamte Browser-Fenster zu verwenden und auf Touch-Geräten einen weißen Hintergrund zu verwenden:

```
.s7smartcropvideoviewer .s7touchinput .s7emaildialog .s7dialog { 
 width:100%; 
 height:100%; 
background-color: #ffffff; 
}
```

Die Dialogfeldkopfzeile besteht aus einem Symbol, einem Titeltext und einer Schaltfläche Schließen. Der Header-Container wird mit dem folgenden CSS-Klassenselektor gesteuert

```
.s7smartcropvideoviewer .s7emaildialog .s7dialogheader
```

**CSS-Eigenschaften der Dialogfeldkopfzeile**

<table id="table_E407E844C9BD4B5DA8B5BBDE0554F9CA"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">-</span> </p> </td> 
   <td colname="col2"> <p> Innerer Abstand für Kopfzeileninhalt. </p> </td> 
  </tr> 
 </tbody> 
</table>

Das Symbol und der Titeltext werden in einen zusätzlichen Container eingeschlossen, der von gesteuert wird.

```
.s7smartcropvideoviewer .s7emaildialog .s7dialogheader .s7dialogline
```

**CSS-Eigenschaften der Dialogfeldzeile**

<table id="table_5B03CF843F0D4B1295A3FC1EB50C56F1"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">-</span> </p> </td> 
   <td colname="col2"> <p> Innerer Abstand für das Kopfzeilensymbol und den Titel </p> </td> 
  </tr> 
 </tbody> 
</table>

Das Kopfzeilensymbol wird mit dem folgenden CSS-Klassenselektor gesteuert

```
.s7smartcropvideoviewer .s7emaildialog .s7dialogheadericon
```

**CSS-Eigenschaften des Dialogfeldkopfzeilensymbols**

<table id="table_DD4B0413721B49CE8E21B4A55BDE8F7D"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Breite </span> </p> </td> 
   <td colname="col2"> <p>Symbolbreite. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Höhe </span> </p> </td> 
   <td colname="col2"> <p>Symbolhöhe. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Hintergrundbild-</span> </p> </td> 
   <td colname="col2"> <p>Symbolbild. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Hintergrundposition </span> </p> </td> 
   <td colname="col2"> <p> Positionieren Sie sie innerhalb des Bildsets, wenn CSS-Sprites verwendet werden. </p> <p>Siehe <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-smartcropvideo/c-html5-aem-smartcropvideo-viewer-customizingviewer/c-html5-aem-smartcropvideo-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> von CSS-Sprites </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

Der Header-Titel wird mit dem folgenden CSS-Klassenselektor gesteuert:

```
.s7smartcropvideoviewer .s7emaildialog .s7dialogheadertext
```

**CSS-Eigenschaften des Dialogfeldkopfzeilentextes**

<table id="table_207B4B13153E425EAB38FC61F382A05F"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">-</span> </p> </td> 
   <td colname="col2"> <p>Schriftstärke. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">-</span> </p> </td> 
   <td colname="col2"> <p>Schrifthöhe </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">-</span> </p> </td> 
   <td colname="col2"> <p>Schriftfamilie. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">-</span> </p> </td> 
   <td colname="col2"> <p>Auffüllung für internen Text. </p> </td> 
  </tr> 
 </tbody> 
</table>

Die Schaltfläche „Schließen“ wird mit dem folgenden CSS-Klassenselektor gesteuert:

```
.s7smartcropvideoviewer .s7emaildialog .s7closebutton
```

**CSS-Eigenschaften des Schließen-Button-**

<table id="table_FAECBC489FC442588E50E3DA0AC16DD7"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Top-</span> </p> </td> 
   <td colname="col2"> <p> Vertikale Position der Schaltfläche relativ zum Kopfzeilencontainer. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> rechte </span> </p> </td> 
   <td colname="col2"> <p> Horizontale Position der Schaltfläche relativ zum Kopfzeilencontainer. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Breite </span> </p> </td> 
   <td colname="col2"> <p>Breite der Schaltfläche. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Höhe </span> </p> </td> 
   <td colname="col2"> <p>Höhe der Schaltfläche. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">-</span> </p> </td> 
   <td colname="col2"> <p>Innerer Abstand der Schaltfläche. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Hintergrundbild-</span> </p> </td> 
   <td colname="col2"> <p>Schaltflächenbild für jeden Status. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Hintergrundposition </span> </p> </td> 
   <td colname="col2"> <p> Positionieren Sie sie innerhalb des Bildsets, wenn CSS-Sprites verwendet werden. </p> <p>Siehe <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-smartcropvideo/c-html5-aem-smartcropvideo-viewer-customizingviewer/c-html5-aem-smartcropvideo-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> von CSS-Sprites </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Diese Schaltfläche unterstützt die `state`-Attributauswahl, mit der verschiedene Skins auf verschiedene Schaltflächenzustände angewendet werden können.

Die QuickInfo für die Schaltfläche „Schließen“ und der Dialogfeldtitel können lokalisiert werden. Siehe [Lokalisierung von Benutzeroberflächenelementen](../../../c-html5-aem-asset-viewers/c-html5-aem-smartcropvideo/r-html5-aem-smartcropvideo-viewer-localization.md#concept-1d5ca2d8480f4064a51eddba13940aad) für weitere Informationen.

Beispiel : Zum Einrichten einer Dialogkopfzeile mit Abstand, einem 24 x 17-Pixel-Symbol und einem fett gedruckten 16-Punkt-Titel. Und schließlich eine Schaltfläche zum Schließen mit 28 x 28 Pixeln, die zwei Pixel oben und zwei Pixel rechts vom Dialogfeld-Container positioniert ist:

```
.s7smartcropvideoviewer .s7emaildialog .s7dialogheader { 
 padding: 10px; 
} 
.s7smartcropvideoviewer .s7emaildialog .s7dialogheader .s7dialogline { 
 padding: 10px 10px 2px; 
} 
.s7smartcropvideoviewer .s7emaildialog .s7dialogheadericon { 
    background-image: url("images/sdk/dlgemail_cap.png"); 
    height: 17px; 
    width: 24px; 
} 
.s7smartcropvideoviewer .s7emaildialog .s7dialogheadertext { 
    font-size: 16pt; 
    font-weight: bold; 
    padding-left: 16px; 
} 
.s7smartcropvideoviewer .s7emaildialog .s7closebutton { 
 top:2px; 
 right:2px; 
 padding:8px; 
 width:28px; 
 height:28px; 
} 
.s7smartcropvideoviewer .s7emaildialog .s7closebutton[state='up'] { 
 background-image:url(images/sdk/close_up.png); 
} 
.s7smartcropvideoviewer .s7emaildialog .s7closebutton[state='over'] { 
 background-image:url(images/sdk/close_over.png); 
} 
.s7smartcropvideoviewer .s7emaildialog .s7closebutton[state='down'] { 
 background-image:url(images/sdk/close_down.png); 
} 
.s7smartcropvideoviewer .s7emaildialog .s7closebutton[state='disabled'] { 
 background-image:url(images/sdk/close_disabled.png); 
}
```

Die Fußzeile besteht aus den Schaltflächen „Abbrechen“ und „E-Mail senden“. Der Fußzeilen-Container wird mit dem folgenden CSS-Klassenselektor gesteuert:

```
.s7smartcropvideoviewer .s7emaildialog .s7dialogfooter
```

**CSS-Eigenschaften des &#x200B;** für die Dialogfeldfußzeile

<table id="table_0AF7AAAB846A46D690896AFD68575669"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">-</span> </p> </td> 
   <td colname="col2"> <p> Rahmen, mit dem die Fußzeile vom Rest des Dialogfelds visuell getrennt werden kann. </p> </td> 
  </tr> 
 </tbody> 
</table>

Die Fußzeile hat einen inneren Container, der beide Schaltflächen behält. Sie wird mit dem folgenden CSS-Klassenselektor gesteuert:

```
.s7smartcropvideoviewer .s7emaildialog .s7dialogbuttoncontainer
```

**CSS-Eigenschaften des Schaltflächen-Containers für Dialogfelder**

<table id="table_C34906888A8145C7A61E503DFC6B08A9"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">-</span> </p> </td> 
   <td colname="col2"> <p> Innerer Abstand zwischen Fußzeile und Schaltflächen. </p> </td> 
  </tr> 
 </tbody> 
</table>

Die Schaltfläche „Abbrechen“ wird mit dem folgenden CSS-Klassenselektor gesteuert:

```
.s7smartcropvideoviewer .s7emaildialog .s7dialogcancelbutton
```

**CSS-Eigenschaften des Dialogfelds Schaltfläche „Abbrechen“**

<table id="table_3DFA90B012F345A3A2A123D6856BE08A"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Breite </span> </p> </td> 
   <td colname="col2"> <p>Breite der Schaltfläche. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Höhe </span> </p> </td> 
   <td colname="col2"> <p>Höhe der Schaltfläche. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">-</span> </p> </td> 
   <td colname="col2"> <p> Textfarbe der Schaltfläche für jeden Status. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">-</span> </p> </td> 
   <td colname="col2"> <p> Hintergrundfarbe der Schaltfläche für jeden Status. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Diese Schaltfläche unterstützt die `state`-Attributauswahl, mit der verschiedene Skins auf verschiedene Schaltflächenzustände angewendet werden können.

Die Schaltfläche „E-Mail senden“ wird mit dem folgenden CSS-Klassenselektor gesteuert:

```
.s7smartcropvideoviewer .s7emaildialog .s7dialogactionbutton
```

**CSS-Eigenschaften der Aktionsschaltfläche des Dialogfelds**

<table id="table_91C75B2470A24DC2AD3973A91FA8B325"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Breite </span> </p> </td> 
   <td colname="col2"> <p>Breite der Schaltfläche. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Höhe </span> </p> </td> 
   <td colname="col2"> <p>Höhe der Schaltfläche. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">-</span> </p> </td> 
   <td colname="col2"> <p> Textfarbe der Schaltfläche für jeden Status. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">-</span> </p> </td> 
   <td colname="col2"> <p> Hintergrundfarbe der Schaltfläche für jeden Status. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Diese Schaltfläche unterstützt die `state`-Attributauswahl, mit der verschiedene Skins auf verschiedene Schaltflächenzustände angewendet werden können.

Darüber hinaus verwenden beide Schaltflächen eine gemeinsame CSS-Klasse, die CSS-Einstellungen enthalten kann, die für andere Dialogfeldschaltflächen identisch sind:

```
.s7smartcropvideoviewer .s7emaildialog .s7dialogfooter .s7button
```

**CSS-Eigenschaften der Schaltfläche**

<table id="table_E735E5EDFC1E4F8A962CEA533A88DD4E"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">-</span> </p> </td> 
   <td colname="col2"> <p>Schriftstärke der Schaltfläche. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">-</span> </p> </td> 
   <td colname="col2"> <p>Schriftgröße der Schaltfläche. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">-</span> </p> </td> 
   <td colname="col2"> <p>Schriftfamilie der Schaltfläche. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> mit </span> Zeilenhöhe </p> </td> 
   <td colname="col2"> <p> Texthöhe innerhalb der Schaltfläche. Beeinflusst die vertikale Ausrichtung. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">-</span> </p> </td> 
   <td colname="col2"> <p>Schlagschatten. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Rand rechts </span> </p> </td> 
   <td colname="col2"> <p>Rechter Button-Rand. </p> </td> 
  </tr> 
 </tbody> 
</table>

Die QuickInfos für die Schaltfläche können lokalisiert werden. Siehe [Lokalisierung von Benutzeroberflächenelementen](../../../c-html5-aem-asset-viewers/c-html5-aem-smartcropvideo/r-html5-aem-smartcropvideo-viewer-localization.md#concept-1d5ca2d8480f4064a51eddba13940aad) für weitere Informationen.

Beispiel: So richten Sie eine Fußzeile für ein Dialogfeld mit der Schaltfläche Abbrechen (64 x 34) und der Schaltfläche E-Mail senden (82 x 34) ein. Und schließlich sind die Textfarbe und die Hintergrundfarbe für jeden Schaltflächenstatus unterschiedlich:

```
.s7smartcropvideoviewer .s7emaildialog .s7dialogfooter { 
    border-top: 1px solid #909090; 
} 
.s7smartcropvideoviewer .s7emaildialog .s7dialogbuttoncontainer { 
    padding-bottom: 6px; 
    padding-top: 10px; 
} 
.s7smartcropvideoviewer .s7emaildialog .s7dialogfooter .s7button { 
    box-shadow: 1px 1px 1px #999999; 
    color: #FFFFFF; 
    font-size: 9pt; 
    font-weight: bold; 
    line-height: 34px; 
    margin-right: 10px; 
} 
.s7smartcropvideoviewer .s7emaildialog .s7dialogcancelbutton { 
 width:64px; 
 height:34px; 
} 
.s7smartcropvideoviewer .s7emaildialog .s7dialogcancelbutton[state='up'] { 
 background-color:#666666; 
 color:#dddddd; 
} 
.s7smartcropvideoviewer .s7emaildialog .s7dialogcancelbutton[state='down'] { 
 background-color:#555555; 
 color:#ffffff; 
} 
.s7smartcropvideoviewer .s7emaildialog .s7dialogcancelbutton[state='over'] { 
 background-color:#555555; 
 color:#ffffff; 
} 
.s7smartcropvideoviewer .s7emaildialog .s7dialogcancelbutton[state='disabled'] { 
 background-color:#b2b2b2; 
 color:#dddddd; 
} 
.s7smartcropvideoviewer .s7emaildialog .s7dialogactionbutton { 
 width:82px; 
 height:34px; 
} 
.s7smartcropvideoviewer .s7emaildialog .s7dialogactionbutton[state='up'] { 
 background-color:#333333; 
 color:#dddddd; 
} 
.s7smartcropvideoviewer .s7emaildialog .s7dialogactionbutton[state='down'] { 
 background-color:#222222; 
 color:#cccccc; 
} 
.s7smartcropvideoviewer .s7emaildialog .s7dialogactionbutton[state='over'] { 
 background-color:#222222; 
 color:#cccccc; 
} 
.s7smartcropvideoviewer .s7emaildialog .s7dialogactionbutton[state='disabled'] { 
 background-color:#b2b2b2; 
 color:#dddddd; 
}
```

Der Hauptdialogbereich zwischen Kopf- und Fußzeile enthält scrollbaren Dialogfeldinhalt und das Bildlauffeld auf der rechten Seite. In allen Fällen verwaltet die Komponente die Breite dieses Bereichs. Sie kann nicht in CSS festgelegt werden. Der Hauptdialogbereich wird mit dem folgenden CSS-Klassenselektor gesteuert:

```
.s7smartcropvideoviewer .s7emaildialog .s7dialogviewarea
```

**CSS-Eigenschaften des Anzeigebereichs-** des Dialogfelds

<table id="table_3FF4691D848A4C4D8EF060B7E79DEEDE"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Höhe </span> </p> </td> 
   <td colname="col2"> <p> Die Höhe des Hauptdialogfeldbereichs. Sie sollte nur angegeben werden, wenn das Dialogfeld im Desktop-Modus funktioniert. Dies gilt nicht, wenn das Dialogfeld so dimensioniert ist, dass es das gesamte Browser-Fenster einnimmt. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">-</span> </p> </td> 
   <td colname="col2"> <p>Die Hintergrundfarbe des Hauptdialogfeldbereichs. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">-</span> </p> </td> 
   <td colname="col2"> <p>Außenrand. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Der Hauptdialogfeldbereich unterstützt die optionale `state`-Attributauswahl. Sie wird auf `sendsuccess` gesetzt, wenn das E-Mail-Formular übermittelt wird und im Dialogfeld eine Bestätigungsmeldung angezeigt wird. Solange die Bestätigungsmeldung klein ist, kann diese Attributauswahl verwendet werden, um die Dialogfelthöhe zu reduzieren, wenn eine solche Bestätigungsmeldung angezeigt wird.

Beispiel: Das Hauptdialogfeld sollte zunächst eine Höhe von 300 Pixeln und bei Anzeige der Bestätigungsmeldung eine Höhe von 100 Pixeln aufweisen. Es sollte ein Rand von 10 Pixeln vorhanden sein und ein weißer Hintergrund verwendet werden:

```
.s7smartcropvideoviewer .s7emaildialog .s7dialogviewarea { 
 background-color:#ffffff; 
 margin:10px; 
 height:300px; 
} 
.s7smartcropvideoviewer .s7emaildialog .s7dialogviewarea[state='sendsuccess'] { 
 height:100px; 
}
```

Alle Formularinhalte (wie Beschriftungen und Eingabefelder) befinden sich in einem Container, der von gesteuert wird.

```
.s7smartcropvideoviewer .s7emaildialog .s7dialogbody
```

Wenn die Höhe dieses Containers größer als der Bereich des Hauptdialogfelds zu sein scheint, wird automatisch ein vertikaler Bildlauf durch die Komponente aktiviert.

**CSS-Eigenschaften des Dialogfeldhauptteils**

<table id="table_5D77F3D5B8CD4B798AA85F722B277F56"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">-</span> </p> </td> 
   <td colname="col2"> <p>Innerer Abstand. </p> </td> 
  </tr> 
 </tbody> 
</table>

Beispiel: So richten Sie Formularinhalte mit zehn Pixel Abstand ein:

```
.s7smartcropvideoviewer .s7emaildialog .s7dialogbody { 
    padding: 10px; 
}
```

Das Dialogfeldformular wird Zeile für Zeile ausgefüllt, wobei jede Zeile einen Teil des Formularinhalts enthält (z. B. eine Beschriftung und ein Texteingabefeld). Eine einzelne Formulareinstellung wird mit dem folgenden CSS-Klassenselektor gesteuert:

```
.s7smartcropvideoviewer .s7emaildialog .s7dialogbody .s7dialogline
```

**CSS-Eigenschaften der Dialogfeldzeile**

<table id="table_2CCCC71B45B444A8B9CE2894129C9C02"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">-</span> </p> </td> 
   <td colname="col2"> <p>Auffüllung der inneren Linie. </p> </td> 
  </tr> 
 </tbody> 
</table>

Beispiel: So richten Sie ein Dialogfeldformular ein, das für jede Zeile zehn Pixel Abstand aufweist:

```
.s7smartcropvideoviewer .s7emaildialog .s7dialogbody .s7dialogline { 
    padding: 10px; 
}
```

Alle statischen Beschriftungen im Dialogfeldformular werden mit

```
.s7smartcropvideoviewer .s7emaildialog .s7dialoglabel
```

Diese Klasse eignet sich nicht zur Steuerung der Größe oder Position von Beschriftungen, da Sie sie auf Texte an verschiedenen Stellen der Benutzeroberfläche des Formulars anwenden können.

**CSS-Eigenschaften der Dialogfeldbezeichnung. &#x200B;**

<table id="table_13C7874807314ADD83A23075ABB4C340"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">-</span> </p> </td> 
   <td colname="col2"> <p>Schriftstärke des Titels </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">-</span> </p> </td> 
   <td colname="col2"> <p>Schriftgröße des Titels. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">-</span> </p> </td> 
   <td colname="col2"> <p>Schriftfamilie des Titels </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">-</span> </p> </td> 
   <td colname="col2"> <p>Textfarbe des Titels </p> </td> 
  </tr> 
 </tbody> 
</table>

Die Dialogfeldbeschriftungen können lokalisiert werden. Siehe [Lokalisierung von Benutzeroberflächenelementen](../../../c-html5-aem-asset-viewers/c-html5-aem-smartcropvideo/r-html5-aem-smartcropvideo-viewer-localization.md#concept-1d5ca2d8480f4064a51eddba13940aad) für weitere Informationen.

Beispiel: Um alle Beschriftungen als grau festzulegen, geben Sie eine Schriftart mit neun Pixeln fett an:

```
.s7smartcropvideoviewer .s7emaildialog .s7dialoglabel { 
    color: #666666; 
    font-size: 9pt; 
    font-weight: bold; 
}
```

Alle statischen Beschriftungen, die links neben den Formulareingabefeldern angezeigt werden, werden mit Folgendem gesteuert:

```
.s7smartcropvideoviewer .s7emaildialog .s7dialoginputlabel
```

**CSS-Eigenschaften der Eingabelabel des Dialogfelds**

<table id="table_B5CF02837BAA42C7B79B6D9DA20792DF"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Breite </span> </p> </td> 
   <td colname="col2"> <p>Die Breite der statischen Beschriftung. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> zur Textausrichtung </span> </p> </td> 
   <td colname="col2"> <p>Die horizontale Textausrichtung. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">-</span> </p> </td> 
   <td colname="col2"> <p>Statischer Titelrand. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">-</span> </p> </td> 
   <td colname="col2"> <p>Auffüllung für statische Beschriftungen. </p> </td> 
  </tr> 
 </tbody> 
</table>

Beispiel: Um Eingabefeldbeschriftungen so einzurichten, dass sie 50 Pixel breit, rechtsbündig, zehn Pixel Abstand und einen zehn Pixel-Rand rechts sind:

```
.s7smartcropvideoviewer .s7emaildialog .s7dialoginputlabel { 
    margin-right: 10px; 
    padding: 10px; 
    text-align: right; 
    width: 50px; 
}
```

Jedes Formulareingabefeld ist in den -Container eingeschlossen, sodass Sie einen benutzerdefinierten Rahmen um das Eingabefeld anwenden können. Sie wird mit dem folgenden CSS-Klassenselektor gesteuert:

```
.s7smartcropvideoviewer .s7emaildialog .s7dialoginputcontainer
```

**CSS-Eigenschaften des Eingabecontainers für das Dialogfeld**

<table id="table_7BC1C5919A54483F8121D928DC63233A"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">-</span> </p> </td> 
   <td colname="col2"> <p>Rahmen um den Eingabefeld-Container. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">-</span> </p> </td> 
   <td colname="col2"> <p>Innerer Abstand. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Der Eingabefeld-Container unterstützt die optionale `state`. Sie wird auf `verifyerror` gesetzt, wenn Benutzende einen Fehler im Eingabedatenformat machen und die Inline-Validierung fehlschlägt. Mit diesem Attributselektor können Sie falsche Benutzereingaben im Formular markieren.

Die meisten Eingabefelder, die sich von der Beschriftung auf der linken Seite bis zum rechten Rand des Dialogfeldkörpers erstrecken (einschließlich der Felder „Von“ und „Nachricht„), werden gesteuert durch:

```
.s7smartcropvideoviewer .s7emaildialog .s7dialoginputwide
```

**CSS-Eigenschaften des Eingabefelds des Dialogfelds**

<table id="table_7275B4365DFA4C0386FA2BDB7204A517"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Breite </span> </p> </td> 
   <td colname="col2"> <p>Breite des Eingabefelds. </p> </td> 
  </tr> 
 </tbody> 
</table>

Das Eingabefeld „An“ ist schmaler, da es rechts Platz für die Schaltfläche „E-Mail entfernen“ bereitstellt. Sie wird mit dem folgenden CSS-Klassenselektor gesteuert:

```
.s7smartcropvideoviewer .s7emaildialog .s7dialoginputshort
```

**CSS-Eigenschaften des kurzen Eingabefelds des Dialogfelds**

<table id="table_DFA9059209FF4184BD483A529424E97F"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Breite </span> </p> </td> 
   <td colname="col2"> <p>Breite des Eingabefelds. </p> </td> 
  </tr> 
 </tbody> 
</table>

Beispiel: So richten Sie ein Formular ein, das einen grauen Rahmen mit einem Pixel und neun Pixel Abstand um alle Eingabefelder hat. So weisen Sie für Felder, bei denen die Validierung nicht erfolgreich ist, denselben Rahmen in roter Farbe auf, sodass das Eingabefeld 250 Pixel breit und der Rest der Eingabefelder 300 Pixel breit ist:

```
.s7smartcropvideoviewer .s7emaildialog .s7dialoginputcontainer { 
    border: 1px solid #CCCCCC; 
    padding: 9px; 
} 
.s7smartcropvideoviewer .s7emaildialog .s7dialoginputcontainer[state="verifyerror"] { 
    border: 1px solid #FF0000; 
} 
.s7smartcropvideoviewer .s7emaildialog .s7dialoginputshort { 
    width: 250px; 
} 
.s7smartcropvideoviewer .s7emaildialog .s7dialoginputwide { 
    width: 300px; 
}
```

Das Eingabefeld für E-Mail-Nachrichten wird ebenfalls wie folgt gesteuert:

```
.s7smartcropvideoviewer .s7emaildialog .s7dialogmessage
```

Mit dieser Klasse können Sie bestimmte Eigenschaften für das zugrunde liegende `TEXTAREA` festlegen.

**CSS-Eigenschaften der Dialogfeldmeldung**

<table id="table_9E9D5A0C3CDB45739615C4C07F8DC046"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Höhe </span> </p> </td> 
   <td colname="col2"> <p>Nachrichtenhöhe. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> von </span> </p> </td> 
   <td colname="col2"> <p>Zeilenumbruchstil. </p> </td> 
  </tr> 
 </tbody> 
</table>

Beispiel: So legen Sie eine E-Mail-Nachricht mit einer Höhe von 50 Pixel und `break-word` Zeilenumbruch fest:

```
.s7smartcropvideoviewer .s7emaildialog .s7dialogmessage { 
    height: 50px; 
    word-wrap: break-word; 
}
```

Mit der Schaltfläche „Weitere E-Mail-Adresse hinzufügen“ kann ein Benutzer mehrere Adressen in ein E-Mail-Formular einfügen. Sie wird mit dem folgenden CSS-Klassenselektor gesteuert:

```
.s7smartcropvideoviewer .s7emaildialog .s7dialogaddemailbutton
```

**CSS-Eigenschaften des Dialogfelds Schaltfläche E-Mail-Adresse hinzufügen**

<table id="table_8829DC0694684E8BA427DFB821F7433D"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Höhe </span> </p> </td> 
   <td colname="col2"> <p>Höhe der Schaltfläche. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">-</span> </p> </td> 
   <td colname="col2"> <p>Textfarbe der Schaltfläche für jeden Status. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Hintergrundbild-</span> </p> </td> 
   <td colname="col2"> <p>Schaltflächenbild für jeden Status. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Hintergrundposition </span> </p> </td> 
   <td colname="col2"> <p>Position des Schaltflächenbildes im Schaltflächenbereich. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">-</span> </p> </td> 
   <td colname="col2"> <p>Schriftstärke der Schaltfläche. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">-</span> </p> </td> 
   <td colname="col2"> <p>Schriftgröße der Schaltfläche. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">-</span> </p> </td> 
   <td colname="col2"> <p>Schriftfamilie der Schaltfläche. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> mit </span> Zeilenhöhe </p> </td> 
   <td colname="col2"> <p>Texthöhe innerhalb der Schaltfläche. Wirkt sich auf die vertikale Ausrichtung aus. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> zur Textausrichtung </span> </p> </td> 
   <td colname="col2"> <p>Horizontale Textausrichtung. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">-</span> </p> </td> 
   <td colname="col2"> <p>Innerer Abstand. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Diese Schaltfläche unterstützt die `state`-Attributauswahl, mit der verschiedene Skins auf verschiedene Schaltflächenzustände angewendet werden können.

Die QuickInfo der Schaltfläche kann lokalisiert werden. Siehe [Lokalisierung von Benutzeroberflächenelementen](../../../c-html5-aem-asset-viewers/c-html5-aem-smartcropvideo/r-html5-aem-smartcropvideo-viewer-localization.md#concept-1d5ca2d8480f4064a51eddba13940aad) für weitere Informationen.

Beispiel: Um die Schaltfläche „Weitere E-Mail-Adresse hinzufügen“ so einzurichten, dass sie 25 Pixel hoch ist, verwenden Sie eine 12-Punkt-Fettschrift mit rechter Ausrichtung und einer anderen Textfarbe und einem anderen Bild für jeden Status:

```
.s7smartcropvideoviewer .s7emaildialog .s7dialogaddemailbutton { 
 text-align:right; 
 font-size:12pt; 
 font-weight:bold; 
 background-position:left center; 
 line-height:25px; 
 padding-left:30px; 
 height:25px; 
} 
.s7smartcropvideoviewer .s7emaildialog .s7dialogaddemailbutton[state='up'] { 
 color:#666666; 
 background-image:url(images/sdk/dlgaddplus_up.png); 
} 
.s7smartcropvideoviewer .s7emaildialog .s7dialogaddemailbutton[state='down'] { 
 color:#000000; 
 background-image:url(images/sdk/dlgaddplus_over.png); 
} 
.s7smartcropvideoviewer .s7emaildialog .s7dialogaddemailbutton[state='over'] { 
 color:#000000; 
 text-decoration:underline; 
 background-image:url(images/sdk/dlgaddplus_over.png); 
} 
.s7smartcropvideoviewer .s7emaildialog .s7dialogaddemailbutton[state='disabled'] { 
 color:#666666; 
 background-image:url(images/sdk/dlgaddplus_up.png); 
}
```

Mit der Schaltfläche „Entfernen“ kann ein Benutzer zusätzliche Adressen aus dem E-Mail-Formular entfernen. Sie wird mit dem folgenden CSS-Klassenselektor gesteuert:

```
.s7smartcropvideoviewer .s7emaildialog .s7dialogremoveemailbutton
```

**CSS-Eigenschaften des Dialogfelds - Schaltfläche zum Entfernen der E-Mail**

<table id="table_79E4C65741E64859B9C9E9DCCB3D050B"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Breite </span> </p> </td> 
   <td colname="col2"> <p>Breite der Schaltfläche. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Höhe </span> </p> </td> 
   <td colname="col2"> <p>Höhe der Schaltfläche. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Hintergrundbild-</span> </p> </td> 
   <td colname="col2"> <p>Schaltflächenbild für jeden Status. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Hintergrundposition </span> </p> </td> 
   <td colname="col2"> <p> Positionieren Sie sie innerhalb des Bildsets, wenn CSS-Sprites verwendet werden. </p> <p>Siehe <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-smartcropvideo/c-html5-aem-smartcropvideo-viewer-customizingviewer/c-html5-aem-smartcropvideo-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> von CSS-Sprites </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Diese Schaltfläche unterstützt die `state`-Attributauswahl, mit der verschiedene Skins auf verschiedene Schaltflächenzustände angewendet werden können.

Die QuickInfo der Schaltfläche kann lokalisiert werden. Siehe [Lokalisierung von Benutzeroberflächenelementen](../../../c-html5-aem-asset-viewers/c-html5-aem-smartcropvideo/r-html5-aem-smartcropvideo-viewer-localization.md#concept-1d5ca2d8480f4064a51eddba13940aad) für weitere Informationen.

Beispiel: So richten Sie eine „Entfernen“-Schaltfläche auf 25 x 25 Pixel ein und verwenden für jeden Status ein anderes Bild:

```
.s7smartcropvideoviewer .s7emaildialog .s7dialogremoveemailbutton { 
 width:25px; 
 height:25px; 
} 
.s7smartcropvideoviewer .s7emaildialog .s7dialogremoveemailbutton[state='up'] { 
 background-image:url(images/sdk/dlgremove_up.png); 
} 
.s7smartcropvideoviewer .s7emaildialog .s7dialogremoveemailbutton[state='over'] { 
 background-image:url(images/sdk/dlgremove_over.png); 
} 
.s7smartcropvideoviewer .s7emaildialog .s7dialogremoveemailbutton[state='down'] { 
 background-image:url(images/sdk/dlgremove_over.png); 
} 
.s7smartcropvideoviewer .s7emaildialog .s7dialogremoveemailbutton[state='disabled'] { 
 background-image:url(images/sdk/dlgremove_up.png); 
}
```

Der freigegebene Inhalt wird unten im Dialogfeld angezeigt und enthält eine Miniaturansicht, einen Titel, eine Ursprungs-URL und eine Beschreibung. Sie wird in einen Container verpackt, der von Folgendem gesteuert wird:

```
.s7smartcropvideoviewer .s7emaildialog .s7dialogbody .s7dialogcontent
```

**CSS-Eigenschaften des &#x200B;**

<table id="table_9C5CBFC2482E4A46BE837573B0B02FE4"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">-</span> </p> </td> 
   <td colname="col2"> <p>Container-Rahmen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">-</span> </p> </td> 
   <td colname="col2"> <p>Innerer Abstand. </p> </td> 
  </tr> 
 </tbody> 
</table>

Beispiel: So richten Sie einen unteren Container ein, der einen gepunkteten Rahmen mit einem Pixel und keinen Abstand aufweist:

```
.s7smartcropvideoviewer .s7emaildialog .s7dialogbody .s7dialogcontent { 
    border: 1px dotted #A0A0A0; 
    padding: 0; 
}
```

Das Miniaturbild wird mit dem folgenden CSS-Klassenselektor gesteuert:

```
.s7smartcropvideoviewer .s7emaildialog .s7dialogthumbnail
```

Die `background-image`-Eigenschaft wird durch die Komponentenlogik festgelegt.

**CSS-Eigenschaften des Miniaturbilds des Dialogfelds**

<table id="table_4C614FF2CEB149DAB5B7D7BC38CD3CAE"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Breite </span> </p> </td> 
   <td colname="col2"> <p>Breite der Miniaturansicht. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Höhe </span> </p> </td> 
   <td colname="col2"> <p>Höhe des Miniaturbilds. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> zur vertikalen Ausrichtung </span> </p> </td> 
   <td colname="col2"> <p>Miniaturansicht für vertikale Ausrichtung. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">-</span> </p> </td> 
   <td colname="col2"> <p>Innerer Abstand. </p> </td> 
  </tr> 
 </tbody> 
</table>

Beispiel: So legen Sie fest, dass die Miniaturansicht 90 x 60 Pixel groß und mit zehn Pixel Abstand oben ausgerichtet ist:

```
.s7smartcropvideoviewer .s7emaildialog .s7dialogthumbnail { 
    height: 60px; 
    padding: 10px; 
    vertical-align: top; 
    width: 90px; 
}
```

Inhaltstitel, Herkunft und Beschreibung werden außerdem in einem Bedienfeld rechts neben der Inhaltsminiatur gruppiert. Sie wird mit dem folgenden CSS-Klassenselektor gesteuert:

```
.s7smartcropvideoviewer .s7emaildialog .s7dialoginfopanel
```

**CSS-Eigenschaften des Informationsbereichs des Dialogfelds**

<table id="table_EDFA6229D8C3468E989E7EC05F23EF3B"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Breite </span> </p> </td> 
   <td colname="col2"> <p>Breite des Bedienfelds. </p> </td> 
  </tr> 
 </tbody> 
</table>

Beispiel: So richten Sie ein Bedienfeld mit Inhaltsinformationen ein, das 300 Pixel breit ist:

```
.s7smartcropvideoviewer .s7emaildialog .s7dialoginfopanel { 
    width: 300px; 
}
```

Der Inhaltstitel wird mit dem folgenden CSS-Klassenselektor gesteuert:

```
.s7smartcropvideoviewer .s7emaildialog .s7dialogtitle
```

**CSS-Eigenschaften des Dialogfeldtitels**

<table id="table_E83C149E66EC474092DF8A180DA9A550"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">-</span> </p> </td> 
   <td colname="col2"> <p>Außenrand. </p> </td> 
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
 </tbody> 
</table>

Beispiel: So richten Sie einen Inhaltstitel so ein, dass er eine fette Schriftart mit einem Rand von zehn Pixeln verwendet:

```
.s7smartcropvideoviewer .s7emaildialog .s7dialogtitle { 
    font-weight: bold; 
    margin: 10px; 
}
```

Der Inhaltsursprung wird mit dem folgenden CSS-Klassenselektor gesteuert:

```
.s7smartcropvideoviewer .s7emaildialog .s7dialogorigin
```

**CSS-Eigenschaften des Inhaltsursprungs &#x200B;** Dialogfelds

<table id="table_51763B532A9C4AE8AE54B69933A8C0B5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">-</span> </p> </td> 
   <td colname="col2"> <p>Außenrand. </p> </td> 
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
 </tbody> 
</table>

Beispiel - Zum Einrichten des Inhaltsursprungs mit einem Rand von zehn Pixeln:

```
.s7smartcropvideoviewer .s7emaildialog .s7dialogorigin { 
    margin: 10px; 
}
```

Die Inhaltsbeschreibung wird mit dem folgenden CSS-Klassenselektor gesteuert:

```
.s7smartcropvideoviewer .s7emaildialog .s7dialogdescription
```

**CSS-Eigenschaften des Dialogfelds Inhaltsbeschreibung**

<table id="table_F0F917ED3D1D4FCE974F48214D287E14"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">-</span> </p> </td> 
   <td colname="col2"> <p>Außenrand. </p> </td> 
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
 </tbody> 
</table>

Beispiel : Einrichten einer Inhaltsbeschreibung mit einem Rand von zehn Pixeln und Verwendung einer Schriftart mit neun Punkten:

```
.s7smartcropvideoviewer .s7emaildialog .s7dialogdescription { 
    font-size: 9pt; 
    margin: 10px; 
}
```

Wenn Benutzende falsche Eingabedaten eingeben und die Inline-Validierung fehlschlägt oder wenn das Dialogfeld beim Senden des Formulars einen Fehler oder eine Bestätigungsmeldung rendern muss, wird oben im Dialogfeldtext eine Meldung angezeigt. Sie wird mit dem folgenden CSS-Klassenselektor gesteuert:

```
.s7smartcropvideoviewer .s7emaildialog .s7dialogerrormessage
```

**CSS-Eigenschaften der Fehlermeldung im Dialogfeld**

<table id="table_C114E1004C334D339C25A3438E8E6614"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Hintergrundbild-</span> </p> </td> 
   <td colname="col2"> <p> Fehlersymbol. Standard ist ein Ausrufezeichen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Hintergrundposition </span> </p> </td> 
   <td colname="col2"> <p> Position des Fehlersymbols innerhalb des Nachrichtenbereichs. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">-</span> </p> </td> 
   <td colname="col2"> <p>Textfarbe der Nachricht. </p> </td> 
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
   <td colname="col1"> <p> <span class="codeph"> mit </span> Zeilenhöhe </p> </td> 
   <td colname="col2"> <p> Texthöhe innerhalb der Nachricht. Beeinflusst die vertikale Ausrichtung. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">-</span> </p> </td> 
   <td colname="col2"> <p>Innerer Abstand. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Diese Nachricht unterstützt den `state` mit den folgenden möglichen Werten: `verifyerror`, `senderror` und `sendsuccess`. Der Wert `verifyerror` wird festgelegt, wenn eine Nachricht aufgrund eines Fehlers bei der Inline-Eingabevalidierung angezeigt wird. Der Wert `senderror` wird festgelegt, wenn ein Backend-E-Mail-Service einen Fehler meldet. Der `sendsuccess` wird beim erfolgreichen Versand der E-Mail festgelegt. Auf diese Weise ist es möglich, die Nachricht je nach Dialogfeldstatus unterschiedlich zu gestalten.

Die Fehlermeldung kann lokalisiert werden. Siehe [Lokalisierung von Benutzeroberflächenelementen](../../../c-html5-aem-asset-viewers/c-html5-aem-smartcropvideo/r-html5-aem-smartcropvideo-viewer-localization.md#concept-1d5ca2d8480f4064a51eddba13940aad) für weitere Informationen.

Beispiel: Um eine Nachricht so einzurichten, dass sie eine fett gedruckte Schriftart mit zehn Punkten verwendet, weisen Sie eine Zeilenhöhe von 25 Pixel und einen Abstand von 20 Pixel auf der linken Seite auf. Verwenden Sie bei einem Fehler außerdem ein Ausrufezeichen-Symbol, einen roten Text und bei Erfolg kein -Symbol und einen grünen Text:

```
.s7smartcropvideoviewer .s7emaildialog .s7dialogerrormessage[state="verifyerror"] { 
    background-image: url("images/sdk/dlgerrimg.png"); 
    color: #FF0000; 
} 
.s7smartcropvideoviewer .s7emaildialog .s7dialogerrormessage[state="senderror"] { 
    background-image: url("images/sdk/dlgerrimg.png"); 
    color: #FF0000; 
} 
.s7smartcropvideoviewer .s7emaildialog .s7dialogerrormessage[state="sendsuccess"] { 
    background-image: none; 
    color: #00B200; 
} 
.s7smartcropvideoviewer .s7emaildialog .s7dialogerrormessage { 
    background-position: left center; 
    font-size: 10pt; 
    font-weight: bold; 
    line-height: 25px; 
    padding-left: 20px; 
}
```

Wenn ein vertikaler Bildlauf erforderlich ist, wird die Bildlaufleiste im Bedienfeld nahe dem rechten Rand des Dialogfelds gerendert, das mit dem folgenden CSS-Klassenselektor gesteuert wird:

```
.s7smartcropvideoviewer .s7emaildialog .s7dialogscrollpanel
```

**CSS-Eigenschaften des Bildlaufbedienfelds des Dialogfelds**

<table id="table_A0C3AC7E00544FFBB8E1364F4CDDB371"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Breite </span> </p> </td> 
   <td colname="col2"> <p>Breite des Bildlaufbedienfelds. </p> </td> 
  </tr> 
 </tbody> 
</table>

Beispiel: So richten Sie ein Bildlauffeld mit einer Breite von 44 Pixeln ein:

```
.s7smartcropvideoviewer .s7emaildialog .s7dialogscrollpanel { 
    width: 44px; 
}
```

Das Erscheinungsbild des Bildlaufleistenbereichs wird mit dem folgenden CSS-Klassenselektor gesteuert:

```
.s7smartcropvideoviewer .s7emaildialog .s7scrollbar
```

**CSS-Eigenschaften der Bildlaufleiste**

<table id="table_2BF74CF43E9B42D79F99A3F5208D7051"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Breite </span> </p> </td> 
   <td colname="col2"> <p> Die Breite der Bildlaufleiste. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Top-</span> </p> </td> 
   <td colname="col2"> <p> Der vertikale Bildlaufbalken, der vom oberen Rand des Bildlaufbedienfelds versetzt ist. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> untere </span> </p> </td> 
   <td colname="col2"> <p> Der vertikale Bildlaufbalken, der vom unteren Rand des Bildlaufbedienfelds versetzt ist. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> rechte </span> </p> </td> 
   <td colname="col2"> <p> Der horizontale Bildlaufbalken, der vom rechten Rand des Bildlaufbedienfelds versetzt ist. </p> </td> 
  </tr> 
 </tbody> 
</table>

Beispiel: So richten Sie eine Bildlaufleiste ein, die 28 Pixel breit ist, und zwar einen Rand von acht Pixeln oben, rechts und unten im Bildlaufbedienfeld:

```
.s7smartcropvideoviewer .s7emaildialog .s7scrollbar { 
    bottom: 8px; 
    right: 8px; 
    top: 8px; 
    width: 28px; 
}
```

Die Bildlaufleistenspur ist der Bereich zwischen den oberen und unteren Bildlaufschaltflächen. Die Komponente legt automatisch die Position und Höhe der Spur fest. Die Spur wird mit dem folgenden CSS-Klassenselektor gesteuert:

```
.s7smartcropvideoviewer .s7emaildialog .s7scrollbar .s7scrolltrack
```

**CSS-Eigenschaften der Scroll-Spur**

<table id="table_EE990E7A342843619EDD84BAD29C6F2A"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Breite </span> </p> </td> 
   <td colname="col2"> <p>Die Spurbreite. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">-</span> </p> </td> 
   <td colname="col2"> <p>Die Hintergrundfarbe der Spur. </p> </td> 
  </tr> 
 </tbody> 
</table>

Beispiel: So richten Sie eine Bildlaufleistenspur ein, die 28 Pixel breit ist und einen grauen Hintergrund hat:

```
.s7smartcropvideoviewer .s7emaildialog .s7scrollbar .s7scrolltrack { 
width:28px; 
background-color: #B2B2B2; 
}
```

Der Daumen der Bildlaufleiste bewegt sich vertikal innerhalb eines Bereichs der Bildlaufspur. Die vertikale Position wird vollständig von der Komponentenlogik gesteuert, jedoch ändert sich die Daumenhöhe je nach Inhaltsmenge nicht dynamisch. Sie können die Höhe der Miniaturen und andere Aspekte mit dem folgenden CSS-Klassenselektor konfigurieren:

```
.s7smartcropvideoviewer .s7emaildialog .s7scrollbar .s7scrollthumb
```

**CSS-Eigenschaften des Thumbs der Bildlaufleiste**

<table id="table_5A4A283A50044A51881D997885674BDF"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Breite </span> </p> </td> 
   <td colname="col2"> <p>Die Breite des Daumens. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Höhe </span> </p> </td> 
   <td colname="col2"> <p>Die Daumenhöhe. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">-</span> </p> </td> 
   <td colname="col2"> <p> Der vertikale Abstand zwischen dem oberen Ende der Spur. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">-</span> </p> </td> 
   <td colname="col2"> <p> Der vertikale Abstand zwischen dem unteren Ende der Spur. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Hintergrundbild-</span> </p> </td> 
   <td colname="col2"> <p>Das Bild, das für einen bestimmten Daumenstatus angezeigt wird. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Hintergrundposition </span> </p> </td> 
   <td colname="col2"> <p> Positionieren Sie sie innerhalb des Bildsets, wenn CSS-Sprites verwendet werden. </p> <p>Siehe <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-smartcropvideo/c-html5-aem-smartcropvideo-viewer-customizingviewer/c-html5-aem-smartcropvideo-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> von CSS-Sprites </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Thumb unterstützt den `state`-Attributselektor , mit dem verschiedene Skins auf verschiedene Daumenzustände angewendet werden können: `up`, `down`, `over` und `disabled`.

Die QuickInfos für die Schaltfläche können lokalisiert werden. Siehe [Lokalisierung von Benutzeroberflächenelementen](../../../c-html5-aem-asset-viewers/c-html5-aem-smartcropvideo/r-html5-aem-smartcropvideo-viewer-localization.md#concept-1d5ca2d8480f4064a51eddba13940aad) für weitere Informationen.

Beispiel - Zum Einrichten eines Thumbs für eine Bildlaufleiste mit 28 x 45 Pixel, einem Rand von zehn Pixeln oben und unten und unterschiedlichen Grafiken für jeden Status:

```
.s7smartcropvideoviewer .s7emaildialog .s7scrollbar .s7scrollthumb { 
    height: 45px; 
    padding-bottom: 10px; 
    padding-top: 10px; 
    width: 28px; 
} 
.s7smartcropvideoviewer .s7emaildialog .s7scrollbar .s7scrollthumb[state="up"] { 
 background-image:url("images/sdk/scrollbar_thumb_up.png"); 
} 
.s7smartcropvideoviewer .s7emaildialog .s7scrollbar .s7scrollthumb[state="down"] { 
 background-image:url("images/sdk/scrollbar_thumb_down.png"); 
} 
.s7smartcropvideoviewer .s7emaildialog .s7scrollbar .s7scrollthumb[state="over"] { 
 background-image:url("images/sdk/scrollbar_thumb_over.png"); 
} 
.s7smartcropvideoviewer .s7emaildialog .s7scrollbar .s7scrollthumb[state="disabled"] { 
 background-image:url("images/sdk/scrollbar_thumb_disabled.png"); 
}
```

Die Darstellung der oberen und unteren Bildlaufschaltflächen wird mit den folgenden CSS-Klassenselektoren gesteuert:

```
.s7smartcropvideoviewer .s7emaildialog .s7scrollbar .s7scrollupbutton
```

```
.s7smartcropvideoviewer .s7emaildialog .s7scrollbar .s7scrolldownbutton  
  
```

**CSS-Eigenschaften der oberen und unteren Bildlaufschaltflächen**

<table id="table_EB853317E08941979B0E141C3C9B2C49"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Breite </span> </p> </td> 
   <td colname="col2"> <p>Die Breite der Schaltfläche. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Höhe </span> </p> </td> 
   <td colname="col2"> <p>Die Höhe der Schaltfläche. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Hintergrundbild-</span> </p> </td> 
   <td colname="col2"> <p>Das Bild, das für einen bestimmten Schaltflächenstatus angezeigt wird. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Hintergrundposition </span> </p> </td> 
   <td colname="col2"> <p> Positionieren Sie sie innerhalb des Bildsets, wenn CSS-Sprites verwendet werden. </p> <p>Siehe <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-smartcropvideo/c-html5-aem-smartcropvideo-viewer-customizingviewer/c-html5-aem-smartcropvideo-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> von CSS-Sprites </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Diese Schaltflächen unterstützen die `state`-Attributauswahl, mit der verschiedene Skins auf verschiedene Schaltflächenzustände angewendet werden können: `up`, `down`, `over` und `disabled`.

Beispiel: So richten Sie Bildlaufschaltflächen ein, die eine Größe von 28 x 32 Pixeln haben und für jeden Status unterschiedliche Bildmotive aufweisen:

```
.s7smartcropvideoviewer .s7emaildialog .s7scrollbar .s7scrollupbutton { 
 width:28px; 
 height:32px; 
} 
.s7smartcropvideoviewer .s7emaildialog .s7scrollbar .s7scrollupbutton[state='up'] { 
background-image:url(images/sdk/scroll_up_up.png); 
} 
.s7smartcropvideoviewer .s7emaildialog .s7scrollbar .s7scrollupbutton[state='over'] { 
 background-image:url(images/sdk/scroll_up_over.png); 
} 
.s7smartcropvideoviewer .s7emaildialog .s7scrollbar .s7scrollupbutton[state='down'] { 
 background-image:url(images/sdk/scroll_up_down.png); 
} 
.s7smartcropvideoviewer .s7emaildialog .s7scrollbar .s7scrollupbutton[state='disabled'] { 
 background-image:url(images/sdk/scroll_up_disabled.png); 
} 
.s7smartcropvideoviewer .s7emaildialog .s7scrollbar .s7scrolldownbutton { 
 width:28px; 
 height:32px; 
} 
.s7smartcropvideoviewer .s7emaildialog .s7scrollbar .s7scrolldownbutton[state='up'] { 
 background-image:url(images/sdk/scroll_down_up.png); 
} 
.s7smartcropvideoviewer .s7emaildialog .s7scrollbar .s7scrolldownbutton[state='over'] { 
 background-image:url(images/sdk/scroll_down_over.png); 
} 
.s7smartcropvideoviewer .s7emaildialog .s7scrollbar .s7scrolldownbutton[state='down'] { 
 background-image:url(images/sdk/scroll_down_down.png); 
} 
.s7smartcropvideoviewer .s7emaildialog .s7scrollbar .s7scrolldownbutton[state='disabled'] { 
 background-image:url(images/sdk/scroll_down_disabled.png); 
}
```
