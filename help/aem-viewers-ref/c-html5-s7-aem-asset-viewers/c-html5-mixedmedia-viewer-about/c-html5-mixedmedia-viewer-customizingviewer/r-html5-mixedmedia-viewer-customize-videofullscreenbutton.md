---
description: Durch Klicken auf die Schaltfläche im Vollbildmodus wird der Viewer in den Vollbildmodus versetzt oder beendet. Es wird verwendet, wenn der Viewer Videos anzeigt und sich in der Steuerungsleiste befindet. Diese Schaltfläche wird nicht angezeigt, wenn der Viewer im Popupmodus funktioniert und das System keinen nativen Vollbildmodus unterstützt.
seo-description: Durch Klicken auf die Schaltfläche im Vollbildmodus wird der Viewer in den Vollbildmodus versetzt oder beendet. Es wird verwendet, wenn der Viewer Videos anzeigt und sich in der Steuerungsleiste befindet. Diese Schaltfläche wird nicht angezeigt, wenn der Viewer im Popupmodus funktioniert und das System keinen nativen Vollbildmodus unterstützt.
seo-title: Schaltfläche "Video im Vollbildmodus"
solution: Experience Manager
title: Schaltfläche "Video im Vollbildmodus"
topic: Dynamic media
uuid: f264154b-eb4d-4dcb-b8c0-e06c383198ae
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef
workflow-type: tm+mt
source-wordcount: '384'
ht-degree: 1%

---


# Schaltfläche für den Vollbildmodus für Videos{#video-full-screen-button}

Durch Klicken auf die Schaltfläche im Vollbildmodus wird der Viewer in den Vollbildmodus versetzt oder beendet. Es wird verwendet, wenn der Viewer Videos anzeigt und sich in der Steuerungsleiste befindet. Diese Schaltfläche wird nicht angezeigt, wenn der Viewer im Popupmodus funktioniert und das System keinen nativen Vollbildmodus unterstützt.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

Sie können die Größe, Skin und Position der Schaltfläche im Vollbildmodus relativ zur Steuerungsleiste, in der sie enthalten ist, mithilfe von CSS festlegen.

Das Erscheinungsbild der Schaltfläche im Vollbildmodus wird mithilfe der CSS-Klassenauswahl gesteuert:

```
.s7mixedmediaviewer .s7fullscreenbutton
```

**CSS-Eigenschaften der Schaltfläche im Vollbildmodus**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Anfang </span> </p> </td> 
   <td colname="col2"> <p> Position vom oberen Rand, einschließlich Auffüllung. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> rechts </span> </p> </td> 
   <td colname="col2"> <p> Position vom rechten Rand, einschließlich Auffüllung. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> links </span> </p> </td> 
   <td colname="col2"> <p> Position vom linken Rand, einschließlich Auffüllung. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> unten </span> </p> </td> 
   <td colname="col2"> <p>Position vom unteren Rand, einschließlich Auffüllung. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p> Die Breite der Schaltfläche im Vollbildmodus. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Die Höhe der Schaltfläche im Vollbildmodus. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image  </span> </p> </td> 
   <td colname="col2"> <p> Das angezeigte Bild für einen Schaltflächenstatus. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position  </span> </p> </td> 
   <td colname="col2"> <p> Position innerhalb des Bildausschnitt, wenn CSS-Sprites verwendet werden. </p> <p>Siehe <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/c-html5-mixedmedia-viewer-customizingviewer/c-html5-mixedmedia-viewer-customizingviewer.md#section-209a43dfbddf4fc589e79cddaf233f50" format="dita" scope="local"> CSS-Sprites </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Diese Schaltfläche unterstützt sowohl die Attributselektoren `state` als auch `selected`, die verwendet werden können, um verschiedene Skins auf verschiedene Schaltflächenzustände anzuwenden. Insbesondere entspricht `selected='true'` dem Status &quot;Vollbild&quot;und `selected='false'` dem Status &quot;normal&quot;.

Die QuickInfo für Schaltflächen kann lokalisiert werden. Weitere Informationen finden Sie unter [Lokale Anpassung der Elemente der Benutzeroberfläche](../../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/c-html5-mixedmedia-viewer-localization.md#concept-16262b8096474d6c9c018c3e99110dd1).

## Beispiel {#section-e8caea0a303c425a8a637c2a47c06355}

Um eine Schaltfläche im Vollbildmodus einzurichten, die 32 x 32 Pixel groß und 6 Pixel von der oberen und rechten Kante der Steuerungsleiste entfernt ist. Zeigen Sie außerdem ein anderes Bild für jeden der vier verschiedenen Schaltflächenzustände an, wenn diese ausgewählt oder nicht ausgewählt sind.

```
.s7mixedmediaviewer . s7fullscreenbutton { 
top:6px; 
right:6px; 
width:32px; 
height:32px; 
} 
.s7mixedmediaviewer .s7fullscreenbutton [selected='false'][state='up'] { 
background-image:url(images/enterFullBtn_up.png); 
} 
.s7mixedmediaviewer .s7fullscreenbutton [selected='false'][state='over'] {  
background-image:url(images/enterFullBtn_over.png); 
} 
.s7mixedmediaviewer .s7fullscreenbutton [selected='false'][state='down'] {  
background-image:url(images/enterFullBtn_down.png); 
} 
.s7mixedmediaviewer .s7fullscreenbutton [selected='false'][state='disabled'] { 
background-image:url(images/enterFullBtn_disabled.png); 
} 
.s7mixedmediaviewer .s7fullscreenbutton [selected='true'][state='up'] {  
background-image:url(images/exitFullBtn_up.png); 
} 
.s7mixedmediaviewer .s7fullscreenbutton [selected='true'][state='over'] {  
background-image:url(images/exitFullBtn_over.png); 
} 
.s7mixedmediaviewer .s7fullscreenbutton [selected='true'][state='down'] {  
background-image:url(images/exitFullBtn_down.png); 
} 
.s7mixedmediaviewer .s7fullscreenbutton [selected='true'][state='disabled'] {  
background-image:url(images/exitFullBtn_disabled.png); } 
}
```

