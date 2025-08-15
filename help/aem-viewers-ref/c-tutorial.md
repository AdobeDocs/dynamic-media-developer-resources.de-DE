---
title: Viewer-Tutorial zu SDK
description: Der SDK-Viewer bietet eine Reihe von JavaScript-basierten Komponenten für die Entwicklung benutzerdefinierter Viewer. Die Viewer sind Web-basierte Programme, mit denen Rich-Media-Inhalte, die von Adobe Dynamic Media bereitgestellt werden, in Web-Seiten eingebettet werden können.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API
role: Developer,User
exl-id: 3a798595-6c65-4a12-983d-3cdc53830d28
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '971'
ht-degree: 0%

---

# Viewer-Tutorial zu SDK{#viewer-sdk-tutorial}

Der SDK-Viewer bietet eine Reihe von JavaScript-basierten Komponenten für die Entwicklung benutzerdefinierter Viewer. Die Viewer sind Web-basierte Programme, mit denen Rich-Media-Inhalte, die von Adobe Dynamic Media bereitgestellt werden, in Web-Seiten eingebettet werden können.

Beispielsweise bietet der SDK interaktives Zoomen und Schwenken. Es bietet außerdem eine 360-Grad-Ansicht und Videowiedergabe von Assets, die über das Backend-Programm namens Dynamic Media Classic in Adobe Dynamic Media hochgeladen wurden.

Obwohl die Komponenten auf HTML5-Funktionen angewiesen sind, sind sie für die Verwendung auf Android™- und Apple iOS-Geräten und -Desktops konzipiert, einschließlich Internet Explorer und höher. Diese Art von Erlebnis bedeutet, dass Sie in der Lage sind, einen einzigen Workflow für alle unterstützten Plattformen bereitzustellen.

SDK besteht aus Benutzeroberflächenkomponenten, aus denen Viewer-Inhalte bestehen. Sie können diese Komponenten durch CSS formatieren, und Nicht-UI-Komponenten, die eine Art unterstützende Rolle haben, z. B. Abrufen von Set-Definitionen und Analysieren oder Tracking. Alle Komponentenverhaltensweisen können über Modifikatoren angepasst werden, die Sie auf verschiedene Weise angeben können, z. B. als `name=value` in der URL.

Dieses Tutorial enthält die folgende Reihenfolge von Aufgaben, um einen einfachen Zoom-Viewer zu erstellen:

