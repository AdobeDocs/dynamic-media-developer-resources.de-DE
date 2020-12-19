---
description: Das Tool zum Weitergeben per E-Mail besteht aus einer Schaltfläche, die dem Social Sharing-Bedienfeld hinzugefügt wird, sowie dem modalen Dialogfeld, das angezeigt wird, wenn das Tool aktiviert wird. Die Position der Schaltfläche wird vollständig vom Social Sharing-Tool verwaltet.
seo-description: Das Tool zum Weitergeben per E-Mail besteht aus einer Schaltfläche, die dem Social Sharing-Bedienfeld hinzugefügt wird, sowie dem modalen Dialogfeld, das angezeigt wird, wenn das Tool aktiviert wird. Die Position der Schaltfläche wird vollständig vom Social Sharing-Tool verwaltet.
seo-title: Email-Freigabe
solution: Experience Manager
title: Email-Freigabe
topic: Dynamic media
uuid: fc60dd7b-651e-458c-9057-693ca1c0afdc
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef
workflow-type: tm+mt
source-wordcount: '3073'
ht-degree: 1%

---


# Email Share{#email-share}

Das Tool zum Weitergeben per E-Mail besteht aus einer Schaltfläche, die dem Social Sharing-Bedienfeld hinzugefügt wird, sowie dem modalen Dialogfeld, das angezeigt wird, wenn das Tool aktiviert wird. Die Position der Schaltfläche wird vollständig vom Social Sharing-Tool verwaltet.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

Das Erscheinungsbild der E-Mail-Freigabe-Schaltfläche wird mit der folgenden CSS-Klassenauswahl gesteuert:

```
.s7ecatalogsearchviewer .s7emailshare
```

**CSS-Eigenschaften des E-Mail-Freigabe-Tools**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Breite der Schaltfläche. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Höhe der Schaltfläche. </p> </td> 
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

Beispiel: Zum Einrichten einer E-Mail-Freigabe-Schaltfläche mit 28 x 28 Pixeln, die für jeden der vier Schaltflächenzustände ein anderes Bild anzeigt.

```
.s7ecatalogsearchviewer .s7emailshare { 
 width:28px; 
 height:28px; 
} 
.s7ecatalogsearchviewer .s7emailshare[state='up'] { 
background-image:url(images/v2/EmailShare_dark_up.png); 
} 
.s7ecatalogsearchviewer .s7emailshare[state='over'] { 
background-image:url(images/v2/EmailShare_dark_over.png); 
} 
.s7ecatalogsearchviewer .s7emailshare[state='down'] { 
background-image:url(images/v2/EmailShare_dark_down.png); 
} 
.s7ecatalogsearchviewer .s7emailshare[state='disabled'] { 
background-image:url(images/v2/EmailShare_dark_disabled.png); 
}
```

Die Hintergrundüberlagerung, die eine Webseite umfasst, wenn das Dialogfeld aktiv ist, wird mit der folgenden CSS-Klassenauswahl gesteuert:

```
.s7ecatalogsearchviewer .s7emaildialog .s7backoverlay
```

**CSS-Eigenschaften der Zurück-Überlagerung**

<table id="table_1A0C28D8C81D413C83D73DEAC53057C5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Deckkraft  </span> </p> </td> 
   <td colname="col2"> <p> Deckkraft der Hintergrundüberlagerung. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color  </span> </p> </td> 
   <td colname="col2"> <p>Hintergrundüberlagerungsfarbe. </p> </td> 
  </tr> 
 </tbody> 
</table>

Beispiel: So richten Sie eine Hintergrundüberlagerung ein, die grau mit einer Deckkraft von 70 % sein soll:

```
.s7ecatalogsearchviewer .s7emaildialog .s7backoverlay { 
 opacity:0.7; 
 background-color:#222222; 
}
```

Standardmäßig wird das modale Dialogfeld auf Desktop-Systemen zentriert angezeigt und nimmt den gesamten Webseitenbereich auf Touch-Geräten. In allen Fällen wird die Positionierung und Größe des Dialogfelds von der Komponente verwaltet. Das Dialogfeld wird mit der folgenden CSS-Klassenauswahl gesteuert:

```
.s7ecatalogsearchviewer .s7emaildialog .s7dialog
```

**CSS-Eigenschaften des Dialogfelds**

<table id="table_5272BC8EF9124018B4290356B95B5559"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> border-radius  </span> </p> </td> 
   <td colname="col2"> <p> Rahmenradius des Dialogfelds (falls das Dialogfeld nicht das gesamte Browserfenster aufnimmt); </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color  </span> </p> </td> 
   <td colname="col2"> <p> Hintergrundfarbe des Dialogfelds; </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width  </span> </p> </td> 
   <td colname="col2"> <p> Sollte entweder nicht eingestellt oder auf 100 % eingestellt sein. In diesem Fall nimmt das Dialogfeld das gesamte Browserfenster in Anspruch (dieser Modus wird auf Touch-Geräten bevorzugt). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height  </span> </p> </td> 
   <td colname="col2"> <p> Sollte entweder nicht eingestellt oder auf 100% eingestellt sein. In diesem Fall nimmt das Dialogfeld das gesamte Browserfenster auf (dieser Modus wird auf Touch-Geräten bevorzugt). </p> </td> 
  </tr> 
 </tbody> 
</table>

Beispiel: So richten Sie ein Dialogfeld ein, das das gesamte Browserfenster nutzt und einen weißen Hintergrund auf Touch-Geräten aufweist:

```
.s7ecatalogsearchviewer .s7touchinput .s7emaildialog .s7dialog { 
 width:100%; 
 height:100%; 
background-color: #ffffff; 
}
```

Die Kopfzeile des Dialogfelds besteht aus einem Symbol, einem Titeltext und einer Schließen-Schaltfläche. Der Header-Container wird mit dem folgenden CSS-Klassenselektor gesteuert

