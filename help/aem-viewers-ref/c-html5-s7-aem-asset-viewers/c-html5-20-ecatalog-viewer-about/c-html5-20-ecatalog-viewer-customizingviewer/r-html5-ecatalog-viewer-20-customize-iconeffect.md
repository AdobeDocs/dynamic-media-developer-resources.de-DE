---
description: Der Zoomindikator wird über dem Hauptbereich der Ansicht angezeigt. Es wird angezeigt, wenn sich das Bild im Reset-Zustand befindet und es auch vom iconeffect-Parameter abhängt.
seo-description: Der Zoomindikator wird über dem Hauptbereich der Ansicht angezeigt. Es wird angezeigt, wenn sich das Bild im Reset-Zustand befindet und es auch vom iconeffect-Parameter abhängt.
seo-title: Symbol, Effekt
solution: Experience Manager
title: Symbol, Effekt
topic: Dynamic media
uuid: 9e8c0c6f-2c45-4acb-9acb-5b8494bfc69b
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef
workflow-type: tm+mt
source-wordcount: '192'
ht-degree: 1%

---


# Symboleffekt{#icon-effect}

Der Zoomindikator wird über dem Hauptbereich der Ansicht angezeigt. Es wird angezeigt, wenn sich das Bild im Reset-Zustand befindet und es auch vom iconeffect-Parameter abhängt.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

Das Erscheinungsbild des Anzeigebereichs wird mit der folgenden CSS-Klassenauswahl gesteuert:

```
.s7ecatalogviewer .s7pageview .s7iconeffect
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
   <td colname="col2"> <p> Position innerhalb des Bildausschnitt, wenn CSS-Sprites verwendet werden. </p> <p>Siehe auch <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-customizingviewer/c-html5-20-ecatalog-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> CSS-Sprites </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Breite des Zoomindikators in Pixel. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Höhe des Zoomindikators in Pixel. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Der Symboleffekt unterstützt die Attributauswahl `media-type`, mit der Sie verschiedene Symboleffekte auf verschiedene Geräte anwenden können. Insbesondere entspricht `media-type='standard'` Desktop-Systemen, bei denen die Mauseingabe normalerweise verwendet wird, und `media-type='multitouch'` Geräten mit Berührungseingabe.

Beispiel: So richten Sie einen Zoomindikator mit 100 x 100 Pixel ein, der für Desktop-Systeme und Touch-Geräte unterschiedliche Grafiken enthält.

```
.s7ecatalogviewer .s7pageview .s7iconeffect { 
 width: 100px; 
 height: 100px; 
} 
.s7ecatalogviewer .s7pageview .s7iconeffect[media-type='standard'] { 
 background-image:url(images/v2/IconEffect_zoom.png); 
} 
.s7ecatalogviewer .s7pageview .s7iconeffect[media-type='multitouch'] { 
 background-image:url(images/v2/IconEffect_pinch.png); 
}
```

