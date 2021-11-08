---
title: Linkfreigabe
description: Das Tool zur Linkfreigabe besteht aus einer Schaltfläche, die zum Social-Freigabe-Bedienfeld hinzugefügt wird, und dem modalen Dialogfeld, das angezeigt wird, wenn das Tool aktiviert wird. Die Position der Schaltfläche wird vollständig vom Social-Freigabe-Tool verwaltet.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop,Video
role: Developer,User
exl-id: null
source-git-commit: 254d1ef05c73e19618b7ad4743c6a242fa177929
workflow-type: tm+mt
source-wordcount: '1374'
ht-degree: 2%

---

# Linkfreigabe{#link-share}

Das Tool zur Linkfreigabe besteht aus einer Schaltfläche, die zum Social-Freigabe-Bedienfeld hinzugefügt wird, und dem modalen Dialogfeld, das angezeigt wird, wenn das Tool aktiviert wird. Die Position der Schaltfläche wird vollständig vom Social-Freigabe-Tool verwaltet.

<!--<a id="section_ADDF98E91AF24F618289D1682A5FB13A"></a>-->

Das Erscheinungsbild der Schaltfläche &quot;Linkfreigabe&quot;wird mit der folgenden CSS-Klassenauswahl gesteuert:

```
.s7smartcropvideoviewer .s7linkshare
```

**CSS-Eigenschaften des Tools zur Linkfreigabe**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Schaltflächenbreite. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Schaltflächenhöhe. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image </span> </p> </td> 
   <td colname="col2"> <p> Das Bild, das für einen bestimmten Schaltflächenstatus angezeigt wird. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p> Position innerhalb des Bildsprites, wenn CSS-Sprites verwendet werden. </p> <p>Siehe <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-smartcropvideo/c-html5-aem-smartcropvideo-viewer-customizingviewer/c-html5-aem-smartcropvideo-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> CSS-Sprites </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Diese Schaltfläche unterstützt `state` -Attributauswahl, die verwendet werden kann, um verschiedene Skins auf verschiedene Schaltflächenzustände anzuwenden.

Sie können die Schaltfläche aus dem Social-Freigabebereich entfernen, indem Sie `display:none` CSS-Eigenschaft in ihrer CSS-Klasse.