```
.s7ecatalogsearchviewer .s7emaildialog .s7dialogheader
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
.s7ecatalogsearchviewer .s7emaildialog .s7dialogheader .s7dialogline
```

**CSS-Eigenschaften der Dialogelinie**

<table id="table_5B03CF843F0D4B1295A3FC1EB50C56F1"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Padding </span> </p> </td> 
   <td colname="col2"> <p> Innenabstand für das Kopfzeilensymbol und den Titel. </p> </td> 
  </tr> 
 </tbody> 
</table>

Das Kopfzeilensymbol wird mit dem folgenden CSS-Klassenselektor gesteuert:

```
.s7ecatalogsearchviewer .s7emaildialog .s7dialogheadericon
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
.s7ecatalogsearchviewer .s7emaildialog .s7dialogheadertext
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
.s7ecatalogsearchviewer .s7emaildialog .s7closebutton
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

Die QuickInfo der Schaltfläche Schließen und der Titel des Dialogfelds können lokalisiert werden. Weitere Informationen finden Sie unter [Lokale Anpassung der Elemente der Benutzeroberfläche](../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74).

Beispiel: Zum Einrichten eines Dialogfeldheaders mit Auffüllung, einem Symbol mit 24 x 17 Pixeln, einem fett gedruckten Titel mit 16 Punkten und einer Schaltfläche mit 28 x 28 Pixel &quot;Schließen&quot;zwei Pixel von oben und zwei Pixel von rechts vom Container des Dialogfelds:

```
.s7ecatalogsearchviewer .s7emaildialog .s7dialogheader { 
 padding: 10px; 
} 
.s7ecatalogsearchviewer .s7emaildialog .s7dialogheader .s7dialogline { 
 padding: 10px 10px 2px; 
} 
.s7ecatalogsearchviewer .s7emaildialog .s7dialogheadericon { 
    background-image: url("images/sdk/dlgemail_cap.png"); 
    height: 17px; 
    width: 24px; 
} 
.s7ecatalogsearchviewer .s7emaildialog .s7dialogheadertext { 
    font-size: 16pt; 
    font-weight: bold; 
    padding-left: 16px; 
} 
.s7ecatalogsearchviewer .s7emaildialog .s7closebutton { 
 top:2px; 
 right:2px; 
 padding:8px; 
 width:28px; 
 height:28px; 
} 
.s7ecatalogsearchviewer .s7emaildialog .s7closebutton[state='up'] { 
 background-image:url(images/sdk/close_up.png); 
} 
.s7ecatalogsearchviewer .s7emaildialog .s7closebutton[state='over'] { 
 background-image:url(images/sdk/close_over.png); 
} 
.s7ecatalogsearchviewer .s7emaildialog .s7closebutton[state='down'] { 
 background-image:url(images/sdk/close_down.png); 
} 
.s7ecatalogsearchviewer .s7emaildialog .s7closebutton[state='disabled'] { 
 background-image:url(images/sdk/close_disabled.png); 
}
```

Die Dialogfußzeile besteht aus den Schaltflächen &quot;Abbrechen&quot;und &quot;E-Mail senden&quot;. Der Container der Fußzeile wird mit der folgenden CSS-Klassenauswahl gesteuert:

```
.s7ecatalogsearchviewer .s7emaildialog .s7dialogfooter
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

Die Fußzeile hat einen inneren Container, der beide Schaltflächen enthält. Sie wird mit der folgenden CSS-Klassenauswahl gesteuert:

```
.s7ecatalogsearchviewer .s7emaildialog .s7dialogbuttoncontainer
```

**CSS-Eigenschaften des Containers für die Schaltfläche &quot;Dialogfeld&quot;**

<table id="table_C34906888A8145C7A61E503DFC6B08A9"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Padding </span> </p> </td> 
   <td colname="col2"> <p> Innere Umrandung zwischen der Fußzeile und den Schaltflächen. </p> </td> 
  </tr> 
 </tbody> 
</table>

Die Schaltfläche &quot;Abbrechen&quot;wird mit dem folgenden CSS-Klassenselektor gesteuert:

