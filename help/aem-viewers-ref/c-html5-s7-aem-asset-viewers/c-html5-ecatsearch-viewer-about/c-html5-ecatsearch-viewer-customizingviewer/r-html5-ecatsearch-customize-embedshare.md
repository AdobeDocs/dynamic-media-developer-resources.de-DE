---
description: Das Werkzeug "Freigabe einbetten"besteht aus einer Schaltfläche, die dem Social Sharing-Bedienfeld hinzugefügt wird, und dem modalen Dialogfeld, das angezeigt wird, wenn das Tool aktiviert wird. Die Position der Schaltfläche wird vollständig vom Social Sharing-Tool verwaltet.
seo-description: Das Werkzeug "Freigabe einbetten"besteht aus einer Schaltfläche, die dem Social Sharing-Bedienfeld hinzugefügt wird, und dem modalen Dialogfeld, das angezeigt wird, wenn das Tool aktiviert wird. Die Position der Schaltfläche wird vollständig vom Social Sharing-Tool verwaltet.
seo-title: Freigabe einbetten
solution: Experience Manager
title: Freigabe einbetten
topic: Dynamic media
uuid: 73d259fe-0978-4f47-95f6-bbfcd3b7bad1
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef
workflow-type: tm+mt
source-wordcount: '2640'
ht-degree: 2%

---


# Share{#embed-share} einbetten

Das Werkzeug &quot;Freigabe einbetten&quot;besteht aus einer Schaltfläche, die dem Social Sharing-Bedienfeld hinzugefügt wird, und dem modalen Dialogfeld, das angezeigt wird, wenn das Tool aktiviert wird. Die Position der Schaltfläche wird vollständig vom Social Sharing-Tool verwaltet.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

Das Erscheinungsbild der Schaltfläche &quot;Freigabe einbetten&quot;wird mit der folgenden CSS-Klassenauswahl gesteuert:

```
.s7ecatalogsearchviewer .s7embedshare
```

**CSS-Eigenschaften des Tools &quot;Freigabe einbetten&quot;**

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
   <td colname="col1"> <p> <span class="codeph"> background-image  </span> </p> </td> 
   <td colname="col2"> <p> Das Bild, das für einen bestimmten Schaltflächenstatus angezeigt wird. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position  </span> </p> </td> 
   <td colname="col2"> <p> Position innerhalb des Bildausschnitt, wenn CSS-Sprites verwendet werden. </p> <p>Siehe auch <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-customizingviewer/c-html5-ecatsearch-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> CSS-Sprites </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Diese Schaltfläche unterstützt die Attributauswahl `state`, mit der verschiedene Skins auf verschiedene Schaltflächenzustände angewendet werden können.

Sie können die Schaltfläche aus dem Social Sharing-Bedienfeld entfernen, indem Sie die CSS-Eigenschaft für `display:none` in der CSS-Klasse festlegen.

Die QuickInfo für Schaltflächen kann lokalisiert werden. Weitere Informationen finden Sie unter [Lokale Anpassung der Elemente der Benutzeroberfläche](../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74).

Beispiel: Zum Einrichten einer Freigabeschaltfläche für die Einbettung, die 28 x 28 Pixel groß ist und für jeden der vier Schaltflächenzustände ein anderes Bild anzeigt:

```
.s7ecatalogsearchviewer .s7embedshare { 
 width:28px; 
 height:28px; 
} 
.s7ecatalogsearchviewer .s7embedshare[state='up'] { 
background-image:url(images/v2/EmbedShare_dark_up.png); 
} 
.s7ecatalogsearchviewer .s7embedshare[state='over'] { 
background-image:url(images/v2/EmbedShare_dark_over.png); 
} 
.s7ecatalogsearchviewer .s7embedshare[state='down'] { 
background-image:url(images/v2/EmbedShare_dark_down.png); 
} 
.s7ecatalogsearchviewer .s7embedshare[state='disabled'] { 
background-image:url(images/v2/EmbedShare_dark_disabled.png); 
}
```

Die Hintergrundüberlagerung, die sich auf der Webseite befindet, wenn das Dialogfeld aktiv ist, wird mit der folgenden CSS-Klassenauswahl gesteuert:

```
.s7ecatalogsearchviewer .s7embeddialog .s7backoverlay
```

**CSS-Eigenschaften der Hintergrundüberlagerung**

<table id="table_DB4183CE8061425084D495A355A941F8"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Deckkraft  </span> </p> </td> 
   <td colname="col2"> <p>Deckkraft der Hintergrundüberlagerung. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color  </span> </p> </td> 
   <td colname="col2"> <p>Hintergrundüberlagerungsfarbe. </p> </td> 
  </tr> 
 </tbody> 
</table>

Beispiel: So richten Sie eine Hintergrundüberlagerung ein, die grau mit einer Deckkraft von 70 % sein soll:

```
.s7ecatalogsearchviewer .s7embeddialog .s7backoverlay { 
 opacity:0.7; 
 background-color:#222222; 
}
```

Standardmäßig wird das modale Dialogfeld auf Desktop-Systemen zentriert angezeigt und nimmt den gesamten Webseitenbereich auf Touch-Geräten. In allen Fällen wird die Positionierung und Größe des Dialogfelds von der Komponente verwaltet. Das Dialogfeld wird mit der folgenden CSS-Klassenauswahl gesteuert:

```
.s7ecatalogsearchviewer .s7embeddialog .s7dialog
```

**CSS-Eigenschaften des Dialogfelds**

<table id="table_E31711ADF4C7446182549244362199A3"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> border-radius  </span> </p> </td> 
   <td colname="col2"> <p> Rahmenradius des Dialogfelds, falls das Dialogfeld nicht den gesamten Browser einnimmt. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color  </span> </p> </td> 
   <td colname="col2"> <p>Hintergrundfarbe des Dialogfelds. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width  </span> </p> </td> 
   <td colname="col2"> <p>Sollte entweder nicht eingestellt oder auf 100 % eingestellt sein. In diesem Fall nimmt das Dialogfeld das gesamte Browserfenster ein (dieser Modus wird auf Touch-Geräten bevorzugt). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height  </span> </p> </td> 
   <td colname="col2"> <p>Sollte entweder nicht eingestellt oder auf 100 % eingestellt sein. In diesem Fall nimmt das Dialogfeld das gesamte Browserfenster ein (dieser Modus wird auf Touch-Geräten bevorzugt). </p> </td> 
  </tr> 
 </tbody> 
