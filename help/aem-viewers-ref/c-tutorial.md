---
title: Viewer-SDK-Tutorial
description: Das Viewer-SDK bietet eine Reihe JavaScript-basierter Komponenten für die benutzerdefinierte Viewer-Entwicklung. Die Viewer sind webbasierte Anwendungen, mit denen von Adobe Dynamic Media bereitgestellte Rich-Media-Inhalte in Webseiten eingebettet werden können.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API
role: Developer,User
exl-id: 3a798595-6c65-4a12-983d-3cdc53830d28
source-git-commit: b89ca96947f751b750623e1f18d2a5d86f0cd759
workflow-type: tm+mt
source-wordcount: '970'
ht-degree: 0%

---

# Viewer-SDK-Tutorial{#viewer-sdk-tutorial}

Das Viewer-SDK bietet eine Reihe JavaScript-basierter Komponenten für die benutzerdefinierte Viewer-Entwicklung. Die Viewer sind webbasierte Anwendungen, mit denen von Adobe Dynamic Media bereitgestellte Rich-Media-Inhalte in Webseiten eingebettet werden können.

Das SDK bietet beispielsweise interaktives Zoomen und Schwenken. Darüber hinaus erhalten Sie eine 360°-Ansicht und Videowiedergabe von Assets, die über die Backend-Anwendung Dynamic Media Classic in Adobe Dynamic Media hochgeladen wurden.

Obwohl die Komponenten auf HTML5-Funktionen basieren, sind sie für die Verwendung auf Android™- und Apple iOS-Geräten und Desktops, einschließlich Internet Explorer und höher, ausgelegt. Diese Art von Erlebnis bedeutet, dass Sie einen einzigen Workflow für alle unterstützten Plattformen bereitstellen können.

Das SDK besteht aus UI-Komponenten, aus denen Viewer-Inhalte bestehen. Sie können diese Komponenten über CSS gestalten und nicht über Benutzeroberflächen-Komponenten verfügen, die eine unterstützende Rolle haben, z. B. Abrufen und Analysieren von Set-Definitionen oder Tracking. Alle Verhaltensweisen von Komponenten können mithilfe von Modifikatoren angepasst werden, die Sie auf verschiedene Weise festlegen können, z. B. `name=value` Paare in der URL.

Dieses Tutorial enthält die folgende Reihenfolge von Aufgaben, mit denen Sie einen einfachen Zoom-Viewer erstellen können:

