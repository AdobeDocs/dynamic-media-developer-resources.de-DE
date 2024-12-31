---
title: Verwenden der Bibliothek für responsive Bilder
description: Um einer Web-Seite die Bibliothek „Responsive Image“ hinzuzufügen und vorhandene Bilder mit der Bibliothek zu verwalten, führen Sie die folgenden Schritte aus.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 2542b9f3-c398-4dbf-afa3-1671fc4fe72a
source-git-commit: b89ca96947f751b750623e1f18d2a5d86f0cd759
workflow-type: tm+mt
source-wordcount: '550'
ht-degree: 0%

---

# Verwenden der Bibliothek für responsive Bilder{#using-responsive-image-library}

Um einer Web-Seite die Bibliothek „Responsive Image“ hinzuzufügen und vorhandene Bilder mit der Bibliothek zu verwalten, führen Sie die folgenden Schritte aus.

**So verwenden Sie die Bibliothek responsiver Bilder**

1. Erstellen Sie [ Dynamic Media Classic eine Bildvorgabe](https://experienceleague.adobe.com/docs/dynamic-media-classic/using/image-sizing/setting-image-presets.html#image-sizing) falls Sie die Bibliothek für responsive Bilder mit Vorgaben verwenden möchten.

   Verwenden Sie beim Definieren von Bildvorgaben, die mit der Bibliothek für responsive Bilder verwendet werden, keine Einstellungen wie `wid=`, `hei=` oder `scl=`, die die Bildgröße beeinflussen. Geben Sie in der Bildvorgabe keine Größenfelder an. Lassen Sie sie stattdessen als leere Werte.
1. Fügen Sie die JavaScript-Bibliotheksdatei zu Ihrer Webseite hinzu.

   Bevor Sie die Bibliotheks-API verwenden können, stellen Sie sicher, dass Sie `responsive_image.js` einbeziehen. Diese JavaScript-Datei befindet sich im `libs/` Unterordner Ihrer standardmäßigen IS-Viewers-Bereitstellung:

   `<s7viewers_root>/libs/responsive_image.js`
1. Vorhandene Bilder einrichten.

   Die -Bibliothek liest bestimmte Konfigurationsattribute aus einer Bildinstanz, mit der sie arbeitet. Definieren Sie Attribute, bevor die `s7responsiveImage`-API-Funktion für ein solches Bild aufgerufen wird.

   Es wird auch empfohlen, die vorhandene Bild-URL in das `data-src`-Attribut einzufügen. Richten Sie dann das vorhandene `src` so ein, dass ein 1x1-GIF-Bild als Daten-URI kodiert ist. Dadurch wird die Anzahl der HTTP-Anfragen reduziert, die von der Web-Seite zum Ladezeitpunkt gesendet werden. Beachten Sie jedoch, dass es bei Bedarf an SEO (Suchmaschinenoptimierung) besser ist, ein `title` Attribut in der Bildinstanz einzurichten.

   Im Folgenden finden Sie ein Beispiel für die Definition `data-breakpoints` Attributs für das Bild und die Verwendung einer 1x1-GIF, die als Daten-URI kodiert ist:

   ```
   <img src="data:image/gif;base64,R0lGODlhAQABAIAAAAAAAP///yH5BAEAAAAALAAAAAABAAEAAAIBRAA7" data-src="https://s7d9.scene7.com/is/image/Scene7SharedAssets/Backpack_B" data-breakpoints="360,720,940">
   ```

1. Rufen Sie die `s7responsiveImage`-API-Funktion für jede Bildinstanz auf, die von der Bibliothek verwaltet wird.

   Rufen Sie die `s7responsiveImage`-API-Funktion für jede Bildinstanz auf, die von der Bibliothek verwaltet wird. Nach einem solchen Aufruf ersetzt die Bibliothek das Originalbild durch das Bild, das von Image Serving heruntergeladen wird, entsprechend der Laufzeitgröße des `IMG` im Web-Seiten-Layout und der Dichte des Gerätebildschirms.

   Der folgende Code ist ein Beispiel für den Aufruf `s7responsiveImage` API-Funktion für ein Bild, unter der Annahme, dass `responsiveImage` eine ID dieses Bildes ist:

   ```
   <script type="text/javascript"> 
    s7responsiveImage(document.getElementById("responsiveImage")); 
   </script>
   ```

## Beispiel {#example-0509a0dd2a8e4fd58b5d39a0df47bd87}

Die -Bibliothek unterstützt die gleichzeitige Arbeit mit vielen Bildinstanzen auf der Web-Seite. Wiederholen Sie daher die obigen Schritte 1 und 2 für jedes Bild, das die Bibliothek verwalten soll.

Es liegt in der Verantwortung der Web-Seite, das Bildelement zu formatieren, um seine Größe flexibel zu gestalten. Die Bibliothek für responsive Bilder unterscheidet nicht zwischen Bildern mit fester Größe und „flüssigen“ Bildern. Wenn es auf ein Bild fester Größe angewendet wird, wird das neue Bild nur einmal geladen.

Der folgende Code ist ein vollständiges Beispiel für eine triviale Web-Seite mit einem einzigen fließenden Bild, das von der Bibliothek Responsive Image verwaltet wird. Das Beispiel enthält einen zusätzlichen CSS-Stil, damit das Bild auf die Fenstergröße des Webbrowsers „reagiert“:

```html {.line-numbers}
<!DOCTYPE html> 
<html> 
 <head> 
  <style type="text/css"> 
  .container { 
   width: 50%; 
  } 
  .fluidimage { 
   max-width: 100%; 
  } 
  </style> 
 </head> 
 <body> 
  <div class="container"> 
   <img id="responsiveImage" src="data:image/gif;base64,R0lGODlhAQABAIAAAAAAAP///yH5BAEAAAAALAAAAAABAAEAAAIBRAA7" data-src="https://s7d9.scene7.com/is/image/Scene7SharedAssets/Backpack_B" data-breakpoints="200,400,600,800" class="fluidimage"> 
  </div> 
  <script type="text/javascript" src="https://s7d9.scene7.com/s7viewers/libs/responsive_image.js"></script> 
  <script type="text/javascript"> 
   s7responsiveImage(document.getElementById("responsiveImage")); 
  </script> 
 </body> 
</html>
```

**Verwenden von smartem Zuschneiden**

In AEM 6.4 und Dynamic Media Viewer 5.9 stehen zwei Modi für smartes Zuschneiden zur Verfügung:

* **Manuell** - Benutzerdefinierte Haltepunkte und entsprechende Bilddienstbefehle werden in einem -Attribut im Bildelement definiert.
* **Smartes Zuschneiden** - Berechnete Ausgabedarstellungen für smartes Zuschneiden werden automatisch vom Versandserver abgerufen. Die beste Ausgabedarstellung wird anhand der Laufzeitgröße des Bildelements ausgewählt.

Um den Modus für smartes Zuschneiden zu verwenden, setzen Sie das `data-mode` auf `smart crop`. Beispiel:

```html {.line-numbers}
<img 
src="data:image/gif;base64,R0lGODlhAQABAIAAAAAAAP///yH5BAEAAAAALAAAAAABAAEAAAIBRAA7" 
data-src="https://imageserver.com/is/image/ExampleCo/SmartCropAsset" 
data-mode="smartcrop">
```

Das zugehörige Bildelement sendet zur Laufzeit ein `s7responsiveViewer`-Ereignis, wenn sich der Breakpoint ändert.

```javascript {.line-numbers}
         responsiveImage.addEventListener("s7responsiveViewer", function (event) { 
           var s7event = event.s7responsiveViewerEvent; 
           if(s7event.type == "breakpointchanged") { 
              console.log("New width: " + s7event.width); 
              console.log("Old width: " + s7event.oldWidth); 
           } 
        });
```