* [Laden Sie die neueste Viewer-SDK von Adobe Developer Connection herunter](c-tutorial.md#section-84dc74c9d8e24a2380b6cf8fc28d7127)
* [Laden Sie die Viewer-SDK](c-tutorial.md#section-98596c276faf4cf79ccf558a9f4432c6)
* [Hinzufügen eines Stils zu Ihrem Viewer](c-tutorial.md#section-3783125360a1425eae5a5a334867cc32)
* [einschließlich Container und ZoomView](c-tutorial.md#section-1a01730663154a508b88cc40c6f35539)
* [Hinzufügen von MediaSet- und Farbfeld-Komponenten zum Viewer](c-tutorial.md#section-02b8c21dd842400e83eae2a48ec265b7)
* [Hinzufügen von Schaltflächen zu einem Viewer](c-tutorial.md#section-1fc334fa0d2b47eb9cdad461725c07be)
* [Vertikales Konfigurieren der Farbfelder](c-tutorial.md#section-91a8829d5b5a4d45a35b7faeb097fcc9)

## Laden Sie die neueste Viewer-SDK von Adobe Developer Connection herunter {#section-84dc74c9d8e24a2380b6cf8fc28d7127}

1. Laden Sie die neueste Viewer-SDK von Adobe Developer Connection <!-- SDK NO LONGER AVAILABLE TO DOWNLOAD;DOUBLE CHECK WITH AMIT. THIS ENTIRE TOPIC IS LIKELY OBSOLETE. [here](https://marketing.adobe.com/developer/devcenter/scene7/show) --> herunter.

   >[!NOTE]
   >
   >Sie können dieses Tutorial abschließen, ohne das Viewer-SDK-Paket herunterladen zu müssen, da die SDK remote geladen wird. Das Viewer-Paket enthält jedoch zusätzliche Beispiele und ein API-Referenzhandbuch, das Sie bei der Erstellung Ihrer eigenen Viewer unterstützen kann.

## Laden des Viewer-SDK {#section-98596c276faf4cf79ccf558a9f4432c6}

1. Richten Sie zunächst eine neue Seite ein, um den grundlegenden Zoom-Viewer zu entwickeln, den Sie erstellen möchten.

   Betrachten Sie diese neue Seite, den Bootstrap- oder Loader-Code, den Sie zum Einrichten einer leeren SDK-Anwendung verwenden. Öffnen Sie Ihren bevorzugten Texteditor und fügen Sie das folgende HTML-Markup ein:

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

   Fügen Sie den folgenden JavaScript-Code innerhalb des `script`-Tags hinzu, damit die `ParameterManager` initialisiert wird. Auf diese Weise können Sie SDK-Komponenten innerhalb der `initViewer` erstellen und instanziieren:

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

1. Speichern Sie die Datei als leere Vorlage. Sie können einen beliebigen Dateinamen verwenden.

   Sie können diese leere Vorlagendatei als Referenz verwenden, wenn Sie zukünftig Viewer erstellen. Diese Vorlage funktioniert lokal und bei Bereitstellung von einem Webserver.

Fügen Sie nun Ihrem Viewer einen Stil hinzu.

## Stil zum Viewer hinzufügen {#section-3783125360a1425eae5a5a334867cc32}

1. Für diesen kompletten Seiten-Viewer, den Sie erstellen, können Sie einige grundlegende Stile hinzufügen.

   Fügen Sie den folgenden `style` am unteren Rand der `head` hinzu:

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

Schließen Sie nun die Komponenten `Container` und `ZoomView` ein.

## Container und ZoomView einschließen {#section-1a01730663154a508b88cc40c6f35539}

1. Erstellen Sie einen tatsächlichen Viewer, indem Sie die Komponenten `Container` und `ZoomView` einbeziehen.

   Fügen Sie die folgenden `include`-Anweisungen am unteren Rand des `<head>` ein, nachdem das [!DNL Utils.js]-Skript geladen wurde:

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

1. Erstellen Sie jetzt Variablen, die auf die verschiedenen SDK-Komponenten verweisen.

   Fügen Sie die folgenden Variablen oben in der anonymen Hauptfunktion direkt über `s7sdk.Util.init()` hinzu:

   ```javascript {.line-numbers}
   var container, zoomView;
   ```

1. Fügen Sie Folgendes in die `initViewer` ein, damit Sie einige Modifikatoren definieren und die entsprechenden Komponenten instanziieren können:

   ```javascript {.line-numbers}
   /* Modifiers can be added directly to ParameterManager instance */ 
   params.push("serverurl", "http://s7d1.scene7.com/is/image"); 
   params.push("asset", "Scene7SharedAssets/ImageSet-Views-Sample"); 
   
   /* Create a viewer container as a parent component for other user interface components that  
      are part of the viewer application and associate event handlers for resize and  
      full-screen notification. The advantage of using Container as the parent is the  
      component's ability to resize and bring itself and its children to full-screen. */ 
   container = new s7sdk.common.Container(null, params, "s7container"); 
   container.addEventListener(s7sdk.event.ResizeEvent.COMPONENT_RESIZE, containerResize, false); 
   
   /* Create ZoomView component */ 
   zoomView = new s7sdk.image.ZoomView("s7container", params, "myZoomView");  
   
   /* We call this to ensure all SDK components are scaled to initial conditions when viewer loads */ 
   resizeViewer(container.getWidth(), container.getHeight());
   ```

1. Damit der obige Code ordnungsgemäß ausgeführt wird, fügen Sie einen `containerResize` Ereignishandler und eine Hilfsfunktion hinzu:

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

   ![Viewer-Beispiel - ein Bild](assets/viewer-1.jpg)

Fügen Sie nun die Komponenten `MediaSet` und `Swatches` zu Ihrem Viewer hinzu.

## Hinzufügen von MediaSet- und Farbfeld-Komponenten zum Viewer {#section-02b8c21dd842400e83eae2a48ec265b7}

1. Damit Benutzerinnen und Benutzer Bilder aus einem Set auswählen können, können Sie die Komponenten `MediaSet` und `Swatches` hinzufügen.

   Fügen Sie die folgenden SDK hinzu:

   ```javascript {.line-numbers}
   s7sdk.Util.lib.include('s7sdk.set.MediaSet'); 
   s7sdk.Util.lib.include('s7sdk.set.Swatches');
   ```

1. Aktualisieren Sie die Variablenliste wie folgt:

   ```javascript {.line-numbers}
   var mediaSet, container, zoomView, swatches;
   ```

1. Instanziieren Sie `MediaSet`- und `Swatches` innerhalb der `initViewer`.

   Stellen Sie sicher, dass Sie die `Swatches`-Instanz nach den Komponenten `ZoomView` und `Container` instanziieren, da andernfalls die `Swatches` durch die Stapelreihenfolge ausgeblendet wird:

   ```javascript {.line-numbers}
   // Create MediaSet to manage assets and add event listener to the NOTF_SET_PARSED event 
   mediaSet = new s7sdk.set.MediaSet(null, params, "mediaSet"); 
   
   // Add MediaSet event listener 
   mediaSet.addEventListener(s7sdk.event.AssetEvent.NOTF_SET_PARSED, onSetParsed, false); 
   
   /* create Swatches component and associate event handler for swatch selection notification */ 
   swatches = new s7sdk.set.Swatches("s7container", params, "mySwatches");   
   swatches.addEventListener(s7sdk.event.AssetEvent.SWATCH_SELECTED_EVENT, swatchSelected, false);
   ```

1. Fügen Sie nun die folgenden Ereignishandlerfunktionen hinzu:

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

1. Positionieren Sie die Farbfelder am unteren Rand des Viewers, indem Sie das folgende CSS zum `style` Element hinzufügen:

   ```CSS {.line-numbers}
   /* Align swatches to bottom of viewer */ 
   .s7swatches { 
       bottom: 0; 
       left: 0; 
       right: 0; 
       height: 150px; 
   }
   ```

1. Vorschau des Viewers anzeigen.

   Beachten Sie, dass sich die Farbfelder unten links im Viewer befinden. Damit die Farbfelder die gesamte Viewer-Breite einnehmen, fügen Sie einen Aufruf hinzu, um die Größe der Farbfelder manuell zu ändern, sobald der Browser der Benutzerin oder des Benutzers die Größe ändert. Fügen Sie der Funktion `resizeViewer` Folgendes hinzu:

   ```javascript {.line-numbers}
   swatches.resize(width, swatches.getHeight());
   ```

   Ihr Viewer sieht jetzt wie die folgende Abbildung aus. Versuchen Sie, die Größe des Browser-Fensters des Viewers zu ändern, und beachten Sie das daraus resultierende Verhalten.

   ![Viewer-Beispiel: zwei Bilder](assets/viewer-2.jpg)

Fügen Sie jetzt die Schaltflächen „Einzoomen“, „Auszoomen“ und „Zurücksetzen des Zooms“ zu Ihrem Viewer hinzu.

## Hinzufügen von Schaltflächen zu einem Viewer {#section-1fc334fa0d2b47eb9cdad461725c07be}

1. Derzeit kann der/die Benutzende nur mithilfe von Klick- oder Touch-Gesten zoomen. Fügen Sie daher einige grundlegende Zoom-Schaltflächen zum Viewer hinzu.

   Fügen Sie die folgenden Schaltflächenkomponenten hinzu:

   ```CSS {.line-numbers}
   s7sdk.Util.lib.include('s7sdk.common.Button');
   ```

1. Aktualisieren Sie die Variablenliste wie folgt:

   ```javascript {.line-numbers}
   var mediaSet, container, zoomView, swatches, zoomInButton, zoomOutButton, zoomResetButton;
   ```

1. Instanziieren Sie Schaltflächen am unteren Rand `initViewer` Funktion.

   Beachten Sie, dass die Reihenfolge wichtig ist, es sei denn, Sie geben die `z-index` in CSS an:

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

1. Definieren Sie nun einige grundlegende Stile für die Schaltflächen, indem Sie dem `style`-Block oben in Ihrer Datei Folgendes hinzufügen:

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

1. Vorschau des Viewers anzeigen. Sie sollte wie folgt aussehen:

   ![Viewer-Beispiel: drei Bilder](assets/viewer-3.jpg)

   Konfigurieren Sie nun die Farbfelder so, dass sie vertikal auf der rechten Seite ausgerichtet sind.

## Vertikales Konfigurieren der Farbfelder {#section-91a8829d5b5a4d45a35b7faeb097fcc9}

1. Sie können Modifikatoren direkt in der `ParameterManager` konfigurieren.

   Fügen Sie Folgendes oben in der `initViewer` hinzu, damit Sie das `Swatches`-Miniatur-Layout als einzelne Zeile konfigurieren können:

   ```javascript {.line-numbers}
   params.push("Swatches.tmblayout", "1,0");
   ```

1. Aktualisieren Sie den folgenden Größenänderungsaufruf in `resizeViewer`:

   ```javascript {.line-numbers}
   swatches.resize(swatches.getWidth(), height);
   ```

1. Bearbeiten Sie die folgende `s7swatches` in `ZoomViewer.css`:

   ```CSS {.line-numbers}
   .s7swatches { 
       top:0 ; 
       bottom: 0; 
       right: 0; 
       width: 150px; 
   }
   ```

1. Vorschau des Viewers anzeigen. Sie sieht wie folgt aus:

   ![Viewer-Beispiel, vier Bild](assets/viewer-4.jpg)

   Ihr einfacher Zoom-Viewer ist jetzt abgeschlossen.

   Dieses Viewer-Tutorial berührt die Grundlagen von Dynamic Media Viewer, die SDK bereitstellt. Bei der Arbeit mit SDK können Sie die verschiedenen Standardkomponenten verwenden, um einfach umfassende Anzeigeerlebnisse für Ihre Zielgruppen zu erstellen und zu gestalten.
