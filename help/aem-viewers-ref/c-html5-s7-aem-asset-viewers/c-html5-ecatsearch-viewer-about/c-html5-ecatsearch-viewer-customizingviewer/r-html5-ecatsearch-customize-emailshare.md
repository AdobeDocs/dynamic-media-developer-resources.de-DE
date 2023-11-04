---
title: Email Share
description: Das Tool für die E-Mail-Freigabe besteht aus einer Schaltfläche, die zum Social-Freigabe-Bedienfeld hinzugefügt wird, und dem modalen Dialogfeld, das bei Aktivierung des Tools angezeigt wird. Die Position der Schaltfläche wird vollständig vom Social-Freigabe-Tool verwaltet.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: a879994d-2f26-4fdd-9a51-73644fc033cd
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '3046'
ht-degree: 2%

---

# Email Share{#email-share}

Das Tool für die E-Mail-Freigabe besteht aus einer Schaltfläche, die zum Social-Freigabe-Bedienfeld hinzugefügt wird, und dem modalen Dialogfeld, das bei Aktivierung des Tools angezeigt wird. Die Position der Schaltfläche wird vollständig vom Social-Freigabe-Tool verwaltet.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

Das Erscheinungsbild der E-Mail-Freigabe-Schaltfläche wird mit der folgenden CSS-Klassenauswahl gesteuert:

```
.s7ecatalogsearchviewer .s7emailshare
```

**CSS-Eigenschaften des Tools für die E-Mail-Freigabe**

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
   <td colname="col1"> <p> <span class="codeph"> background-image </span> </p> </td> 
   <td colname="col2"> <p> Das Bild, das für einen bestimmten Schaltflächenstatus angezeigt wird. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p> Position innerhalb des Bildsprites, wenn CSS-Sprites verwendet werden. </p> <p>Siehe auch <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-customizingviewer/c-html5-ecatsearch-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> CSS-Sprites </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Diese Schaltfläche unterstützt `state` -Attributauswahl, die verwendet werden kann, um verschiedene Skins auf verschiedene Schaltflächenzustände anzuwenden.

Sie können die Schaltfläche aus dem Social-Freigabebereich entfernen, indem Sie `display:none` CSS-Eigenschaft in der zugehörigen CSS-Klasse.

Die QuickInfo der Schaltfläche kann lokalisiert werden. Siehe [Lokalisierung der Elemente der Benutzeroberfläche](../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) für weitere Informationen.

Beispiel: Zum Einrichten einer E-Mail-Freigabe-Schaltfläche mit 28 x 28 Pixel, die für jeden der vier verschiedenen Schaltflächenstatus ein anderes Bild anzeigt.

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

Die Hintergrundüberlagerung, die die Webseite abdeckt, wenn das Dialogfeld aktiv ist, wird mit der folgenden CSS-Klassenauswahl gesteuert:

```
.s7ecatalogsearchviewer .s7emaildialog .s7backoverlay
```

**CSS-Eigenschaften der Rücken-Überlagerung**

<table id="table_1A0C28D8C81D413C83D73DEAC53057C5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Deckkraft </span> </p> </td> 
   <td colname="col2"> <p> Deckkraft der Hintergrundüberlagerung. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p>Hintergrundüberlagerungsfarbe. </p> </td> 
  </tr> 
 </tbody> 
</table>

Beispiel: Um eine Hintergrundüberlagerung einzurichten, die grau mit einer Deckkraft von 70 % ist:

```
.s7ecatalogsearchviewer .s7emaildialog .s7backoverlay { 
 opacity:0.7; 
 background-color:#222222; 
}
```

Standardmäßig wird das modale Dialogfeld auf Desktop-Systemen zentriert auf dem Bildschirm angezeigt und nimmt den gesamten Webseitenbereich auf Touch-Geräten. In allen Fällen wird die Positionierung und Größe des Dialogfelds von der Komponente verwaltet. Das Dialogfeld wird mit dem folgenden CSS-Klassenselektor gesteuert:

```
.s7ecatalogsearchviewer .s7emaildialog .s7dialog
```

**CSS-Eigenschaften des Dialogfelds**

