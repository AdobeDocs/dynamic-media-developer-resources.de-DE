---
title: Nach links drehen
description: Durch Klicken oder Tippen auf diese Schaltfläche wird das Bild in der Hauptansicht nach links gedreht. Diese Schaltfläche wird auf Mobiltelefonen nicht angezeigt, um Platz auf dem Bildschirm zu sparen. Außerdem wird die Schaltfläche ausgeblendet, wenn ein mehrdimensionales Rotationsset verwendet wird. Sie können die Schaltfläche mithilfe von CSS skalieren, mit der Haut versehen und positionieren.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: 0c7ca422-f4ac-4ad1-ab51-8521b4d4b20e
source-git-commit: cdc85af782ebc492ae2303469a7f4f54b5bc09c8
workflow-type: tm+mt
source-wordcount: '330'
ht-degree: 0%

---

# Nach links drehen{#spin-left-button}

Durch Klicken auf diese Schaltfläche wird das Bild in der Hauptansicht nach links gedreht. Diese Schaltfläche wird auf Mobiltelefonen nicht angezeigt, um Platz auf dem Bildschirm zu sparen. Außerdem wird die Schaltfläche ausgeblendet, wenn ein mehrdimensionales Rotationsset verwendet wird. Sie können die Schaltfläche mithilfe von CSS skalieren, mit der Haut versehen und positionieren.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**CSS-Eigenschaften der Rotationssymbole**

Die Schaltfläche wird zu einem internen Container hinzugefügt, der mit dem CSS-Klassenselektor DIV-gesteuert wird:

```
.s7mixedmediaviewer .s7spinbuttons
```

<table id="table_94EE3F5BBE4547C0B4943471CEE7EDE4"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS-Eigenschaft </p> </th> 
   <th colname="col2" class="entry"> <p>Beschreibung </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Top-</span> </p> </td> 
   <td colname="col2"> <p>Position ab dem oberen Rahmen, einschließlich Auffüllung. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> rechte </span> </p> </td> 
   <td colname="col2"> <p>Position vom rechten Rand aus, einschließlich Abstand. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> linker </span> </p> </td> 
   <td colname="col2"> <p>Position vom linken Rand aus, einschließlich Auffüllung. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> untere </span> </p> </td> 
   <td colname="col2"> <p>Position ab dem unteren Rand, einschließlich Abstand. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Breite </span> </p> </td> 
   <td colname="col2"> <p>Breite der Schaltfläche. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Höhe </span> </p> </td> 
   <td colname="col2"> <p>Höhe der Schaltfläche. </p> </td> 
  </tr> 
 </tbody> 
</table>

Das Erscheinungsbild dieser Schaltfläche im Container wird mit dem CSS-Klassenselektor gesteuert:

```
.s7mixedmediaviewer .s7spinbuttons .s7panleftbutton
```

<table id="table_3EC45539877A479DB83E8FC69142450B"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS-Eigenschaft </p> </th> 
   <th colname="col2" class="entry"> <p>Beschreibung </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Top-</span> </p> </td> 
   <td colname="col2"> <p>Position ab dem oberen Rahmen, einschließlich Auffüllung. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> rechte </span> </p> </td> 
   <td colname="col2"> <p>Position vom rechten Rand aus, einschließlich Abstand. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> linker </span> </p> </td> 
   <td colname="col2"> <p>Position vom linken Rand aus, einschließlich Auffüllung. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> untere </span> </p> </td> 
   <td colname="col2"> <p>Position ab dem unteren Rand, einschließlich Abstand. </p> </td> 
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
   <td colname="col2"> <p>Das Bild, das für einen bestimmten Schaltflächenstatus angezeigt wird. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Hintergrundposition </span> </p> </td> 
   <td colname="col2"> <p> Positionieren Sie sie innerhalb des Bildsets, wenn CSS-Sprites verwendet werden. </p> <p>Siehe <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/c-html5-mixedmedia-viewer-customizingviewer/c-html5-mixedmedia-viewer-customizingviewer.md#section-209a43dfbddf4fc589e79cddaf233f50" format="dita" scope="local"> von CSS-Sprites </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Diese Schaltfläche unterstützt die `state`-Attributauswahl, mit der verschiedene Skins auf verschiedene Schaltflächenzustände angewendet werden können.

Die QuickInfos für die Schaltfläche können lokalisiert werden. Siehe [Lokalisierung von Benutzeroberflächenelementen](../../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/c-html5-mixedmedia-viewer-localization.md#concept-16262b8096474d6c9c018c3e99110dd1) für weitere Informationen.

Beispiel - So richten Sie eine linke Drehschaltfläche ein, die 28 x 28 Pixel groß ist und sich am linken Rand des inneren Containers befindet. Schließlich zeigt für jeden der vier verschiedenen Schaltflächenstatus ein eigenes Bild an:

```
.s7mixedmediaviewer .s7spinbuttons .s7panleftbutton { 
 position:absolute; 
 left: 0px; 
 width:28px; 
 height:28px; 
 background-size:contain; 
 } 
.s7mixedmediaviewer .s7spinbuttons .s7panleftbutton[state='up'] { 
background-image:url(images/v2/SpinLeftButton_light_up.png); 
} 
.s7mixedmediaviewer .s7spinbuttons .s7panleftbutton[state='over'] { 
background-image:url(images/v2/SpinLeftButton_light_over.png); 
} 
.s7mixedmediaviewer .s7spinbuttons .s7panleftbutton[state='down'] { 
background-image:url(images/v2/SpinLeftButton_light_down.png); 
} 
.s7mixedmediaviewer .s7spinbuttons .s7panleftbutton[state='disabled'] { 
background-image:url(images/v2/SpinLeftButton_light_disabled.png); 
}
```