```
.s7ecatalogsearchviewer .s7emaildialog .s7dialogcancelbutton
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
>Diese Schaltfläche unterstützt die Attributauswahl `state`, mit der verschiedene Skins auf verschiedene Schaltflächenzustände angewendet werden können.

Die Schaltfläche &quot;E-Mail senden&quot;wird mit der folgenden CSS-Klassenauswahl gesteuert:

```
.s7ecatalogsearchviewer .s7emaildialog .s7dialogactionbutton
```

**CSS-Eigenschaften der Aktionsschaltfläche des Dialogfelds**

<table id="table_91C75B2470A24DC2AD3973A91FA8B325"> 
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
.s7ecatalogsearchviewer .s7emaildialog .s7dialogfooter .s7button
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

Diese Schaltflächen-QuickInfos können lokalisiert werden. Weitere Informationen finden Sie unter [Lokale Anpassung der Elemente der Benutzeroberfläche](../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74).

Beispiel: So richten Sie eine Fußzeile des Dialogfelds mit der Schaltfläche &quot;Abbrechen&quot;im Format 64 x 34 und einer Schaltfläche &quot;Senden per E-Mail&quot;im Format 82 x 34 ein, wobei die Textfarbe und die Hintergrundfarbe je nach Schaltflächenstatus unterschiedlich sind:

```
.s7ecatalogsearchviewer .s7emaildialog .s7dialogfooter { 
    border-top: 1px solid #909090; 
} 
.s7ecatalogsearchviewer .s7emaildialog .s7dialogbuttoncontainer { 
    padding-bottom: 6px; 
    padding-top: 10px; 
} 
.s7ecatalogsearchviewer .s7emaildialog .s7dialogfooter .s7button { 
    box-shadow: 1px 1px 1px #999999; 
    color: #FFFFFF; 
    font-size: 9pt; 
    font-weight: bold; 
    line-height: 34px; 
    margin-right: 10px; 
} 
.s7ecatalogsearchviewer .s7emaildialog .s7dialogcancelbutton { 
 width:64px; 
 height:34px; 
} 
.s7ecatalogsearchviewer .s7emaildialog .s7dialogcancelbutton[state='up'] { 
 background-color:#666666; 
 color:#dddddd; 
} 
.s7ecatalogsearchviewer .s7emaildialog .s7dialogcancelbutton[state='down'] { 
 background-color:#555555; 
 color:#ffffff; 
} 
.s7ecatalogsearchviewer .s7emaildialog .s7dialogcancelbutton[state='over'] { 
 background-color:#555555; 
 color:#ffffff; 
} 
.s7ecatalogsearchviewer .s7emaildialog .s7dialogcancelbutton[state='disabled'] { 
 background-color:#b2b2b2; 
 color:#dddddd; 
} 
.s7ecatalogsearchviewer .s7emaildialog .s7dialogactionbutton { 
 width:82px; 
 height:34px; 
} 
.s7ecatalogsearchviewer .s7emaildialog .s7dialogactionbutton[state='up'] { 
 background-color:#333333; 
 color:#dddddd; 
} 
.s7ecatalogsearchviewer .s7emaildialog .s7dialogactionbutton[state='down'] { 
 background-color:#222222; 
 color:#cccccc; 
} 
.s7ecatalogsearchviewer .s7emaildialog .s7dialogactionbutton[state='over'] { 
 background-color:#222222; 
 color:#cccccc; 
} 
.s7ecatalogsearchviewer .s7emaildialog .s7dialogactionbutton[state='disabled'] { 
 background-color:#b2b2b2; 
 color:#dddddd; 
}
```

Der Hauptdialogbereich (zwischen der Kopf- und Fußzeile) enthält durchlaufbare Dialogfeldinhalte und den Bildlaufbereich auf der rechten Seite. In allen Fällen verwaltet die Komponente die Breite dieses Bereichs, es ist nicht möglich, es in CSS festzulegen. Der Hauptdialogbereich wird mit der folgenden CSS-Klassenauswahl gesteuert:

```
.s7ecatalogsearchviewer .s7emaildialog .s7dialogviewarea
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

>[!NOTE]
>
>Der Hauptdialogfeldbereich unterstützt die optionale Attributauswahl `state`. Es ist auf `sendsuccess` eingestellt, wenn das E-Mail-Formular gesendet wird und das Dialogfeld eine Bestätigungsmeldung anzeigt. Solange die Bestätigungsmeldung klein ist, kann mit dieser Attributauswahl die Höhe des Dialogfelds verringert werden, wenn eine solche Bestätigungsmeldung angezeigt wird.

Beispiel: Um den Bereich des Hauptdialogfelds auf eine anfängliche Höhe von 300 Pixel und eine Höhe von 100 Pixel festzulegen, haben Sie einen Ränder von 10 Pixel und einen weißen Hintergrund:

```
.s7ecatalogsearchviewer .s7emaildialog .s7dialogviewarea { 
 background-color:#ffffff; 
 margin:10px; 
 height:300px; 
} 
.s7ecatalogsearchviewer .s7emaildialog .s7dialogviewarea[state='sendsuccess'] { 
 height:100px; 
}
```

Der gesamte Formularinhalt (wie Beschriftungen und Eingabefelder) befindet sich in einem Container, der mit der folgenden CSS-Klassenauswahl gesteuert wird:

```
.s7ecatalogsearchviewer .s7emaildialog .s7dialogbody
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
.s7ecatalogsearchviewer .s7emaildialog .s7dialogbody { 
    padding: 10px; 
}
```

Das Dialogfeldformular wird zeilenweise ausgefüllt, wobei jede Zeile einen Teil des Formularinhalts enthält (z. B. eine Beschriftung und ein Texteingabefeld). Eine einzelne Formularzeile wird mit der folgenden CSS-Klassenauswahl gesteuert:

```
.s7ecatalogsearchviewer .s7emaildialog .s7dialogbody .s7dialogline
```

**CSS-Eigenschaften der Dialogfeldzeile**

<table id="table_2CCCC71B45B444A8B9CE2894129C9C02"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Padding </span> </p> </td> 
   <td colname="col2"> <p>Innenzeilenfüllung. </p> </td> 
  </tr> 
 </tbody> 
</table>

Beispiel: So richten Sie ein Dialogfeld ein, in dem jede Zeile mit zehn Pixeln aufgefüllt werden kann:

```
.s7ecatalogsearchviewer .s7emaildialog .s7dialogbody .s7dialogline { 
    padding: 10px; 
}
```

Alle statischen Beschriftungen im Dialogfeld werden mit der folgenden CSS-Klassenauswahl gesteuert:

```
.s7ecatalogsearchviewer .s7emaildialog .s7dialoglabel
```

Diese Klasse eignet sich nicht zum Steuern der Größe oder Position von Beschriftungen, da Sie sie auf Texte an verschiedenen Stellen der Benutzeroberfläche des Formulars anwenden können.

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

Beispiel: So richten Sie alle Beschriftungen auf grau, fett und mit einer Schrift von neun Pixeln ein:

```
.s7ecatalogsearchviewer .s7emaildialog .s7dialoglabel { 
    color: #666666; 
    font-size: 9pt; 
    font-weight: bold; 
}
```

Alle statischen Beschriftungen, die links neben den Formulareingabefeldern angezeigt werden, werden wie folgt gesteuert:

```
.s7ecatalogsearchviewer .s7emaildialog .s7dialoginputlabel
```

**CSS-Eigenschaften der Beschriftung für die Eingabe im Dialogfeld**