<table id="table_5272BC8EF9124018B4290356B95B5559"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> border-radius </span> </p> </td> 
   <td colname="col2"> <p> Rahmenradius des Dialogfelds (falls das Dialogfeld nicht das gesamte Browser-Fenster akzeptiert); </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p> Hintergrundfarbe des Dialogfelds; </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p> Sollte entweder nicht festgelegt oder auf 100 % eingestellt sein. In diesem Fall nimmt das Dialogfeld das gesamte Browser-Fenster auf (dieser Modus wird auf Touch-Geräten bevorzugt). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p> Sollte entweder nicht festgelegt oder auf 100 % eingestellt sein. In diesem Fall nimmt das Dialogfeld das gesamte Browser-Fenster in Anspruch (dieser Modus wird auf Touch-Geräten bevorzugt). </p> </td> 
  </tr> 
 </tbody> 
</table>

Beispiel: Zum Einrichten eines Dialogfelds, das das gesamte Browser-Fenster verwendet und einen weißen Hintergrund auf Touch-Geräten aufweist:

```
.s7ecatalogsearchviewer .s7touchinput .s7emaildialog .s7dialog { 
 width:100%; 
 height:100%; 
background-color: #ffffff; 
}
```

Die Kopfzeile des Dialogfelds besteht aus einem Symbol, einem Titeltext und einer Schaltfläche &quot;Schließen&quot;. Der Kopfzeilencontainer wird mit dem folgenden CSS-Klassenselektor gesteuert

```
.s7ecatalogsearchviewer .s7emaildialog .s7dialogheader
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
.s7ecatalogsearchviewer .s7emaildialog .s7dialogheader .s7dialogline
```

**CSS-Eigenschaften der Dialogfeldzeile**

<table id="table_5B03CF843F0D4B1295A3FC1EB50C56F1"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Padding </span> </p> </td> 
   <td colname="col2"> <p> Innerer Abstand für das Kopfzeilensymbol und den Titel. </p> </td> 
  </tr> 
 </tbody> 
</table>

Das Kopfzeilensymbol wird mit der folgenden CSS-Klassenauswahl gesteuert:

```
.s7ecatalogsearchviewer .s7emaildialog .s7dialogheadericon
```

**CSS-Eigenschaften des Kopfzeilensymbols im Dialogfeld**

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
   <td colname="col2"> <p> Position innerhalb des Bildsprites, wenn CSS-Sprites verwendet werden. </p> <p>Siehe auch <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-customizingviewer/c-html5-ecatsearch-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> CSS-Sprites </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

Der Kopfzeilentitel wird mit der folgenden CSS-Klassenauswahl gesteuert:

```
.s7ecatalogsearchviewer .s7emaildialog .s7dialogheadertext
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
.s7ecatalogsearchviewer .s7emaildialog .s7closebutton
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
   <td colname="col2"> <p> Position innerhalb des Bildsprites, wenn CSS-Sprites verwendet werden. </p> <p>Siehe auch <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-customizingviewer/c-html5-ecatsearch-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> CSS-Sprites </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Diese Schaltfläche unterstützt `state` -Attributauswahl, die verwendet werden kann, um verschiedene Skins auf verschiedene Schaltflächenzustände anzuwenden.

Die QuickInfo der Schaltfläche Schließen und der Titel des Dialogfelds können lokalisiert werden. Siehe [Lokalisierung der Elemente der Benutzeroberfläche](../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) für weitere Informationen.

Beispiel: Zum Einrichten einer Dialogfeldkopfzeile mit Abstand, einem 24 x 17 Pixel langen Symbol und einem fett gedruckten 16-Punkt-Titel. Und schließlich wurden mit einer 28 x 28 Pixel großen Schließen-Schaltfläche zwei Pixel von der oberen Seite und zwei Pixel von der rechten Seite des Dialogfeldcontainers positioniert:

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

Die Dialogfußzeile besteht aus den Schaltflächen Abbrechen und E-Mail senden . Der Fußzeilencontainer wird mit der folgenden CSS-Klassenauswahl gesteuert:

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

Die Fußzeile verfügt über einen inneren Container, der beide Schaltflächen enthält. Sie wird mit dem folgenden CSS-Klassenselektor gesteuert:

```
.s7ecatalogsearchviewer .s7emaildialog .s7dialogbuttoncontainer
```

**CSS-Eigenschaften des Schaltflächenbehälters des Dialogfelds**

<table id="table_C34906888A8145C7A61E503DFC6B08A9"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Padding </span> </p> </td> 
   <td colname="col2"> <p> Innerer Abstand zwischen Fußzeile und Schaltflächen. </p> </td> 
  </tr> 
 </tbody> 
</table>

Die Schaltfläche Abbrechen wird mit der folgenden CSS-Klassenauswahl gesteuert:

```
.s7ecatalogsearchviewer .s7emaildialog .s7dialogcancelbutton
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