Die QuickInfo der Schaltfläche kann lokalisiert werden. Siehe [Lokalisierung der Elemente der Benutzeroberfläche](../../../c-html5-aem-asset-viewers/c-html5-aem-smartcropvideo/r-html5-aem-smartcropvideo-viewer-localization.md#concept-1d5ca2d8480f4064a51eddba13940aad) für weitere Informationen.

Beispiel: Zum Einrichten einer Linkfreigabe-Schaltfläche mit 28 x 28 Pixel und zum Anzeigen eines anderen Bildes für jeden der vier verschiedenen Schaltflächenstatus:

```
.s7smartcropvideoviewer .s7linkshare { 
 width:28px; 
 height:28px; 
} 
.s7smartcropvideoviewer .s7linkshare[state='up'] { 
background-image:url(images/v2/LinkShare_dark_up.png); 
} 
.s7smartcropvideoviewer .s7linkshare[state='over'] { 
background-image:url(images/v2/LinkShare_dark_over.png); 
} 
.s7smartcropvideoviewer .s7linkshare[state='down'] { 
background-image:url(images/v2/LinkShare_dark_down.png); 
} 
.s7smartcropvideoviewer .s7linkshare[state='disabled'] { 
background-image:url(images/v2/LinkShare_dark_disabled.png); 
}
```

Die Hintergrundüberlagerung, die die Webseite abdeckt, wenn das Dialogfeld aktiv ist, wird mit der folgenden CSS-Klassenauswahl gesteuert:

```
.s7smartcropvideoviewer .s7linkdialog .s7backoverlay
```

**CSS-Eigenschaften der Hintergrundüberlagerung**

<table id="table_DB4183CE8061425084D495A355A941F8"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Deckkraft </span> </p> </td> 
   <td colname="col2"> <p>Deckkraft der Hintergrundüberlagerung. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p>Hintergrundüberlagerungsfarbe. </p> </td> 
  </tr> 
 </tbody> 
</table>

Beispiel: Um eine Hintergrundüberlagerung einzurichten, die grau mit einer Deckkraft von 70 % ist:

```
.s7smartcropvideoviewer .s7linkdialog .s7backoverlay { 
 opacity:0.7; 
 background-color:#222222; 
}
```

Standardmäßig wird das modale Dialogfeld zentriert auf dem Bildschirm auf Desktop-Systemen angezeigt und nimmt den gesamten Webseitenbereich auf Touch-Geräten. In allen Fällen wird die Positionierung und Größe des Dialogfelds von der Komponente verwaltet. Das Dialogfeld wird mit dem folgenden CSS-Klassenselektor gesteuert:

```
.s7smartcropvideoviewer .s7linkdialog .s7dialog
```

**CSS-Eigenschaften des Dialogfelds**

<table id="table_E31711ADF4C7446182549244362199A3"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> border-radius </span> </p> </td> 
   <td colname="col2"> <p> Rahmenradius des Dialogfelds, falls das Dialogfeld nicht den gesamten Browser annimmt. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p>Hintergrundfarbe des Dialogfelds. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Sollte entweder nicht festgelegt oder auf 100 % eingestellt sein. In diesem Fall nimmt das Dialogfeld das gesamte Browser-Fenster in Anspruch (dieser Modus wird auf Touch-Geräten empfohlen). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Sollte entweder nicht festgelegt oder auf 100 % eingestellt sein. In diesem Fall nimmt das Dialogfeld das gesamte Browser-Fenster in Anspruch (dieser Modus wird auf Touch-Geräten empfohlen). </p> </td> 
  </tr> 
 </tbody> 
</table>

Beispiel: Um das Dialogfeld so einzurichten, dass es das gesamte Browser-Fenster mit weißem Hintergrund auf Touch-Geräten verwendet:

```
.s7smartcropvideoviewer .s7touchinput .s7linkdialog .s7dialog { 
 width:100%; 
 height:100%; 
background-color: #ffffff; 
}
```

Die Kopfzeile des Dialogfelds besteht aus einem Symbol, einem Titeltext und einer Schaltfläche zum Schließen. Der Kopfzeilencontainer wird mit

```
.s7smartcropvideoviewer .s7linkdialog .s7dialogheader
```

**CSS-Eigenschaften des Dialogfeldheaders**

<table id="table_E407E844C9BD4B5DA8B5BBDE0554F9CA"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Padding </span> </p> </td> 
   <td colname="col2"> <p> Innerer Abstand für Kopfzeileninhalte. </p> </td> 
  </tr> 
 </tbody> 
</table>

Das Symbol und der Titeltext werden in einen zusätzlichen Container eingeschlossen, der mit

```
.s7smartcropvideoviewer .s7linkdialog .s7dialogheader .s7dialogline
```

**CSS-Eigenschaften der Dialogfeldzeile**

<table id="table_5B03CF843F0D4B1295A3FC1EB50C56F1"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Padding </span> </p> </td> 
   <td colname="col2"> <p> Innerer Abstand für das Kopfzeilensymbol und den Titel </p> </td> 
  </tr> 
 </tbody> 
</table>

Das Kopfzeilensymbol wird mit dem folgenden CSS-Klassenselektor gesteuert

```
.s7smartcropvideoviewer .s7linkdialog .s7dialogheadericon
```

**CSS-Eigenschaften des Kopfzeilensymbols des Dialogfelds**

<table id="table_DD4B0413721B49CE8E21B4A55BDE8F7D"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Symbolbreite. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Symbolhöhe. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image </span> </p> </td> 
   <td colname="col2"> <p>Symbolbild. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p> Position innerhalb des Bildsprites, wenn CSS-Sprites verwendet werden. </p> <p>Siehe <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-smartcropvideo/c-html5-aem-smartcropvideo-viewer-customizingviewer/c-html5-aem-smartcropvideo-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> CSS-Sprites </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

Der Kopfzeilentitel wird mit der folgenden CSS-Klassenauswahl gesteuert:

```
.s7smartcropvideoviewer .s7linkdialog .s7dialogheadertext
```

**CSS-Eigenschaften des Kopfzeilentextes des Dialogfelds**

<table id="table_207B4B13153E425EAB38FC61F382A05F"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Schriftstärke </span> </p> </td> 
   <td colname="col2"> <p>Schriftstärke. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Schriftgröße </span> </p> </td> 
   <td colname="col2"> <p>Schrifthöhe. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Schriftfamilie </span> </p> </td> 
   <td colname="col2"> <p>Schriftfamilie. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Padding </span> </p> </td> 
   <td colname="col2"> <p>Interner Textabstand. </p> </td> 
  </tr> 
 </tbody> 
</table>

Die Schaltfläche &quot;Schließen&quot;wird mit dem folgenden CSS-Klassenselektor gesteuert:

```
.s7smartcropvideoviewer .s7linkdialog .s7closebutton
```

**CSS-Eigenschaften der Schließen-Schaltfläche **

<table id="table_FAECBC489FC442588E50E3DA0AC16DD7"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Anfang </span> </p> </td> 
   <td colname="col2"> <p> Vertikale Schaltflächenposition relativ zum Kopfzeilencontainer </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> rechts </span> </p> </td> 
   <td colname="col2"> <p> Horizontale Schaltflächenposition relativ zum Kopfzeilencontainer </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Schaltflächenbreite. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Schaltflächenhöhe. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Padding </span> </p> </td> 
   <td colname="col2"> <p>Innerer Abstand der Schaltfläche. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image </span> </p> </td> 
   <td colname="col2"> <p>Schaltflächenbild für jeden Status. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p> Position innerhalb des Bildsprites, wenn CSS-Sprites verwendet werden. </p> <p>Siehe <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-smartcropvideo/c-html5-aem-smartcropvideo-viewer-customizingviewer/c-html5-aem-smartcropvideo-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> CSS-Sprites </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Diese Schaltfläche unterstützt `state` -Attributauswahl, die verwendet werden kann, um verschiedene Skins auf verschiedene Schaltflächenzustände anzuwenden.

Die QuickInfo der Schaltfläche Schließen und der Titel des Dialogfelds können lokalisiert werden. Siehe [Lokalisierung der Elemente der Benutzeroberfläche](../../../c-html5-aem-asset-viewers/c-html5-aem-smartcropvideo/r-html5-aem-smartcropvideo-viewer-localization.md#concept-1d5ca2d8480f4064a51eddba13940aad) für weitere Informationen.

Beispiel: Zum Einrichten einer Dialogfeldkopfzeile mit Abstand, einem 22 x 12 Pixel langen Symbol und einem fett gedruckten 16-Punkt-Titel. Schließlich eine 28 x 28 Pixel große Schaltfläche Schließen , die zwei Pixel von der oberen Seite und zwei Pixel von der rechten Seite des Dialogfeldcontainers positioniert ist:

```
.s7smartcropvideoviewer .s7linkdialog .s7dialogheader { 
 padding: 10px; 
} 
.s7smartcropvideoviewer .s7linkdialog .s7dialogheader .s7dialogline { 
 padding: 10px 10px 2px; 
} 
.s7smartcropvideoviewer .s7linkdialog .s7dialogheadericon { 
    background-image: url("images/sdk/dlglink_cap.png"); 
    height: 12px; 
    width: 22px; 
} 
.s7smartcropvideoviewer .s7linkdialog .s7dialogheadertext { 
    font-size: 16pt; 
    font-weight: bold; 
    padding-left: 16px; 
} 
.s7smartcropvideoviewer .s7linkdialog .s7closebutton { 
 top:2px; 
 right:2px; 
 padding:8px; 
 width:28px; 
 height:28px; 
} 
.s7smartcropvideoviewer .s7linkdialog .s7closebutton[state='up'] { 
 background-image:url(images/sdk/close_up.png); 
} 
.s7smartcropvideoviewer .s7linkdialog .s7closebutton[state='over'] { 
 background-image:url(images/sdk/close_over.png); 
} 
.s7smartcropvideoviewer .s7linkdialog .s7closebutton[state='down'] { 
 background-image:url(images/sdk/close_down.png); 
} 
.s7smartcropvideoviewer .s7linkdialog .s7closebutton[state='disabled'] { 
 background-image:url(images/sdk/close_disabled.png); 
}
```

Die Fußzeile des Dialogfelds besteht aus der Schaltfläche &quot;Abbrechen&quot;. Der Fußzeilencontainer wird mit der folgenden CSS-Klassenauswahl gesteuert:

```
.s7smartcropvideoviewer .s7linkdialog .s7dialogfooter
```

**CSS-Eigenschaften der Fußzeile des Dialogfelds **

<table id="table_0AF7AAAB846A46D690896AFD68575669"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> rand </span> </p> </td> 
   <td colname="col2"> <p> Rand, mit dem Sie die Fußzeile visuell vom Rest des Dialogfelds trennen können. </p> </td> 
  </tr> 
 </tbody> 
</table>

Die Fußzeile verfügt über einen inneren Container, der die Schaltfläche behält. Sie wird mit dem folgenden CSS-Klassenselektor gesteuert:

```
.s7smartcropvideoviewer .s7linkdialog .s7dialogbuttoncontainer
```

**CSS-Eigenschaften des Schaltflächenbehälters des Dialogfelds**

<table id="table_C34906888A8145C7A61E503DFC6B08A9"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Padding </span> </p> </td> 
   <td colname="col2"> <p> Abstand zwischen Fußzeile und Schaltfläche innen. </p> </td> 
  </tr> 
 </tbody> 
</table>

Die Schaltfläche Alle auswählen wird mit dem folgenden CSS-Klassenselektor gesteuert:

```
.s7smartcropvideoviewer .s7linkdialog .s7dialogactionbutton
```

Die Schaltfläche ist nur auf Desktop-Systemen verfügbar.

**CSS-Eigenschaften der Schaltfläche &quot;Alle auswählen&quot;**

<table id="table_021D0467632F49FEBFDF4CF96D2D67C7"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Schaltflächenbreite. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Schaltflächenhöhe. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> color </span> </p> </td> 
   <td colname="col2"> <p> Schaltflächentextfarbe für jeden Status. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p> Schaltflächen-Hintergrundfarbe für jeden Status. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Die Schaltfläche Alle auswählen unterstützt die `state` -Attributauswahl, die verwendet werden kann, um verschiedene Skins auf verschiedene Schaltflächenzustände anzuwenden.

Die Schaltfläche Abbrechen wird mit der folgenden CSS-Klassenauswahl gesteuert:

```
.s7smartcropvideoviewer .s7linkdialog .s7dialogcancelbutton
```

**CSS-Eigenschaften der Schaltfläche &quot;Abbrechen&quot;im Dialogfeld**

<table id="table_3DFA90B012F345A3A2A123D6856BE08A"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Schaltflächenbreite. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Schaltflächenhöhe. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> color </span> </p> </td> 
   <td colname="col2"> <p> Schaltflächentextfarbe für jeden Status. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p> Schaltflächen-Hintergrundfarbe für jeden Status. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Diese Schaltfläche unterstützt `state` -Attributauswahl, die verwendet werden kann, um verschiedene Skins auf verschiedene Schaltflächenzustände anzuwenden.

Darüber hinaus verwenden beide Schaltflächen eine gemeinsame CSS-Klasse, die CSS-Einstellungen enthalten kann, die für andere Dialogfeldschaltflächen identisch sind:

```
.s7smartcropvideoviewer .s7linkdialog .s7dialogfooter .s7button
```

**CSS-Eigenschaften der Schaltfläche**

<table id="table_E735E5EDFC1E4F8A962CEA533A88DD4E"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Schriftstärke </span> </p> </td> 
   <td colname="col2"> <p>Schriftstärke der Schaltfläche. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Schriftgröße </span> </p> </td> 
   <td colname="col2"> <p>Schriftgröße der Schaltfläche. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Schriftfamilie </span> </p> </td> 
   <td colname="col2"> <p>Schriftfamilie der Schaltflächen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> line-height </span> </p> </td> 
   <td colname="col2"> <p> Texthöhe innerhalb der Schaltfläche. Beeinflusst die vertikale Ausrichtung. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> box-Shadow </span> </p> </td> 
   <td colname="col2"> <p>Schlagschatten </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margin-right </span> </p> </td> 
   <td colname="col2"> <p>Rand der rechten Schaltfläche. </p> </td> 
  </tr> 
 </tbody> 
</table>

Die QuickInfos für Schaltflächen können lokalisiert werden. Siehe [Lokalisierung der Elemente der Benutzeroberfläche](../../../c-html5-aem-asset-viewers/c-html5-aem-smartcropvideo/r-html5-aem-smartcropvideo-viewer-localization.md#concept-1d5ca2d8480f4064a51eddba13940aad) für weitere Informationen.

Beispiel: Zum Einrichten einer Fußzeile des Dialogfelds mit einer Schaltfläche &quot;Abbrechen&quot;von 64 x 34, deren Textfarbe und Hintergrundfarbe je nach Schaltflächenstatus unterschiedlich sind:

```
.s7smartcropvideoviewer .s7linkdialog .s7dialogfooter { 
    border-top: 1px solid #909090; 
} 
.s7smartcropvideoviewer .s7linkdialog .s7dialogbuttoncontainer { 
    padding-bottom: 6px; 
    padding-top: 10px; 
} 
.s7smartcropvideoviewer .s7linkdialog .s7dialogfooter .s7button { 
    box-shadow: 1px 1px 1px #999999; 
    color: #FFFFFF; 
    font-size: 9pt; 
    font-weight: bold; 
    line-height: 34px; 
    margin-right: 10px; 
} 
.s7smartcropvideoviewer .s7linkdialog .s7dialogcancelbutton { 
 width:64px; 
 height:34px; 
} 
.s7smartcropvideoviewer .s7linkdialog .s7dialogcancelbutton[state='up'] { 
 background-color:#666666; 
 color:#dddddd; 
} 
.s7smartcropvideoviewer .s7linkdialog .s7dialogcancelbutton[state='down'] { 
 background-color:#555555; 
 color:#ffffff; 
} 
.s7smartcropvideoviewer .s7linkdialog .s7dialogcancelbutton[state='over'] { 
 background-color:#555555; 
 color:#ffffff; 
} 
.s7smartcropvideoviewer .s7linkdialog .s7dialogcancelbutton[state='disabled'] { 
 background-color:#b2b2b2; 
 color:#dddddd; 
} 
.s7smartcropvideoviewer .s7linkdialog .s7dialogactionbutton { 
 width:82px; 
 height:34px; 
} 
.s7smartcropvideoviewer .s7linkdialog .s7dialogactionbutton[state='up'] { 
 background-color:#333333; 
 color:#dddddd; 
} 
.s7smartcropvideoviewer .s7linkdialog .s7dialogactionbutton[state='down'] { 
 background-color:#222222; 
 color:#cccccc; 
} 
.s7smartcropvideoviewer .s7linkdialog .s7dialogactionbutton[state='over'] { 
 background-color:#222222; 
 color:#cccccc; 
} 
.s7smartcropvideoviewer .s7linkdialog .s7dialogactionbutton[state='disabled'] { 
 background-color:#b2b2b2; 
 color:#dddddd; 
}
```

Der Hauptdialogbereich (zwischen der Kopf- und Fußzeile) enthält Dialogfeldinhalte. In jedem Fall verwaltet die Komponente die Breite dieses Bereichs. Es ist nicht möglich, ihn in CSS festzulegen. Der Hauptdialogbereich wird mit der folgenden CSS-Klassenauswahl gesteuert:

```
.s7smartcropvideoviewer .s7linkdialog .s7dialogviewarea
```

**CSS-Eigenschaften des Dialogfelds, in dem der Anzeigebereich angezeigt wird **

<table id="table_3FF4691D848A4C4D8EF060B7E79DEEDE"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p> Die Höhe des Hauptdialogfeld-Bereichs. Sie sollte nur angegeben werden, wenn das Dialogfeld im Desktop-Modus funktioniert. Dies ist nicht möglich, wenn die Größe des Dialogfelds so geändert wird, dass es das gesamte Browser-Fenster belegt. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p>Die Hintergrundfarbe des Hauptdialogfeld-Bereichs. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margin </span> </p> </td> 
   <td colname="col2"> <p>Außenrand. </p> </td> 
  </tr> 
 </tbody> 
</table>

Beispiel: Zum Einrichten eines Hauptdialogfeld-Bereichs mit einer Höhe von 300 Pixel, einer zehnten Pixelbreite und einem weißen Hintergrund:

```
.s7smartcropvideoviewer .s7linkdialog .s7dialogviewarea { 
 background-color:#ffffff; 
 margin:10px; 
 height:300px; 
}
```

Der gesamte Formularinhalt (z. B. Beschriftungen und Eingabefelder) befindet sich in einem Container, der mit

```
.s7smartcropvideoviewer .s7linkdialog .s7dialogbody
```

**CSS-Eigenschaften des Dialogfeldtexts **

<table id="table_5D77F3D5B8CD4B798AA85F722B277F56"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Padding </span> </p> </td> 
   <td colname="col2"> <p>Innenabstand. </p> </td> 
  </tr> 
 </tbody> 
</table>

Beispiel: Zum Einrichten von Formularinhalten mit zehn Pixelabständen:

```
.s7smartcropvideoviewer .s7linkdialog .s7dialogbody { 
    padding: 10px; 
}
```

Alle statischen Beschriftungen im Dialogfeldformular werden mit

```
.s7smartcropvideoviewer .s7linkdialog .s7dialoglabel
```

Diese Klasse eignet sich nicht zur Steuerung der Größe oder Position der Beschriftung, da Sie sie auf Texte an verschiedenen Stellen der Formular-Benutzeroberfläche anwenden können.

**CSS-Eigenschaften der Dialogfeldbeschriftung. **

<table id="table_13C7874807314ADD83A23075ABB4C340"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Schriftstärke </span> </p> </td> 
   <td colname="col2"> <p>Schriftgröße beschriften. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Schriftgröße </span> </p> </td> 
   <td colname="col2"> <p>Schriftgröße beschriften. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Schriftfamilie </span> </p> </td> 
   <td colname="col2"> <p>Schriftfamilie beschriften. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> color </span> </p> </td> 
   <td colname="col2"> <p>Textfarbe beschriften. </p> </td> 
  </tr> 
 </tbody> 
</table>

Die Beschriftungen des Dialogfelds können lokalisiert werden. Siehe [Lokalisierung der Elemente der Benutzeroberfläche](../../../c-html5-aem-asset-viewers/c-html5-aem-smartcropvideo/r-html5-aem-smartcropvideo-viewer-localization.md#concept-1d5ca2d8480f4064a51eddba13940aad) für weitere Informationen.

Beispiel: Um alle Beschriftungen so einzurichten, dass sie grau und fett mit einer 9-Pixel-Schriftart sind:

```
.s7smartcropvideoviewer .s7linkdialog .s7dialoglabel { 
    color: #666666; 
    font-size: 9pt; 
    font-weight: bold; 
}
```

Die Größe der Textkopie, die über dem Link angezeigt wird, wird mit der folgenden CSS-Klassenauswahl gesteuert:

```
.s7smartcropvideoviewer .s7linkdialog .s7dialoginputwide
```

**CSS-Eigenschaften des für die gesamte Eingabe des Dialogfelds vorgesehenen Felds**

<table id="table_7275B4365DFA4C0386FA2BDB7204A517"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Textbreite. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Padding </span> </p> </td> 
   <td colname="col2"> <p>Innenabstand. </p> </td> 
  </tr> 
 </tbody> 
</table>

Beispiel: Zum Festlegen einer Textkopie auf eine Breite von 430 Pixel und einen Abstand von zehn Pixel am unteren Rand:

```
.s7smartcropvideoviewer .s7linkdialog .s7dialoginputwide { 
    padding-bottom: 10px; 
    width: 430px; 
}
```

Der Freigabe-Link ist in einen Container eingeschlossen und wird mit der folgenden CSS-Klassenauswahl gesteuert:

```
.s7smartcropvideoviewer .s7linkdialog .s7dialoginputcontainer
```

**CSS-Eigenschaften des Dialogfeldeingabecontainers**

<table id="table_7BC1C5919A54483F8121D928DC63233A"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> rand </span> </p> </td> 
   <td colname="col2"> <p>Rand um den Container des freigegebenen Links. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Padding </span> </p> </td> 
   <td colname="col2"> <p>Innenabstand. </p> </td> 
  </tr> 
 </tbody> 
</table>

Beispiel: Zum Festlegen eines grauen Rahmens von einem Pixel um den Einbettungscode-Text und einer Umrandung von neun Pixeln:

```
.s7smartcropvideoviewer .s7linkdialog .s7dialoginputcontainer { 
    border: 1px solid #CCCCCC; 
    padding: 9px; 
}
```

Der Freigabe-Link selbst wird mit der folgenden CSS-Klassenauswahl gesteuert:

```
.s7smartcropvideoviewer .s7linkdialog .s7dialoglink
```

**CSS-Eigenschaften des Dialogfeldfreigabe-Links**

<table id="table_65CF778F5BDA45118208538DCBE203FB"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Linkbreite freigeben. </p> </td> 
  </tr> 
 </tbody> 
</table>

Beispiel: Um den Freigabe-Link auf eine Breite von 450 Pixel festzulegen:

```
.s7smartcropvideoviewer .s7linkdialog .s7dialoglink { 
    width: 450px; 
}
```