<table id="table_B5CF02837BAA42C7B79B6D9DA20792DF"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width  </span> </p> </td> 
   <td colname="col2"> <p>Die Breite der statischen Beschriftung. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> text-align  </span> </p> </td> 
   <td colname="col2"> <p>Die horizontale Textausrichtung. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margin  </span> </p> </td> 
   <td colname="col2"> <p>Statischer Rand für Beschriftungen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Padding </span> </p> </td> 
   <td colname="col2"> <p>Statische Auffüllung der Beschriftung. </p> </td> 
  </tr> 
 </tbody> 
</table>

Beispiel: Um die Beschriftungen für Eingabefelder auf eine Breite von 50 Pixeln, rechtsbündig, mit einer Auffüllung von zehn Pixeln und einem Rand von zehn Pixeln rechts festzulegen, müssen Sie Folgendes festlegen:

```
.s7ecatalogsearchviewer .s7emaildialog .s7dialoginputlabel { 
    margin-right: 10px; 
    padding: 10px; 
    text-align: right; 
    width: 50px; 
}
```

Jedes Formulareingabefeld wird in den Container eingeschlossen, mit dem Sie einen benutzerdefinierten Rahmen um das Eingabefeld anwenden können. Sie wird mit der folgenden CSS-Klassenauswahl gesteuert:

```
.s7ecatalogsearchviewer .s7emaildialog .s7dialoginputcontainer
```

**CSS-Eigenschaften des Containers für die Eingabe im Dialogfeld**

<table id="table_7BC1C5919A54483F8121D928DC63233A"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> rand </span> </p> </td> 
   <td colname="col2"> <p>Ränder um den Container des Eingabefelds. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Padding </span> </p> </td> 
   <td colname="col2"> <p>Innenabstand. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Der Container für Eingabefelder unterstützt die optionale Attributauswahl `state`. Sie ist auf `verifyerror` eingestellt, wenn der Benutzer einen Fehler im Eingabedatenformat macht und die Inline-Überprüfung fehlschlägt. Mit dieser Attributauswahl können Sie falsche Benutzereingaben im Formular hervorheben.

Die meisten Eingabefelder, die sich von der Beschriftung links bis rechts im Dialogfeld (einschließlich Feld &quot;Von&quot;und Feld &quot;Meldung&quot;) ausbreiten, werden mit der folgenden CSS-Klassenauswahl gesteuert:

```
.s7ecatalogsearchviewer .s7emaildialog .s7dialoginputwide
```

**CSS-Eigenschaften des Dialogfelds geben breites Feld ein**

<table id="table_7275B4365DFA4C0386FA2BDB7204A517"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width  </span> </p> </td> 
   <td colname="col2"> <p>Breite des Eingabefelds. </p> </td> 
  </tr> 
 </tbody> 
</table>

Das Feld &quot;An&quot;ist schmaler, da es rechts Platz für die Schaltfläche &quot;E-Mail entfernen&quot;einräumt. Sie wird mit der folgenden CSS-Klassenauswahl gesteuert:

```
.s7ecatalogsearchviewer .s7emaildialog .s7dialoginputshort
```

**CSS-Eigenschaften des Dialogfelds Eingabe-Kurzfelds**

<table id="table_DFA9059209FF4184BD483A529424E97F"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width  </span> </p> </td> 
   <td colname="col2"> <p>Breite des Eingabefelds. </p> </td> 
  </tr> 
 </tbody> 
</table>

Beispiel: So richten Sie ein Formular so ein, dass es einen grauen Rand von einem Pixel mit einer Auffüllung von neun Pixeln um alle Eingabefelder hat. für Felder, bei denen die Überprüfung fehlschlägt, denselben roten Rand haben, bis das Feld 250 Pixel breit ist und die übrigen Eingabefelder 300 Pixel breit:

```
.s7ecatalogsearchviewer .s7emaildialog .s7dialoginputcontainer { 
    border: 1px solid #CCCCCC; 
    padding: 9px; 
} 
.s7ecatalogsearchviewer .s7emaildialog .s7dialoginputcontainer[state="verifyerror"] { 
    border: 1px solid #FF0000; 
} 
.s7ecatalogsearchviewer .s7emaildialog .s7dialoginputshort { 
    width: 250px; 
} 
.s7ecatalogsearchviewer .s7emaildialog .s7dialoginputwide { 
    width: 300px; 
}
```

Das Eingabefeld für E-Mail-Nachrichten wird zusätzlich gesteuert durch:

```
.s7ecatalogsearchviewer .s7emaildialog .s7dialogmessage
```

Mit dieser Klasse können Sie spezifische Eigenschaften für das zugrunde liegende `TEXTAREA`-Element festlegen.

**CSS-Eigenschaften der Dialogfeldmeldung**

<table id="table_9E9D5A0C3CDB45739615C4C07F8DC046"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height  </span> </p> </td> 
   <td colname="col2"> <p>Meldungshöhe. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> word-wrap  </span> </p> </td> 
   <td colname="col2"> <p>Umbruchstil. </p> </td> 
  </tr> 
 </tbody> 
</table>

Beispiel: So richten Sie eine E-Mail-Nachricht auf eine Höhe von 50 Pixel ein und verwenden Sie das Umbrechen von `break-word`-Wörtern:

```
.s7ecatalogsearchviewer .s7emaildialog .s7dialogmessage { 
    height: 50px; 
    word-wrap: break-word; 
}
```

hinzufügen Schaltfläche &quot;Weitere E-Mail-Adresse&quot;ermöglicht es dem Benutzer, im E-Mail-Formular mehr als eine Adresse hinzuzufügen. Sie wird mit der folgenden CSS-Klassenauswahl gesteuert:

```
.s7ecatalogsearchviewer .s7emaildialog .s7dialogaddemailbutton
```