</table>

Beispiel: Um das Dialogfeld so einzurichten, dass das gesamte Browserfenster mit einem weißen Hintergrund auf Touch-Geräten verwendet wird:

```
.s7ecatalogsearchviewer .s7touchinput .s7embeddialog .s7dialog { 
 width:100%; 
 height:100%; 
background-color: #ffffff; 
}
```

Die Kopfzeile des Dialogfelds besteht aus einem Symbol, einem Titeltext und einer Schaltfläche zum Schließen. Der Container der Kopfzeile wird mit

```
.s7ecatalogsearchviewer .s7embeddialog .s7dialogheader
```

**CSS-Eigenschaften der Kopfzeile des Dialogfelds**

<table id="table_E407E844C9BD4B5DA8B5BBDE0554F9CA"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Padding </span> </p> </td> 
   <td colname="col2"> <p> Innenabstand für Kopfzeileninhalte. </p> </td> 
  </tr> 
 </tbody> 
</table>

Das Symbol und der Titeltext werden in einen zusätzlichen Container eingeschlossen, der mit

```
.s7ecatalogsearchviewer .s7embeddialog .s7dialogheader .s7dialogline
```

**CSS-Eigenschaften der Dialogelinie**

<table id="table_5B03CF843F0D4B1295A3FC1EB50C56F1"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Padding </span> </p> </td> 
   <td colname="col2"> <p> Innenabstand für das Kopfzeilensymbol und den Titel </p> </td> 
  </tr> 
 </tbody> 
</table>

Das Kopfzeilensymbol wird mit der folgenden CSS-Klassenauswahl gesteuert

```
.s7ecatalogsearchviewer .s7embeddialog .s7dialogheadericon
```

**CSS-Eigenschaften des Dialogfeldkopfzeilensymbols**

<table id="table_DD4B0413721B49CE8E21B4A55BDE8F7D"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width  </span> </p> </td> 
   <td colname="col2"> <p>Symbolbreite </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height  </span> </p> </td> 
   <td colname="col2"> <p>Symbolhöhe. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image  </span> </p> </td> 
   <td colname="col2"> <p>Symbolbild. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position  </span> </p> </td> 
   <td colname="col2"> <p> Position innerhalb des Bildausschnitt, wenn CSS-Sprites verwendet werden. </p> <p>Siehe auch <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-customizingviewer/c-html5-ecatsearch-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> CSS-Sprites </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

Der Kopfzeilentitel wird mit der folgenden CSS-Klassenauswahl gesteuert:

```
.s7ecatalogsearchviewer .s7embeddialog .s7dialogheadertext
```

**CSS-Eigenschaften des Dialogfeldkopfzeilentextes**

<table id="table_207B4B13153E425EAB38FC61F382A05F"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-Gewichtung  </span> </p> </td> 
   <td colname="col2"> <p>Schriftart-Gewichtung. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size  </span> </p> </td> 
   <td colname="col2"> <p>Schrifthöhe. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family  </span> </p> </td> 
   <td colname="col2"> <p>Schriftfamilie. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Padding </span> </p> </td> 
   <td colname="col2"> <p>Interne Textfüllung. </p> </td> 
  </tr> 
 </tbody> 
</table>

Die Schließen-Schaltfläche wird mit dem folgenden CSS-Klassenselektor gesteuert:

```
.s7ecatalogsearchviewer .s7embeddialog .s7closebutton
```

**CSS-Eigenschaften der Schließen-Schaltfläche **

<table id="table_FAECBC489FC442588E50E3DA0AC16DD7"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Anfang </span> </p> </td> 
   <td colname="col2"> <p> Vertikale Schaltflächenposition relativ zum Container der Kopfzeile. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> rechts </span> </p> </td> 
   <td colname="col2"> <p> Horizontale Schaltflächenposition relativ zum Container der Kopfzeile. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width  </span> </p> </td> 
   <td colname="col2"> <p>Schaltflächenbreite. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height  </span> </p> </td> 
   <td colname="col2"> <p>Schaltflächenhöhe. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Padding </span> </p> </td> 
   <td colname="col2"> <p>Innenabstand der Schaltfläche. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image  </span> </p> </td> 
   <td colname="col2"> <p>Schaltflächenbild für jeden Status. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position  </span> </p> </td> 
   <td colname="col2"> <p> Position innerhalb des Bildausschnitt, wenn CSS-Sprites verwendet werden. </p> <p>Siehe auch <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-customizingviewer/c-html5-ecatsearch-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> CSS-Sprites </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Diese Schaltfläche unterstützt die Attributauswahl `state`, mit der verschiedene Skins auf verschiedene Schaltflächenzustände angewendet werden können.

Die QuickInfo für Schaltflächen kann lokalisiert werden. Weitere Informationen finden Sie unter [Lokale Anpassung der Elemente der Benutzeroberfläche](../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74).

Beispiel: Zum Einrichten einer Dialogkopfzeile mit Auffüllung, einem Symbol mit 24 x 14 Pixeln, einem fett gedruckten Titel mit 16 Punkten und einer Schließen-Schaltfläche mit 28 x 28 Pixeln, die zwei Pixel von oben und zwei Pixel von rechts vom Dialog-Container positioniert werden:

```
.s7ecatalogsearchviewer .s7embeddialog .s7dialogheader { 
 padding: 10px; 
} 
.s7ecatalogsearchviewer .s7embeddialog .s7dialogheader .s7dialogline { 
 padding: 10px 10px 2px; 
} 
.s7ecatalogsearchviewer .s7embeddialog .s7dialogheadericon { 
    background-image: url("images/sdk/dlgembed_cap.png"); 
    height: 14px; 
    width: 24px; 
} 
.s7ecatalogsearchviewer .s7embeddialog .s7dialogheadertext { 
    font-size: 16pt; 
    font-weight: bold; 
    padding-left: 16px; 
} 
.s7ecatalogsearchviewer .s7embeddialog .s7closebutton { 
 top:2px; 
 right:2px; 
 padding:8px; 
 width:28px; 
 height:28px; 
} 
.s7ecatalogsearchviewer .s7embeddialog .s7closebutton[state='up'] { 
 background-image:url(images/sdk/close_up.png); 
} 
.s7ecatalogsearchviewer .s7embeddialog .s7closebutton[state='over'] { 
 background-image:url(images/sdk/close_over.png); 
} 
.s7ecatalogsearchviewer .s7embeddialog .s7closebutton[state='down'] { 
 background-image:url(images/sdk/close_down.png); 
} 
.s7ecatalogsearchviewer .s7embeddialog .s7closebutton[state='disabled'] { 
 background-image:url(images/sdk/close_disabled.png); 
}
```

