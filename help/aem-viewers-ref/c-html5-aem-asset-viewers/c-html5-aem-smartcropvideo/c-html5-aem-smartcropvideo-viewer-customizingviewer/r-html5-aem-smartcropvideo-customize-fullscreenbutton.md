---
title: Schaltfläche im Vollbildmodus
description: Über die Schaltfläche im Vollbildmodus gelangt der Player für smartes Zuschneiden zum Vollbildmodus, wenn ein Benutzer darauf klickt.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop,Video
role: Developer,User
exl-id: 79b57f6d-17d2-48af-9414-b0ab9d24fbdc
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '244'
ht-degree: 0%

---

# Schaltfläche im Vollbildmodus{#full-screen-button}

Über die Schaltfläche im Vollbildmodus gelangt der Player für smartes Zuschneiden zum Vollbildmodus, wenn ein Benutzer darauf klickt.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

Sie können die Schaltfläche im Vollbildmodus in Bezug auf die sie enthaltende Steuerleiste über CSS anpassen, gestalten und positionieren.

Das Erscheinungsbild der Schaltfläche im Vollbildmodus wird mit der CSS-Klassenauswahl gesteuert:

```
.s7smartcropvideoviewer .s7fullscreenbutton
```

**CSS-Eigenschaften der Vollbildschaltfläche**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> top </span> </p> </td> 
   <td colname="col2"> <p> Position vom oberen Rand, einschließlich Abstand. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> rechts </span> </p> </td> 
   <td colname="col2"> <p> Position vom rechten Rand, einschließlich Abstand. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> left </span> </p> </td> 
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
   <td colname="col1"> <p> <span class="codeph"> Höhe </span> </p> </td> 
   <td colname="col2"> <p>Die Höhe der Schaltfläche im Vollbildmodus. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image </span> </p> </td> 
   <td colname="col2"> <p> Das angezeigte Bild für einen gegebenen Schaltflächenstatus. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p> Position innerhalb des Bildsprites, wenn CSS-Sprites verwendet werden. </p> <p>Siehe <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-smartcropvideo/c-html5-aem-smartcropvideo-viewer-customizingviewer/c-html5-aem-smartcropvideo-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> CSS-Sprites </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Diese Schaltfläche unterstützt sowohl die Attribute `state` als auch `selected`, die verwendet werden können, um verschiedene Skins auf verschiedene Schaltflächenzustände anzuwenden. Insbesondere entspricht `selected='true'` dem Status &quot;Vollbild&quot;und `selected='false'` dem Status &quot;normal&quot;.

Die QuickInfo der Schaltfläche kann lokalisiert werden. Weitere Informationen finden Sie unter [Lokalisierung von Benutzeroberflächenelementen](../../../c-html5-aem-asset-viewers/c-html5-aem-smartcropvideo/r-html5-aem-smartcropvideo-viewer-localization.md#concept-1d5ca2d8480f4064a51eddba13940aad) .

## Beispiel {#section-e8caea0a303c425a8a637c2a47c06355}

So richten Sie eine Vollbildschaltfläche von 32 x 32 Pixel ein und positionieren 6 Pixel von der oberen und rechten Kante der Steuerleiste. Zeigen Sie außerdem ein anderes Bild für jeden der vier Schaltflächenstatus an, wenn diese ausgewählt sind oder nicht ausgewählt sind.

```
.s7smartcropvideoviewer . s7fullscreenbutton { 
top:6px; 
right:6px; 
width:32px; 
height:32px; 
} 
.s7smartcropvideoviewer .s7fullscreenbutton [selected='false'][state='up'] { 
background-image:url(images/enterFullBtn_up.png); 
} 
.s7smartcropvideoviewer .s7fullscreenbutton [selected='false'][state='over'] {  
background-image:url(images/enterFullBtn_over.png); 
} 
.s7smartcropvideoviewer .s7fullscreenbutton [selected='false'][state='down'] {  
background-image:url(images/enterFullBtn_down.png); 
} 
.s7smartcropvideoviewer .s7fullscreenbutton [selected='false'][state='disabled'] { 
background-image:url(images/enterFullBtn_disabled.png); 
} 
.s7smartcropvideoviewer .s7fullscreenbutton [selected='true'][state='up'] {  
background-image:url(images/exitFullBtn_up.png); 
} 
.s7smartcropvideoviewer .s7fullscreenbutton [selected='true'][state='over'] {  
background-image:url(images/exitFullBtn_over.png); 
} 
.s7smartcropvideoviewer .s7fullscreenbutton [selected='true'][state='down'] {  
background-image:url(images/exitFullBtn_down.png); 
} 
.s7smartcropvideoviewer .s7fullscreenbutton [selected='true'][state='disabled'] {  
background-image:url(images/exitFullBtn_disabled.png); } 
}
```