**CSS-Eigenschaften des Dialogfelds Schaltfläche &quot;E-Mail-Adresse hinzufügen&quot;**

<table id="table_8829DC0694684E8BA427DFB821F7433D"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height  </span> </p> </td> 
   <td colname="col2"> <p>Schaltflächenhöhe. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> color  </span> </p> </td> 
   <td colname="col2"> <p>Schaltflächentextfarbe für jeden Status. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image  </span> </p> </td> 
   <td colname="col2"> <p>Schaltflächenbild für jeden Status. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position  </span> </p> </td> 
   <td colname="col2"> <p>Position des Schaltflächenbilds im Schaltflächenbereich. </p> </td> 
  </tr> 
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
   <td colname="col2"> <p>Texthöhe innerhalb der Schaltfläche. Betrifft die vertikale Ausrichtung. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> text-align  </span> </p> </td> 
   <td colname="col2"> <p>Horizontale Textausrichtung. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Padding </span> </p> </td> 
   <td colname="col2"> <p>Innenabstand. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Diese Schaltfläche unterstützt die Attributauswahl `state`, mit der verschiedene Skins auf verschiedene Schaltflächenzustände angewendet werden können.

Die QuickInfo für Schaltflächen kann lokalisiert werden. Weitere Informationen finden Sie unter [Lokale Anpassung der Elemente der Benutzeroberfläche](../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74).

Beispiel: Um die Schaltfläche &quot;Hinzufügen weitere E-Mail-Adresse&quot;auf eine Höhe von 25 Pixel festzulegen, verwenden Sie eine 12-Punkt-Schriftart mit der rechten Ausrichtung und eine andere Textfarbe und ein anderes Bild für jeden Status:

```
.s7ecatalogsearchviewer .s7emaildialog .s7dialogaddemailbutton { 
 text-align:right; 
 font-size:12pt; 
 font-weight:bold; 
 background-position:left center; 
 line-height:25px; 
 padding-left:30px; 
 height:25px; 
} 
.s7ecatalogsearchviewer .s7emaildialog .s7dialogaddemailbutton[state='up'] { 
 color:#666666; 
 background-image:url(images/sdk/dlgaddplus_up.png); 
} 
.s7ecatalogsearchviewer .s7emaildialog .s7dialogaddemailbutton[state='down'] { 
 color:#000000; 
 background-image:url(images/sdk/dlgaddplus_over.png); 
} 
.s7ecatalogsearchviewer .s7emaildialog .s7dialogaddemailbutton[state='over'] { 
 color:#000000; 
 text-decoration:underline; 
 background-image:url(images/sdk/dlgaddplus_over.png); 
} 
.s7ecatalogsearchviewer .s7emaildialog .s7dialogaddemailbutton[state='disabled'] { 
 color:#666666; 
 background-image:url(images/sdk/dlgaddplus_up.png); 
}
```

Mit der Schaltfläche &quot;Entfernen&quot;können Benutzer zusätzliche Adressen aus dem E-Mail-Formular entfernen. Sie wird mit der folgenden CSS-Klassenauswahl gesteuert:

```
.s7ecatalogsearchviewer .s7emaildialog .s7dialogremoveemailbutton
```

**CSS-Eigenschaften des Dialogfelds entfernen E-Mail-Schaltfläche**

<table id="table_79E4C65741E64859B9C9E9DCCB3D050B"> 
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

Beispiel: Um die Schaltfläche &quot;Entfernen&quot;so einzurichten, dass sie 25 x 25 Pixel groß ist und für jeden Status ein anderes Bild verwendet wird:

```
.s7ecatalogsearchviewer .s7emaildialog .s7dialogremoveemailbutton { 
 width:25px; 
 height:25px; 
} 
.s7ecatalogsearchviewer .s7emaildialog .s7dialogremoveemailbutton[state='up'] { 
 background-image:url(images/sdk/dlgremove_up.png); 
} 
.s7ecatalogsearchviewer .s7emaildialog .s7dialogremoveemailbutton[state='over'] { 
 background-image:url(images/sdk/dlgremove_over.png); 
} 
.s7ecatalogsearchviewer .s7emaildialog .s7dialogremoveemailbutton[state='down'] { 
 background-image:url(images/sdk/dlgremove_over.png); 
} 
.s7ecatalogsearchviewer .s7emaildialog .s7dialogremoveemailbutton[state='disabled'] { 
 background-image:url(images/sdk/dlgremove_up.png); 
}
```

Der freigegebene Inhalt wird unten im Dialogfeld angezeigt und enthält eine Miniaturansicht, einen Titel, eine Herkünfte-URL und eine Beschreibung. Er wird in einen Container eingeschlossen, der mit der folgenden CSS-Klassenauswahl gesteuert wird:

```
.s7ecatalogsearchviewer .s7emaildialog .s7dialogbody .s7dialogcontent
```

**CSS-Eigenschaften des Dialogfeldinhalts **

<table id="table_9C5CBFC2482E4A46BE837573B0B02FE4"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> rand </span> </p> </td> 
   <td colname="col2"> <p>Container. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Padding </span> </p> </td> 
   <td colname="col2"> <p>Innenabstand. </p> </td> 
  </tr> 
 </tbody> 
</table>

Beispiel: So richten Sie einen unteren Container ein, der einen gepunkteten Rahmen von einem Pixel und keine Auffüllung hat:

```
.s7ecatalogsearchviewer .s7emaildialog .s7dialogbody .s7dialogcontent { 
    border: 1px dotted #A0A0A0; 
    padding: 0; 
}
```

Miniaturbild wird mit der folgenden CSS-Klassenauswahl gesteuert:

```
.s7ecatalogsearchviewer .s7emaildialog .s7dialogthumbnail
```

Die `background-image`-Eigenschaft wird durch die Komponentenlogik festgelegt.

