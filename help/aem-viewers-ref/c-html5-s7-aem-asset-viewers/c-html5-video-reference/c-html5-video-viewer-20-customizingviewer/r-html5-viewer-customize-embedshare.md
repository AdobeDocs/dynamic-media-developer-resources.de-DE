---
title: Freigabe einbetten
description: Das Werkzeug Freigabe einbetten besteht aus einer Schaltfläche, die zum Social-Freigabe-Bereich hinzugefügt wird, und dem modalen Dialogfeld, das angezeigt wird, wenn das Tool aktiviert wird. Die Position der Schaltfläche wird vollständig vom Social-Freigabe-Tool verwaltet.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Video
role: Developer,User
exl-id: e29a81b8-67f3-4367-b21c-d5902420bc85
source-git-commit: 97fbf820590b53de5a1e6ce904e44d6b0ef9a214
workflow-type: tm+mt
source-wordcount: '2617'
ht-degree: 0%

---

# Freigabe einbetten{#embed-share}

Das Werkzeug Freigabe einbetten besteht aus einer Schaltfläche, die zum Social-Freigabe-Bereich hinzugefügt wird, und dem modalen Dialogfeld, das angezeigt wird, wenn das Tool aktiviert wird. Die Position der Schaltfläche wird vollständig vom Social-Freigabe-Tool verwaltet.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

Das Erscheinungsbild der Schaltfläche &quot;Freigabe einbetten&quot;wird mit der folgenden CSS-Klassenauswahl gesteuert:

```
.s7videoviewer .s7embedshare
```

**CSS-Eigenschaften des Tools für die Einbettungsfreigabe**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Schaltflächenbreite. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Höhe </span> </p> </td> 
   <td colname="col2"> <p>Schaltflächenhöhe. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image </span> </p> </td> 
   <td colname="col2"> <p> Das Bild, das für einen bestimmten Schaltflächenstatus angezeigt wird. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p> Position innerhalb des Bildsprites, wenn CSS-Sprites verwendet werden. </p> <p>Siehe <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-viewer-20-customizingviewer/c-html5-video-viewer-20-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> CSS-Sprites </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Diese Schaltfläche unterstützt die &quot;`state`&quot;-Attributauswahl, mit der verschiedene Skins auf unterschiedliche Schaltflächenzustände angewendet werden können.

Sie können die Schaltfläche aus dem Social-Freigabebereich entfernen, indem Sie die CSS-Eigenschaft `display:none` in der CSS-Klasse festlegen.

