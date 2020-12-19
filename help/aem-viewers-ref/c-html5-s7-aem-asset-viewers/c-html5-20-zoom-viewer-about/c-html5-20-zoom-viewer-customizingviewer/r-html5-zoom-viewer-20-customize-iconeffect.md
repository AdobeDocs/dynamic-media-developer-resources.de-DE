---
description: Der Zoomindikator wird über dem Hauptbereich der Ansicht angezeigt. Es wird angezeigt, wenn sich das Bild im Reset-Zustand befindet und es auch vom iconeffect-Parameter abhängt.
seo-description: Der Zoomindikator wird über dem Hauptbereich der Ansicht angezeigt. Es wird angezeigt, wenn sich das Bild im Reset-Zustand befindet und es auch vom iconeffect-Parameter abhängt.
seo-title: Symbol, Effekt
solution: Experience Manager
title: Symbol, Effekt
topic: Dynamic media
uuid: 5daf15ec-fcc5-4e37-924e-9a2cd6c0d167
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef
workflow-type: tm+mt
source-wordcount: '194'
ht-degree: 1%

---


# Symboleffekt{#icon-effect}

Der Zoomindikator wird über dem Hauptbereich der Ansicht angezeigt. Es wird angezeigt, wenn sich das Bild im Reset-Zustand befindet und es auch vom iconeffect-Parameter abhängt.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**CSS-Eigenschaften des Haupt-Viewer-Bereichs**

Das Erscheinungsbild des Anzeigebereichs wird mit der folgenden CSS-Klassenauswahl gesteuert:

```
.s7zoomviewer .s7zoomview .s7iconeffect
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
   <td colname="col1"> <p> <span class="codeph"> background-image  </span> </p> </td> 
   <td colname="col2"> <p> Bildmaterial für Zoomindikatoren </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position  </span> </p> </td> 
   <td colname="col2"> <p> Position innerhalb des Bildausschnitt, wenn CSS-Sprites verwendet werden. </p> <p>Siehe <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-flyout-viewer-20-about/c-html5-flyout-viewer-20-customizingviewer/c-html5-flyout-viewer-20-customizingviewer.md#section-0711ece44a4740168cfd7624c9010bd1" format="dita" scope="local"> CSS-Sprites </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Breite des Zoomindikators. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Höhe des Zoomindikators. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Der Symboleffekt unterstützt die Attributauswahl `media-type`, mit der Sie verschiedene Symboleffekte auf verschiedene Geräte anwenden können. Insbesondere entspricht `media-type='standard'` Desktop-Systemen, bei denen die Mauseingabe normalerweise verwendet wird, und `media-type='multitouch'` Geräten mit Berührungseingabe.

Beispiel: So richten Sie einen Zoomindikator mit 100 x 100 Pixel ein, der für Desktop-Systeme und Touch-Geräte unterschiedliche Grafiken enthält.

```
.s7zoomviewer .s7zoomview .s7iconeffect { 
 width: 100px; 
 height: 100px; 
} 
.s7zoomviewer .s7zoomview .s7iconeffect[media-type='standard'] { 
 background-image:url(images/v2/IconEffect_zoom.png); 
} 
.s7zoomviewer .s7zoomview .s7iconeffect[media-type='multitouch'] { 
 background-image:url(images/v2/IconEffect_pinch.png); 
}
```