**CSS-Eigenschaften des Miniaturbilds des Dialogfelds**

<table id="table_4C614FF2CEB149DAB5B7D7BC38CD3CAE"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width  </span> </p> </td> 
   <td colname="col2"> <p>Breite der Miniaturansicht. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height  </span> </p> </td> 
   <td colname="col2"> <p>Höhe der Miniaturansichten. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> vertical-align  </span> </p> </td> 
   <td colname="col2"> <p>Miniaturansicht für vertikale Ausrichtung. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Padding </span> </p> </td> 
   <td colname="col2"> <p>Innenabstand. </p> </td> 
  </tr> 
 </tbody> 
</table>

Beispiel: Um die Miniaturansicht auf 90 x 60 Pixel und die obere Ausrichtung mit 10 Pixel Abstand festzulegen,

```
.s7ecatalogsearchviewer .s7emaildialog .s7dialogthumbnail { 
    height: 60px; 
    padding: 10px; 
    vertical-align: top; 
    width: 90px; 
}
```

Titel, Herkunft und Beschreibung des Inhalts werden weiter in einem Bereich rechts neben der Inhaltsminiaturansicht gruppiert. Sie wird mit der folgenden CSS-Klassenauswahl gesteuert:

```
.s7ecatalogsearchviewer .s7emaildialog .s7dialoginfopanel
```

**CSS-Eigenschaften des Infofelds-Dialogfelds**

<table id="table_EDFA6229D8C3468E989E7EC05F23EF3B"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width  </span> </p> </td> 
   <td colname="col2"> <p>Bedienfeldbreite. </p> </td> 
  </tr> 
 </tbody> 
</table>

Beispiel: So richten Sie ein Inhaltsinformationsbedienfeld auf eine Breite von 300 Pixel ein:

```
.s7ecatalogsearchviewer .s7emaildialog .s7dialoginfopanel { 
    width: 300px; 
}
```

Der Inhaltstitel wird mit der folgenden CSS-Klassenauswahl gesteuert:

```
.s7ecatalogsearchviewer .s7emaildialog .s7dialogtitle
```

**CSS-Eigenschaften des Dialogfeldtitels**

<table id="table_E83C149E66EC474092DF8A180DA9A550"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margin  </span> </p> </td> 
   <td colname="col2"> <p>Äußerer Rand. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-Gewichtung  </span> </p> </td> 
   <td colname="col2"> <p>Schriftart-Gewichtung. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size  </span> </p> </td> 
   <td colname="col2"> <p>Schriftgröße. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family  </span> </p> </td> 
   <td colname="col2"> <p>Schriftfamilie. </p> </td> 
  </tr> 
 </tbody> 
</table>

Beispiel: So richten Sie einen Inhaltstitel ein, um eine fett gedruckte Schrift mit einem Ränder von zehn Pixeln zu verwenden:

```
.s7ecatalogsearchviewer .s7emaildialog .s7dialogtitle { 
    font-weight: bold; 
    margin: 10px; 
}
```

Content Herkunft wird mit der folgenden CSS-Klassenauswahl gesteuert:

```
.s7ecatalogsearchviewer .s7emaildialog .s7dialogorigin
```

**CSS-Eigenschaften der Herkunft des Inhalts des Dialogfelds **

<table id="table_51763B532A9C4AE8AE54B69933A8C0B5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margin  </span> </p> </td> 
   <td colname="col2"> <p>Äußerer Rand. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-Gewichtung  </span> </p> </td> 
   <td colname="col2"> <p>Schriftart-Gewichtung. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size  </span> </p> </td> 
   <td colname="col2"> <p>Schriftgröße. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family  </span> </p> </td> 
   <td colname="col2"> <p>Schriftfamilie. </p> </td> 
  </tr> 
 </tbody> 
</table>

Beispiel: So richten Sie die Content-Herkunft auf einen 10-Pixel-Rand ein:

```
.s7ecatalogsearchviewer .s7emaildialog .s7dialogorigin { 
    margin: 10px; 
}
```

Die Inhaltsbeschreibung wird mit der folgenden CSS-Klassenauswahl gesteuert:

```
.s7ecatalogsearchviewer .s7emaildialog .s7dialogdescription
```

**CSS-Eigenschaften der Inhaltsbeschreibung des Dialogfelds**

<table id="table_F0F917ED3D1D4FCE974F48214D287E14"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margin  </span> </p> </td> 
   <td colname="col2"> <p>Äußerer Rand. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-Gewichtung  </span> </p> </td> 
   <td colname="col2"> <p>Schriftart-Gewichtung. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size  </span> </p> </td> 
   <td colname="col2"> <p>Schriftgröße. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family  </span> </p> </td> 
   <td colname="col2"> <p>Schriftfamilie. </p> </td> 
  </tr> 
 </tbody> 
</table>

Beispiel: So richten Sie eine Inhaltsbeschreibung mit einem Rand von zehn Pixeln ein und verwenden eine Schrift mit neun Punkten:

```
.s7ecatalogsearchviewer .s7emaildialog .s7dialogdescription { 
    font-size: 9pt; 
    margin: 10px; 
}
```

Wenn ein Benutzer falsche Eingabedaten eingibt und die Inline-Überprüfung fehlschlägt oder wenn beim Senden des Formulars im Dialogfeld ein Fehler oder eine Bestätigungsmeldung ausgegeben werden muss, wird oben im Dialogfeld eine Meldung angezeigt. Sie wird mit der folgenden CSS-Klassenauswahl gesteuert:

```
.s7ecatalogsearchviewer .s7emaildialog .s7dialogerrormessage
```

**CSS-Eigenschaften der Fehlermeldung im Dialogfeld**

