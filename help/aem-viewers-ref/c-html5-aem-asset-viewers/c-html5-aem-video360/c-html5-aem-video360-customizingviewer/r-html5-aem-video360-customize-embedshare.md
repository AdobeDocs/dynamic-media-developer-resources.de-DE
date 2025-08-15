---
title: Freigabe einbetten
description: Das Tool zum Freigeben von Einbettungen besteht aus einer Schaltfläche, die zum Bedienfeld Social-Media-Freigabe und zum modalen Dialogfeld hinzugefügt wird, das angezeigt wird, wenn das Tool aktiviert wird. Die Position der Schaltfläche wird vollständig vom Tool Social Share verwaltet.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,360 VR Video
role: Developer,User
exl-id: 08ba7a29-8b17-4167-a9f3-82aa4cf65556
source-git-commit: 97fbf820590b53de5a1e6ce904e44d6b0ef9a214
workflow-type: tm+mt
source-wordcount: '2631'
ht-degree: 0%

---

# Freigabe einbetten{#embed-share}

Das Tool zum Freigeben von Einbettungen besteht aus einer Schaltfläche, die zum Bedienfeld Social-Media-Freigabe und zum modalen Dialogfeld hinzugefügt wird, das angezeigt wird, wenn das Tool aktiviert wird. Die Position der Schaltfläche wird vollständig vom Tool Social Share verwaltet.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

Das Erscheinungsbild der Freigabeschaltfläche Einbetten wird mit dem folgenden CSS-Klassenselektor gesteuert:

```
.s7video360viewer .s7embedshare
```

**CSS-Eigenschaften des Einbettungs-Freigabe-Tools**

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
   <td colname="col2"> <p> Positionieren Sie sie innerhalb des Bildsets, wenn CSS-Sprites verwendet werden. </p> <p>Siehe auch <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-customizingviewer/c-html5-aem-video360-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> CSS Sprites-</a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Diese Schaltfläche unterstützt die `state`-Attributauswahl, mit der verschiedene Skins auf verschiedene Schaltflächenzustände angewendet werden können.

Sie können die Schaltfläche aus dem Bedienfeld Social-Freigabe entfernen, indem Sie `display:none` CSS-Eigenschaft für die CSS-Klasse festlegen.