Die QuickInfo der Schaltfläche kann lokalisiert werden. Weitere Informationen finden Sie unter [Lokalisierung von Benutzeroberflächenelementen](../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/r-html5-video-viewer-20-localization.md#concept-1d5ca2d8480f4064a51eddba13940aad) .

Beispiel: So richten Sie eine eingebettete Freigabeschaltfläche mit 28 x 28 Pixel ein und zeigen für jeden der vier verschiedenen Schaltflächenstatus ein anderes Bild an:

```
.s7videoviewer .s7embedshare { 
 width:28px; 
 height:28px; 
} 
.s7videoviewer .s7embedshare[state='up'] { 
background-image:url(images/v2/EmbedShare_dark_up.png); 
} 
.s7videoviewer .s7embedshare[state='over'] { 
background-image:url(images/v2/EmbedShare_dark_over.png); 
} 
.s7videoviewer .s7embedshare[state='down'] { 
background-image:url(images/v2/EmbedShare_dark_down.png); 
} 
.s7videoviewer .s7embedshare[state='disabled'] { 
background-image:url(images/v2/EmbedShare_dark_disabled.png); 
}
```

Die Hintergrundüberlagerung, die die Webseite abdeckt, wenn das Dialogfeld aktiv ist, wird mit der folgenden CSS-Klassenauswahl gesteuert:

```
.s7videoviewer .s7embeddialog .s7backoverlay
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
.s7videoviewer .s7embeddialog .s7backoverlay { 
 opacity:0.7; 
 background-color:#222222; 
}
```

Standardmäßig wird das modale Dialogfeld zentriert auf dem Bildschirm auf Desktop-Systemen angezeigt und nimmt den gesamten Webseitenbereich auf Touch-Geräten. In allen Fällen wird die Positionierung und Größe des Dialogfelds von der Komponente verwaltet. Das Dialogfeld wird mit dem folgenden CSS-Klassenselektor gesteuert:

```
.s7videoviewer .s7embeddialog .s7dialog
```

**CSS-Eigenschaften des Dialogfelds**

<table id="table_E31711ADF4C7446182549244362199A3"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> border-radius </span> </p> </td> 
   <td colname="col2"> <p> Rahmenradius des Dialogfelds, falls das Dialogfeld nicht den gesamten Browser akzeptiert. </p> </td> 
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
   <td colname="col1"> <p> <span class="codeph"> Höhe </span> </p> </td> 
   <td colname="col2"> <p>Sollte entweder nicht festgelegt oder auf 100 % eingestellt sein. In diesem Fall nimmt das Dialogfeld das gesamte Browser-Fenster in Anspruch (dieser Modus wird auf Touch-Geräten empfohlen). </p> </td> 
  </tr> 
 </tbody> 
</table>

Beispiel: Um das Dialogfeld so einzurichten, dass es das gesamte Browser-Fenster mit weißem Hintergrund auf Touch-Geräten verwendet:

```
.s7videoviewer .s7touchinput .s7embeddialog .s7dialog { 
 width:100%; 
 height:100%; 
background-color: #ffffff; 
}
```

Die Kopfzeile des Dialogfelds besteht aus einem Symbol, einem Titeltext und einer Schaltfläche zum Schließen. Der Kopfzeilencontainer wird mit

```
.s7videoviewer .s7embeddialog .s7dialogheader
```

**CSS-Eigenschaften des Dialogfeldheaders**

<table id="table_E407E844C9BD4B5DA8B5BBDE0554F9CA"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Auffüllung </span> </p> </td> 
   <td colname="col2"> <p> Innerer Abstand für Kopfzeileninhalte. </p> </td> 
  </tr> 
 </tbody> 
</table>

Das Symbol und der Titeltext werden in einen zusätzlichen Container eingeschlossen, der mit

```
.s7videoviewer .s7embeddialog .s7dialogheader .s7dialogline
```

**CSS-Eigenschaften der Dialogfeldzeile**

<table id="table_5B03CF843F0D4B1295A3FC1EB50C56F1"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Auffüllung </span> </p> </td> 
   <td colname="col2"> <p> Innerer Abstand für das Kopfzeilensymbol und den Titel </p> </td> 
  </tr> 
 </tbody> 
</table>

Das Kopfzeilensymbol wird mit dem folgenden CSS-Klassenselektor gesteuert

```
.s7videoviewer .s7embeddialog .s7dialogheadericon
```

**CSS-Eigenschaften des Kopfzeilensymbols des Dialogfelds**

<table id="table_DD4B0413721B49CE8E21B4A55BDE8F7D"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Symbolbreite. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Höhe </span> </p> </td> 
   <td colname="col2"> <p>Symbolhöhe. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image </span> </p> </td> 
   <td colname="col2"> <p>Symbolbild. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p> Position innerhalb des Bildsprites, wenn CSS-Sprites verwendet werden. </p> <p>Siehe <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-viewer-20-customizingviewer/c-html5-video-viewer-20-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> CSS-Sprites </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

Der Kopfzeilentitel wird mit der folgenden CSS-Klassenauswahl gesteuert:

```
.s7videoviewer .s7embeddialog .s7dialogheadertext
```

**CSS-Eigenschaften des Kopfzeilentextes des Dialogfelds**

<table id="table_207B4B13153E425EAB38FC61F382A05F"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-weight </span> </p> </td> 
   <td colname="col2"> <p>Schriftstärke. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size </span> </p> </td> 
   <td colname="col2"> <p>Schrifthöhe. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Schriftfamilie </span> </p> </td> 
   <td colname="col2"> <p>Schriftfamilie. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Auffüllung </span> </p> </td> 
   <td colname="col2"> <p>Interner Textabstand. </p> </td> 
  </tr> 
 </tbody> 
</table>

Die Schaltfläche &quot;Schließen&quot;wird mit dem folgenden CSS-Klassenselektor gesteuert:

```
.s7videoviewer .s7embeddialog .s7closebutton
```

**CSS-Eigenschaften der Schließen-Schaltfläche **

<table id="table_FAECBC489FC442588E50E3DA0AC16DD7"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> top </span> </p> </td> 
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
   <td colname="col1"> <p> <span class="codeph"> Höhe </span> </p> </td> 
   <td colname="col2"> <p>Schaltflächenhöhe. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Auffüllung </span> </p> </td> 
   <td colname="col2"> <p>Innerer Abstand der Schaltfläche. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image </span> </p> </td> 
   <td colname="col2"> <p>Schaltflächenbild für jeden Status. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p> Position innerhalb des Bildsprites, wenn CSS-Sprites verwendet werden. </p> <p>Siehe <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-viewer-20-customizingviewer/c-html5-video-viewer-20-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> CSS-Sprites </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Diese Schaltfläche unterstützt die &quot;`state`&quot;-Attributauswahl, mit der verschiedene Skins auf unterschiedliche Schaltflächenzustände angewendet werden können.

Die QuickInfo der Schaltfläche Schließen und der Titel des Dialogfelds können lokalisiert werden. Weitere Informationen finden Sie unter [Lokalisierung von Benutzeroberflächenelementen](../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/r-html5-video-viewer-20-localization.md#concept-1d5ca2d8480f4064a51eddba13940aad) .

Beispiel: Um die Kopfzeile des Dialogfelds mit Abstand einzurichten, klicken Sie auf das Symbol mit 24 x 14 Pixel und geben Sie einen fett gedruckten Titel mit 16 Punkten ein. Und schließlich eine 28 x 28 Pixel lange Schließen-Schaltfläche, die zwei Pixel von der Oberseite und zwei Pixel von der rechten Seite des Dialogfeldcontainers positioniert:

```
.s7videoviewer .s7embeddialog .s7dialogheader { 
 padding: 10px; 
} 
.s7videoviewer .s7embeddialog .s7dialogheader .s7dialogline { 
 padding: 10px 10px 2px; 
} 
.s7videoviewer .s7embeddialog .s7dialogheadericon { 
    background-image: url("images/sdk/dlgembed_cap.png"); 
    height: 14px; 
    width: 24px; 
} 
.s7videoviewer .s7embeddialog .s7dialogheadertext { 
    font-size: 16pt; 
    font-weight: bold; 
    padding-left: 16px; 
} 
.s7videoviewer .s7embeddialog .s7closebutton { 
 top:2px; 
 right:2px; 
 padding:8px; 
 width:28px; 
 height:28px; 
} 
.s7videoviewer .s7embeddialog .s7closebutton[state='up'] { 
 background-image:url(images/sdk/close_up.png); 
} 
.s7videoviewer .s7embeddialog .s7closebutton[state='over'] { 
 background-image:url(images/sdk/close_over.png); 
} 
.s7videoviewer .s7embeddialog .s7closebutton[state='down'] { 
 background-image:url(images/sdk/close_down.png); 
} 
.s7videoviewer .s7embeddialog .s7closebutton[state='disabled'] { 
 background-image:url(images/sdk/close_disabled.png); 
}
```

Die Fußzeile des Dialogfelds besteht aus der Schaltfläche &quot;Abbrechen&quot;. Der Fußzeilencontainer wird mit der folgenden CSS-Klassenauswahl gesteuert:

```
.s7videoviewer .s7embeddialog .s7dialogfooter
```

**CSS-Eigenschaften der Fußzeile des Dialogfelds **

<table id="table_0AF7AAAB846A46D690896AFD68575669"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> border </span> </p> </td> 
   <td colname="col2"> <p> Rand, mit dem Sie die Fußzeile visuell vom Rest des Dialogfelds trennen können. </p> </td> 
  </tr> 
 </tbody> 
</table>

Die Fußzeile verfügt über einen inneren Container, der die Schaltfläche behält. Sie wird mit dem folgenden CSS-Klassenselektor gesteuert:

```
.s7videoviewer .s7embeddialog .s7dialogbuttoncontainer
```

**CSS-Eigenschaften des Dialogfeldschaltflächen-Containers**

<table id="table_C34906888A8145C7A61E503DFC6B08A9"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Auffüllung </span> </p> </td> 
   <td colname="col2"> <p> Abstand zwischen Fußzeile und Schaltfläche innen. </p> </td> 
  </tr> 
 </tbody> 
</table>

Die Schaltfläche Alle auswählen wird mit dem folgenden CSS-Klassenselektor gesteuert:

```
.s7videoviewer .s7embeddialog .s7dialogactionbutton
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
   <td colname="col1"> <p> <span class="codeph"> Höhe </span> </p> </td> 
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
>Die Schaltfläche Alle auswählen unterstützt die Attributauswahl `state` , mit der verschiedene Skins auf unterschiedliche Schaltflächenstatus angewendet werden können.

Die Schaltfläche Abbrechen wird mit der folgenden CSS-Klassenauswahl gesteuert:

```
.s7videoviewer .s7embeddialog .s7dialogcancelbutton
```

**CSS-Eigenschaften des Dialogfelds &quot;Abbrechen&quot;-Schaltfläche**

<table id="table_3DFA90B012F345A3A2A123D6856BE08A"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Schaltflächenbreite. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Höhe </span> </p> </td> 
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
>Die Schaltfläche &quot;Abbrechen&quot;unterstützt die &quot;`state`&quot;-Attributauswahl, mit der verschiedene Skins auf unterschiedliche Schaltflächenzustände angewendet werden können.

Darüber hinaus verwenden beide Schaltflächen eine gemeinsame CSS-Klasse, die CSS-Einstellungen enthalten kann, die für andere Dialogfeldschaltflächen identisch sind:

```
.s7videoviewer .s7embeddialog .s7dialogfooter .s7button
```

**CSS-Eigenschaften der Schaltfläche**

<table id="table_E735E5EDFC1E4F8A962CEA533A88DD4E"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-weight </span> </p> </td> 
   <td colname="col2"> <p>Schriftstärke der Schaltfläche. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size </span> </p> </td> 
   <td colname="col2"> <p>Schriftgröße der Schaltfläche. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Schriftfamilie </span> </p> </td> 
   <td colname="col2"> <p>Schaltflächenschriftart. </p> </td> 
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

Die QuickInfos für Schaltflächen können lokalisiert werden. Weitere Informationen finden Sie unter [Lokalisierung von Benutzeroberflächenelementen](../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/r-html5-video-viewer-20-localization.md#concept-1d5ca2d8480f4064a51eddba13940aad) .

Beispiel: Zum Einrichten einer Fußzeile des Dialogfelds mit einer Schaltfläche &quot;Abbrechen&quot;von 64 x 34, deren Textfarbe und Hintergrundfarbe je nach Schaltflächenstatus unterschiedlich sind:

```
.s7videoviewer .s7embeddialog .s7dialogfooter { 
    border-top: 1px solid #909090; 
} 
.s7videoviewer .s7embeddialog .s7dialogbuttoncontainer { 
    padding-bottom: 6px; 
    padding-top: 10px; 
} 
.s7videoviewer .s7embeddialog .s7dialogfooter .s7button { 
    box-shadow: 1px 1px 1px #999999; 
    color: #FFFFFF; 
    font-size: 9pt; 
    font-weight: bold; 
    line-height: 34px; 
    margin-right: 10px; 
} 
.s7videoviewer .s7embeddialog .s7dialogcancelbutton { 
 width:64px; 
 height:34px; 
} 
.s7videoviewer .s7embeddialog .s7dialogcancelbutton[state='up'] { 
 background-color:#666666; 
 color:#dddddd; 
} 
.s7videoviewer .s7embeddialog .s7dialogcancelbutton[state='down'] { 
 background-color:#555555; 
 color:#ffffff; 
} 
.s7videoviewer .s7embeddialog .s7dialogcancelbutton[state='over'] { 
 background-color:#555555; 
 color:#ffffff; 
} 
.s7videoviewer .s7embeddialog .s7dialogcancelbutton[state='disabled'] { 
 background-color:#b2b2b2; 
 color:#dddddd; 
} 
.s7videoviewer .s7embeddialog .s7dialogactionbutton { 
 width:82px; 
 height:34px; 
} 
.s7videoviewer .s7embeddialog .s7dialogactionbutton[state='up'] { 
 background-color:#333333; 
 color:#dddddd; 
} 
.s7videoviewer .s7embeddialog .s7dialogactionbutton[state='down'] { 
 background-color:#222222; 
 color:#cccccc; 
} 
.s7videoviewer .s7embeddialog .s7dialogactionbutton[state='over'] { 
 background-color:#222222; 
 color:#cccccc; 
} 
.s7videoviewer .s7embeddialog .s7dialogactionbutton[state='disabled'] { 
 background-color:#b2b2b2; 
 color:#dddddd; 
}
```

Der Hauptdialogbereich zwischen der Kopf- und Fußzeile enthält bildlauffähigen Dialogfeldinhalt und Bildlaufbereich auf der rechten Seite. In allen Fällen verwaltet die Komponente die Breite dieses Bereichs. Es ist nicht möglich, ihn in CSS festzulegen. Der Hauptdialogbereich wird mit der folgenden CSS-Klassenauswahl gesteuert:

```
.s7videoviewer .s7embeddialog .s7dialogviewarea
```

**CSS-Eigenschaften des Dialogfelds, in dem der Anzeigebereich angezeigt wird **

<table id="table_3FF4691D848A4C4D8EF060B7E79DEEDE"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Höhe </span> </p> </td> 
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
.s7videoviewer .s7embeddialog .s7dialogviewarea { 
 background-color:#ffffff; 
 margin:10px; 
 height:300px; 
}
```

Der gesamte Formularinhalt (wie Beschriftungen und Eingabefelder) befindet sich in einem Container, der mit

```
.s7videoviewer .s7embeddialog .s7dialogbody
```

Wenn die Höhe dieses Containers größer als der Hauptdialogfeld-Bereich zu sein scheint, wird automatisch ein vertikaler Bildlauf von der Komponente aktiviert.

**CSS-Eigenschaften des Dialogfeldtexts **

<table id="table_5D77F3D5B8CD4B798AA85F722B277F56"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Auffüllung </span> </p> </td> 
   <td colname="col2"> <p>Innerer Abstand. </p> </td> 
  </tr> 
 </tbody> 
</table>

Beispiel: Zum Einrichten von Formularinhalten mit zehn Pixelabständen:

```
.s7videoviewer .s7embeddialog .s7dialogbody { 
    padding: 10px; 
}
```

Alle statischen Beschriftungen im Dialogfeldformular werden mit

```
.s7videoviewer .s7embeddialog .s7dialoglabel
```

Diese Klasse eignet sich nicht zur Steuerung der Größe oder Position der Beschriftung, da Sie sie auf Texte an verschiedenen Stellen der Formular-Benutzeroberfläche anwenden können.

**CSS-Eigenschaften der Dialogfeldbeschriftung. **

<table id="table_13C7874807314ADD83A23075ABB4C340"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-weight </span> </p> </td> 
   <td colname="col2"> <p>Schriftgröße beschriften. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size </span> </p> </td> 
   <td colname="col2"> <p>Schriftgröße beschriften </p> </td> 
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

Die QuickInfos für die Beschriftungen des Dialogfelds können lokalisiert werden. Weitere Informationen finden Sie unter [Lokalisierung von Benutzeroberflächenelementen](../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/r-html5-video-viewer-20-localization.md#concept-1d5ca2d8480f4064a51eddba13940aad) .

Beispiel: Um alle Beschriftungen so einzurichten, dass sie grau und fett mit einer 9-Pixel-Schriftart sind:

```
.s7videoviewer .s7embeddialog .s7dialoglabel { 
    color: #666666; 
    font-size: 9pt; 
    font-weight: bold; 
}
```

Die Größe der Textkopie, die über dem Einbettungscode angezeigt wird, wird mit der folgenden CSS-Klassenauswahl gesteuert:

```
.s7videoviewer .s7embeddialog .s7dialoginputwide
```

**CSS-Eigenschaften des Eingabefelds des Dialogfelds**

<table id="table_7275B4365DFA4C0386FA2BDB7204A517"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Breite des Eingabefelds. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Auffüllung </span> </p> </td> 
   <td colname="col2"> <p>Innerer Abstand. </p> </td> 
  </tr> 
 </tbody> 
</table>

Beispiel: Zum Festlegen einer Textkopie auf eine Breite von 430 Pixel und einen Abstand von zehn Pixel am unteren Rand:

```
.s7videoviewer .s7embeddialog .s7dialoginputwide { 
    padding-bottom: 10px; 
    width: 430px; 
}
```

Der Einbettungscode wird in Container eingeschlossen und mit der folgenden CSS-Klassenauswahl gesteuert:

```
.s7videoviewer .s7embeddialog .s7dialoginputcontainer
```

**CSS-Eigenschaften des Dialogfeldeingabecontainers**

<table id="table_7BC1C5919A54483F8121D928DC63233A"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Die Breite des Einbettungscode-Containers. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> border </span> </p> </td> 
   <td colname="col2"> <p>Ränder um den Einbettungscode-Container. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Auffüllung </span> </p> </td> 
   <td colname="col2"> <p>Innerer Abstand. </p> </td> 
  </tr> 
 </tbody> 
</table>

Beispiel: Um einen grauen Rahmen von einem Pixel um den Einbettungscode-Text festzulegen, legen Sie eine Breite von 430 Pixel fest und weisen einen Abstand von zehn Pixeln auf:

```
.s7videoviewer .s7embeddialog .s7dialoginputcontainer { 
    border: 1px solid #CCCCCC; 
    padding: 10px; 
    width: 430px; 
}
```

Der tatsächliche Einbettungscode-Text wird mit der folgenden CSS-Klassenauswahl gesteuert:

```
.s7videoviewer .s7embeddialog .s7dialoginputcontainer
```

**CSS-Eigenschaften des Dialogfeldeingabecontainers**

<table id="table_FEEF66150C69489BB42A2408EBFCE928"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> word-wrap </span> </p> </td> 
   <td colname="col2"> <p>Wortumbruchstil. </p> </td> 
  </tr> 
 </tbody> 
</table>

Beispiel - So richten Sie eingebetteten Code so ein, dass `break-word` Wortumbruch verwendet wird:

```
.s7videoviewer .s7embeddialog .s7dialogmessage { 
    word-wrap: break-word; 
}
```

Beschriftung und Dropdown-Liste der Einbettungsgröße befinden sich unten im Dialogfeld und werden in einen Container eingefügt, der mit der folgenden CSS-Klassenauswahl gesteuert wird:

```
.s7videoviewer .s7embeddialog .s7dialogembedsizepanel
```

**CSS-Eigenschaften des Dialogfelds Einbettungsgrößenbereich**

<table id="table_6BA2769361BA4EC4AB7D250EC9486CB2"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Auffüllung </span> </p> </td> 
   <td colname="col2"> <p>Innerer Abstand. </p> </td> 
  </tr> 
 </tbody> 
</table>

Beispiel: Zum Einrichten eines Bedienfelds für die Einbettungsgröße mit zehn Pixel Abstand:

```
.s7videoviewer .s7embeddialog .s7dialogembedsizepanel { 
    padding: 10px; 
}
```

Die Größe und Ausrichtung der Beschriftung für die Einbettungsgröße wird mit der folgenden CSS-Klassenauswahl gesteuert:

```
.s7videoviewer .s7embeddialog .s7dialogembedsizepanel
```

**CSS-Eigenschaften des Dialogfelds Einbettungsgrößenbereich**

<table id="table_8E50C63C9B1349999251CDB5E5AD3D1D"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> vertical-align </span> </p> </td> 
   <td colname="col2"> <p>Vertikale Ausrichtung der Beschriftung. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Beschriftungsbreite. </p> </td> 
  </tr> 
 </tbody> 
</table>

Beispiel: Zum Festlegen der Beschriftung für die Einbettungsgröße auf die obere Ausrichtung und eine Breite von 80 Pixel:

```
.s7videoviewer .s7embeddialog .s7dialogembedsizelabel { 
    vertical-align: top; 
    width: 80px; 
}
```

Die Breite des Kombinationsfelds für die Einbettungsgröße wird mit der folgenden CSS-Klassenauswahl gesteuert:

```
.s7videoviewer .s7embeddialog .s7combobox
```

**CSS-Eigenschaften des Kombinationsfelds**

<table id="table_C0FEA0C7353F40039204641BB3F1AE14"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Breite des Kombinationsfeldes. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Das Kombinationsfeld unterstützt die &quot;`expanded`&quot;-Attributauswahl mit möglichen Werten von `true` und `false`. Der Wert `true` wird verwendet, wenn das Kombinationsfeld eine der vordefinierten Einbettungsgrößen anzeigt. Daher sollte die gesamte verfügbare Breite verwendet werden. Der Wert `false` wird verwendet, wenn im Kombinationsfeld die Option &quot;Benutzerdefinierte Größe&quot;ausgewählt ist. Daher sollte er verkleinert werden, um Platz für benutzerdefinierte Eingabefelder für Breite und Höhe zu schaffen.

Beispiel - So legen Sie fest, dass das Kombinationsfeld für die Einbettungsgröße bei der Anzeige eines vordefinierten Elements 300 Pixel breit und bei der Anzeige einer benutzerdefinierten Größe 110 Pixel breit ist:

```
.s7videoviewer .s7embeddialog .s7combobox[expanded="true"] { 
    width: 300px; 
} 
.s7videoviewer .s7embeddialog .s7combobox[expanded="false"] { 
    width: 110px; 
}
```

Die Höhe des Kombinationsfeldtextes wird durch ein spezielles inneres Element definiert und mithilfe des folgenden CSS-Klassenselektors gesteuert:

```
.s7videoviewer .s7embeddialog .s7combobox .s7comboboxtext
```

**CSS-Eigenschaften des Kombinationsfeld-Textes**

<table id="table_AB60032BF337433F8455DE20AFBA29AB"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Höhe </span> </p> </td> 
   <td colname="col2"> <p>Texthöhe im Kombinationsfeld. </p> </td> 
  </tr> 
 </tbody> 
</table>

Beispiel: Zum Festlegen der Höhe des Kombinationsfelds für die Einbettungsgröße auf 40 Pixel:

```
.s7videoviewer .s7embeddialog .s7combobox .s7comboboxtext { 
    height: 40px; 
}
```

Das Kombinationsfeld verfügt über eine Dropdown-Schaltfläche rechts und wird mit der folgenden CSS-Klassenauswahl gesteuert:

```
.s7videoviewer .s7embeddialog .s7combobox .s7comboboxbutton
```

**CSS-Eigenschaften der Kombinationsfeld-Schaltfläche**

<table id="table_70E127FA21264366AD5DBBD7DF40EBAA"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> top </span> </p> </td> 
   <td colname="col2"> <p>Vertikale Schaltflächenposition innerhalb des Kombinationsfelds. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> rechts </span> </p> </td> 
   <td colname="col2"> <p>Horizontale Schaltflächenposition innerhalb des Kombinationsfelds. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Schaltflächenbreite. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Höhe </span> </p> </td> 
   <td colname="col2"> <p>Schaltflächenhöhe. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image </span> </p> </td> 
   <td colname="col2"> <p>Schaltflächenbild für jeden Status. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p> Position innerhalb des Bildsprites, wenn CSS-Sprites verwendet werden. </p> <p>Siehe <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-viewer-20-customizingviewer/c-html5-video-viewer-20-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> CSS-Sprites </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

Diese Schaltfläche unterstützt die &quot;`state`&quot;-Attributauswahl, mit der verschiedene Skins auf unterschiedliche Schaltflächenzustände angewendet werden können.

Beispiel: Um eine Dropdown-Schaltfläche auf 28 x 28 Pixel festzulegen und für jeden Status ein eigenes Bild anzuzeigen:

```
.s7videoviewer .s7embeddialog .s7combobox .s7comboboxbutton { 
 width:28px; 
 height:28px; 
} 
.s7videoviewer .s7embeddialog .s7combobox .s7comboboxbutton[state='up'] { 
 background-image:url(images/sdk/cboxbtndn_up.png); 
} 
.s7videoviewer .s7embeddialog .s7combobox .s7comboboxbutton[state='over'] { 
 background-image:url(images/sdk/cboxbtndn_over.png); 
} 
.s7videoviewer .s7embeddialog .s7combobox .s7comboboxbutton[state='down'] { 
 background-image:url(images/sdk/cboxbtndn_over.png); 
} 
.s7videoviewer .s7embeddialog .s7combobox .s7comboboxbutton[state='disabled'] { 
 background-image:url(images/sdk/cboxbtndn_up.png); 
}
```

Der Bereich mit der Liste der Einbettungsgrößen, die beim Öffnen des Kombinationsfelds angezeigt wird, wird mit der folgenden CSS-Klassenauswahl gesteuert:

```
.s7videoviewer .s7embeddialog .s7comboboxdropdown
```

Die Größe und Position des Bedienfelds wird durch die Komponente gesteuert. Es ist nicht möglich, sie über CSS zu ändern.

**CSS-Eigenschaften des Dropdown-Menüs &quot;Kombinationsfeld&quot;**

<table id="table_FA7345321C6A4E63B4B78ECF81CE18DB"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> border </span> </p> </td> 
   <td colname="col2"> <p>Bereichsrand. </p> </td> 
  </tr> 
 </tbody> 
</table>

Beispiel: Zum Festlegen des Bereichs für das Kombinationsfeld mit einem grauen Rahmen von einem Pixel:

```
.s7videoviewer .s7embeddialog .s7comboboxdropdown { 
    border: 1px solid #CCCCCC; 
}
```

Ein einzelnes Element in einem Dropdown-Bedienfeld, das mit der folgenden CSS-Klassenauswahl gesteuert wird:

```
.s7videoviewer .s7embeddialog .s7dropdownitemanchor
```

**CSS-Eigenschaften des Dropdown-Element-Ankers**

<table id="table_FD42FDD56F89463A97FD292FAA04DA5A"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p>Elementhintergrund. </p> </td> 
  </tr> 
 </tbody> 
</table>

Beispiel: Zum Festlegen des Bereichselements für das Kombinationsfeld mit einem weißen Hintergrund:

```
.s7videoviewer .s7embeddialog .s7dropdownitemanchor { 
    background-color: #FFFFFF; 
}
```

Ein Häkchen, das links neben dem ausgewählten Element im Kombinationsfeld angezeigt wird, das mit der folgenden CSS-Klassenauswahl gesteuert wird:

```
.s7videoviewer .s7embeddialog .s7checkmark
```

**CSS-Eigenschaften des Kontrollkästchenfelds**

<table id="table_8E01F5461CD04AC18B2C3725A961476A"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Symbolbreite. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Höhe </span> </p> </td> 
   <td colname="col2"> <p>Symbolhöhe. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image </span> </p> </td> 
   <td colname="col2"> <p>Elementbild. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p> Position innerhalb des Bildsprites, wenn CSS-Sprites verwendet werden. </p> <p>Siehe <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-viewer-20-customizingviewer/c-html5-video-viewer-20-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> CSS-Sprites </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

Beispiel - zum Festlegen des Kontrollkästchensymbols auf 25 x 25 Pixel:

```
.s7videoviewer .s7embeddialog .s7checkmark { 
    background-image: url("images/sdk/cboxchecked.png"); 
    height: 25px; 
    width: 25px; 
}
```

Wenn die Option &quot;Benutzerdefinierte Größe&quot;im Kombinationsfeld &quot;Einbettungsgröße&quot;ausgewählt ist, werden im Dialogfeld rechts zwei zusätzliche Eingabefelder angezeigt, mit denen der Benutzer eine benutzerdefinierte Einbettungsgröße eingeben kann. Diese Felder sind in einen Container eingeschlossen, der mit der folgenden CSS-Klassenauswahl gesteuert wird:

```
.s7videoviewer .s7embeddialog .s7dialogcustomsizepanel
```

**CSS-Eigenschaften des Dialogfelds, Bereich für benutzerdefinierte Größe**

<table id="table_B00829EA550F4E5E8F51B1C6ADACCD34"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> left </span> </p> </td> 
   <td colname="col2"> <p> Abstand vom Kombinationsfeld für die Einbettungsgröße. </p> </td> 
  </tr> 
 </tbody> 
</table>

Beispiel: Zum Festlegen des Bereichs für Eingabefelder mit benutzerdefinierter Größe auf 20 Pixel rechts neben dem Kombinationsfeld:

```
.s7videoviewer .s7embeddialog .s7dialogcustomsizepanel { 
    left: 20px; 
}
```

Jedes Eingabefeld für die benutzerdefinierte Größe wird in einen Container eingeschlossen, der einen Rahmen rendert und den Rand zwischen den Feldern festlegt. Sie wird mit dem folgenden CSS-Klassenselektor gesteuert:

```
.s7videoviewer .s7embeddialog .s7dialogcustomsize
```

**CSS-Eigenschaften des Dialogfelds, benutzerdefinierte Größe**

<table id="table_A8A04BE1988641618D0A412B8AEEE1C5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> border </span> </p> </td> 
   <td colname="col2"> <p>Rand um das Eingabefeld herum. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p> Breite des Eingabefelds. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margin </span> </p> </td> 
   <td colname="col2"> <p> Spanne der Eingabefelder. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Auffüllung </span> </p> </td> 
   <td colname="col2"> <p> Füllung des Eingabefelds. </p> </td> 
  </tr> 
 </tbody> 
</table>

Beispiel - So legen Sie fest, dass Eingabefelder für die benutzerdefinierte Größe einen grauen Rahmen, einen Rand und einen Abstand von einem Pixel sowie eine Breite von 70 Pixel aufweisen:

```
.s7videoviewer .s7embeddialog .s7dialogcustomsize { 
    border: 1px solid #CCCCCC; 
    margin-right: 20px; 
    padding-left: 2px; 
    padding-right: 2px; 
    width: 70px; 
}
```

Wenn ein vertikaler Bildlauf erforderlich ist, wird die Bildlaufleiste im Bereich nahe der rechten Kante des Dialogfelds gerendert, das mit der folgenden CSS-Klassenauswahl gesteuert wird:

```
.s7videoviewer .s7embeddialog .s7dialogscrollpanel
```

**CSS-Eigenschaften des Bildlaufbereichs des Dialogfelds**

<table id="table_BA37E577E0884C919383F84080E2DD28"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Bildlaufbereichbreite. </p> </td> 
  </tr> 
 </tbody> 
</table>

Beispiel: Um ein Bildlaufbedienfeld einzurichten, das eine Breite von 44 Pixel aufweist

```
.s7videoviewer .s7embeddialog .s7dialogscrollpanel { 
    width: 44px; 
}
```

Das Erscheinungsbild des Bildlaufleistenbereichs wird mit der folgenden CSS-Klassenauswahl gesteuert:

```
.s7videoviewer .s7embeddialog .s7scrollbar
```

**CSS-Eigenschaften der Bildlaufleiste**

<table id="table_066492417FCA43929017993D7326CDB8"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Breite der Bildlaufleiste. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> top </span> </p> </td> 
   <td colname="col2"> <p> Der Versatz der vertikalen Bildlaufleiste am oberen Rand des Bildlaufbereichs. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> unten </span> </p> </td> 
   <td colname="col2"> <p> Der Versatz der vertikalen Bildlaufleiste am unteren Rand des Bildlaufbereichs. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> rechts </span> </p> </td> 
   <td colname="col2"> <p> Der horizontale Versatz der Bildlaufleiste am rechten Rand des Bildlaufbereichs. </p> </td> 
  </tr> 
 </tbody> 
</table>

Beispiel: Um eine Bildlaufleiste einzurichten, die 28 Pixel breit ist und eine 8-Pixel-Spanne von oben, rechts und unten im Bildlaufbedienfeld hat:

```
.s7videoviewer .s7embeddialog .s7scrollbar { 
    bottom: 8px; 
    right: 8px; 
    top: 8px; 
    width: 28px; 
}
```

Die Bildlaufleisten-Spur ist der Bereich zwischen den oberen und unteren Bildlauftasten. Die Komponente legt automatisch die Position und Höhe der Spur fest. Die Verfolgung wird mit dem folgenden CSS-Klassenselektor gesteuert

```
.s7videoviewer .s7embeddialog .s7scrollbar .s7scrolltrack
```

**CSS-Eigenschaften des Bildlaufleisten-Trackings**

<table id="table_19CF5503C1D34ED9998D4F4A6DA7D5D5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Spurbreite. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p> Hintergrundfarbe verfolgen. </p> </td> 
  </tr> 
 </tbody> 
</table>

Beispiel: Zum Einrichten einer Bildlaufleiste, die 28 Pixel breit ist und einen grauen Hintergrund hat:

```
.s7videoviewer .s7embeddialog .s7scrollbar .s7scrolltrack { 
width:28px; 
background-color: #B2B2B2; 
}
```

Der Bildlaufleisten-Daumen bewegt sich in einem Bildlaufverfolgungsbereich vertikal. Seine vertikale Position wird vollständig durch die Komponentenlogik gesteuert. Die Thumb-Höhe ändert sich jedoch nicht dynamisch in Abhängigkeit von der Menge des Inhalts. Die Thumb-Höhe und andere Aspekte können mit der folgenden CSS-Klassenauswahl konfiguriert werden:

```
.s7videoviewer .s7embeddialog .s7scrollbar .s7scrollthumb
```

**CSS-Eigenschaften des Bildlaufleisten-Thumbs**

<table id="table_90BC468FE138441C9DBAB1EB109F3DB0"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Rahmenbreite. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Höhe </span> </p> </td> 
   <td colname="col2"> <p>Schubhöhe. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> padding-top </span> </p> </td> 
   <td colname="col2"> <p>Der vertikale Abstand zwischen dem oberen Ende des Gleises. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> padding-bottom </span> </p> </td> 
   <td colname="col2"> <p> Der vertikale Abstand zwischen dem unteren Ende des Gleises. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image </span> </p> </td> 
   <td colname="col2"> <p> Das Bild, das für einen bestimmten Daumenstatus angezeigt wird. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Thumb unterstützt die &quot;`state`&quot;-Attributauswahl, die verwendet werden kann, um verschiedene Fahnen auf verschiedene Daumenzustände anzuwenden: `up`, `down`, `over` und `disabled`.

Beispiel: Um einen Bildlaufleisten-Daumen mit 28 x 45 Pixel einzurichten, hat einen zehn Pixelrand oben und unten und hat für jeden Status ein anderes Bildmaterial:

```
.s7videoviewer .s7embeddialog .s7scrollbar .s7scrollthumb { 
    height: 45px; 
    padding-bottom: 10px; 
    padding-top: 10px; 
    width: 28px; 
} 
.s7videoviewer .s7embeddialog .s7scrollbar .s7scrollthumb[state="up"] { 
 background-image:url("images/sdk/scrollbar_thumb_up.png"); 
} 
.s7videoviewer .s7embeddialog .s7scrollbar .s7scrollthumb[state="down"] { 
 background-image:url("images/sdk/scrollbar_thumb_down.png"); 
} 
.s7videoviewer .s7embeddialog .s7scrollbar .s7scrollthumb[state="over"] { 
 background-image:url("images/sdk/scrollbar_thumb_over.png"); 
} 
.s7videoviewer .s7embeddialog .s7scrollbar .s7scrollthumb[state="disabled"] { 
 background-image:url("images/sdk/scrollbar_thumb_disabled.png"); 
}
```

Das Erscheinungsbild der oberen und unteren Bildlaufschaltflächen wird mithilfe der folgenden CSS-Klassenselektoren gesteuert:

```
.s7videoviewer .s7embeddialog .s7scrollbar .s7scrollupbutton 
```

```
.s7videoviewer .s7embeddialog .s7scrollbar .s7scrolldownbutton
```

Es ist nicht möglich, Bildlaufschaltflächen mithilfe der CSS-Eigenschaften oben, links, unten und rechts zu positionieren. Stattdessen werden sie von der Viewer-Logik automatisch positioniert.

**CSS-Eigenschaften der oberen und unteren Bildlaufschaltflächen**

<table id="table_554BFCFEAF4F43A9AE5F741DC126F833"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Schaltflächenbreite. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Höhe </span> </p> </td> 
   <td colname="col2"> <p>Schaltflächenhöhe. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image </span> </p> </td> 
   <td colname="col2"> <p> Das für einen bestimmten Schaltflächenstatus angezeigte Bild. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p> Position innerhalb des Bildsprites, wenn CSS-Sprites verwendet werden. </p> <p>Siehe <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-viewer-20-customizingviewer/c-html5-video-viewer-20-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> CSS-Sprites </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Diese Schaltflächen unterstützen den Attributselektor `state` , der verwendet werden kann, um unterschiedliche Schaltflächenzustände anzuwenden: `up`, `down`, `over` und `disabled`.

Die QuickInfos für Schaltflächen können lokalisiert werden. Weitere Informationen finden Sie unter [Lokalisierung von Benutzeroberflächenelementen](../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/r-html5-video-viewer-20-localization.md#concept-1d5ca2d8480f4064a51eddba13940aad) .

Beispiel: Zum Einrichten von Bildlaufschaltflächen mit 28 x 32 Pixel und unterschiedlicher Grafik für jeden Status:

```
.s7videoviewer .s7embeddialog .s7scrollbar .s7scrollupbutton { 
 width:28px; 
 height:32px; 
} 
.s7videoviewer .s7embeddialog .s7scrollbar .s7scrollupbutton[state='up'] { 
background-image:url(images/sdk/scroll_up_up.png); 
} 
.s7videoviewer .s7embeddialog .s7scrollbar .s7scrollupbutton[state='over'] { 
 background-image:url(images/sdk/scroll_up_over.png); 
} 
.s7videoviewer .s7embeddialog .s7scrollbar .s7scrollupbutton[state='down'] { 
 background-image:url(images/sdk/scroll_up_down.png); 
} 
.s7videoviewer .s7embeddialog .s7scrollbar .s7scrollupbutton[state='disabled'] { 
 background-image:url(images/sdk/scroll_up_disabled.png); 
} 
.s7videoviewer .s7embeddialog .s7scrollbar .s7scrolldownbutton { 
 width:28px; 
 height:32px; 
} 
.s7videoviewer .s7embeddialog .s7scrollbar .s7scrolldownbutton[state='up'] { 
 background-image:url(images/sdk/scroll_down_up.png); 
} 
.s7videoviewer .s7embeddialog .s7scrollbar .s7scrolldownbutton[state='over'] { 
 background-image:url(images/sdk/scroll_down_over.png); 
} 
.s7videoviewer .s7embeddialog .s7scrollbar .s7scrolldownbutton[state='down'] { 
 background-image:url(images/sdk/scroll_down_down.png); 
} 
.s7videoviewer .s7embeddialog .s7scrollbar .s7scrolldownbutton[state='disabled'] { 
 background-image:url(images/sdk/scroll_down_disabled.png); 
}
```