Die Schaltfläche E-Mail senden wird mit der folgenden CSS-Klassenauswahl gesteuert:

```
.s7ecatalogsearchviewer .s7emaildialog .s7dialogactionbutton
```

**CSS-Eigenschaften der Aktionsschaltfläche des Dialogfelds**

<table id="table_91C75B2470A24DC2AD3973A91FA8B325"> 
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
.s7ecatalogsearchviewer .s7emaildialog .s7dialogfooter .s7button
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

Die QuickInfos dieser Schaltfläche können lokalisiert werden. Siehe [Lokalisierung der Elemente der Benutzeroberfläche](../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) für weitere Informationen.

Beispiel: Zum Einrichten einer Footer mit der Schaltfläche Abbrechen 64 x 34 und einer Schaltfläche für den Versand einer E-Mail mit 82 x 34, deren Textfarbe und Hintergrundfarbe je nach Schaltflächenstatus unterschiedlich sind:

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

Der Hauptdialogbereich (zwischen der Kopfzeile und der Fußzeile) enthält bildlauffähigen Dialogfeldinhalt und Bildlaufbereich auf der rechten Seite. In allen Fällen verwaltet die Komponente die Breite dieses Bereichs. Es ist nicht möglich, ihn in CSS festzulegen. Der Hauptdialogbereich wird mit der folgenden CSS-Klassenauswahl gesteuert:

