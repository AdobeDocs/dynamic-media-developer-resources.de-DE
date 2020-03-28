---
description: Um einer Webseite eine Bibliothek mit interaktiven Bildern hinzuzufügen und vorhandene Bilder mit der Bibliothek zu verwalten, führen Sie die folgenden Schritte aus.
seo-description: Um einer Webseite eine Bibliothek mit interaktiven Bildern hinzuzufügen und vorhandene Bilder mit der Bibliothek zu verwalten, führen Sie die folgenden Schritte aus.
seo-title: Verwenden der Bibliothek für interaktives Bild
solution: Experience Manager
title: Verwenden der Bibliothek für interaktives Bild
topic: Scene7 Image Serving - Image Rendering API
uuid: 325cdc8d-2bfa-4f9b-bf88-51d1dcc6c495
translation-type: tm+mt
source-git-commit: 87164dbf805a179f7bdeecd7cc6140c3456b61bb

---


# Verwenden der Bibliothek für interaktives Bild{#using-responsive-image-library}

Um einer Webseite eine Bibliothek mit interaktiven Bildern hinzuzufügen und vorhandene Bilder mit der Bibliothek zu verwalten, führen Sie die folgenden Schritte aus.

**So verwenden Sie die Bibliothek &quot;Responsive Image&quot;**

1. In SPS [erstellen Sie eine Bildvorgabe](http://help.adobe.com/en_US/scene7/using/WS2F6A1049-B41F-447d-A520-91227F9CDABF.html) , falls Sie die Bibliothek für interaktives Bild mit Vorgaben verwenden möchten.

   Verwenden Sie beim Definieren von Bildvorgaben, die mit der Bibliothek für interaktive Bilder verwendet werden, keine Einstellungen, die sich auf die Bildgröße auswirken, z. B. `wid=`, `hei=`oder `scl=`. Geben Sie keine Größenfelder in der Bildvorgabe an. Lassen Sie sie stattdessen als leere Werte.
1. Hinzufügen Sie die JavaScript-Bibliotheksdatei auf Ihre Webseite.

   Bevor Sie die Bibliotheks-API verwenden können, stellen Sie sicher, dass Sie `responsive_image.js`diese einschließen. Diese JavaScript-Datei befindet sich im `libs/` Unterordner Ihrer standardmäßigen IS-Viewer-Bereitstellung:

   `<s7viewers_root>/libs/responsive_image.js`
1. Richten Sie vorhandene Bilder ein.

   Die Bibliothek liest bestimmte Konfigurationsattribute aus einer Bildinstanz, mit der sie arbeitet. Definieren Sie Attribute, bevor die `s7responsiveImage` API-Funktion für ein solches Bild aufgerufen wird.

   Es wird außerdem empfohlen, die vorhandene Bild-URL in das `data-src` Attribut einzufügen. Richten Sie dann das vorhandene `src` Attribut so ein, dass ein 1x1 GIF-Bild als Daten-URI kodiert wird. Dadurch wird die Anzahl der HTTP-Anforderungen verringert, die von der Webseite zum Ladezeitpunkt gesendet werden. Beachten Sie jedoch, dass es besser ist, ein `title` Attribut für die Bildinstanz einzurichten, wenn SEO (Suchmaschinenoptimierung) benötigt wird.

   Im Folgenden finden Sie ein Beispiel für die Definition des `data-breakpoints` Attributs für das Bild und die Verwendung eines 1x1 GIF, das als Daten-URI kodiert wurde:

   ```
   <img src="data:image/gif;base64,R0lGODlhAQABAIAAAAAAAP///yH5BAEAAAAALAAAAAABAAEAAAIBRAA7" data-src="https://s7d9.scene7.com/is/image/Scene7SharedAssets/Backpack_B" data-breakpoints="360,720,940">
   ```

1. Rufen Sie die `s7responsiveImage` API-Funktion für jede Bildinstanz auf, die von der Bibliothek verwaltet wird.

   Rufen Sie die `s7responsiveImage` API-Funktion für jede Bildinstanz auf, die von der Bibliothek verwaltet wird. Nach einem solchen Aufruf ersetzt die Bibliothek das Originalbild durch das Bild, das gemäß der Laufzeitgröße des `IMG` Elements im Webseitenlayout und der Bildschirmdichte des Geräts vom Image Serving heruntergeladen wird.

   Der folgende Code ist ein Beispiel für den Aufruf der `s7responsiveImage` API-Funktion für ein Bild, vorausgesetzt, dass es sich um eine ID des Bildes `responsiveImage` handelt:

   ```
   <script type="text/javascript"> 
    s7responsiveImage(document.getElementById("responsiveImage")); 
   </script>
   ```

## Beispiel {#example-0509a0dd2a8e4fd58b5d39a0df47bd87}

Die Bibliothek unterstützt das gleichzeitige Arbeiten mit vielen Bildinstanzen auf der Webseite. Wiederholen Sie daher die obigen Schritte 1 und 2 für jedes Bild, das von der Bibliothek verwaltet werden soll.

Es liegt in der Verantwortung der Webseite, das Bildelement zu gestalten, um es flexibel in der Größe zu gestalten. In der Bibliothek für interaktives Bild selbst wird nicht zwischen Bildern mit fester Größe und Bildern mit &quot;flüssiger&quot;Darstellung unterschieden. Wenn es auf ein Bild mit fester Größe angewendet wird, wird das neue Bild nur einmal geladen.

Der folgende Code ist ein vollständiges Beispiel für eine triviale Webseite, auf der ein einzelnes, von der Bibliothek für interaktives Bild verwaltetes fließendes Bild angezeigt wird. Das Beispiel enthält zusätzliche CSS-Stile, damit das Bild &quot;responsiv&quot;zur Größe des Webbrowser-Fensters wird:

```
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

**Verwenden von intelligentem Beschneiden**

In AEM 6.4 und Scene7 Viewers 5.9 stehen zwei Smart-Beschneidungsmodi zur Verfügung:

* **Manuell** - benutzerdefinierte Haltepunkte und entsprechende Bilddienstbefehle werden innerhalb eines Attributs im Bildelement definiert.
* **Smart Crop** - Berechnete Smart-Schnittdarstellungen werden automatisch vom Versand-Server abgerufen. Die beste Darstellung wird unter Verwendung der Laufzeitgröße des Bildelements ausgewählt.

Um den Smart-Zuschneidemodus zu verwenden, setzen Sie das `data-mode` Attribut auf `smart crop`. Beispiel:

```
<img 
src="data:image/gif;base64,R0lGODlhAQABAIAAAAAAAP///yH5BAEAAAAALAAAAAABAAEAAAIBRAA7" 
data-src="https://imageserver.com/is/image/ExampleCo/SmartCropAsset" 
data-mode="smartcrop">
```

Das zugehörige Bildelement löst während der Laufzeit ein `s7responsiveViewer` Ereignis aus, wenn sich der Haltepunkt ändert.

```
         responsiveImage.addEventListener("s7responsiveViewer", function (event) { 
           var s7event = event.s7responsiveViewerEvent; 
           if(s7event.type == "breakpointchanged") { 
              console.log("New width: " + s7event.width); 
              console.log("Old width: " + s7event.oldWidth); 
           } 
        });
```
