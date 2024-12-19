---
title: Video-Vollbildschaltfläche
description: Die Vollbildschaltfläche bewirkt, dass der Viewer in den Vollbildmodus wechselt oder diesen verlässt, wenn er vom Benutzer ausgewählt wird. Er wird verwendet, wenn der Viewer ein Video anzeigt und in der Steuerleiste positioniert ist. Diese Schaltfläche wird nicht angezeigt, wenn der Viewer im Popup-Modus funktioniert und das System keinen nativen Vollbildmodus unterstützt.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: 45811efa-95f6-4b6d-96f8-9e5437a55f0e
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '312'
ht-degree: 0%

---

# Video-Vollbildschaltfläche{#video-full-screen-button}

Die Vollbildschaltfläche bewirkt, dass der Viewer in den Vollbildmodus wechselt oder diesen verlässt, wenn er vom Benutzer ausgewählt wird. Er wird verwendet, wenn der Viewer ein Video anzeigt und in der Steuerleiste positioniert ist. Diese Schaltfläche wird nicht angezeigt, wenn der Viewer im Popup-Modus funktioniert und das System keinen nativen Vollbildmodus unterstützt.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

Sie können die Vollbildschaltfläche per CSS skalieren, ausrichten und positionieren, und zwar relativ zur Steuerleiste, in der sie enthalten ist.

Das Erscheinungsbild der Vollbildschaltfläche wird mit dem CSS-Klassenselektor gesteuert:

```
.s7mixedmediaviewer .s7fullscreenbutton
```

**CSS-Eigenschaften der Vollbildschaltfläche**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Top-</span> </p> </td> 
   <td colname="col2"> <p> Position ab dem oberen Rahmen, einschließlich Auffüllung. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> rechte </span> </p> </td> 
   <td colname="col2"> <p> Position vom rechten Rand aus, einschließlich Abstand. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> linker </span> </p> </td> 
   <td colname="col2"> <p> Position vom linken Rand aus, einschließlich Auffüllung. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> untere </span> </p> </td> 
   <td colname="col2"> <p>Position ab dem unteren Rand, einschließlich Abstand. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Breite </span> </p> </td> 
   <td colname="col2"> <p> Die Breite der Vollbildschaltfläche. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Höhe </span> </p> </td> 
   <td colname="col2"> <p>Die Höhe der Vollbildschaltfläche. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Hintergrundbild-</span> </p> </td> 
   <td colname="col2"> <p> Das angezeigte Bild für einen bestimmten Schaltflächenstatus. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Hintergrundposition </span> </p> </td> 
   <td colname="col2"> <p> Positionieren Sie sie innerhalb des Bildsets, wenn CSS-Sprites verwendet werden. </p> <p>Siehe <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/c-html5-mixedmedia-viewer-customizingviewer/c-html5-mixedmedia-viewer-customizingviewer.md#section-209a43dfbddf4fc589e79cddaf233f50" format="dita" scope="local"> von CSS-Sprites </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Diese Schaltfläche unterstützt sowohl den `state`- als auch den `selected`-Attributselektor, mit dem verschiedene Skins auf verschiedene Schaltflächenzustände angewendet werden können. Insbesondere entspricht `selected='true'` dem „Vollbild“-Zustand und `selected='false'` dem „Normal“-Zustand.

Die QuickInfo der Schaltfläche kann lokalisiert werden. Siehe [Lokalisierung von Benutzeroberflächenelementen](../../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/c-html5-mixedmedia-viewer-localization.md#concept-16262b8096474d6c9c018c3e99110dd1) für weitere Informationen.

## Beispiel {#section-e8caea0a303c425a8a637c2a47c06355}

So richten Sie eine Vollbildschaltfläche ein, die 32 x 32 Pixel groß ist und 6 Pixel vom oberen und rechten Rand der Steuerleiste entfernt positioniert ist. Zeigen Sie außerdem für jeden der vier verschiedenen Schaltflächenstatus ein anderes Bild an, wenn Sie ausgewählt sind oder nicht.

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
