---
title: Social Share
description: Das Social Share-Tool wird standardmäßig in der oberen linken Ecke angezeigt. Er besteht aus einer Schaltfläche und einem Bereich, der sich erweitert, wenn der Benutzer auf eine Schaltfläche klickt oder tippt, und einzelne Tools zur Freigabe enthält.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: b65b8846-3287-47ae-bdb6-6cac768cece0
source-git-commit: edc127dc6e2ae2d9bd5feed08c8bc896c8c39747
workflow-type: tm+mt
source-wordcount: '330'
ht-degree: 0%

---

# Social Share{#social-share}

Das Social Share-Tool wird standardmäßig in der oberen linken Ecke angezeigt. Er besteht aus einer Schaltfläche und einem Bereich, der sich erweitert, wenn der Benutzer auf eine Schaltfläche klickt oder tippt, und einzelne Tools zur Freigabe enthält.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

Die Position und Größe des Tools für die Freigabe in sozialen Netzwerken in der Viewer-Benutzeroberfläche wird wie folgt gesteuert:

```
.s7ecatalogviewer .s7socialshare
```

**CSS-Eigenschaften des Tools für die Freigabe in sozialen Netzwerken**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margin-top </span> </p> </td> 
   <td colname="col2"> <p> Der Versatz am oberen Rand der Steuerleiste. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margin=left </span> </p> </td> 
   <td colname="col2"> <p> Der Abstand zur nächsten Schaltfläche links oder zur linken Seite der Steuerleiste, wenn es sich um die erste Schaltfläche in einer Zeile handelt. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p> Die Breite des Social-Sharing-Tools. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Die Höhe des Social-Sharing-Tools. </p> </td> 
  </tr> 
 </tbody> 
</table>

Beispiel: So richten Sie ein Social-Sharing-Tool ein, das vier Pixel von der Oberseite und fünf Pixel von der rechten Seite des Viewer-Containers positioniert und auf 28 x 28 Pixel skaliert ist:

```
.s7ecatalogviewer .s7socialshare { 
margin-top: 4px; 
margin-left: 10px; width:28px; 
 height:28px; 
}
```

Das Erscheinungsbild der Schaltfläche für das Social-Sharing-Tool wird mit der folgenden CSS-Klassenauswahl gesteuert:

```
.s7ecatalogviewer .s7socialshare .s7socialbutton
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
   <td colname="col2"> <p> Position innerhalb des Bildsprites, wenn CSS-Sprites verwendet werden. </p> <p>Siehe auch <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-customizingviewer/c-html5-20-ecatalog-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> CSS-Sprites </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Diese Schaltfläche unterstützt `state` -Attributauswahl, die verwendet werden kann, um verschiedene Skins auf verschiedene Schaltflächenzustände anzuwenden.

Die QuickInfo der Schaltfläche kann lokalisiert werden. Siehe [Lokalisierung der Elemente der Benutzeroberfläche](../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) für weitere Informationen.

Beispiel - So richten Sie eine Schaltfläche für das Social-Sharing-Tool ein, die für jeden der vier verschiedenen Schaltflächenstatus ein anderes Bild anzeigt:

```
.s7ecatalogviewer .s7socialshare .s7socialbutton[state='up'] { 
background-image:url(images/v2/SocialShare_video_dark_up.png); 
} 
.s7ecatalogviewer .s7socialshare .s7socialbutton[state='over'] { 
background-image:url(images/v2/SocialShare_dark_over.png); 
} 
.s7ecatalogviewer .s7socialshare .s7socialbutton[state='down'] { 
background-image:url(images/v2/SocialShare_dark_down.png); 
} 
.s7ecatalogviewer .s7socialshare .s7socialbutton[state='disabled'] { 
background-image:url(images/v2/SocialShare_dark_disabled.png); 
}
```

Das Erscheinungsbild des Bedienfelds, das die einzelnen Symbole für die Freigabe in sozialen Netzwerken enthält, wird mit der folgenden CSS-Klassenauswahl gesteuert:

```
.s7ecatalogviewer .s7socialshare .s7socialsharepanel
```

**CSS-Eigenschaften des Bedienfelds &quot;Social Share&quot;**

<table id="table_86E777A5851F47D6A49D966E24A9A6CD"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p>Die Hintergrundfarbe des Bedienfelds. </p> </td> 
  </tr> 
 </tbody> 
</table>

Beispiel: So richten Sie ein Bedienfeld mit transparenter Farbe ein:

```
.s7ecatalogviewer .s7socialshare .s7socialsharepanel { 
 background-color: transparent; 
}
```
