---
title: Verwenden der Bibliothek "Responsives Bild"
description: Führen Sie die folgenden Schritte aus, um eine Bibliothek für responsives Bild zu einer Webseite hinzuzufügen und vorhandene Bilder mit der Bibliothek zu verwalten.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 2542b9f3-c398-4dbf-afa3-1671fc4fe72a
source-git-commit: b89ca96947f751b750623e1f18d2a5d86f0cd759
workflow-type: tm+mt
source-wordcount: '550'
ht-degree: 0%

---

# Verwenden der Bibliothek &quot;Responsives Bild&quot;{#using-responsive-image-library}

Führen Sie die folgenden Schritte aus, um eine Bibliothek für responsives Bild zu einer Webseite hinzuzufügen und vorhandene Bilder mit der Bibliothek zu verwalten.

**Verwenden der Bibliothek für responsive Bilder**

1. Erstellen Sie in Dynamic Media Classic [eine Bildvorgabe](https://experienceleague.adobe.com/docs/dynamic-media-classic/using/image-sizing/setting-image-presets.html#image-sizing) , falls Sie die Bibliothek für responsives Bild mit Vorgaben verwenden möchten.

   Verwenden Sie beim Definieren von Bildvorgaben, die mit der responsiven Bildbibliothek verwendet werden, keine Einstellungen, die sich auf die Bildgröße auswirken, z. B. `wid=`, `hei=` oder `scl=`. Geben Sie in der Bildvorgabe keine Größenfelder an. Lassen Sie sie stattdessen als leere Werte.
1. Fügen Sie die JavaScript-Bibliotheksdatei zu Ihrer Webseite hinzu.

   Bevor Sie die Bibliotheks-API verwenden können, stellen Sie sicher, dass Sie `responsive_image.js` einbeziehen. Diese JavaScript-Datei befindet sich im Unterordner `libs/` Ihrer standardmäßigen IS-Viewer-Bereitstellung:

   `<s7viewers_root>/libs/responsive_image.js`
1. Vorhandene Bilder einrichten.

   Die Bibliothek liest bestimmte Konfigurationsattribute aus einer Bildinstanz, mit der sie arbeitet. Definieren Sie Attribute, bevor die API-Funktion `s7responsiveImage` für ein solches Bild aufgerufen wird.

   Es wird außerdem empfohlen, die vorhandene Bild-URL in das Attribut `data-src` zu setzen. Richten Sie dann das vorhandene Attribut `src` ein, damit ein 1x1-GIF-Bild als Daten-URI kodiert wird. Dadurch wird die Anzahl der HTTP-Anfragen reduziert, die von der Webseite zum Ladezeitpunkt gesendet werden. Beachten Sie jedoch, dass es besser ist, ein `title` -Attribut in der Bildinstanz einzurichten, wenn SEO (Suchmaschinenoptimierung) benötigt wird.

   Im Folgenden finden Sie ein Beispiel für die Definition des Attributs `data-breakpoints` für das Bild und die Verwendung einer 1x1-GIF, die als Daten-URI kodiert ist:

   ```
   <img src="data:image/gif;base64,R0lGODlhAQABAIAAAAAAAP///yH5BAEAAAAALAAAAAABAAEAAAIBRAA7" data-src="https://s7d9.scene7.com/is/image/Scene7SharedAssets/Backpack_B" data-breakpoints="360,720,940">
   ```

1. Rufen Sie die API-Funktion `s7responsiveImage` für jede Bildinstanz auf, die von der Bibliothek verwaltet wird.

   Rufen Sie die API-Funktion `s7responsiveImage` für jede Bildinstanz auf, die von der Bibliothek verwaltet wird. Nach einem solchen Aufruf ersetzt die Bibliothek das Originalbild durch das Bild, das vom Image Serving heruntergeladen wird, entsprechend der Laufzeitgröße des Elements `IMG` im Web-Seitenlayout und der Dichte des Gerätebildschirms.

   Der folgende Code ist ein Beispiel für den Aufruf der API-Funktion `s7responsiveImage` für ein Bild, vorausgesetzt, `responsiveImage` ist eine ID dieses Bildes:

   ```
   <script type="text/javascript"> 
    s7responsiveImage(document.getElementById("responsiveImage")); 
   </script>
   ```

## Beispiel {#example-0509a0dd2a8e4fd58b5d39a0df47bd87}

Die Bibliothek unterstützt das gleichzeitige Arbeiten mit vielen Bildinstanzen auf der Web-Seite. Wiederholen Sie daher die obigen Schritte 1 und 2 für jedes Bild, das von der Bibliothek verwaltet werden soll.

Es liegt in der Verantwortung der Webseite, das Bildelement so zu gestalten, dass es flexibel in der Größe ist. Die Bibliothek für responsives Bild selbst unterscheidet nicht zwischen Bildern mit fester Größe und Bildern mit &quot;fließendem Inhalt&quot;. Wenn es auf ein Bild mit fester Größe angewendet wird, wird das neue Bild nur einmal geladen.

Der folgende Code ist ein vollständiges Beispiel für eine triviale Web-Seite mit einem einzelnen fließenden Bild, das von der Bibliothek für responsives Bild verwaltet wird. Das Beispiel enthält zusätzliche CSS-Stile, um das Bild entsprechend der Fenstergröße des Webbrowsers &quot;responsiv&quot;zu machen:

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

**Verwenden des smarten Zuschnitts**

In AEM 6.4 und Dynamic Media Viewers 5.9 sind zwei Modi für smartes Zuschneiden verfügbar:

* **Manuell** - Benutzerdefinierte Haltepunkte und entsprechende Image Service-Befehle werden innerhalb eines Attributs im Bildelement definiert.
* **Smartes Zuschneiden** - Berechnete Ausgabedarstellungen für smartes Zuschneiden werden automatisch vom Bereitstellungsserver abgerufen. Die beste Ausgabedarstellung wird mithilfe der Laufzeitgröße des Bildelements ausgewählt.

Um den Modus Smartes Zuschneiden zu verwenden, legen Sie das Attribut `data-mode` auf `smart crop` fest. Beispiel:

```html {.line-numbers}
<img 
src="data:image/gif;base64,R0lGODlhAQABAIAAAAAAAP///yH5BAEAAAAALAAAAAABAAEAAAIBRAA7" 
data-src="https://imageserver.com/is/image/ExampleCo/SmartCropAsset" 
data-mode="smartcrop">
```

Das verknüpfte Bildelement sendet während der Laufzeit ein `s7responsiveViewer` -Ereignis, wenn sich der Haltepunkt ändert.

```javascript {.line-numbers}
         responsiveImage.addEventListener("s7responsiveViewer", function (event) { 
           var s7event = event.s7responsiveViewerEvent; 
           if(s7event.type == "breakpointchanged") { 
              console.log("New width: " + s7event.width); 
              console.log("Old width: " + s7event.oldWidth); 
           } 
        });
```