```
.s7ecatalogsearchviewer .s7emaildialog .s7dialogviewarea
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

>[!NOTE]
>
>Der Hauptdialogfeld-Bereich unterstützt das optionale `state` -Attributauswahl. Sie wird auf `sendsuccess` wenn das E-Mail-Formular gesendet wird und das Dialogfeld eine Bestätigungsmeldung anzeigt. Solange die Bestätigungsmeldung klein ist, kann diese Attributauswahl verwendet werden, um die Höhe des Dialogfelds zu reduzieren, wenn eine solche Bestätigungsmeldung angezeigt wird.

Beispiel: Um den Hauptdialogfeld-Bereich so einzurichten, dass er zunächst eine Höhe von 300 Pixel und bei Anzeige der Bestätigungsmeldung eine Höhe von 100 Pixel aufweist, haben Sie einen zehnten Pixelrand und verwenden Sie einen weißen Hintergrund:

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

Wenn die Höhe dieses Containers größer als der Hauptdialogfeld-Bereich zu sein scheint, wird automatisch ein vertikaler Bildlauf von der Komponente aktiviert.

**CSS-Eigenschaften des Dialogfeldtexts **

<table id="table_5D77F3D5B8CD4B798AA85F722B277F56"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Padding </span> </p> </td> 
   <td colname="col2"> <p>Innerer Abstand. </p> </td> 
  </tr> 
 </tbody> 
</table>

Beispiel: Zum Einrichten von Formularinhalten mit zehn Pixelabständen:

```
.s7ecatalogsearchviewer .s7emaildialog .s7dialogbody { 
    padding: 10px; 
}
```

Dialogfeldformular wird zeilenweise ausgefüllt, wobei jede Zeile einen Teil des Formularinhalts enthält (z. B. eine Beschriftung und ein Texteingabefeld). Eine einzelne Formularzeile wird mit der folgenden CSS-Klassenauswahl gesteuert:

```
.s7ecatalogsearchviewer .s7emaildialog .s7dialogbody .s7dialogline
```

**CSS-Eigenschaften der Dialogfeldzeile**

<table id="table_2CCCC71B45B444A8B9CE2894129C9C02"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Padding </span> </p> </td> 
   <td colname="col2"> <p>Inner Line padding. </p> </td> 
  </tr> 
 </tbody> 
</table>

Beispiel: Zum Einrichten eines Dialogfeldformulars mit zehn Pixelabständen pro Zeile:

```
.s7ecatalogsearchviewer .s7emaildialog .s7dialogbody .s7dialogline { 
    padding: 10px; 
}
```

Alle statischen Beschriftungen im Dialogfeldformular werden mit der folgenden CSS-Klassenauswahl gesteuert:

```
.s7ecatalogsearchviewer .s7emaildialog .s7dialoglabel
```

Diese Klasse eignet sich nicht zum Steuern der Größe oder Position von Beschriftungen, da Sie sie auf Texte an verschiedenen Stellen der Formular-Benutzeroberfläche anwenden können.

**CSS-Eigenschaften der Dialogfeldbeschriftung. **

<table id="table_13C7874807314ADD83A23075ABB4C340"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Schriftstärke </span> </p> </td> 
   <td colname="col2"> <p>Schriftgröße beschriften. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Schriftgröße </span> </p> </td> 
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

Dialogfeldbeschriftungen können lokalisiert werden. Siehe [Lokalisierung der Elemente der Benutzeroberfläche](../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) für weitere Informationen.

Beispiel: Um alle Beschriftungen mit einer 9-Pixel-Schriftart auf grau und fett festzulegen:

```
.s7ecatalogsearchviewer .s7emaildialog .s7dialoglabel { 
    color: #666666; 
    font-size: 9pt; 
    font-weight: bold; 
}
```

Alle statischen Beschriftungen, die links von den Formulareingabefeldern angezeigt werden, werden wie folgt gesteuert:

```
.s7ecatalogsearchviewer .s7emaildialog .s7dialoginputlabel
```

**CSS-Eigenschaften der Eingabebeschriftung des Dialogfelds**

<table id="table_B5CF02837BAA42C7B79B6D9DA20792DF"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Die Breite der statischen Beschriftung. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> text-align </span> </p> </td> 
   <td colname="col2"> <p>Die horizontale Textausrichtung. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margin </span> </p> </td> 
   <td colname="col2"> <p>Statische Beschriftungsrand. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Padding </span> </p> </td> 
   <td colname="col2"> <p>Statischer Abstand von Beschriftungen. </p> </td> 
  </tr> 
 </tbody> 
</table>

Beispiel: Um Eingabefelder so einzurichten, dass sie eine Breite von 50 Pixel, eine rechtsbündige Ausrichtung, zehn Pixel Abstand und einen zehn Pixel Rand auf der rechten Seite aufweisen:

```
.s7ecatalogsearchviewer .s7emaildialog .s7dialoginputlabel { 
    margin-right: 10px; 
    padding: 10px; 
    text-align: right; 
    width: 50px; 
}
```

Jedes Formulareingabefeld wird in den Container eingeschlossen, mit dem Sie einen benutzerdefinierten Rahmen um das Eingabefeld anwenden können. Sie wird mit dem folgenden CSS-Klassenselektor gesteuert:

```
.s7ecatalogsearchviewer .s7emaildialog .s7dialoginputcontainer
```

**CSS-Eigenschaften des Eingabecontainers des Dialogfelds**

<table id="table_7BC1C5919A54483F8121D928DC63233A"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> rand </span> </p> </td> 
   <td colname="col2"> <p>Ränder um den Eingabefeld-Container. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Padding </span> </p> </td> 
   <td colname="col2"> <p>Innerer Abstand. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Der Eingabefelder-Container unterstützt optional `state` -Attributauswahl. Sie wird auf `verifyerror` wenn der Benutzer einen Fehler im Eingabedatenformat macht und die Inline-Validierung fehlschlägt. Mit dieser Attributauswahl können Sie falsche Benutzereingaben im Formular hervorheben.

Die meisten Eingabefelder, die sich von der Beschriftung links bis zum rechten Rand des Dialogfeldtextes (einschließlich Feld Von und Feld Nachricht ) erstrecken, werden mit der folgenden CSS-Klassenauswahl gesteuert:

```
.s7ecatalogsearchviewer .s7emaildialog .s7dialoginputwide
```

**CSS-Eigenschaften des für die gesamte Eingabe des Dialogfelds vorgesehenen Felds**

<table id="table_7275B4365DFA4C0386FA2BDB7204A517"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Breite des Eingabefelds. </p> </td> 
  </tr> 
 </tbody> 
</table>

Das Feld An ist enger, da auf der rechten Seite Platz für die Schaltfläche E-Mail entfernen zugewiesen wird. Sie wird mit dem folgenden CSS-Klassenselektor gesteuert:

```
.s7ecatalogsearchviewer .s7emaildialog .s7dialoginputshort
```

**CSS-Eigenschaften des Dialogfelds geben Kurzfeld ein**

<table id="table_DFA9059209FF4184BD483A529424E97F"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Breite des Eingabefelds. </p> </td> 
  </tr> 
 </tbody> 
</table>

Beispiel: Um ein Formular so einzurichten, dass es einen grauen Rahmen von einem Pixel mit neun Pixel Abstand um alle Eingabefelder hat. So legen Sie für Felder, bei denen die Validierung fehlschlägt, denselben roten Rahmen fest. Und schließlich, um 250 Pixel breit bis Feld und die übrigen Eingabefelder 300 Pixel breit zu haben:

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

Das Eingabefeld für E-Mail-Nachrichten wird auch wie folgt gesteuert:

```
.s7ecatalogsearchviewer .s7emaildialog .s7dialogmessage
```

Mit dieser Klasse können Sie bestimmte Eigenschaften für den zugrunde liegenden `TEXTAREA` -Element.

**CSS-Eigenschaften der Dialogfeldmeldung**

<table id="table_9E9D5A0C3CDB45739615C4C07F8DC046"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Nachrichtenhöhe. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> word-wrap </span> </p> </td> 
   <td colname="col2"> <p>Wortumbruchstil. </p> </td> 
  </tr> 
 </tbody> 
</table>

Beispiel: Zum Einrichten einer E-Mail-Nachricht mit einer Höhe von 50 Pixel und zur Verwendung von `break-word` Wortumbruch:

```
.s7ecatalogsearchviewer .s7emaildialog .s7dialogmessage { 
    height: 50px; 
    word-wrap: break-word; 
}
```

Über die Schaltfläche Weitere E-Mail-Adresse hinzufügen können Benutzer mehr als eine Adresse im E-Mail-Formular hinzufügen. Sie wird mit dem folgenden CSS-Klassenselektor gesteuert:

```
.s7ecatalogsearchviewer .s7emaildialog .s7dialogaddemailbutton
```

**CSS-Eigenschaften des Dialogfelds Schaltfläche zum Hinzufügen von E-Mail-Adressen**

<table id="table_8829DC0694684E8BA427DFB821F7433D"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Schaltflächenhöhe. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> color </span> </p> </td> 
   <td colname="col2"> <p>Schaltflächentextfarbe für jeden Status. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image </span> </p> </td> 
   <td colname="col2"> <p>Schaltflächenbild für jeden Status. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p>Schaltflächenbildposition innerhalb des Schaltflächenbereichs. </p> </td> 
  </tr> 
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
   <td colname="col2"> <p>Schaltflächenschriftart. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> line-height </span> </p> </td> 
   <td colname="col2"> <p>Texthöhe innerhalb der Schaltfläche. Beeinflusst die vertikale Ausrichtung. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> text-align </span> </p> </td> 
   <td colname="col2"> <p>Horizontale Textausrichtung. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Padding </span> </p> </td> 
   <td colname="col2"> <p>Innerer Abstand. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Diese Schaltfläche unterstützt `state` -Attributauswahl, die verwendet werden kann, um verschiedene Skins auf verschiedene Schaltflächenzustände anzuwenden.

Die QuickInfo der Schaltfläche kann lokalisiert werden. Siehe [Lokalisierung der Elemente der Benutzeroberfläche](../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) für weitere Informationen.

Beispiel: Um die Schaltfläche &quot;Weitere E-Mail-Adresse hinzufügen&quot;auf eine Höhe von 25 Pixel festzulegen, verwenden Sie eine 12-Punkt-fett gedruckte Schriftart mit der rechten Ausrichtung sowie eine andere Textfarbe und ein anderes Bild für jeden Status:

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

Mit der Schaltfläche Entfernen können Benutzer zusätzliche Adressen aus dem E-Mail-Formular entfernen. Sie wird mit dem folgenden CSS-Klassenselektor gesteuert:

```
.s7ecatalogsearchviewer .s7emaildialog .s7dialogremoveemailbutton
```

**CSS-Eigenschaften des Dialogfelds entfernen die E-Mail-Schaltfläche**

<table id="table_79E4C65741E64859B9C9E9DCCB3D050B"> 
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
   <td colname="col2"> <p>Schaltflächenbild für jeden Status. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p> Position innerhalb des Bildsprites, wenn CSS-Sprites verwendet werden. </p> <p>Siehe auch <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-customizingviewer/c-html5-ecatsearch-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> CSS-Sprites </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Diese Schaltfläche unterstützt `state` -Attributauswahl, die verwendet werden kann, um verschiedene Skins auf verschiedene Schaltflächenzustände anzuwenden.

Die QuickInfo der Schaltfläche kann lokalisiert werden. Siehe [Lokalisierung der Elemente der Benutzeroberfläche](../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) für weitere Informationen.

Beispiel: Um eine Schaltfläche &quot;Entfernen&quot;einzurichten, die 25 x 25 Pixel groß ist, und für jeden Status ein anderes Bild zu verwenden:

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

Der freigegebene Inhalt wird unten im Hauptteil des Dialogfelds angezeigt und enthält eine Miniaturansicht, einen Titel, eine Ursprungs-URL und eine Beschreibung. Sie wird in einen Container eingeschlossen, der mit der folgenden CSS-Klassenauswahl gesteuert wird:

```
.s7ecatalogsearchviewer .s7emaildialog .s7dialogbody .s7dialogcontent
```

**CSS-Eigenschaften des Dialogfeldinhalts **

<table id="table_9C5CBFC2482E4A46BE837573B0B02FE4"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> rand </span> </p> </td> 
   <td colname="col2"> <p>Container-Rahmen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Padding </span> </p> </td> 
   <td colname="col2"> <p>Innerer Abstand. </p> </td> 
  </tr> 
 </tbody> 
</table>

Beispiel: Zum Einrichten eines unteren Containers mit einem gepunkteten Rahmen von einem Pixel und ohne Abstand:

```
.s7ecatalogsearchviewer .s7emaildialog .s7dialogbody .s7dialogcontent { 
    border: 1px dotted #A0A0A0; 
    padding: 0; 
}
```

Das Miniaturbild wird mit der folgenden CSS-Klassenauswahl gesteuert:

```
.s7ecatalogsearchviewer .s7emaildialog .s7dialogthumbnail
```

Die `background-image` -Eigenschaft wird durch die Komponentenlogik festgelegt.

**CSS-Eigenschaften des Miniaturbilds des Dialogfelds**

<table id="table_4C614FF2CEB149DAB5B7D7BC38CD3CAE"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Breite der Miniaturansicht. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Höhe der Miniaturansicht. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> vertikale Ausrichtung </span> </p> </td> 
   <td colname="col2"> <p>Miniaturansicht für die vertikale Ausrichtung. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Padding </span> </p> </td> 
   <td colname="col2"> <p>Innerer Abstand. </p> </td> 
  </tr> 
 </tbody> 
</table>

Beispiel: Um die Miniaturansicht auf 90 x 60 Pixel festzulegen und die Miniaturansicht mit zehn Pixel Abstand oben auszurichten:

```
.s7ecatalogsearchviewer .s7emaildialog .s7dialogthumbnail { 
    height: 60px; 
    padding: 10px; 
    vertical-align: top; 
    width: 90px; 
}
```

Titel, Ursprung und Beschreibung des Inhalts werden weiter in einem Bereich rechts neben der Inhaltsminiatur gruppiert. Sie wird mit dem folgenden CSS-Klassenselektor gesteuert:

```
.s7ecatalogsearchviewer .s7emaildialog .s7dialoginfopanel
```

**CSS-Eigenschaften des Informationsbereichs für das Dialogfeld**

<table id="table_EDFA6229D8C3468E989E7EC05F23EF3B"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Bedienfeldbreite. </p> </td> 
  </tr> 
 </tbody> 
</table>

Beispiel: Zum Einrichten eines Inhaltsinformationsbereichs mit einer Breite von 300 Pixel:

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
   <td colname="col1"> <p> <span class="codeph"> margin </span> </p> </td> 
   <td colname="col2"> <p>Außenrand. </p> </td> 
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
 </tbody> 
</table>

Beispiel: Zum Einrichten eines Inhaltstitels für die Verwendung einer fett gedruckten Schriftart mit einer zehnten Pixelbreite:

```
.s7ecatalogsearchviewer .s7emaildialog .s7dialogtitle { 
    font-weight: bold; 
    margin: 10px; 
}
```

Die Inhaltsquelle wird mit der folgenden CSS-Klassenauswahl gesteuert:

```
.s7ecatalogsearchviewer .s7emaildialog .s7dialogorigin
```

**CSS-Eigenschaften des Inhaltsherweises des Dialogfelds **

<table id="table_51763B532A9C4AE8AE54B69933A8C0B5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margin </span> </p> </td> 
   <td colname="col2"> <p>Außenrand. </p> </td> 
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
 </tbody> 
</table>

Beispiel: Zum Einrichten des Inhaltsursprungs mit einer zehnfachen Spanne:

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
   <td colname="col1"> <p> <span class="codeph"> margin </span> </p> </td> 
   <td colname="col2"> <p>Außenrand. </p> </td> 
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
 </tbody> 
</table>

Beispiel: Zum Einrichten einer Inhaltsbeschreibung mit einer zehnten Pixelbreite und einer neun Punkt-Schriftart:

```
.s7ecatalogsearchviewer .s7emaildialog .s7dialogdescription { 
    font-size: 9pt; 
    margin: 10px; 
}
```

Wenn ein Benutzer falsche Eingabedaten eingibt und die Inline-Validierung fehlschlägt, wird oben im Dialogfeldtext eine Meldung angezeigt. Diese Meldung wird auch angezeigt, wenn das Dialogfeld beim Senden des Formulars einen Fehler oder eine Bestätigungsmeldung rendern muss. Sie wird mit dem folgenden CSS-Klassenselektor gesteuert:

```
.s7ecatalogsearchviewer .s7emaildialog .s7dialogerrormessage
```

**CSS-Eigenschaften der Fehlermeldung im Dialogfeld**

<table id="table_C114E1004C334D339C25A3438E8E6614"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image </span> </p> </td> 
   <td colname="col2"> <p> Fehlersymbol. Standard ist ein Ausrufezeichen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p> Die Fehlersymbolposition innerhalb des Nachrichtenbereichs. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> color </span> </p> </td> 
   <td colname="col2"> <p>Textfarbe der Nachricht. </p> </td> 
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
   <td colname="col1"> <p> <span class="codeph"> line-height </span> </p> </td> 
   <td colname="col2"> <p> Texthöhe innerhalb der Nachricht. Beeinflusst die vertikale Ausrichtung. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Padding </span> </p> </td> 
   <td colname="col2"> <p>Innerer Abstand. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Diese Nachricht unterstützt die `state` -Attributauswahl mit den folgenden möglichen Werten: `verifyerror`, `senderror`, und `sendsuccess`. Der Wert `verifyerror` wird festgelegt, wenn eine Nachricht aufgrund eines Fehlers bei der Überprüfung der Inline-Eingabe angezeigt wird. Der Wert `senderror` wird festgelegt, wenn ein Backend-E-Mail-Dienst einen Fehler meldet. Der Wert `sendsuccess` festgelegt ist, wenn E-Mail erfolgreich gesendet wurde. Auf diese Weise kann die Nachricht je nach Status des Dialogfelds unterschiedlich formatiert werden.

Die QuickInfo der Schaltfläche kann lokalisiert werden.

Siehe [Lokalisierung der Elemente der Benutzeroberfläche](../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) für weitere Informationen.

Beispiel: Um eine Nachricht so einzurichten, dass sie eine 10-Punkt-Fettschrift verwendet, haben Sie eine 25-Pixel-Zeilenhöhe und einen 20-Pixel-Abstand auf der linken Seite. Verwenden Sie abschließend ein Ausrufezeichen-Symbol, roten Text, wenn ein Fehler auftritt, und kein Symbol und grüner Text, wenn ein Erfolg eintritt:

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

Wenn ein vertikaler Bildlauf erforderlich ist, wird die Bildlaufleiste im Bedienfeld nahe der rechten Kante des Dialogfelds gerendert, das mit der folgenden CSS-Klassenauswahl gesteuert wird:

```
.s7ecatalogsearchviewer .s7emaildialog .s7dialogscrollpanel
```

**CSS-Eigenschaften des Bildlauffensters des Dialogfelds**

<table id="table_A0C3AC7E00544FFBB8E1364F4CDDB371"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Bildlaufbereichbreite. </p> </td> 
  </tr> 
 </tbody> 
</table>

Beispiel: Um ein Bildlaufbedienfeld mit einer Breite von 44 Pixel einzurichten:

```
.s7ecatalogsearchviewer .s7emaildialog .s7dialogscrollpanel { 
    width: 44px; 
}
```

Das Erscheinungsbild des Bildlaufleistenbereichs wird mit der folgenden CSS-Klassenauswahl gesteuert:

```
.s7ecatalogsearchviewer .s7emaildialog .s7scrollbar
```

**CSS-Eigenschaften der Bildlaufleiste**

<table id="table_2BF74CF43E9B42D79F99A3F5208D7051"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p> Die Breite der Bildlaufleiste. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Anfang </span> </p> </td> 
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

Beispiel: Um eine Bildlaufleiste einzurichten, die 28 Pixel breit ist, und eine 8-Pixel-Spanne von oben, rechts und unten im Bildlaufbereich festzulegen:

```
.s7ecatalogsearchviewer .s7emaildialog .s7scrollbar { 
    bottom: 8px; 
    right: 8px; 
    top: 8px; 
    width: 28px; 
}
```

Die Bildlaufleisten-Spur ist der Bereich zwischen den oberen und unteren Bildlauftasten. Die Komponente legt automatisch die Position und Höhe der Spur fest. Die Verfolgung wird mit dem folgenden CSS-Klassenselektor gesteuert:

```
.s7ecatalogsearchviewer .s7emaildialog .s7scrollbar .s7scrolltrack
```

**CSS-Eigenschaften der Bildlaufspur**

<table id="table_EE990E7A342843619EDD84BAD29C6F2A"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Die Spurbreite. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p>Die Hintergrundfarbe der Verfolgung. </p> </td> 
  </tr> 
 </tbody> 
</table>

Beispiel: Zum Einrichten einer Bildlaufleiste, die 28 Pixel breit ist und einen grauen Hintergrund hat:

```
.s7ecatalogsearchviewer .s7emaildialog .s7scrollbar .s7scrolltrack { 
width:28px; 
background-color: #B2B2B2; 
}
```

Der Bildlaufleisten-Daumen bewegt sich in einem Bildlaufbereich vertikal. Seine vertikale Position wird vollständig von der Komponentenlogik gesteuert, die Daumenhöhe ändert sich jedoch nicht dynamisch in Abhängigkeit von der Inhaltsmenge. Sie können die Daumenhöhe und andere Aspekte mit dem folgenden CSS-Klassenselektor konfigurieren:

```
.s7ecatalogsearchviewer .s7emaildialog .s7scrollbar .s7scrollthumb
```

**CSS-Eigenschaften der Bildlaufleisten-Miniatur**

<table id="table_5A4A283A50044A51881D997885674BDF"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Die Daumenbreite. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Die Daumenhöhe. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Auffüllung </span> </p> </td> 
   <td colname="col2"> <p> Der vertikale Abstand zwischen dem oberen Ende des Gleises. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> padding-bottom </span> </p> </td> 
   <td colname="col2"> <p> Der vertikale Abstand zwischen dem unteren Ende des Gleises. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image </span> </p> </td> 
   <td colname="col2"> <p>Das Bild, das für einen bestimmten Daumenstatus angezeigt wird. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p> Position innerhalb des Bildsprites, wenn CSS-Sprites verwendet werden. </p> <p>Siehe auch <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-customizingviewer/c-html5-ecatsearch-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> CSS-Sprites </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Thumb unterstützt die `state` -Attribut-Selektor, der verwendet werden kann, um verschiedene Skins auf verschiedene Daumenstatus anzuwenden: `up`, `down`, `over`, und `disabled`.

Beispiel: Zum Einrichten eines Bildlaufleisten-Daumens mit 28 x 45 Pixel, einer zehnten Pixelspanne oben und unten und unterschiedlicher Abbildung für jeden Status:

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

Das Erscheinungsbild der oberen und unteren Bildlaufschaltflächen wird mithilfe der folgenden CSS-Klassenselektoren gesteuert:

```
.s7ecatalogsearchviewer .s7emaildialog .s7scrollbar .s7scrollupbutton
```

```
.s7ecatalogsearchviewer .s7emaildialog .s7scrollbar .s7scrolldownbutton
```

Es ist nicht möglich, Bildlaufschaltflächen mithilfe von CSS zu positionieren `top`, `left`, `bottom`, und `right` Eigenschaften. Stattdessen werden sie von der Viewer-Logik automatisch positioniert.

**CSS-Eigenschaften der Schaltflächen für den oberen und unteren Bildlauf**

<table id="table_EB853317E08941979B0E141C3C9B2C49"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Die Schaltflächenbreite. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Die Schaltflächenhöhe. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image </span> </p> </td> 
   <td colname="col2"> <p>Das Bild, das für einen bestimmten Schaltflächenstatus angezeigt wird. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p> Position innerhalb des Bildsprites, wenn CSS-Sprites verwendet werden. </p> <p>Siehe auch <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-customizingviewer/c-html5-ecatsearch-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> CSS-Sprites </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Diese Schaltflächen unterstützen `state` -Attributauswahl, die verwendet werden kann, um verschiedene Skins auf verschiedene Schaltflächenzustände anzuwenden: `up`, `down`, `over`, und `disabled`.

Die QuickInfo der Schaltfläche kann lokalisiert werden. Siehe [Lokalisierung der Elemente der Benutzeroberfläche](../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) für weitere Informationen.

Beispiel: Zum Einrichten von Bildlaufschaltflächen mit 28 x 32 Pixel und unterschiedlicher Grafik für jeden Status:

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
