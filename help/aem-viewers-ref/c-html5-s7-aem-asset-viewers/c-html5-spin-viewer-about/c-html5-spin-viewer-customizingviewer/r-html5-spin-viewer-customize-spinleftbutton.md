---
title: Schaltfläche "Nach links drehen"
description: Wenn Sie auf diese Schaltfläche klicken oder tippen, wird das Bild in der Hauptansicht nach links gedreht. Diese Schaltfläche wird nicht auf Mobiltelefonen angezeigt, um die Grundstücksgröße auf dem Bildschirm zu sparen. Außerdem ist die Schaltfläche ausgeblendet, wenn ein mehrdimensionales Rotationsset verwendet wird. Sie können die Schaltfläche mithilfe von CSS vergrößern, verkleinern und positionieren.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Spin Sets
role: Developer,User
exl-id: 2dba30d5-d257-4427-9476-ab695b6603aa
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '329'
ht-degree: 4%

---

# Schaltfläche &quot;Nach links drehen&quot;{#spin-left-button}

Wenn Sie auf diese Schaltfläche klicken oder tippen, wird das Bild in der Hauptansicht nach links gedreht. Diese Schaltfläche wird nicht auf Mobiltelefonen angezeigt, um die Grundstücksgröße auf dem Bildschirm zu sparen. Außerdem ist die Schaltfläche ausgeblendet, wenn ein mehrdimensionales Rotationsset verwendet wird. Sie können die Schaltfläche mithilfe von CSS vergrößern, verkleinern und positionieren.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**CSS-Eigenschaften der Rotationsschaltflächen**

Die Schaltfläche wird einem internen Container hinzugefügt, der mit dem CSS-Klassenselektor DIV gesteuert wird:

```
.s7spinviewer .s7spinbuttons
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
   <td colname="col1"> <p> <span class="codeph"> Anfang </span> </p> </td> 
   <td colname="col2"> <p>Position vom oberen Rand, einschließlich Abstand. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> rechts </span> </p> </td> 
   <td colname="col2"> <p>Position vom rechten Rand, einschließlich Abstand. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> links </span> </p> </td> 
   <td colname="col2"> <p>Position vom linken Rand, einschließlich Abstand. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> unten </span> </p> </td> 
   <td colname="col2"> <p>Position vom unteren Rand, einschließlich Abstand. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Breite der Schaltfläche. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Höhe der Schaltfläche. </p> </td> 
  </tr> 
 </tbody> 
</table>

Das Erscheinungsbild dieser Schaltfläche im Container wird mit dem CSS-Klassenselektor gesteuert:

```
.s7spinviewer .s7spinbuttons .s7panleftbutton
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
   <td colname="col1"> <p> <span class="codeph"> Anfang </span> </p> </td> 
   <td colname="col2"> <p>Position vom oberen Rand, einschließlich Abstand. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> rechts </span> </p> </td> 
   <td colname="col2"> <p>Position vom rechten Rand, einschließlich Abstand. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> links </span> </p> </td> 
   <td colname="col2"> <p>Position vom linken Rand, einschließlich Abstand. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> unten </span> </p> </td> 
   <td colname="col2"> <p>Position vom unteren Rand, einschließlich Abstand. </p> </td> 
  </tr> 
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
   <td colname="col2"> <p>Das Bild, das für einen bestimmten Schaltflächenstatus angezeigt wird. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p>Position innerhalb des Bildsprites, wenn CSS-Sprites verwendet werden. </p> <p>Siehe <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-spin-viewer-about/c-html5-spin-viewer-customizingviewer/c-html5-spin-viewer-customizingviewer.md#section-b671c70acf284cb0aea678c2d2e4babc" format="dita" scope="local"> CSS-Sprites </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Diese Schaltfläche unterstützt `state` -Attributauswahl, die verwendet werden kann, um verschiedene Skins auf verschiedene Schaltflächenzustände anzuwenden.

Die QuickInfo der Schaltfläche kann lokalisiert werden. Siehe [Lokalisierung der Elemente der Benutzeroberfläche](../../../c-html5-s7-aem-asset-viewers/c-html5-spin-viewer-about/c-html5-spin-viewer-localization.md#concept-e35c15c9e82648328806cdc6aa255d98) für weitere Informationen.

Beispiel: Um eine Schaltfläche mit der linken Maustaste einzurichten, die 28 x 28 Pixel groß ist und sich auf der linken Kante des inneren Containers befindet. Schließlich zeigt für jeden der vier Schaltflächenstatus ein anderes Bild an:

```
.s7spinviewer .s7spinbuttons .s7panleftbutton { 
 position:absolute; 
 left: 0px; 
 width:28px; 
 height:28px; 
 background-size:contain; 
 } 
.s7spinviewer .s7spinbuttons .s7panleftbutton[state='up'] { 
background-image:url(images/v2/SpinLeftButton_light_up.png); 
} 
.s7spinviewer .s7spinbuttons .s7panleftbutton[state='over'] { 
background-image:url(images/v2/SpinLeftButton_light_over.png); 
} 
.s7spinviewer .s7spinbuttons .s7panleftbutton[state='down'] { 
background-image:url(images/v2/SpinLeftButton_light_down.png); 
} 
.s7spinviewer .s7spinbuttons .s7panleftbutton[state='disabled'] { 
background-image:url(images/v2/SpinLeftButton_light_disabled.png); 
}
```