<table id="table_C114E1004C334D339C25A3438E8E6614"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image  </span> </p> </td> 
   <td colname="col2"> <p> Fehlersymbol. Standard ist ein Ausrufezeichen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position  </span> </p> </td> 
   <td colname="col2"> <p> Fehlersymbolposition innerhalb des Nachrichtenbereichs. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> color  </span> </p> </td> 
   <td colname="col2"> <p>Textfarbe der Nachricht. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-Gewichtung  </span> </p> </td> 
   <td colname="col2"> <p>Schriftart-Gewichtung. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size  </span> </p> </td> 
   <td colname="col2"> <p>Schriftgröße. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family  </span> </p> </td> 
   <td colname="col2"> <p>Schriftfamilie. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> line-height  </span> </p> </td> 
   <td colname="col2"> <p> Texthöhe in der Nachricht. Betrifft die vertikale Ausrichtung. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Padding </span> </p> </td> 
   <td colname="col2"> <p>Innenabstand. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Diese Meldung unterstützt die Attributauswahl `state` mit den folgenden möglichen Werten: `verifyerror`, `senderror` und `sendsuccess`. `verifyerror` festgelegt wird, wenn eine Nachricht aufgrund eines Inline-Validierungsfehlers angezeigt wird;  `senderror` festgelegt wird, wenn ein Back-End-E-Mail-Dienst einen Fehler meldet;  `sendsuccess` festgelegt, wenn E-Mail erfolgreich gesendet wurde. Auf diese Weise kann die Nachricht je nach Status des Dialogfelds unterschiedlich formatiert werden.

Die QuickInfo für Schaltflächen kann lokalisiert werden. Weitere Informationen finden Sie unter [Lokale Anpassung der Elemente der Benutzeroberfläche](../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74).

Beispiel: Wenn Sie eine Meldung einrichten möchten, die eine fett gedruckte Schrift mit 10 Punkten verwendet, die Zeilenhöhe mit 25 Pixel, die Auffüllung mit 20 Pixel auf der linken Seite, ein Ausrufezeichen-Symbol, roter Text bei einem Fehler und kein Symbol und grüner Text bei einem Erfolg:

```
.s7ecatalogsearchviewer .s7emaildialog .s7dialogerrormessage[state="verifyerror"] { 
    background-image: url("images/sdk/dlgerrimg.png"); 
    color: #FF0000; 
} 
.s7ecatalogsearchviewer .s7emaildialog .s7dialogerrormessage[state="senderror"] { 
    background-image: url("images/sdk/dlgerrimg.png"); 
    color: #FF0000; 
} 
.s7ecatalogsearchviewer .s7emaildialog .s7dialogerrormessage[state="sendsuccess"] { 
    background-image: none; 
    color: #00B200; 
} 
.s7ecatalogsearchviewer .s7emaildialog .s7dialogerrormessage { 
    background-position: left center; 
    font-size: 10pt; 
    font-weight: bold; 
    line-height: 25px; 
    padding-left: 20px; 
}
```

Wenn ein vertikaler Bildlauf erforderlich ist, wird die Bildlaufleiste im Bedienfeld neben dem rechten Rand des Dialogfelds gerendert, das mit der folgenden CSS-Klassenauswahl gesteuert wird:

```
.s7ecatalogsearchviewer .s7emaildialog .s7dialogscrollpanel
```

**CSS-Eigenschaften des Bedienfelds für den Bildlauf im Dialogfeld**

<table id="table_A0C3AC7E00544FFBB8E1364F4CDDB371"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width  </span> </p> </td> 
   <td colname="col2"> <p>Breite des Bildlaufbedienfelds. </p> </td> 
  </tr> 
 </tbody> 
</table>

Beispiel: So richten Sie ein Bildlaufbedienfeld auf eine Breite von 44 Pixel ein:

```
.s7ecatalogsearchviewer .s7emaildialog .s7dialogscrollpanel { 
    width: 44px; 
}
```

Das Erscheinungsbild des Bildlaufleistenbereichs wird mithilfe der folgenden CSS-Klassenauswahl gesteuert:

```
.s7ecatalogsearchviewer .s7emaildialog .s7scrollbar
```

**CSS-Eigenschaften der Bildlaufleiste**

<table id="table_2BF74CF43E9B42D79F99A3F5208D7051"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width  </span> </p> </td> 
   <td colname="col2"> <p> Die Breite der Bildlaufleiste. </p> </td> 
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

Beispiel: Zum Einrichten einer Bildlaufleiste mit einer Breite von 28 Pixeln und einem Rand von acht Pixeln von oben, rechts und unten im Bildlaufbedienfeld:

```
.s7ecatalogsearchviewer .s7emaildialog .s7scrollbar { 
    bottom: 8px; 
    right: 8px; 
    top: 8px; 
    width: 28px; 
}
```

Die Bildlaufleistenspur ist der Bereich zwischen den Schaltflächen für den oberen und unteren Bildlauf. Die Komponente legt automatisch die Position und Höhe der Leiste fest. Die Spur wird mit der folgenden CSS-Klassenauswahl gesteuert:

```
.s7ecatalogsearchviewer .s7emaildialog .s7scrollbar .s7scrolltrack
```

**CSS-Eigenschaften der Bildlaufspur**

<table id="table_EE990E7A342843619EDD84BAD29C6F2A"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width  </span> </p> </td> 
   <td colname="col2"> <p>Die Spurbreite. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color  </span> </p> </td> 
   <td colname="col2"> <p>Die Trackhintergrundfarbe. </p> </td> 
  </tr> 
 </tbody> 
</table>

Beispiel: So richten Sie eine Bildlaufleistenspur ein, die 28 Pixel breit und einen grauen Hintergrund hat:

```
.s7ecatalogsearchviewer .s7emaildialog .s7scrollbar .s7scrolltrack { 
width:28px; 
background-color: #B2B2B2; 
}
```