Die QuickInfo der Schaltfläche kann lokalisiert werden. Siehe [Lokalisierung von Benutzeroberflächenelementen](../../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-localization.md#concept-16262b8096474d6c9c018c3e99110dd1) für weitere Informationen.

**Beispiel** - Zum Einrichten einer Freigabeschaltfläche für die Einbettung mit 28 x 28 Pixeln, in der für jeden der vier Schaltflächenstatus ein anderes Bild angezeigt wird:

```
.s7video360viewer .s7embedshare { 
 width:28px; 
 height:28px; 
} 
.s7video360viewer .s7embedshare[state='up'] { 
background-image:url(images/v2/EmbedShare_dark_up.png); 
} 
.s7video360viewer .s7embedshare[state='over'] { 
background-image:url(images/v2/EmbedShare_dark_over.png); 
} 
.s7video360viewer .s7embedshare[state='down'] { 
background-image:url(images/v2/EmbedShare_dark_down.png); 
} 
.s7video360viewer .s7embedshare[state='disabled'] { 
background-image:url(images/v2/EmbedShare_dark_disabled.png); 
}
```

Die Hintergrundüberlagerung, die die Web-Seite abdeckt, wenn das Dialogfeld aktiv ist, wird mit dem folgenden CSS-Klassenselektor gesteuert:

```
.s7video360viewer .s7embeddialog .s7backoverlay
```

**CSS-Eigenschaften der Hintergrundüberlagerung**

<table id="table_DB4183CE8061425084D495A355A941F8"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">-</span> </p> </td> 
   <td colname="col2"> <p>Deckkraft der Hintergrundüberlagerung. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">-</span> </p> </td> 
   <td colname="col2"> <p>Hintergrundfarbe der Überlagerung. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Beispiel** - So richten Sie eine Hintergrundüberlagerung ein, die mit einer Deckkraft von 70 % grau dargestellt wird:

```
.s7video360viewer .s7embeddialog .s7backoverlay { 
 opacity:0.7; 
 background-color:#222222; 
}
```

Standardmäßig wird das modale Dialogfeld auf Desktop-Systemen zentriert auf dem Bildschirm angezeigt und nimmt auf Touch-Geräten den gesamten Web-Seitenbereich ein. In allen Fällen werden die Positionierung und Größe des Dialogfelds von der Komponente verwaltet. Das Dialogfeld wird mit dem folgenden CSS-Klassenselektor gesteuert:

```
.s7video360viewer .s7embeddialog .s7dialog
```

**CSS-Eigenschaften des Dialogfelds**

<table id="table_E31711ADF4C7446182549244362199A3"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">-</span> </p> </td> 
   <td colname="col2"> <p> Der Rahmenradius des Dialogfelds, falls das Dialogfeld nicht den gesamten Browser enthält. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">-</span> </p> </td> 
   <td colname="col2"> <p>Hintergrundfarbe des Dialogfelds. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Breite </span> </p> </td> 
   <td colname="col2"> <p>Sollte entweder deaktiviert oder auf 100 % eingestellt sein. In diesem Fall nimmt das Dialogfeld das gesamte Browser-Fenster ein (dieser Modus wird auf Touch-Geräten bevorzugt). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Höhe </span> </p> </td> 
   <td colname="col2"> <p>Sollte entweder deaktiviert oder auf 100 % eingestellt sein. In diesem Fall nimmt das Dialogfeld das gesamte Browser-Fenster ein (dieser Modus wird auf Touch-Geräten bevorzugt). </p> </td> 
  </tr> 
 </tbody> 
</table>

**Beispiel** - Zum Einrichten des Dialogfelds, sodass das gesamte Browser-Fenster verwendet wird und der Hintergrund auf Touch-Geräten weiß ist:

```
.s7video360viewer .s7touchinput .s7embeddialog .s7dialog { 
 width:100%; 
 height:100%; 
background-color: #ffffff; 
}
```

Die Dialogfeldkopfzeile besteht aus einem Symbol, einem Titeltext und einer Schließen-Schaltfläche. Der Header-Container wird gesteuert durch

```
.s7video360viewer .s7embeddialog .s7dialogheader
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

Das Symbol und der Titeltext werden in einen zusätzlichen Container eingeschlossen, der wie folgt gesteuert wird:

```
.s7video360viewer .s7embeddialog .s7dialogheader .s7dialogline
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

Das Kopfzeilensymbol wird mit dem folgenden CSS-Klassenselektor gesteuert:

```
.s7video360viewer .s7embeddialog .s7dialogheadericon
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
   <td colname="col2"> <p> Positionieren Sie sie innerhalb des Bildsets, wenn CSS-Sprites verwendet werden. </p> <p>Siehe auch <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-customizingviewer/c-html5-aem-video360-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> CSS Sprites-</a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

Der Header-Titel wird mit dem folgenden CSS-Klassenselektor gesteuert:

```
.s7video360viewer .s7embeddialog .s7dialogheadertext
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
.s7video360viewer .s7embeddialog .s7closebutton
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
   <td colname="col2"> <p> Positionieren Sie sie innerhalb des Bildsets, wenn CSS-Sprites verwendet werden. </p> <p>Siehe auch <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-customizingviewer/c-html5-aem-video360-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> CSS Sprites-</a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Diese Schaltfläche unterstützt die `state`-Attributauswahl, mit der verschiedene Skins auf verschiedene Schaltflächenzustände angewendet werden können.

Die QuickInfo der Schaltfläche kann lokalisiert werden. Siehe [Lokalisierung von Benutzeroberflächenelementen](../../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-localization.md#concept-16262b8096474d6c9c018c3e99110dd1) für weitere Informationen.

**Beispiel** - Zum Einrichten einer Dialogkopfzeile mit Abstand, einem 24 x 14-Pixel-Symbol und einem fett gedruckten 16-Punkt-Titel. Und schließlich eine Schaltfläche zum Schließen von 28 x 28 Pixeln, die zwei Pixel oben und zwei Pixel rechts vom Dialogfeld-Container positioniert ist:

```
.s7video360viewer .s7embeddialog .s7dialogheader { 
 padding: 10px; 
} 
.s7video360viewer .s7embeddialog .s7dialogheader .s7dialogline { 
 padding: 10px 10px 2px; 
} 
.s7video360viewer .s7embeddialog .s7dialogheadericon { 
    background-image: url("images/sdk/dlgembed_cap.png"); 
    height: 14px; 
    width: 24px; 
} 
.s7video360viewer .s7embeddialog .s7dialogheadertext { 
    font-size: 16pt; 
    font-weight: bold; 
    padding-left: 16px; 
} 
.s7video360viewer .s7embeddialog .s7closebutton { 
 top:2px; 
 right:2px; 
 padding:8px; 
 width:28px; 
 height:28px; 
} 
.s7video360viewer .s7embeddialog .s7closebutton[state='up'] { 
 background-image:url(images/sdk/close_up.png); 
} 
.s7video360viewer .s7embeddialog .s7closebutton[state='over'] { 
 background-image:url(images/sdk/close_over.png); 
} 
.s7video360viewer .s7embeddialog .s7closebutton[state='down'] { 
 background-image:url(images/sdk/close_down.png); 
} 
.s7video360viewer .s7embeddialog .s7closebutton[state='disabled'] { 
 background-image:url(images/sdk/close_disabled.png); 
}
```

Die Fußzeile des Dialogfelds besteht aus der Schaltfläche „Abbrechen“. Der Fußzeilen-Container wird mit dem folgenden CSS-Klassenselektor gesteuert:

```
.s7video360viewer .s7embeddialog .s7dialogfooter
```

**CSS-Eigenschaften des &#x200B;** für die Dialogfeldfußzeile

<table id="table_0AF7AAAB846A46D690896AFD68575669"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">-</span> </p> </td> 
   <td colname="col2"> <p> Rahmen, mit dem Sie die Fußzeile vom Rest des Dialogfelds visuell trennen können. </p> </td> 
  </tr> 
 </tbody> 
</table>

Die Fußzeile hat einen inneren Container, der die Schaltfläche behält. Sie wird mit dem folgenden CSS-Klassenselektor gesteuert:

```
.s7video360viewer .s7embeddialog .s7dialogbuttoncontainer
```

**CSS-Eigenschaften des Schaltflächen-Containers für Dialogfelder**

<table id="table_C34906888A8145C7A61E503DFC6B08A9"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">-</span> </p> </td> 
   <td colname="col2"> <p> Innerer Abstand zwischen Fußzeile und Schaltfläche. </p> </td> 
  </tr> 
 </tbody> 
</table>

Die Schaltfläche „Alle auswählen“ wird mit dem folgenden CSS-Klassenselektor gesteuert:

```
.s7video360viewer .s7embeddialog .s7dialogactionbutton
```

Die Schaltfläche ist nur auf Desktop-Systemen verfügbar.

**CSS-Eigenschaften der Schaltfläche „Alle auswählen“**

<table id="table_021D0467632F49FEBFDF4CF96D2D67C7"> 
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
>Die Schaltfläche Alle auswählen unterstützt die `state`-Attributauswahl, mit der verschiedene Skins auf verschiedene Schaltflächenzustände angewendet werden können.

Die Schaltfläche „Abbrechen“ wird mit dem folgenden CSS-Klassenselektor gesteuert:

```
.s7video360viewer .s7embeddialog .s7dialogcancelbutton
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

Darüber hinaus verwenden beide Schaltflächen eine gemeinsame CSS-Klasse, die CSS-Einstellungen enthalten kann, die für andere Dialogfeldschaltflächen identisch sind:

```
.s7video360viewer .s7embeddialog .s7dialogfooter .s7button
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

Die QuickInfo der Schaltfläche kann lokalisiert werden. Siehe [Lokalisierung von Benutzeroberflächenelementen](../../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-localization.md#concept-16262b8096474d6c9c018c3e99110dd1) für weitere Informationen.

**Beispiel** - zum Einrichten einer Dialogfeldfußzeile mit einer Schaltfläche Abbrechen (64 x 34), die eine Textfarbe und eine Hintergrundfarbe hat, die für jeden Schaltflächenstatus unterschiedlich ist:

```
.s7video360viewer .s7embeddialog .s7dialogfooter { 
    border-top: 1px solid #909090; 
} 
.s7video360viewer .s7embeddialog .s7dialogbuttoncontainer { 
    padding-bottom: 6px; 
    padding-top: 10px; 
} 
.s7video360viewer .s7embeddialog .s7dialogfooter .s7button { 
    box-shadow: 1px 1px 1px #999999; 
    color: #FFFFFF; 
    font-size: 9pt; 
    font-weight: bold; 
    line-height: 34px; 
    margin-right: 10px; 
} 
.s7video360viewer .s7embeddialog .s7dialogcancelbutton { 
 width:64px; 
 height:34px; 
} 
.s7video360viewer .s7embeddialog .s7dialogcancelbutton[state='up'] { 
 background-color:#666666; 
 color:#dddddd; 
} 
.s7video360viewer .s7embeddialog .s7dialogcancelbutton[state='down'] { 
 background-color:#555555; 
 color:#ffffff; 
} 
.s7video360viewer .s7embeddialog .s7dialogcancelbutton[state='over'] { 
 background-color:#555555; 
 color:#ffffff; 
} 
.s7video360viewer .s7embeddialog .s7dialogcancelbutton[state='disabled'] { 
 background-color:#b2b2b2; 
 color:#dddddd; 
} 
.s7video360viewer .s7embeddialog .s7dialogactionbutton { 
 width:82px; 
 height:34px; 
} 
.s7video360viewer .s7embeddialog .s7dialogactionbutton[state='up'] { 
 background-color:#333333; 
 color:#dddddd; 
} 
.s7video360viewer .s7embeddialog .s7dialogactionbutton[state='down'] { 
 background-color:#222222; 
 color:#cccccc; 
} 
.s7video360viewer .s7embeddialog .s7dialogactionbutton[state='over'] { 
 background-color:#222222; 
 color:#cccccc; 
} 
.s7video360viewer .s7embeddialog .s7dialogactionbutton[state='disabled'] { 
 background-color:#b2b2b2; 
 color:#dddddd; 
} 
```

Der Hauptdialogbereich zwischen Kopf- und Fußzeile enthält scrollbaren Dialogfeldinhalt und das Bildlauffeld auf der rechten Seite. In allen Fällen verwaltet die Komponente die Breite dieses Bereichs. Sie kann nicht in CSS festgelegt werden. Der Hauptdialogbereich wird mit dem folgenden CSS-Klassenselektor gesteuert:

```
.s7video360viewer .s7embeddialog .s7dialogviewarea
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

**Beispiel** - Zum Einrichten eines Hauptdialogfeldbereichs mit einer Höhe von 300 Pixel haben Sie einen Rand von 10 Pixel und verwenden einen weißen Hintergrund:

```
.s7video360viewer .s7embeddialog .s7dialogviewarea { 
 background-color:#ffffff; 
 margin:10px; 
 height:300px; 
}
```

Der gesamte Formularinhalt (z. B. Beschriftungen und Eingabefelder) befindet sich in einem Container, der mit dem folgenden CSS-Klassenselektor gesteuert wird:

```
.s7video360viewer .s7embeddialog .s7dialogbody
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

**Beispiel** - um den Formularinhalt so einzurichten, dass er zehn Pixel Abstand aufweist:

```
.s7video360viewer .s7embeddialog .s7dialogbody { 
    padding: 10px; 
}
```

Alle statischen Beschriftungen im Dialogfeldformular werden mit

```
.s7video360viewer .s7embeddialog .s7dialoglabel
```

Diese Klasse ist nicht zur Steuerung der Größe oder Position der Beschriftung geeignet, da Sie sie auf Texte an verschiedenen Stellen der Benutzeroberfläche des Formulars anwenden können.

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

Dialogfeldbeschriftungen können lokalisiert werden. Siehe [Lokalisierung von Benutzeroberflächenelementen](../../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-localization.md#concept-16262b8096474d6c9c018c3e99110dd1) für weitere Informationen.

**Beispiel** - Um alle Beschriftungen als grau festzulegen, verwenden Sie eine fett gedruckte Schriftart mit neun Pixeln:

```
.s7video360viewer .s7embeddialog .s7dialoglabel { 
    color: #666666; 
    font-size: 9pt; 
    font-weight: bold; 
}
```

Die Größe der Textkopie, die über dem Einbettungs-Code angezeigt wird, wird mit dem folgenden CSS-Klassenselektor gesteuert:

```
.s7video360viewer .s7embeddialog .s7dialoginputwide
```

**CSS-Eigenschaften des Eingabefelds des Dialogfelds**

<table id="table_7275B4365DFA4C0386FA2BDB7204A517"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Breite </span> </p> </td> 
   <td colname="col2"> <p>Breite des Eingabefelds. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">-</span> </p> </td> 
   <td colname="col2"> <p>Innerer Abstand. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Beispiel** - Zum Festlegen der Textkopie auf eine Breite von 430 Pixeln und mit einem Abstand von zehn Pixeln am unteren Rand:

```
.s7video360viewer .s7embeddialog .s7dialoginputwide { 
    padding-bottom: 10px; 
    width: 430px; 
}
```

Der Einbettungs-Code wird in einen Container eingeschlossen und mit dem folgenden CSS-Klassenselektor gesteuert:

```
.s7video360viewer .s7embeddialog .s7dialoginputcontainer
```

**CSS-Eigenschaften des Eingabecontainers für das Dialogfeld**

<table id="table_7BC1C5919A54483F8121D928DC63233A"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Breite </span> </p> </td> 
   <td colname="col2"> <p>Die Breite des eingebetteten Code-Containers. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">-</span> </p> </td> 
   <td colname="col2"> <p>Rahmen um den Einbettungs-Code-Container </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">-</span> </p> </td> 
   <td colname="col2"> <p>Innerer Abstand. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Beispiel** - Um einen grauen Rahmen von einem Pixel um den Einbettungs-Code-Text festzulegen, breiten Sie ihn 430 Pixel und haben Sie einen Abstand von zehn Pixeln:

```
.s7video360viewer .s7embeddialog .s7dialoginputcontainer { 
    border: 1px solid #CCCCCC; 
    padding: 10px; 
    width: 430px; 
}
```

Der tatsächliche Einbettungs-Code-Text wird mit dem folgenden CSS-Klassenselektor gesteuert:

```
.s7video360viewer .s7embeddialog .s7dialoginputcontainer
```

**CSS-Eigenschaften des Eingabecontainers für das Dialogfeld**

<table id="table_FEEF66150C69489BB42A2408EBFCE928"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> von </span> </p> </td> 
   <td colname="col2"> <p>Zeilenumbruchstil. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Beispiel** - So konfigurieren Sie Einbettungs-Code für die Verwendung `break-word` Wortumbruchs:

```
.s7video360viewer .s7embeddialog .s7dialogmessage { 
    word-wrap: break-word; 
}
```

Beschriftung und Dropdown-Liste für Einbettungsgröße befinden sich unten im Dialogfeld und werden in einen Container eingefügt, der mit dem folgenden CSS-Klassenselektor gesteuert wird:

```
.s7video360viewer .s7embeddialog .s7dialogembedsizepanel
```

**CSS-Eigenschaften des Bedienfelds „Einbettungsgröße“ des Dialogfelds**

<table id="table_6BA2769361BA4EC4AB7D250EC9486CB2"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">-</span> </p> </td> 
   <td colname="col2"> <p>Innerer Abstand. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Beispiel** - Zum Einrichten eines Bedienfelds „Größe einbetten“, das zehn Pixel Abstand aufweist:

```
.s7video360viewer .s7embeddialog .s7dialogembedsizepanel { 
    padding: 10px; 
}
```

Die Größe und Ausrichtung der Beschriftung für die Einbettungsgröße wird mit dem folgenden CSS-Klassenselektor gesteuert:

```
.s7video360viewer .s7embeddialog .s7dialogembedsizepanel
```

**CSS-Eigenschaften des Bedienfelds „Einbettungsgröße“ des Dialogfelds**

<table id="table_8E50C63C9B1349999251CDB5E5AD3D1D"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> zur vertikalen Ausrichtung </span> </p> </td> 
   <td colname="col2"> <p>Vertikale Ausrichtung des Titels. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Breite </span> </p> </td> 
   <td colname="col2"> <p>Titelbreite. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Beispiel** - Zum Festlegen der Beschriftung für die Einbettungsgröße, dass sie oben ausgerichtet ist und 80 Pixel breit ist:

```
.s7video360viewer .s7embeddialog .s7dialogembedsizelabel { 
    vertical-align: top; 
    width: 80px; 
}
```

Die Breite des Kombinationsfelds Einbettungsgröße wird mit dem folgenden CSS-Klassenselektor gesteuert:

```
.s7video360viewer .s7embeddialog .s7combobox
```

**CSS-Eigenschaften des Kombinationsfelds**

<table id="table_C0FEA0C7353F40039204641BB3F1AE14"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Breite </span> </p> </td> 
   <td colname="col2"> <p>Breite des Kombinationsfelds. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Das Kombinationsfeld unterstützt den `expanded` mit möglichen Werten von `true` und `false`. Der `true` wird verwendet, wenn das Kombinationsfeld eine der vordefinierten Einbettungsgrößen anzeigt. Daher sollte die gesamte verfügbare Breite eingenommen werden. Der `false` wird verwendet, wenn die Option Benutzerdefinierte Größe im Kombinationsfeld ausgewählt ist. Er sollte daher verkleinert werden, um Platz für benutzerdefinierte Eingabefelder für Breite und Höhe zu schaffen.

**Beispiel** - Zum Festlegen des Kombinationsfelds „Einbettungsgröße“, dass es bei der Anzeige eines vordefinierten Elements 300 Pixel breit und bei der Anzeige einer benutzerdefinierten Größe 110 Pixel breit ist:

```
.s7video360viewer .s7embeddialog .s7combobox[expanded="true"] { 
    width: 300px; 
} 
.s7video360viewer .s7embeddialog .s7combobox[expanded="false"] { 
    width: 110px; 
}
```

Die Höhe des Kombinationsfeldtextes wird durch ein spezielles inneres Element definiert und mit dem folgenden CSS-Klassenselektor gesteuert:

```
.s7video360viewer .s7embeddialog .s7combobox .s7comboboxtext
```

**CSS-Eigenschaften des Kombinationsfeld-Texts**

<table id="table_AB60032BF337433F8455DE20AFBA29AB"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Höhe </span> </p> </td> 
   <td colname="col2"> <p>Textfeld-Höhe. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Beispiel** - Zum Festlegen der Einbettungsgröße für die Textfeldhöhe auf 40 Pixel:

```
.s7video360viewer .s7embeddialog .s7combobox .s7comboboxtext { 
    height: 40px; 
}
```

Das Kombinationsfeld verfügt auf der rechten Seite über eine Schaltfläche „Dropdown“ und wird mit dem folgenden CSS-Klassenselektor gesteuert:

```
.s7video360viewer .s7embeddialog .s7combobox .s7comboboxbutton
```

**CSS-Eigenschaften der Kombinationsfeld-Schaltfläche**

<table id="table_70E127FA21264366AD5DBBD7DF40EBAA"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Top-</span> </p> </td> 
   <td colname="col2"> <p>Vertikale Position der Schaltfläche im Kombinationsfeld. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> rechte </span> </p> </td> 
   <td colname="col2"> <p>Horizontale Position der Schaltfläche im Kombinationsfeld. </p> </td> 
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
   <td colname="col1"> <p> <span class="codeph"> Hintergrundbild-</span> </p> </td> 
   <td colname="col2"> <p>Schaltflächenbild für jeden Status. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Hintergrundposition </span> </p> </td> 
   <td colname="col2"> <p> Positionieren Sie sie innerhalb des Bildsets, wenn CSS-Sprites verwendet werden. </p> <p>Siehe auch <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-customizingviewer/c-html5-aem-video360-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> CSS Sprites-</a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Diese Schaltfläche unterstützt die `state`-Attributauswahl, mit der verschiedene Skins auf verschiedene Schaltflächenzustände angewendet werden können.

**Beispiel** - Zum Festlegen einer Dropdown-Schaltfläche auf 28 x 28 Pixel und zum Erstellen eines separaten Bildes für jeden Status:

```
.s7video360viewer .s7embeddialog .s7combobox .s7comboboxbutton { 
 width:28px; 
 height:28px; 
} 
.s7video360viewer .s7embeddialog .s7combobox .s7comboboxbutton[state='up'] { 
 background-image:url(images/sdk/cboxbtndn_up.png); 
} 
.s7video360viewer .s7embeddialog .s7combobox .s7comboboxbutton[state='over'] { 
 background-image:url(images/sdk/cboxbtndn_over.png); 
} 
.s7video360viewer .s7embeddialog .s7combobox .s7comboboxbutton[state='down'] { 
 background-image:url(images/sdk/cboxbtndn_over.png); 
} 
.s7video360viewer .s7embeddialog .s7combobox .s7comboboxbutton[state='disabled'] { 
 background-image:url(images/sdk/cboxbtndn_up.png); 
}
```

Das Bedienfeld mit der Liste der Einbettungsgrößen, die angezeigt wird, wenn das Kombinationsfeld geöffnet wird, wird mit dem folgenden CSS-Klassenselektor gesteuert:

```
.s7video360viewer .s7embeddialog .s7comboboxdropdown
```

Größe und Position des Bedienfelds werden von der Komponente gesteuert. Es ist nicht möglich, sie über CSS zu ändern.

**CSS-Eigenschaften der Dropdown-Liste Kombinationsfeld**

<table id="table_FA7345321C6A4E63B4B78ECF81CE18DB"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">-</span> </p> </td> 
   <td colname="col2"> <p>Rahmen des Bedienfelds. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Beispiel**: So legen Sie für das Kombinationsfeld einen grauen Rahmen von einem Pixel fest:

```
.s7video360viewer .s7embeddialog .s7comboboxdropdown { 
    border: 1px solid #CCCCCC; 
}
```

Ein einzelnes Element in einem Dropdown-Bedienfeld, das mit dem folgenden CSS-Klassenselektor gesteuert wird:

```
.s7video360viewer .s7embeddialog .s7dropdownitemanchor
```

**CSS-Eigenschaften des Dropdown-Element-Ankers**

<table id="table_FD42FDD56F89463A97FD292FAA04DA5A"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">-</span> </p> </td> 
   <td colname="col2"> <p>Element-Hintergrund. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Beispiel** - Zum Festlegen des Kombinationsfeld-Bedienfeldelements auf einen weißen Hintergrund:

```
.s7video360viewer .s7embeddialog .s7dropdownitemanchor { 
    background-color: #FFFFFF; 
}
```

Ein Häkchen, das links neben dem ausgewählten Element im Kombinationsfeld angezeigt wird und mit der folgenden CSS-Klassenauswahl gesteuert wird:

```
.s7video360viewer .s7embeddialog .s7checkmark
```

**CSS-Eigenschaften des Kontrollkästchens**

<table id="table_8E01F5461CD04AC18B2C3725A961476A"> 
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
   <td colname="col2"> <p>Bild des Elements. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Hintergrundposition </span> </p> </td> 
   <td colname="col2"> <p> Positionieren Sie sie innerhalb des Bildsets, wenn CSS-Sprites verwendet werden. </p> <p>Siehe auch <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-customizingviewer/c-html5-aem-video360-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> CSS Sprites-</a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Beispiel** - Zum Festlegen des Häkchensymbols auf 25 x 25 Pixel:

```
.s7video360viewer .s7embeddialog .s7checkmark { 
    background-image: url("images/sdk/cboxchecked.png"); 
    height: 25px; 
    width: 25px; 
}
```

Wenn die Option „Benutzerdefinierte Größe“ im Kombinationsfeld Einbettungsgröße ausgewählt ist, werden im Dialogfeld rechts zwei zusätzliche Eingabefelder angezeigt, damit der Benutzer eine benutzerdefinierte Einbettungsgröße eingeben kann. Diese Felder werden in einen Container eingeschlossen, der mit dem folgenden CSS-Klassenselektor gesteuert wird:

```
.s7video360viewer .s7embeddialog .s7dialogcustomsizepanel
```

**CSS-Eigenschaften des Dialogfelds „Bedienfeld mit benutzerdefinierter Größe“**

<table id="table_B00829EA550F4E5E8F51B1C6ADACCD34"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> linker </span> </p> </td> 
   <td colname="col2"> <p> Abstand zum Kombinationsfeld Einbettungsgröße . </p> </td> 
  </tr> 
 </tbody> 
</table>

**Beispiel** - Zum Festlegen des Bedienfelds für benutzerdefinierte Eingabefelder auf 20 Pixel rechts neben dem Kombinationsfeld:

```
.s7video360viewer .s7embeddialog .s7dialogcustomsizepanel { 
    left: 20px; 
}
```

Jedes Eingabefeld mit benutzerdefinierter Größe ist in einen Container eingeschlossen, der einen Rahmen rendert und den Rand zwischen den Feldern festlegt. Sie wird mit dem folgenden CSS-Klassenselektor gesteuert:

```
.s7video360viewer .s7embeddialog .s7dialogcustomsize
```

**CSS-Eigenschaften des Dialogfelds - Benutzerdefinierte Größe**

<table id="table_A8A04BE1988641618D0A412B8AEEE1C5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">-</span> </p> </td> 
   <td colname="col2"> <p>Rahmen um das Eingabefeld. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Breite </span> </p> </td> 
   <td colname="col2"> <p> Breite des Eingabefelds. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">-</span> </p> </td> 
   <td colname="col2"> <p> Rand des Eingabefelds. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">-</span> </p> </td> 
   <td colname="col2"> <p> Auffüllung des Eingabefelds. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Beispiel** - So legen Sie für die Eingabefelder mit benutzerdefinierter Größe einen grauen Rahmen, einen Rand und einen Abstand von einem Pixel fest und sind 70 Pixel breit:

```
.s7video360viewer .s7embeddialog .s7dialogcustomsize { 
    border: 1px solid #CCCCCC; 
    margin-right: 20px; 
    padding-left: 2px; 
    padding-right: 2px; 
    width: 70px; 
}
```

Wenn ein vertikaler Bildlauf erforderlich ist, wird die Bildlaufleiste im Bereich nahe dem rechten Rand des Dialogfelds gerendert, der mit dem folgenden CSS-Klassenselektor gesteuert wird:

```
.s7video360viewer .s7embeddialog .s7dialogscrollpanel
```

**CSS-Eigenschaften des Bildlaufbedienfelds des Dialogfelds**

<table id="table_BA37E577E0884C919383F84080E2DD28"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Breite </span> </p> </td> 
   <td colname="col2"> <p>Breite des Bildlaufbedienfelds. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Beispiel** - Zum Einrichten eines Bildlauffelds mit einer Breite von 44 Pixel

```
.s7video360viewer .s7embeddialog .s7dialogscrollpanel { 
    width: 44px; 
}
```

Das Erscheinungsbild des Bildlaufleistenbereichs wird mit dem folgenden CSS-Klassenselektor gesteuert:

```
.s7video360viewer .s7embeddialog .s7scrollbar
```

**CSS-Eigenschaften der Bildlaufleiste**

<table id="table_066492417FCA43929017993D7326CDB8"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Breite </span> </p> </td> 
   <td colname="col2"> <p>Breite der Bildlaufleiste. </p> </td> 
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

**Beispiel** - So richten Sie eine Bildlaufleiste ein, die 28 Pixel breit ist und einen acht Pixel umfassenden Rand vom oberen, rechten und unteren Rand des Bildlaufbedienfelds aufweist:

```
.s7video360viewer .s7embeddialog .s7scrollbar { 
    bottom: 8px; 
    right: 8px; 
    top: 8px; 
    width: 28px; 
}
```

Die Bildlaufleistenspur ist der Bereich zwischen den oberen und unteren Bildlaufschaltflächen. Die Komponente legt automatisch die Position und Höhe der Spur fest. Die Spur wird mit dem folgenden CSS-Klassenselektor gesteuert

```
.s7video360viewer .s7embeddialog .s7scrollbar .s7scrolltrack
```

**CSS-Eigenschaften des Bildlaufleisten-Tracks**

<table id="table_19CF5503C1D34ED9998D4F4A6DA7D5D5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Breite </span> </p> </td> 
   <td colname="col2"> <p>Spurbreite. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">-</span> </p> </td> 
   <td colname="col2"> <p> Hintergrundfarbe der Spur. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Beispiel** - zum Einrichten einer Bildlaufleistenspur mit einer Breite von 28 Pixeln und einem grauen Hintergrund:

```
.s7video360viewer .s7embeddialog .s7scrollbar .s7scrolltrack { 
width:28px; 
background-color: #B2B2B2; 
}
```

Der Daumen der Bildlaufleiste bewegt sich vertikal innerhalb eines Bereichs der Bildlaufspur. Seine vertikale Position wird vollständig durch die Komponentenlogik gesteuert. Die Höhe der Daumen ändert sich jedoch nicht dynamisch je nach Inhaltsmenge. Die Höhe des Daumens und andere Aspekte können mit dem folgenden CSS-Klassenselektor konfiguriert werden:

```
.s7video360viewer .s7embeddialog .s7scrollbar .s7scrollthumb
```

**CSS-Eigenschaften des Thumbs der Bildlaufleiste**

<table id="table_90BC468FE138441C9DBAB1EB109F3DB0"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Breite </span> </p> </td> 
   <td colname="col2"> <p>Daumenbreite. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Höhe </span> </p> </td> 
   <td colname="col2"> <p>Daumenhöhe. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">-</span> </p> </td> 
   <td colname="col2"> <p>Der vertikale Abstand zwischen dem oberen Ende der Spur. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">-</span> </p> </td> 
   <td colname="col2"> <p> Der vertikale Abstand zwischen dem unteren Ende der Spur. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Hintergrundbild-</span> </p> </td> 
   <td colname="col2"> <p> Das für einen bestimmten Miniaturbildstatus angezeigte Bild. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Hintergrundposition </span> </p> </td> 
   <td colname="col2"> <p> Positionieren Sie sie innerhalb des Bildsets, wenn CSS-Sprites verwendet werden. </p> <p>Siehe auch <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-customizingviewer/c-html5-aem-video360-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> CSS Sprites-</a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Thumb unterstützt den `state`-Attributselektor , mit dem verschiedene Skins auf verschiedene Daumenzustände angewendet werden können: `up`, `down`, `over` und `disabled`.

**Beispiel** - Zum Einrichten eines Thumb für Bildlaufleisten mit 28 x 45 Pixel, einem Rand von zehn Pixeln oben und unten und unterschiedlichen Grafiken für jeden Status:

```
.s7video360viewer .s7embeddialog .s7scrollbar .s7scrollthumb { 
    height: 45px; 
    padding-bottom: 10px; 
    padding-top: 10px; 
    width: 28px; 
} 
.s7video360viewer .s7embeddialog .s7scrollbar .s7scrollthumb[state="up"] { 
 background-image:url("images/sdk/scrollbar_thumb_up.png"); 
} 
.s7video360viewer .s7embeddialog .s7scrollbar .s7scrollthumb[state="down"] { 
 background-image:url("images/sdk/scrollbar_thumb_down.png"); 
} 
.s7video360viewer .s7embeddialog .s7scrollbar .s7scrollthumb[state="over"] { 
 background-image:url("images/sdk/scrollbar_thumb_over.png"); 
} 
.s7video360viewer .s7embeddialog .s7scrollbar .s7scrollthumb[state="disabled"] { 
 background-image:url("images/sdk/scrollbar_thumb_disabled.png"); 
}
```

Die Darstellung der oberen und unteren Bildlaufschaltflächen wird mit den folgenden CSS-Klassenselektoren gesteuert:

```
.s7video360viewer .s7embeddialog .s7scrollbar .s7scrollupbutton
```

```
.s7video360viewer .s7embeddialog .s7scrollbar .s7scrolldownbutton
```

Scroll-Schaltflächen können nicht mit den Eigenschaften CSS `top`, `left`, `bottom` und `right` positioniert werden. Stattdessen werden sie von der Viewer-Logik automatisch positioniert.

**CSS-Eigenschaften der oberen und unteren Bildlaufschaltflächen**

<table id="table_554BFCFEAF4F43A9AE5F741DC126F833"> 
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
   <td colname="col2"> <p> Das für einen bestimmten Schaltflächenstatus angezeigte Bild. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Hintergrundposition </span> </p> </td> 
   <td colname="col2"> <p> Positionieren Sie sie innerhalb des Bildsets, wenn CSS-Sprites verwendet werden. </p> <p>Siehe auch <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-customizingviewer/c-html5-aem-video360-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> CSS Sprites-</a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Diese Schaltflächen unterstützen die `state`-Attributauswahl, mit der verschiedene Skins auf verschiedene Schaltflächenzustände angewendet werden können: `up`, `down`, `over` und `disabled`.

Die QuickInfos für die Schaltfläche können lokalisiert werden. Siehe [Lokalisierung von Benutzeroberflächenelementen](../../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-localization.md#concept-16262b8096474d6c9c018c3e99110dd1) für weitere Informationen.

**Beispiel** - Zum Einrichten von Bildlaufschaltflächen mit einer Größe von 28 x 32 Pixeln, die für jeden Status unterschiedliche Grafiken aufweisen:

```
.s7video360viewer .s7embeddialog .s7scrollbar .s7scrollupbutton { 
 width:28px; 
 height:32px; 
} 
.s7video360viewer .s7embeddialog .s7scrollbar .s7scrollupbutton[state='up'] { 
background-image:url(images/sdk/scroll_up_up.png); 
} 
.s7video360viewer .s7embeddialog .s7scrollbar .s7scrollupbutton[state='over'] { 
 background-image:url(images/sdk/scroll_up_over.png); 
} 
.s7video360viewer .s7embeddialog .s7scrollbar .s7scrollupbutton[state='down'] { 
 background-image:url(images/sdk/scroll_up_down.png); 
} 
.s7video360viewer .s7embeddialog .s7scrollbar .s7scrollupbutton[state='disabled'] { 
 background-image:url(images/sdk/scroll_up_disabled.png); 
} 
.s7video360viewer .s7embeddialog .s7scrollbar .s7scrolldownbutton { 
 width:28px; 
 height:32px; 
} 
.s7video360viewer .s7embeddialog .s7scrollbar .s7scrolldownbutton[state='up'] { 
 background-image:url(images/sdk/scroll_down_up.png); 
} 
.s7video360viewer .s7embeddialog .s7scrollbar .s7scrolldownbutton[state='over'] { 
 background-image:url(images/sdk/scroll_down_over.png); 
} 
.s7video360viewer .s7embeddialog .s7scrollbar .s7scrolldownbutton[state='down'] { 
 background-image:url(images/sdk/scroll_down_down.png); 
} 
.s7video360viewer .s7embeddialog .s7scrollbar .s7scrolldownbutton[state='disabled'] { 
 background-image:url(images/sdk/scroll_down_disabled.png); 
}
```
