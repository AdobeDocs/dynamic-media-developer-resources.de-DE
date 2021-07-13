---
description: Die Schaltfläche im Vollbildmodus bewirkt, dass der Videoplayer den Vollbildmodus aufruft oder verlässt, wenn ein Benutzer darauf klickt.
solution: Experience Manager
title: Schaltfläche "Vollbild"
feature: Dynamic Media Classic,Viewer,SDK/API,interaktive Videos
role: Developer,User
exl-id: ed9c9d37-f871-4094-9c6e-931d0f6edff1
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '258'
ht-degree: 2%

---

# Schaltfläche &quot;Vollbild&quot;{#full-screen-button}

Die Schaltfläche im Vollbildmodus bewirkt, dass der Videoplayer den Vollbildmodus aufruft oder verlässt, wenn ein Benutzer darauf klickt.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

Sie können die Vollbildschaltfläche in Bezug auf die sie enthaltende Steuerleiste durch CSS anpassen, gestalten und positionieren.

Das Erscheinungsbild der Schaltfläche im Vollbildmodus wird mit der CSS-Klassenauswahl gesteuert:

```
.s7interactivevideoviewer .s7fullscreenbutton
```

**CSS-Eigenschaften der Schaltfläche &quot;Vollbild&quot;**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Anfang </span> </p> </td> 
   <td colname="col2"> <p> Position vom oberen Rand, einschließlich Abstand. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> rechts </span> </p> </td> 
   <td colname="col2"> <p> Position vom rechten Rand, einschließlich Abstand. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> links </span> </p> </td> 
   <td colname="col2"> <p> Position vom linken Rand, einschließlich Abstand. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> unten </span> </p> </td> 
   <td colname="col2"> <p>Position vom unteren Rand, einschließlich Abstand. </p> </td> 
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
   <td colname="col2"> <p> Das angezeigte Bild für einen gegebenen Schaltflächenstatus. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position  </span> </p> </td> 
   <td colname="col2"> <p> Position innerhalb des Bildsprites, wenn CSS-Sprites verwendet werden. </p> <p>Siehe <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-customizingviewer/c-html5-aem-int-video-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> CSS-Sprites </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Diese Schaltfläche unterstützt die Attributselektoren `state` und `selected`, die verwendet werden können, um verschiedene Skins auf unterschiedliche Schaltflächenzustände anzuwenden. Insbesondere entspricht `selected='true'` dem Status &quot;Vollbild&quot;und `selected='false'` dem Status &quot;normal&quot;.

Die QuickInfo der Schaltfläche kann lokalisiert werden. Weitere Informationen finden Sie unter [Lokalisierung von Benutzeroberflächenelementen](../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74).

## Beispiel {#section-e8caea0a303c425a8a637c2a47c06355}

So richten Sie eine Vollbildschaltfläche von 32 x 32 Pixel ein und positionieren 6 Pixel von der oberen und rechten Kante der Steuerleiste. Zeigen Sie außerdem ein anderes Bild für jeden der vier Schaltflächenstatus an, wenn diese ausgewählt sind oder nicht ausgewählt sind.

```
.s7interactivevideoviewer . s7fullscreenbutton { 
top:6px; 
right:6px; 
width:32px; 
height:32px; 
} 
.s7interactivevideoviewer .s7fullscreenbutton [selected='false'][state='up'] { 
background-image:url(images/enterFullBtn_up.png); 
} 
.s7interactivevideoviewer .s7fullscreenbutton [selected='false'][state='over'] {  
background-image:url(images/enterFullBtn_over.png); 
} 
.s7interactivevideoviewer .s7fullscreenbutton [selected='false'][state='down'] {  
background-image:url(images/enterFullBtn_down.png); 
} 
.s7interactivevideoviewer .s7fullscreenbutton [selected='false'][state='disabled'] { 
background-image:url(images/enterFullBtn_disabled.png); 
} 
.s7interactivevideoviewer .s7fullscreenbutton [selected='true'][state='up'] {  
background-image:url(images/exitFullBtn_up.png); 
} 
.s7interactivevideoviewer .s7fullscreenbutton [selected='true'][state='over'] {  
background-image:url(images/exitFullBtn_over.png); 
} 
.s7interactivevideoviewer .s7fullscreenbutton [selected='true'][state='down'] {  
background-image:url(images/exitFullBtn_down.png); 
} 
.s7interactivevideoviewer .s7fullscreenbutton [selected='true'][state='disabled'] {  
background-image:url(images/exitFullBtn_disabled.png); } 
}
```
