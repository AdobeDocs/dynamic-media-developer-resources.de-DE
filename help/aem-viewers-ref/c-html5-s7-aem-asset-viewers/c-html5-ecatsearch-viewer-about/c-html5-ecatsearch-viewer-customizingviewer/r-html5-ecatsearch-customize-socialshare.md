---
description: Das Social Sharing-Tool wird standardmäßig in der oberen linken Ecke angezeigt. Es besteht aus einer Schaltfläche und einem Bereich, der erweitert wird, wenn der Benutzer auf eine Schaltfläche klickt oder darauf tippt und einzelne Freigabewerkzeuge enthält.
seo-description: Das Social Sharing-Tool wird standardmäßig in der oberen linken Ecke angezeigt. Es besteht aus einer Schaltfläche und einem Bereich, der erweitert wird, wenn der Benutzer auf eine Schaltfläche klickt oder darauf tippt und einzelne Freigabewerkzeuge enthält.
seo-title: Social Sharing
solution: Experience Manager
title: Social Sharing
topic: Dynamic media
uuid: 6d463eb1-c6bf-4f1c-90e4-b5ef1e5a1538
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef

---


# Social Sharing{#social-share}

Das Social Sharing-Tool wird standardmäßig in der oberen linken Ecke angezeigt. Es besteht aus einer Schaltfläche und einem Bereich, der erweitert wird, wenn der Benutzer auf eine Schaltfläche klickt oder darauf tippt und einzelne Freigabewerkzeuge enthält.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

Die Position und Größe des Social Sharing-Tools in der Benutzeroberfläche des Viewers wird wie folgt gesteuert:

```
.s7ecatalogsearchviewer .s7socialshare
```

**CSS-Eigenschaften des Social Sharing-Tools**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margin-top </span> </p> </td> 
   <td colname="col2"> <p> Der Offset vom oberen Rand der Steuerleiste. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margin=left </span> </p> </td> 
   <td colname="col2"> <p> Der Abstand zur nächsten Schaltfläche links oder zur linken Seite der Steuerungsleiste, wenn dies die erste Schaltfläche in einer Zeile ist. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p> Die Breite des Social Sharing-Tools. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Die Höhe des Social Sharing-Tools. </p> </td> 
  </tr> 
 </tbody> 
</table>

Beispiel: Richten Sie ein Social Sharing-Tool ein, das vier Pixel von oben und fünf Pixel von rechts vom Viewer-Container positioniert wird und eine Größe von 28 x 28 Pixel aufweist.

```
.s7ecatalogsearchviewer .s7socialshare { 
margin-top: 4px; 
margin-left: 10px; width:28px; 
 height:28px; 
}
```

Das Erscheinungsbild der Schaltfläche für das Social Sharing-Tool wird mit der folgenden CSS-Klassenauswahl gesteuert:

```
.s7ecatalogsearchviewer .s7socialshare .s7socialbutton
```

**CSS-Eigenschaften der Social-Schaltfläche**

<table id="table_A18B6978EC304C378F5FE92DD44D138D"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image </span> </p> </td> 
   <td colname="col2"> <p> Das Bild, das für einen bestimmten Schaltflächenstatus angezeigt wird. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p> Position innerhalb des Bildausschnitt, wenn CSS-Sprites verwendet werden. </p> <p>Siehe auch <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-customizingviewer/c-html5-ecatsearch-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> CSS-Sprites </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Diese Schaltfläche unterstützt die `state` Attributauswahl, mit der verschiedene Skins auf verschiedene Schaltflächenzustände angewendet werden können.

Die QuickInfo für Schaltflächen kann lokalisiert werden. Weitere Informationen finden Sie unter [Lokale Anpassung der Elemente](../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) der Benutzeroberfläche.

Beispiel: Richten Sie eine Social Sharing-Tool-Schaltfläche ein, mit der für jeden der vier Schaltflächenzustände ein anderes Bild angezeigt wird.

```
.s7ecatalogsearchviewer .s7socialshare .s7socialbutton[state='up'] { 
background-image:url(images/v2/SocialShare_video_dark_up.png); 
} 
.s7ecatalogsearchviewer .s7socialshare .s7socialbutton[state='over'] { 
background-image:url(images/v2/SocialShare_dark_over.png); 
} 
.s7ecatalogsearchviewer .s7socialshare .s7socialbutton[state='down'] { 
background-image:url(images/v2/SocialShare_dark_down.png); 
} 
.s7ecatalogsearchviewer .s7socialshare .s7socialbutton[state='disabled'] { 
background-image:url(images/v2/SocialShare_dark_disabled.png); 
}
```

Das Erscheinungsbild des Bedienfelds mit den einzelnen Social Sharing-Symbolen wird mithilfe der folgenden CSS-Klassenauswahl gesteuert:

```
.s7ecatalogsearchviewer .s7socialshare .s7socialsharepanel
```

**CSS-Eigenschaften des Social Sharing-Bedienfelds**

<table id="table_86E777A5851F47D6A49D966E24A9A6CD"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p>Die Hintergrundfarbe des Bedienfelds. </p> </td> 
  </tr> 
 </tbody> 
</table>

Beispiel: Richten Sie ein Bedienfeld ein, das eine transparente Farbe hat:

```
.s7ecatalogsearchviewer .s7socialshare .s7socialsharepanel { 
 background-color: transparent; 
}
```