Der Bildlauffeld bewegt sich vertikal innerhalb eines Bildlaufverfolgungsbereichs. Seine vertikale Position wird vollständig durch die Komponentenlogik gesteuert, die Höhe des Daumens ändert sich jedoch nicht dynamisch je nach Inhaltsmenge. Sie können die Thumb-Höhe und andere Aspekte mit der folgenden CSS-Klassenauswahl konfigurieren:

```
.s7ecatalogsearchviewer .s7emaildialog .s7scrollbar .s7scrollthumb
```

**CSS-Eigenschaften der Bildlaufleiste**

<table id="table_5A4A283A50044A51881D997885674BDF"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width  </span> </p> </td> 
   <td colname="col2"> <p>Die Daumenbreite. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height  </span> </p> </td> 
   <td colname="col2"> <p>Die Daumenhöhe. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> padding-top  </span> </p> </td> 
   <td colname="col2"> <p> Die vertikale Umrandung zwischen der Oberkante der Leiste. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> padding-bottom  </span> </p> </td> 
   <td colname="col2"> <p> Die vertikale Umrandung zwischen dem unteren Ende der Leiste. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image  </span> </p> </td> 
   <td colname="col2"> <p>Das Bild, das für einen bestimmten Daumenstatus angezeigt wird. </p> </td> 
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

Beispiel: Zum Einrichten eines Bildlauffensters mit 28 x 45 Pixeln, einem Ränder von 10 Pixeln am oberen und unteren Rand und unterschiedlicher Grafik für jeden Status:

```
.s7ecatalogsearchviewer .s7emaildialog .s7scrollbar .s7scrollthumb { 
    height: 45px; 
    padding-bottom: 10px; 
    padding-top: 10px; 
    width: 28px; 
} 
.s7ecatalogsearchviewer .s7emaildialog .s7scrollbar .s7scrollthumb[state="up"] { 
 background-image:url("images/sdk/scrollbar_thumb_up.png"); 
} 
.s7ecatalogsearchviewer .s7emaildialog .s7scrollbar .s7scrollthumb[state="down"] { 
 background-image:url("images/sdk/scrollbar_thumb_down.png"); 
} 
.s7ecatalogsearchviewer .s7emaildialog .s7scrollbar .s7scrollthumb[state="over"] { 
 background-image:url("images/sdk/scrollbar_thumb_over.png"); 
} 
.s7ecatalogsearchviewer .s7emaildialog .s7scrollbar .s7scrollthumb[state="disabled"] { 
 background-image:url("images/sdk/scrollbar_thumb_disabled.png"); 
}
```

Das Erscheinungsbild der Schaltflächen für den oberen und unteren Bildlauf wird mithilfe der folgenden CSS-Klassenselektoren gesteuert:

```
.s7ecatalogsearchviewer .s7emaildialog .s7scrollbar .s7scrollupbutton
```

```
.s7ecatalogsearchviewer .s7emaildialog .s7scrollbar .s7scrolldownbutton
```

Es ist nicht möglich, Bildlaufschaltflächen mit den Eigenschaften CSS `top`, `left`, `bottom` und `right` zu positionieren. Stattdessen werden sie von der Viewer-Logik automatisch positioniert.

**CSS-Eigenschaften der Schaltflächen für den oberen und unteren Bildlauf**

<table id="table_EB853317E08941979B0E141C3C9B2C49"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width  </span> </p> </td> 
   <td colname="col2"> <p>Die Schaltflächenbreite. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height  </span> </p> </td> 
   <td colname="col2"> <p>Die Schaltflächenhöhe. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image  </span> </p> </td> 
   <td colname="col2"> <p>Das Bild, das für einen bestimmten Schaltflächenstatus angezeigt wird. </p> </td> 
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

Die QuickInfo für Schaltflächen kann lokalisiert werden. Weitere Informationen finden Sie unter [Lokale Anpassung der Elemente der Benutzeroberfläche](../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74).

Beispiel: So richten Sie Bildlaufschaltflächen ein, die 28 x 32 Pixel groß sind und für jeden Status ein anderes Bildmaterial haben:

```
.s7ecatalogsearchviewer .s7emaildialog .s7scrollbar .s7scrollupbutton { 
 width:28px; 
 height:32px; 
} 
.s7ecatalogsearchviewer .s7emaildialog .s7scrollbar .s7scrollupbutton[state='up'] { 
background-image:url(images/sdk/scroll_up_up.png); 
} 
.s7ecatalogsearchviewer .s7emaildialog .s7scrollbar .s7scrollupbutton[state='over'] { 
 background-image:url(images/sdk/scroll_up_over.png); 
} 
.s7ecatalogsearchviewer .s7emaildialog .s7scrollbar .s7scrollupbutton[state='down'] { 
 background-image:url(images/sdk/scroll_up_down.png); 
} 
.s7ecatalogsearchviewer .s7emaildialog .s7scrollbar .s7scrollupbutton[state='disabled'] { 
 background-image:url(images/sdk/scroll_up_disabled.png); 
} 
.s7ecatalogsearchviewer .s7emaildialog .s7scrollbar .s7scrolldownbutton { 
 width:28px; 
 height:32px; 
} 
.s7ecatalogsearchviewer .s7emaildialog .s7scrollbar .s7scrolldownbutton[state='up'] { 
 background-image:url(images/sdk/scroll_down_up.png); 
} 
.s7ecatalogsearchviewer .s7emaildialog .s7scrollbar .s7scrolldownbutton[state='over'] { 
 background-image:url(images/sdk/scroll_down_over.png); 
} 
.s7ecatalogsearchviewer .s7emaildialog .s7scrollbar .s7scrolldownbutton[state='down'] { 
 background-image:url(images/sdk/scroll_down_down.png); 
} 
.s7ecatalogsearchviewer .s7emaildialog .s7scrollbar .s7scrolldownbutton[state='disabled'] { 
 background-image:url(images/sdk/scroll_down_disabled.png); 
}
```