Die Dialogfußzeile besteht aus der Schaltfläche &quot;Abbrechen&quot;. Der Container der Fußzeile wird mit der folgenden CSS-Klassenauswahl gesteuert:

```
.s7ecatalogsearchviewer .s7embeddialog .s7dialogfooter
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

Die Fußzeile hat einen inneren Container, der die Schaltfläche behält. Sie wird mit der folgenden CSS-Klassenauswahl gesteuert:

```
.s7ecatalogsearchviewer .s7embeddialog .s7dialogbuttoncontainer
```

**CSS-Eigenschaften des Containers für die Schaltfläche &quot;Dialogfeld&quot;**

<table id="table_C34906888A8145C7A61E503DFC6B08A9"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Padding </span> </p> </td> 
   <td colname="col2"> <p> Innere Umrandung zwischen der Fußzeile und der Schaltfläche. </p> </td> 
  </tr> 
 </tbody> 
</table>

Die Schaltfläche &quot;Alle auswählen&quot;wird mit dem folgenden CSS-Klassenselektor gesteuert:

```
.s7ecatalogsearchviewer .s7embeddialog .s7dialogactionbutton
```

Die Schaltfläche ist nur auf Desktop-Systemen verfügbar.

**CSS-Eigenschaften der Schaltfläche &quot;Alles auswählen&quot;**

<table id="table_021D0467632F49FEBFDF4CF96D2D67C7"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width  </span> </p> </td> 
   <td colname="col2"> <p>Schaltflächenbreite. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height  </span> </p> </td> 
   <td colname="col2"> <p>Schaltflächenhöhe. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> color </span> </p> </td> 
   <td colname="col2"> <p> Schaltflächentextfarbe für jeden Status. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color  </span> </p> </td> 
   <td colname="col2"> <p> Hintergrundfarbe der Schaltflächen für jeden Status. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Die Schaltfläche &quot;Alles auswählen&quot;unterstützt die Attributauswahl `state`, mit der verschiedene Skins auf verschiedene Schaltflächenzustände angewendet werden können.

Die Schaltfläche &quot;Abbrechen&quot;wird mit dem folgenden CSS-Klassenselektor gesteuert:

```
.s7ecatalogsearchviewer .s7embeddialog .s7dialogcancelbutton
```

**CSS-Eigenschaften der Schaltfläche &quot;Abbrechen&quot;im Dialogfeld**

<table id="table_3DFA90B012F345A3A2A123D6856BE08A"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width  </span> </p> </td> 
   <td colname="col2"> <p>Schaltflächenbreite. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height  </span> </p> </td> 
   <td colname="col2"> <p>Schaltflächenhöhe. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> color  </span> </p> </td> 
   <td colname="col2"> <p> Schaltflächentextfarbe für jeden Status. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color  </span> </p> </td> 
   <td colname="col2"> <p> Hintergrundfarbe der Schaltflächen für jeden Status. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Diese Schaltfläche unterstützt die Attributauswahl `state`, mit der verschiedene Skins auf verschiedene Schaltflächenzustände angewendet werden können.

Darüber hinaus verwenden beide Schaltflächen dieselbe CSS-Klasse, die CSS-Einstellungen enthalten kann, die für andere Dialogfeldschaltflächen gleich sind:

```
.s7ecatalogsearchviewer .s7embeddialog .s7dialogfooter .s7button
```

**CSS-Eigenschaften der Schaltfläche**

<table id="table_E735E5EDFC1E4F8A962CEA533A88DD4E"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-Gewichtung  </span> </p> </td> 
   <td colname="col2"> <p>Gewichtung der Schaltflächenschrift. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size  </span> </p> </td> 
   <td colname="col2"> <p>Schaltflächenschriftgröße </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family  </span> </p> </td> 
   <td colname="col2"> <p>Schaltflächenschriftfamilie. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> line-height  </span> </p> </td> 
   <td colname="col2"> <p> Texthöhe innerhalb der Schaltfläche. Betrifft die vertikale Ausrichtung. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> box-shadow  </span> </p> </td> 
   <td colname="col2"> <p>Schlagschatten. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margin-right  </span> </p> </td> 
   <td colname="col2"> <p>Ränder der rechten Schaltfläche. </p> </td> 
  </tr> 
 </tbody> 
</table>

Die QuickInfo für Schaltflächen kann lokalisiert werden. Weitere Informationen finden Sie unter [Lokale Anpassung der Elemente der Benutzeroberfläche](../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74).

Beispiel: Zum Einrichten einer Fußzeile des Dialogfelds mit der Schaltfläche &quot;Abbrechen&quot;im Format 64 x 34, einer Schaltfläche &quot;Alles auswählen&quot;im Format 82 x 34 und einer für jeden Schaltflächenstatus unterschiedlichen Textfarbe und Hintergrundfarbe:

```
.s7ecatalogsearchviewer .s7embeddialog .s7dialogfooter { 
    border-top: 1px solid #909090; 
} 
.s7ecatalogsearchviewer .s7embeddialog .s7dialogbuttoncontainer { 
    padding-bottom: 6px; 
    padding-top: 10px; 
} 
.s7ecatalogsearchviewer .s7embeddialog .s7dialogfooter .s7button { 
    box-shadow: 1px 1px 1px #999999; 
    color: #FFFFFF; 
    font-size: 9pt; 
    font-weight: bold; 
    line-height: 34px; 
    margin-right: 10px; 
} 
.s7ecatalogsearchviewer .s7embeddialog .s7dialogcancelbutton { 
 width:64px; 
 height:34px; 
} 
.s7ecatalogsearchviewer .s7embeddialog .s7dialogcancelbutton[state='up'] { 
 background-color:#666666; 
 color:#dddddd; 
} 
.s7ecatalogsearchviewer .s7embeddialog .s7dialogcancelbutton[state='down'] { 
 background-color:#555555; 
 color:#ffffff; 
} 
.s7ecatalogsearchviewer .s7embeddialog .s7dialogcancelbutton[state='over'] { 
 background-color:#555555; 
 color:#ffffff; 
} 
.s7ecatalogsearchviewer .s7embeddialog .s7dialogcancelbutton[state='disabled'] { 
 background-color:#b2b2b2; 
 color:#dddddd; 
} 
.s7ecatalogsearchviewer .s7embeddialog .s7dialogactionbutton { 
 width:82px; 
 height:34px; 
} 
.s7ecatalogsearchviewer .s7embeddialog .s7dialogactionbutton[state='up'] { 
 background-color:#333333; 
 color:#dddddd; 
} 
.s7ecatalogsearchviewer .s7embeddialog .s7dialogactionbutton[state='down'] { 
 background-color:#222222; 
 color:#cccccc; 
} 
.s7ecatalogsearchviewer .s7embeddialog .s7dialogactionbutton[state='over'] { 
 background-color:#222222; 
 color:#cccccc; 
} 
.s7ecatalogsearchviewer .s7embeddialog .s7dialogactionbutton[state='disabled'] { 
 background-color:#b2b2b2; 
 color:#dddddd; 
}
```

Der Hauptdialogbereich (zwischen der Kopf- und Fußzeile) enthält durchlaufbare Dialogfeldinhalte und den Bildlaufbereich auf der rechten Seite. In allen Fällen verwaltet die Komponente die Breite dieses Bereichs, es ist nicht möglich, es in CSS festzulegen. Der Hauptdialogbereich wird mit der folgenden CSS-Klassenauswahl gesteuert:

```
.s7ecatalogsearchviewer .s7embeddialog .s7dialogviewarea
```

**CSS-Eigenschaften des Dialogfelds für den Anzeigebereich **

<table id="table_3FF4691D848A4C4D8EF060B7E79DEEDE"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height  </span> </p> </td> 
   <td colname="col2"> <p> Die Höhe des Hauptdialogfeldbereichs. Sie sollte nur angegeben werden, wenn das Dialogfeld im Desktop-Modus funktioniert. Dies ist nicht möglich, wenn die Größe des Dialogfelds die Größe des gesamten Browserfensters einnimmt. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color  </span> </p> </td> 
   <td colname="col2"> <p>Die Hintergrundfarbe des Hauptdialogfeldbereichs. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margin </span> </p> </td> 
   <td colname="col2"> <p>Äußerer Rand. </p> </td> 
  </tr> 
 </tbody> 
</table>

Beispiel: Um einen Hauptdialogfeldbereich auf eine Höhe von 300 Pixel festzulegen, haben Sie einen Ränder von 10 Pixeln und verwenden Sie einen weißen Hintergrund:

```
.s7ecatalogsearchviewer .s7embeddialog .s7dialogviewarea { 
 background-color:#ffffff; 
 margin:10px; 
 height:300px; 
}
```

Der gesamte Formularinhalt (wie Beschriftungen und Eingabefelder) befindet sich in einem Container, der mit der folgenden CSS-Klassenauswahl gesteuert wird:

```
.s7ecatalogsearchviewer .s7embeddialog .s7dialogbody
```

Wenn die Höhe dieses Containers größer als der des Hauptdialogfelds zu sein scheint, wird automatisch ein vertikaler Bildlauf von der Komponente aktiviert.

**CSS-Eigenschaften des Dialogfeldtextes **

<table id="table_5D77F3D5B8CD4B798AA85F722B277F56"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Padding </span> </p> </td> 
   <td colname="col2"> <p>Innenabstand. </p> </td> 
  </tr> 
 </tbody> 
</table>

Beispiel: So richten Sie Formularinhalte mit einer Auffüllung von zehn Pixeln ein:

```
.s7ecatalogsearchviewer .s7embeddialog .s7dialogbody { 
    padding: 10px; 
}
```

Alle statischen Beschriftungen im Dialogfeld werden mit

```
.s7ecatalogsearchviewer .s7embeddialog .s7dialoglabel
```

Diese Klasse eignet sich nicht zur Steuerung der Beschriftungsgröße oder -position, da Sie sie an verschiedenen Stellen der Benutzeroberfläche des Formulars auf Texte anwenden können.

**CSS-Eigenschaften der Beschriftung des Dialogfelds. **

<table id="table_13C7874807314ADD83A23075ABB4C340"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-Gewichtung  </span> </p> </td> 
   <td colname="col2"> <p>Gewichtung der Beschriftungsschrift </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size  </span> </p> </td> 
   <td colname="col2"> <p>Schriftgröße beschriften. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family  </span> </p> </td> 
   <td colname="col2"> <p>Schriftfamilie beschriften. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> color  </span> </p> </td> 
   <td colname="col2"> <p>Beschriftungstextfarbe. </p> </td> 
  </tr> 
 </tbody> 
</table>

Dialogfeldbeschriftungen können lokalisiert werden. Weitere Informationen finden Sie unter [Lokale Anpassung der Elemente der Benutzeroberfläche](../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74).

Beispiel: So richten Sie alle Beschriftungen so ein, dass sie grau und fett mit einer Schrift von neun Pixeln sind:

```
.s7ecatalogsearchviewer .s7embeddialog .s7dialoglabel { 
    color: #666666; 
    font-size: 9pt; 
    font-weight: bold; 
}
```

Die Größe der Textkopie, die über dem Einbettungscode angezeigt wird, wird mit der folgenden CSS-Klassenauswahl gesteuert:

```
.s7ecatalogsearchviewer .s7embeddialog .s7dialoginputwide
```

**CSS-Eigenschaften des Dialogfelds geben breites Feld ein**

<table id="table_7275B4365DFA4C0386FA2BDB7204A517"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width  </span> </p> </td> 
   <td colname="col2"> <p>Breite des Eingabefelds. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Padding </span> </p> </td> 
   <td colname="col2"> <p>Innenabstand. </p> </td> 
  </tr> 
 </tbody> 
</table>

Beispiel: Um die Textkopie auf eine Breite von 430 Pixeln festzulegen und unten eine Auffüllung von 10 Pixeln einzustellen,

```
.s7ecatalogsearchviewer .s7embeddialog .s7dialoginputwide { 
    padding-bottom: 10px; 
    width: 430px; 
}
```

Der Einbettungscode wird in Container eingeschlossen und mit der folgenden CSS-Klassenauswahl gesteuert:

```
.s7ecatalogsearchviewer .s7embeddialog .s7dialoginputcontainer
```

**CSS-Eigenschaften des Containers für die Eingabe im Dialogfeld**

<table id="table_7BC1C5919A54483F8121D928DC63233A"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width  </span> </p> </td> 
   <td colname="col2"> <p>Die Breite des Einbettungscode-Containers. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> rand </span> </p> </td> 
   <td colname="col2"> <p>Ränder um den Einbettungscode-Container. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Padding </span> </p> </td> 
   <td colname="col2"> <p>Innenabstand. </p> </td> 
  </tr> 
 </tbody> 
</table>

Beispiel: Um einen grauen Rahmen von einem Pixel um den eingebetteten Code festzulegen, muss der Text 430 Pixel breit sein und eine zehnPixel lange Auffüllung aufweisen:

```
.s7ecatalogsearchviewer .s7embeddialog .s7dialoginputcontainer { 
    border: 1px solid #CCCCCC; 
    padding: 10px; 
    width: 430px; 
}
```

Der tatsächliche Einbettungscode-Text wird mit der folgenden CSS-Klassenauswahl gesteuert:

```
.s7ecatalogsearchviewer .s7embeddialog .s7dialoginputcontainer
```

**CSS-Eigenschaften des Containers für die Eingabe im Dialogfeld**

<table id="table_FEEF66150C69489BB42A2408EBFCE928"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> word-wrap  </span> </p> </td> 
   <td colname="col2"> <p>Umbruchstil. </p> </td> 
  </tr> 
 </tbody> 
</table>

Beispiel: So richten Sie Einbettungscode für die Verwendung von `break-word` Wortumbruch ein:

```
.s7ecatalogsearchviewer .s7embeddialog .s7dialogmessage { 
    word-wrap: break-word; 
}
```

Beschriftung und Dropdown-Liste der Einbettungsgröße befinden sich unten im Dialogfeld und werden in einen Container eingefügt, der mit der folgenden CSS-Klassenauswahl gesteuert wird:

```
.s7ecatalogsearchviewer .s7embeddialog .s7dialogembedsizepanel
```

**CSS-Eigenschaften des Bedienfelds &quot;Einbettungsgröße&quot;des Dialogfelds**

<table id="table_6BA2769361BA4EC4AB7D250EC9486CB2"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Padding </span> </p> </td> 
   <td colname="col2"> <p>Innenabstand. </p> </td> 
  </tr> 
 </tbody> 
</table>

Beispiel: So richten Sie ein Bedienfeld für die Einbettungsgröße ein, das zehn Pixel Abstand hat:

```
.s7ecatalogsearchviewer .s7embeddialog .s7dialogembedsizepanel { 
    padding: 10px; 
}
```

Die Größe und Ausrichtung der Beschriftung der Einbettgröße wird mit der folgenden CSS-Klassenauswahl gesteuert:

```
.s7ecatalogsearchviewer .s7embeddialog .s7dialogembedsizepanel
```

**CSS-Eigenschaften des Bedienfelds &quot;Einbettungsgröße&quot;des Dialogfelds**

<table id="table_8E50C63C9B1349999251CDB5E5AD3D1D"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> vertical-align  </span> </p> </td> 
   <td colname="col2"> <p>Ausrichtung der vertikalen Beschriftung. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width  </span> </p> </td> 
   <td colname="col2"> <p>Beschriftungsbreite. </p> </td> 
  </tr> 
 </tbody> 
</table>

Beispiel: So legen Sie fest, dass die Beschriftung für die Einbettungsgröße oben ausgerichtet und 80 Pixel breit ist:

```
.s7ecatalogsearchviewer .s7embeddialog .s7dialogembedsizelabel { 
    vertical-align: top; 
    width: 80px; 
}
```

Die Breite des Kombinationsfelds für die Einbettgröße wird mit der folgenden CSS-Klassenauswahl gesteuert:

```
.s7ecatalogsearchviewer .s7embeddialog .s7combobox
```

**CSS-Eigenschaften des Kombinationsfeldes**

<table id="table_C0FEA0C7353F40039204641BB3F1AE14"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width  </span> </p> </td> 
   <td colname="col2"> <p>Breite des Kombinationsfeldes. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Das Kombinationsfeld unterstützt die Attributauswahl `expanded` mit möglichen Werten von `true` und `false`. `true` wird verwendet, wenn das Kombinationsfeld eine der vordefinierten Einbettungsgrößen anzeigt. Daher sollte die gesamte verfügbare Breite verwendet werden. `false` wird verwendet, wenn im Kombinationsfeld die Option &quot;Benutzerdefinierte Größe&quot;ausgewählt ist. Daher sollte sie verringert werden, um Platz für benutzerdefinierte Eingabe-Felder für Breite und Höhe zu schaffen.

Beispiel: Das Kombinationsfeld für die Einbettungsgröße muss bei der Anzeige eines vordefinierten Elements 300 Pixel breit und bei der Anzeige einer benutzerdefinierten Größe 110 Pixel breit sein:

```
.s7ecatalogsearchviewer .s7embeddialog .s7combobox[expanded="true"] { 
    width: 300px; 
} 
.s7ecatalogsearchviewer .s7embeddialog .s7combobox[expanded="false"] { 
    width: 110px; 
}
```

Die Höhe des Kombinationsfeldtextes wird durch ein spezielles inneres Element definiert und mit der folgenden CSS-Klassenauswahl gesteuert:

```
.s7ecatalogsearchviewer .s7embeddialog .s7combobox .s7comboboxtext
```

**CSS-Eigenschaften des Kombinationsfeldtexts**

<table id="table_AB60032BF337433F8455DE20AFBA29AB"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height  </span> </p> </td> 
   <td colname="col2"> <p>Texthöhe des Kombinationsfeldes </p> </td> 
  </tr> 
 </tbody> 
</table>

Beispiel: So legen Sie die Höhe des Kombinationsfeldeinsatzes auf 40 Pixel fest:

```
.s7ecatalogsearchviewer .s7embeddialog .s7combobox .s7comboboxtext { 
    height: 40px; 
}
```

Das Kombinationsfeld verfügt über eine Dropdownschaltfläche auf der rechten Seite und wird mit der folgenden CSS-Klassenauswahl gesteuert:

```
.s7ecatalogsearchviewer .s7embeddialog .s7combobox .s7comboboxbutton
```

**CSS-Eigenschaften der Schaltfläche &quot;Kombinationsfeld&quot;**

<table id="table_70E127FA21264366AD5DBBD7DF40EBAA"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Anfang </span> </p> </td> 
   <td colname="col2"> <p>Vertikale Schaltflächenposition im Kombinationsfeld. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> rechts </span> </p> </td> 
   <td colname="col2"> <p>Horizontale Schaltflächenposition innerhalb des Kombinationsfelds. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width  </span> </p> </td> 
   <td colname="col2"> <p>Schaltflächenbreite. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height  </span> </p> </td> 
   <td colname="col2"> <p>Schaltflächenhöhe. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image  </span> </p> </td> 
   <td colname="col2"> <p>Schaltflächenbild für jeden Status. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position  </span> </p> </td> 
   <td colname="col2"> <p> Position innerhalb des Bildausschnitt, wenn CSS-Sprites verwendet werden. </p> <p>Siehe auch <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-customizingviewer/c-html5-ecatsearch-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> CSS-Sprites </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Diese Schaltfläche unterstützt die Attributauswahl `state`, mit der verschiedene Skins auf verschiedene Schaltflächenzustände angewendet werden können.

Beispiel: Um eine Dropdown-Schaltfläche auf 28 x 28 Pixel festzulegen und für jeden Status ein separates Bild anzuzeigen:

```
.s7ecatalogsearchviewer .s7embeddialog .s7combobox .s7comboboxbutton { 
 width:28px; 
 height:28px; 
} 
.s7ecatalogsearchviewer .s7embeddialog .s7combobox .s7comboboxbutton[state='up'] { 
 background-image:url(images/sdk/cboxbtndn_up.png); 
} 
.s7ecatalogsearchviewer .s7embeddialog .s7combobox .s7comboboxbutton[state='over'] { 
 background-image:url(images/sdk/cboxbtndn_over.png); 
} 
.s7ecatalogsearchviewer .s7embeddialog .s7combobox .s7comboboxbutton[state='down'] { 
 background-image:url(images/sdk/cboxbtndn_over.png); 
} 
.s7ecatalogsearchviewer .s7embeddialog .s7combobox .s7comboboxbutton[state='disabled'] { 
 background-image:url(images/sdk/cboxbtndn_up.png); 
}
```

Der Bereich mit der Liste der beim Öffnen des Kombinationsfeldes angezeigten Einbettungsgrößen wird mit der folgenden CSS-Klassenauswahl gesteuert:

```
.s7ecatalogsearchviewer .s7embeddialog .s7comboboxdropdown
```

Größe und Position des Bedienfelds werden durch die Komponente gesteuert. Es ist nicht möglich, sie mithilfe von CSS zu ändern.

**CSS-Eigenschaften der Dropdownliste &quot;Kombinationsfeld&quot;**

<table id="table_FA7345321C6A4E63B4B78ECF81CE18DB"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> rand </span> </p> </td> 
   <td colname="col2"> <p>Bereichsrand. </p> </td> 
  </tr> 
 </tbody> 
</table>

Beispiel: Das Kombinationsfeld muss einen grauen Rahmen von einem Pixel haben:

```
.s7ecatalogsearchviewer .s7embeddialog .s7comboboxdropdown { 
    border: 1px solid #CCCCCC; 
}
```

Ein einzelnes Element in einem Dropdown-Bedienfeld, das mit der folgenden CSS-Klassenauswahl gesteuert wird:

```
.s7ecatalogsearchviewer .s7embeddialog .s7dropdownitemanchor
```

**CSS-Eigenschaften des Dropdownelement-Ankerpunkts**

<table id="table_FD42FDD56F89463A97FD292FAA04DA5A"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color  </span> </p> </td> 
   <td colname="col2"> <p>Elementhintergrund. </p> </td> 
  </tr> 
 </tbody> 
</table>

Beispiel: So legen Sie fest, dass das Kombinationsfeld einen weißen Hintergrund hat:

```
.s7ecatalogsearchviewer .s7embeddialog .s7dropdownitemanchor { 
    background-color: #FFFFFF; 
}
```

Ein Häkchen links neben dem ausgewählten Element im Kombinationsfeld, das mit der folgenden CSS-Klassenauswahl gesteuert wird:

```
.s7ecatalogsearchviewer .s7embeddialog .s7checkmark
```

**CSS-Eigenschaften des Kontrollkästchens**

<table id="table_8E01F5461CD04AC18B2C3725A961476A"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width  </span> </p> </td> 
   <td colname="col2"> <p>Symbolbreite </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height  </span> </p> </td> 
   <td colname="col2"> <p>Symbolhöhe. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image  </span> </p> </td> 
   <td colname="col2"> <p>Objektbild. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position  </span> </p> </td> 
   <td colname="col2"> <p> Position innerhalb des Bildausschnitt, wenn CSS-Sprites verwendet werden. </p> <p>Siehe auch <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-customizingviewer/c-html5-ecatsearch-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> CSS-Sprites </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

Beispiel: So legen Sie das Häkchensymbol auf 25 x 25 Pixel fest:

```
.s7ecatalogsearchviewer .s7embeddialog .s7checkmark { 
    background-image: url("images/sdk/cboxchecked.png"); 
    height: 25px; 
    width: 25px; 
}
```

Wenn im Kombinationsfeld &quot;Einbettungsgröße&quot;die Option &quot;Benutzerdefinierte Größe&quot;aktiviert ist, werden im Dialogfeld rechts zwei zusätzliche Eingabefelder angezeigt, damit der Benutzer eine benutzerdefinierte Einbettungsgröße eingeben kann. Diese Felder sind in einen Container eingeschlossen, der mit der folgenden CSS-Klassenauswahl gesteuert wird:

```
.s7ecatalogsearchviewer .s7embeddialog .s7dialogcustomsizepanel
```

**CSS-Eigenschaften des benutzerdefinierten Bedienfelds für die Größe des Dialogfelds**

<table id="table_B00829EA550F4E5E8F51B1C6ADACCD34"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> links </span> </p> </td> 
   <td colname="col2"> <p> Abstand zum Kombinationsfeld für die Einbettungsgröße. </p> </td> 
  </tr> 
 </tbody> 
</table>

Beispiel: Legen Sie für das Bedienfeld für Eingabefelder mit benutzerdefinierter Größe einen Wert von 20 Pixel rechts neben dem Kombinationsfeld fest:

```
.s7ecatalogsearchviewer .s7embeddialog .s7dialogcustomsizepanel { 
    left: 20px; 
}
```

Jedes Eingabefeld mit benutzerdefinierter Größe wird in einen Container eingeschlossen, der einen Rand darstellt und den Rand zwischen den Feldern festlegt. Sie wird mit der folgenden CSS-Klassenauswahl gesteuert:

```
.s7ecatalogsearchviewer .s7embeddialog .s7dialogcustomsize
```

**CSS-Eigenschaften des Dialogfelds benutzerdefinierte Größe**

<table id="table_A8A04BE1988641618D0A412B8AEEE1C5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> rand </span> </p> </td> 
   <td colname="col2"> <p>Ränder um das Eingabefeld. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width  </span> </p> </td> 
   <td colname="col2"> <p> Breite des Eingabefelds. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margin  </span> </p> </td> 
   <td colname="col2"> <p> Rand des Eingabefelds. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Padding </span> </p> </td> 
   <td colname="col2"> <p> Auffüllung des Eingabefelds. </p> </td> 
  </tr> 
 </tbody> 
</table>

Beispiel: So legen Sie fest, dass Eingabefelder mit benutzerdefinierter Größe einen grauen Rahmen von einem Pixel, einen Rand und eine Auffüllung haben und eine Breite von 70 Pixel haben:

```
.s7ecatalogsearchviewer .s7embeddialog .s7dialogcustomsize { 
    border: 1px solid #CCCCCC; 
    margin-right: 20px; 
    padding-left: 2px; 
    padding-right: 2px; 
    width: 70px; 
}
```

Wenn ein vertikaler Bildlauf erforderlich ist, wird die Bildlaufleiste im Bedienfeld neben der rechten Kante des Dialogfelds gerendert, das mit der folgenden CSS-Klassenauswahl gesteuert wird:

```
.s7ecatalogsearchviewer .s7embeddialog .s7dialogscrollpanel
```

**CSS-Eigenschaften des Bedienfelds für den Bildlauf im Dialogfeld**

<table id="table_BA37E577E0884C919383F84080E2DD28"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width  </span> </p> </td> 
   <td colname="col2"> <p>Breite des Bildlaufbedienfelds. </p> </td> 
  </tr> 
 </tbody> 
</table>

Beispiel: So richten Sie einen Bildlaufbereich auf eine Breite von 44 Pixel ein

```
.s7ecatalogsearchviewer .s7embeddialog .s7dialogscrollpanel { 
    width: 44px; 
}
```

Das Erscheinungsbild des Bildlaufleistenbereichs wird mithilfe der folgenden CSS-Klassenauswahl gesteuert:

```
.s7ecatalogsearchviewer .s7embeddialog .s7scrollbar
```

**CSS-Eigenschaften der Bildlaufleiste**

<table id="table_066492417FCA43929017993D7326CDB8"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width  </span> </p> </td> 
   <td colname="col2"> <p>Bildlaufleistenbreite </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Anfang </span> </p> </td> 
   <td colname="col2"> <p> Der Versatz der vertikalen Bildlaufleiste am oberen Rand des Bildlaufbedienfelds. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> unten </span> </p> </td> 
   <td colname="col2"> <p> Der Versatz der vertikalen Bildlaufleiste am unteren Rand des Bildlaufbedienfelds. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> rechts </span> </p> </td> 
   <td colname="col2"> <p> Der horizontale Versatz der Bildlaufleiste vom rechten Rand des Bildlaufbedienfelds. </p> </td> 
  </tr> 
 </tbody> 
</table>

Beispiel: Um eine Bildlaufleiste einzurichten, die 28 Pixel breit ist und einen 8 Pixel breiten Rand von oben, rechts und unten im Bildlaufbedienfeld hat:

```
.s7ecatalogsearchviewer .s7embeddialog .s7scrollbar { 
    bottom: 8px; 
    right: 8px; 
    top: 8px; 
    width: 28px; 
}
```

Die Bildlaufleistenspur ist der Bereich zwischen den Schaltflächen für den oberen und unteren Bildlauf. Die Komponente legt automatisch die Position und Höhe der Leiste fest. Die Verfolgung wird mit dem folgenden CSS-Klassenselektor gesteuert

```
.s7ecatalogsearchviewer .s7embeddialog .s7scrollbar .s7scrolltrack
```

**CSS-Eigenschaften der Bildlaufleistenspur**

<table id="table_19CF5503C1D34ED9998D4F4A6DA7D5D5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width  </span> </p> </td> 
   <td colname="col2"> <p>Spurbreite. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color  </span> </p> </td> 
   <td colname="col2"> <p> Hintergrundfarbe verfolgen. </p> </td> 
  </tr> 
 </tbody> 
</table>

Beispiel: So richten Sie eine Bildlaufleistenspur ein, die 28 Pixel breit und einen grauen Hintergrund hat:

```
.s7ecatalogsearchviewer .s7embeddialog .s7scrollbar .s7scrolltrack { 
width:28px; 
background-color: #B2B2B2; 
}
```

Der Bildlaufleistenminiaturbereich bewegt sich vertikal innerhalb eines Bildlaufspurbereichs. Seine vertikale Position wird vollständig durch die Komponentenlogik gesteuert. Die Höhe des Thumbs ändert sich jedoch nicht dynamisch je nach Inhaltsmenge. Die Thumb-Höhe und andere Aspekte können mit der folgenden CSS-Klassenauswahl konfiguriert werden:

```
.s7ecatalogsearchviewer .s7embeddialog .s7scrollbar .s7scrollthumb
```

**CSS-Eigenschaften der Bildlaufleiste**

<table id="table_90BC468FE138441C9DBAB1EB109F3DB0"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width  </span> </p> </td> 
   <td colname="col2"> <p>Thumb-Breite. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height  </span> </p> </td> 
   <td colname="col2"> <p>Daumenhöhe. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> padding-top  </span> </p> </td> 
   <td colname="col2"> <p>Die vertikale Umrandung zwischen der Oberkante der Leiste. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> padding-bottom  </span> </p> </td> 
   <td colname="col2"> <p> Die vertikale Umrandung zwischen dem unteren Ende der Leiste. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image  </span> </p> </td> 
   <td colname="col2"> <p> Das für einen bestimmten Daumenstatus angezeigte Bild. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position  </span> </p> </td> 
   <td colname="col2"> <p> Position innerhalb des Bildausschnitt, wenn CSS-Sprites verwendet werden. </p> <p>Siehe auch <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-customizingviewer/c-html5-ecatsearch-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> CSS-Sprites </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Thumb unterstützt die Attributauswahl `state`, die verwendet werden kann, um verschiedene Skins auf verschiedene Daumenzustände anzuwenden: `up`, `down`, `over` und `disabled`.

Beispiel: Zum Einrichten eines Bildlaufleistenminiaturbilds mit 28 x 45 Pixel, einem zehn Pixel breiten Rand am oberen und unteren Rand und unterschiedlicher Grafik für jeden Status:

```
.s7ecatalogsearchviewer .s7embeddialog .s7scrollbar .s7scrollthumb { 
    height: 45px; 
    padding-bottom: 10px; 
    padding-top: 10px; 
    width: 28px; 
} 
.s7ecatalogsearchviewer .s7embeddialog .s7scrollbar .s7scrollthumb[state="up"] { 
 background-image:url("images/sdk/scrollbar_thumb_up.png"); 
} 
.s7ecatalogsearchviewer .s7embeddialog .s7scrollbar .s7scrollthumb[state="down"] { 
 background-image:url("images/sdk/scrollbar_thumb_down.png"); 
} 
.s7ecatalogsearchviewer .s7embeddialog .s7scrollbar .s7scrollthumb[state="over"] { 
 background-image:url("images/sdk/scrollbar_thumb_over.png"); 
} 
.s7ecatalogsearchviewer .s7embeddialog .s7scrollbar .s7scrollthumb[state="disabled"] { 
 background-image:url("images/sdk/scrollbar_thumb_disabled.png"); 
}
```

Das Erscheinungsbild der Schaltflächen für den oberen und unteren Bildlauf wird mithilfe der folgenden CSS-Klassenselektoren gesteuert:

```
.s7ecatalogsearchviewer .s7embeddialog .s7scrollbar .s7scrollupbutton
```

```
.s7ecatalogsearchviewer .s7embeddialog .s7scrollbar .s7scrolldownbutton
```

Es ist nicht möglich, Bildlaufschaltflächen mit den Eigenschaften CSS `top`, `left`, `bottom` und `right` zu positionieren. Stattdessen werden sie von der Viewer-Logik automatisch positioniert.

**CSS-Eigenschaften der Schaltflächen für den oberen und unteren Bildlauf**

<table id="table_554BFCFEAF4F43A9AE5F741DC126F833"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width  </span> </p> </td> 
   <td colname="col2"> <p>Schaltflächenbreite. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height  </span> </p> </td> 
   <td colname="col2"> <p>Schaltflächenhöhe. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image  </span> </p> </td> 
   <td colname="col2"> <p> Das für einen Schaltflächenstatus angezeigte Bild. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position  </span> </p> </td> 
   <td colname="col2"> <p> Position innerhalb des Bildausschnitt, wenn CSS-Sprites verwendet werden. </p> <p>Siehe auch <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-customizingviewer/c-html5-ecatsearch-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> CSS-Sprites </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Diese Schaltflächen unterstützen die Attributauswahl `state`, mit der verschiedene Skins auf verschiedene Schaltflächenzustände angewendet werden können: `up`, `down`, `over` und `disabled`.

Die QuickInfos für Schaltflächen können lokalisiert werden. Weitere Informationen finden Sie unter [Lokale Anpassung der Elemente der Benutzeroberfläche](../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74).

Beispiel: So richten Sie Bildlaufschaltflächen ein, die 28 x 32 Pixel groß sind und für jeden Status ein anderes Bildmaterial haben:

```
.s7ecatalogsearchviewer .s7embeddialog .s7scrollbar .s7scrollupbutton { 
 width:28px; 
 height:32px; 
} 
.s7ecatalogsearchviewer .s7embeddialog .s7scrollbar .s7scrollupbutton[state='up'] { 
background-image:url(images/sdk/scroll_up_up.png); 
} 
.s7ecatalogsearchviewer .s7embeddialog .s7scrollbar .s7scrollupbutton[state='over'] { 
 background-image:url(images/sdk/scroll_up_over.png); 
} 
.s7ecatalogsearchviewer .s7embeddialog .s7scrollbar .s7scrollupbutton[state='down'] { 
 background-image:url(images/sdk/scroll_up_down.png); 
} 
.s7ecatalogsearchviewer .s7embeddialog .s7scrollbar .s7scrollupbutton[state='disabled'] { 
 background-image:url(images/sdk/scroll_up_disabled.png); 
} 
.s7ecatalogsearchviewer .s7embeddialog .s7scrollbar .s7scrolldownbutton { 
 width:28px; 
 height:32px; 
} 
.s7ecatalogsearchviewer .s7embeddialog .s7scrollbar .s7scrolldownbutton[state='up'] { 
 background-image:url(images/sdk/scroll_down_up.png); 
} 
.s7ecatalogsearchviewer .s7embeddialog .s7scrollbar .s7scrolldownbutton[state='over'] { 
 background-image:url(images/sdk/scroll_down_over.png); 
} 
.s7ecatalogsearchviewer .s7embeddialog .s7scrollbar .s7scrolldownbutton[state='down'] { 
 background-image:url(images/sdk/scroll_down_down.png); 
} 
.s7ecatalogsearchviewer .s7embeddialog .s7scrollbar .s7scrolldownbutton[state='disabled'] { 
 background-image:url(images/sdk/scroll_down_disabled.png); 
}
```