* [Herunterladen des neuesten Viewer-SDK aus Adobe Developer Connection](c-tutorial.md#section-84dc74c9d8e24a2380b6cf8fc28d7127)
* [Laden des Viewer-SDK](c-tutorial.md#section-98596c276faf4cf79ccf558a9f4432c6)
* [Hinzufügen von Stilen zum Viewer](c-tutorial.md#section-3783125360a1425eae5a5a334867cc32)
* [Einschließen von Container und ZoomView](c-tutorial.md#section-1a01730663154a508b88cc40c6f35539)
* [Hinzufügen von MediaSet- und Farbfeldkomponenten zum Viewer](c-tutorial.md#section-02b8c21dd842400e83eae2a48ec265b7)
* [Hinzufügen von Schaltflächen zum Viewer](c-tutorial.md#section-1fc334fa0d2b47eb9cdad461725c07be)
* [Vertikale Konfiguration der Farbfelder](c-tutorial.md#section-91a8829d5b5a4d45a35b7faeb097fcc9)

## Herunterladen des neuesten Viewer-SDK aus Adobe Developer Connection {#section-84dc74c9d8e24a2380b6cf8fc28d7127}

1. Herunterladen des neuesten Viewer-SDK aus Adobe Developer Connection <!-- SDK NO LONGER AVAILABLE TO DOWNLOAD;DOUBLE CHECK WITH AMIT. THIS ENTIRE TOPIC IS LIKELY OBSOLETE. [here](https://marketing.adobe.com/developer/devcenter/scene7/show) -->.

   >[!NOTE]
   >
   >Sie können dieses Tutorial abschließen, ohne das Viewer-SDK-Paket herunterladen zu müssen, da das SDK remote geladen wird. Das Viewer-Paket enthält jedoch zusätzliche Beispiele und ein API-Referenzhandbuch, das Sie bei der Erstellung Ihrer eigenen Viewer unterstützen kann.

## Laden des Viewer-SDK {#section-98596c276faf4cf79ccf558a9f4432c6}

1. Richten Sie zunächst eine neue Seite ein, um den einfachen Zoom-Viewer zu entwickeln, den Sie erstellen werden.

   Betrachten Sie diese neue Seite mit dem Bootstrap- oder Lader-Code, den Sie zum Einrichten einer leeren SDK-Anwendung verwenden. Öffnen Sie Ihren bevorzugten Texteditor und fügen Sie das folgende HTML-Markup ein:

   ```html {.line-numbers}
   <!DOCTYPE html> 
   <html> 
       <head> 
           <meta http-equiv="Content-Type" content="text/html; charset=utf-8" /> 
           <meta name="viewport" content="user-scalable=no, height=device-height, width=device-width, initial-scale=1.0, maximum-scale=1.0"/> 
   
           <!-- Hiding the Safari on iPhone OS UI components --> 
           <meta name="apple-mobile-web-app-capable" content="yes"/> 
           <meta name="apple-mobile-web-app-status-bar-style" content="black"/> 
           <meta name="apple-touch-fullscreen" content="no"/> 
   
           <title>Custom Viewer</title> 
   
           <!-- 
               Include Utils.js before you use any of the SDK components. This file  
               contains SDK utilities and global functions that are used to initialize the viewer and load viewer  
               components. The path to the Utils.js determines which version of the SDK that the viewer uses. You  
               can use a relative path if the viewer is deployed on one of the Adobe Dynamic Media servers and it is served  
               from the same domain. Otherwise, specify a full path to one of Adobe Dynamic Media servers that have the SDK  
               installed.  
           --> 
           <script language="javascript" type="text/javascript"      
                   src="http://s7d1.scene7.com/s7sdk/2.8/js/s7sdk/utils/Utils.js"></script> 
   
       </head> 
       <body> 
           <script language="javascript" type="text/javascript"> 
           </script>  
       </body> 
   </html>
   ```

   Fügen Sie den folgenden JavaScript-Code innerhalb der `script` -Tag, damit es die `ParameterManager`. Auf diese Weise können Sie sich auf die Erstellung und Instanziierung von SDK-Komponenten im `initViewer` Funktion:

   ```javascript {.line-numbers}
   /* We create a self-running anonymous function to encapsulate variable scope. Placing code inside such 
      a function is optional, but this prevents variables from polluting the global object.  */ 
   (function () { 
   
       // Initialize the SDK   
       s7sdk.Util.init(); 
   
       /* Create an instance of the ParameterManager component to collect components' configuration 
          that can come from a viewer preset, URL, or the HTML page itself. The ParameterManager  
          component also sends a notification s7sdk.Event.SDK_READY when all needed files are loaded 
          and the configuration parameters are processed. The other components should never be initialized 
          outside this handler. After defining the handler for the s7sdk.Event.SDK_READY event, it 
          is safe to initiate configuration initialization by calling ParameterManager.init(). */ 
       var params = new s7sdk.ParameterManager(); 
   
       /* Event handler for s7sdk.Event.SDK_READY dispatched by ParameterManager to initialize various components of  
          this viewer. */ 
       function initViewer() { 
   
       }  
   
       /* Add event handler for the s7sdk.Event.SDK_READY event dispatched by the ParameterManager when all modifiers 
          are processed and it is safe to initialize the viewer. */ 
       params.addEventListener(s7sdk.Event.SDK_READY, initViewer, false); 
   
       /* Initiate configuration initialization of ParameterManager. */ 
       params.init(); 
   
   }());
   ```

1. Speichern Sie die Datei als leere Vorlage. Sie können jeden gewünschten Dateinamen verwenden.

   Sie werden diese leere Vorlagendatei als Referenz verwenden, wenn Sie in Zukunft Viewer erstellen. Diese Vorlage funktioniert lokal und wenn sie von einem Webserver bereitgestellt wird.

Fügen Sie Ihrem Viewer jetzt Stil hinzu.

## Hinzufügen von Stilen zum Viewer {#section-3783125360a1425eae5a5a334867cc32}

1. Für diesen vollständigen Seiten-Viewer, den Sie erstellen, können Sie einige grundlegende Stile hinzufügen.

   Fügen Sie Folgendes hinzu: `style` -Block am unteren Rand des `head`:

   ```html {.line-numbers}
   <style> 
       html, body { 
           width: 100%; 
           height: 100%; 
       } 
       body { 
           /* Remove any padding and margin around the edges of the browser window */ 
           padding: 0; 
           margin: 0; 
   
           /* We set overflow to hidden so that scroll bars do not flicker when resizing the window */ 
           overflow: hidden; 
       } 
   </style>
   ```

Schließen Sie nun die Komponenten ein `Container` und `ZoomView`.

## Einschließen von Container und ZoomView {#section-1a01730663154a508b88cc40c6f35539}

1. Erstellen eines tatsächlichen Viewers durch Einschließen der Komponenten `Container` und `ZoomView`.

   Fügen Sie Folgendes ein: `include` -Anweisungen am Ende der `<head>` element - nach dem [!DNL Utils.js] Skript geladen wird:

   ```javascript {.line-numbers}
   <!-- 
       Add an "include" statement with a related module for each component that is needed for that particular  
       viewer. Check API documentation to see a complete list of components and their modules. 
   --> 
   <script language="javascript" type="text/javascript"> 
       s7sdk.Util.lib.include('s7sdk.common.Container');  
       s7sdk.Util.lib.include('s7sdk.image.ZoomView');  
   </script>
   ```

1. Erstellen Sie jetzt Variablen, um auf die verschiedenen SDK-Komponenten zu verweisen.

   Fügen Sie oben in der anonymen Hauptfunktion die folgenden Variablen hinzu: `s7sdk.Util.init()`:

   ```javascript {.line-numbers}
   var container, zoomView;
   ```

1. Fügen Sie Folgendes in die `initViewer` -Funktion, damit Sie einige Modifikatoren definieren und die entsprechenden Komponenten instanziieren können:

   ```javascript {.line-numbers}
   /* Modifiers can be added directly to ParameterManager instance */ 
   params.push("serverurl", "http://s7d1.scene7.com/is/image"); 
   params.push("asset", "Scene7SharedAssets/ImageSet-Views-Sample"); 
   
   /* Create a viewer container as a parent component for other user interface components that  
      are part of the viewer application and associate event handlers for resize and  
      full screen notification. The advantage of using Container as the parent is the  
      component's ability to resize and bring itself and its children to full screen. */ 
   container = new s7sdk.common.Container(null, params, "s7container"); 
   container.addEventListener(s7sdk.event.ResizeEvent.COMPONENT_RESIZE, containerResize, false); 
   
   /* Create ZoomView component */ 
   zoomView = new s7sdk.image.ZoomView("s7container", params, "myZoomView");  
   
   /* We call this to ensure all SDK components are scaled to initial conditions when viewer loads */ 
   resizeViewer(container.getWidth(), container.getHeight());
   ```

1. Damit der obige Code ordnungsgemäß ausgeführt werden kann, fügen Sie einen `containerResize` Ereignishandler und eine Hilfsfunktion:

   ```javascript {.line-numbers}
   /* Event handler for s7sdk.event.ResizeEvent.COMPONENT_RESIZE events dispatched by Container to resize 
      various view components included in this viewer. */ 
   function containerResize(event) { 
       resizeViewer(event.s7event.w, event.s7event.h); 
   } 
   
   /* Resize viewer components */ 
   function resizeViewer(width, height) { 
       zoomView.resize(width, height); 
   }
   ```

1. Zeigen Sie eine Vorschau der Seite an, damit Sie sehen können, was Sie erstellt haben. Ihre Seite sollte wie folgt aussehen:

   ![Beispiel für ein Bild](assets/viewer-1.jpg)

Fügen Sie nun die Komponenten hinzu `MediaSet` und `Swatches` an Ihren Viewer.

## Hinzufügen von MediaSet- und Farbfeldkomponenten zum Viewer {#section-02b8c21dd842400e83eae2a48ec265b7}

1. Um Benutzern die Möglichkeit zu geben, Bilder aus einem Set auszuwählen, können Sie die Komponenten hinzufügen `MediaSet` und `Swatches`.

   Fügen Sie das folgende SDK hinzu:

   ```javascript {.line-numbers}
   s7sdk.Util.lib.include('s7sdk.set.MediaSet'); 
   s7sdk.Util.lib.include('s7sdk.set.Swatches');
   ```

1. Aktualisieren Sie die Variablenliste mit folgendem Code:

   ```javascript {.line-numbers}
   var mediaSet, container, zoomView, swatches;
   ```

1. Instanziieren `MediaSet` und `Swatches` Komponenten innerhalb der `initViewer` -Funktion.

   Instanziieren Sie unbedingt die `Swatches` -Instanz nach der `ZoomView` und `Container` Komponenten, andernfalls wird die Stapelreihenfolge `Swatches`:

   ```javascript {.line-numbers}
   // Create MediaSet to manage assets and add event listener to the NOTF_SET_PARSED event 
   mediaSet = new s7sdk.set.MediaSet(null, params, "mediaSet"); 
   
   // Add MediaSet event listener 
   mediaSet.addEventListener(s7sdk.event.AssetEvent.NOTF_SET_PARSED, onSetParsed, false); 
   
   /* create Swatches component and associate event handler for swatch selection notification */ 
   swatches = new s7sdk.set.Swatches("s7container", params, "mySwatches");   
   swatches.addEventListener(s7sdk.event.AssetEvent.SWATCH_SELECTED_EVENT, swatchSelected, false);
   ```

1. Fügen Sie nun die folgenden Ereignis-Handler-Funktionen hinzu:

   ```javascript {.line-numbers}
   /* Event handler for the s7sdk.event.AssetEvent.NOTF_SET_PARSED event dispatched by MediaSet to 
      assign the asset to the Swatches when parsing is complete. */ 
   function onSetParsed(e) { 
   
       // set media set for Swatches to display  
       var mediasetDesc = e.s7event.asset;  
       swatches.setMediaSet(mediasetDesc); 
   
       // select the first swatch by default  
       swatches.selectSwatch(0, true);      
   } 
   
   /* Event handler for s7sdk.event.AssetEvent.SWATCH_SELECTED_EVENT events dispatched by Swatches to switch 
      the image in the ZoomView when a different swatch is selected. */ 
   function swatchSelected(event) {     
       zoomView.setItem(event.s7event.asset);  
   }
   ```

1. Positionieren Sie die Farbfelder am unteren Rand des Viewers, indem Sie dem `style` element:

   ```CSS {.line-numbers}
   /* Align swatches to bottom of viewer */ 
   .s7swatches { 
       bottom: 0; 
       left: 0; 
       right: 0; 
       height: 150px; 
   }
   ```

1. Vorschau des Viewers

   Beachten Sie, dass sich die Farbfelder unten links im Viewer befinden. Damit die Farbfelder die gesamte Viewer-Breite annehmen, fügen Sie einen Aufruf hinzu, um die Größe der Farbfelder manuell zu ändern, sobald der Benutzer die Größe seines Browsers ändert. Fügen Sie Folgendes zum `resizeViewer` Funktion:

   ```javascript {.line-numbers}
   swatches.resize(width, swatches.getHeight());
   ```

   Ihr Viewer sieht nun wie das folgende Bild aus. Versuchen Sie, die Größe des Browser-Fensters des Viewers zu ändern, und beachten Sie das daraus resultierende Verhalten.

   ![Beispiel für zwei Bilder im Viewer](assets/viewer-2.jpg)

Fügen Sie Ihrem Viewer jetzt Schaltflächen zum Vergrößern, Verkleinern und Zurücksetzen des Zooms hinzu.

## Hinzufügen von Schaltflächen zum Viewer {#section-1fc334fa0d2b47eb9cdad461725c07be}

1. Derzeit kann der Benutzer nur mit Klick- oder Berührungsgesten zoomen. Fügen Sie daher einige einfache Zoom-Steuerelement-Schaltflächen zum Viewer hinzu.

   Fügen Sie die folgenden Schaltflächenkomponenten hinzu:

   ```CSS {.line-numbers}
   s7sdk.Util.lib.include('s7sdk.common.Button');
   ```

1. Aktualisieren Sie die Variablenliste mit folgendem Code:

   ```javascript {.line-numbers}
   var mediaSet, container, zoomView, swatches, zoomInButton, zoomOutButton, zoomResetButton;
   ```

1. Schaltflächen unten instanziieren `initViewer` -Funktion.

   Beachten Sie, dass die Reihenfolge wichtig ist, es sei denn, Sie geben die `z-index` in CSS:

   ```CSS {.line-numbers}
   /* Create Zoom In, Zoom Out and Zoom Reset buttons */ 
   zoomInButton  = new s7sdk.common.ZoomInButton("s7container", params, "zoomInBtn"); 
   zoomOutButton = new s7sdk.common.ZoomOutButton("s7container", params, "zoomOutBtn"); 
   zoomResetButton = new s7sdk.common.ZoomResetButton("s7container", params, "zoomResetBtn"); 
   
   /* Add handlers for zoom in, zoom out and zoom reset buttons inline. */ 
   zoomInButton.addEventListener("click", function() { zoomView.zoomIn(); }); 
   zoomOutButton.addEventListener("click", function() { zoomView.zoomOut(); }); 
   zoomResetButton.addEventListener("click", function() { zoomView.zoomReset(); });
   ```

1. Definieren Sie nun einige grundlegende Stile für die Schaltflächen, indem Sie Folgendes zum `style` -Block oben in Ihrer -Datei:

   ```CSS {.line-numbers}
   /* define styles common to all button components and their sub-classes */ 
   .s7button { 
       position:absolute; 
       width: 28px; 
       height: 28px; 
       z-index:100; 
   } 
   
   /* position individual buttons*/ 
   .s7zoominbutton  { 
       top: 50px; 
       left: 50px; 
    } 
   .s7zoomoutbutton  { 
       top: 50px; 
       left: 80px; 
    } 
   .s7zoomresetbutton  { 
       top: 50px; 
       left: 110px; 
    }
   ```

1. Vorschau des Viewers Sie sollte wie folgt aussehen:

   ![Beispiel für drei Bilder](assets/viewer-3.jpg)

   Konfigurieren Sie nun die Farbfelder so, dass sie vertikal auf der rechten Seite ausgerichtet sind.

## Vertikale Konfiguration der Farbfelder {#section-91a8829d5b5a4d45a35b7faeb097fcc9}

1. Sie können Modifikatoren direkt im `ParameterManager` -Instanz.

   Fügen Sie oben im `initViewer` -Funktion, damit Sie die `Swatches` Miniaturlayout als einzelne Zeile:

   ```javascript {.line-numbers}
   params.push("Swatches.tmblayout", "1,0");
   ```

1. Aktualisieren Sie den folgenden Größenaufruf in `resizeViewer`:

   ```javascript {.line-numbers}
   swatches.resize(swatches.getWidth(), height);
   ```

1. Bearbeiten Sie Folgendes `s7swatches` Regel in `ZoomViewer.css`:

   ```CSS {.line-numbers}
   .s7swatches { 
       top:0 ; 
       bottom: 0; 
       right: 0; 
       width: 150px; 
   }
   ```

1. Vorschau des Viewers Es sieht wie folgt aus:

   ![Viewer-Beispiel: Vier Bild](assets/viewer-4.jpg)

   Ihr einfacher Zoom-Viewer ist jetzt fertig.

   Dieses Viewer-Tutorial behandelt die Grundlagen dessen, was das Dynamic Media Viewer SDK bietet. Bei der Arbeit mit dem SDK können Sie die verschiedenen Standardkomponenten verwenden, um mühelos Rich-View-Erlebnisse für Ihre Zielgruppen zu erstellen und zu gestalten.
