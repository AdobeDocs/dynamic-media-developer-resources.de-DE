---
description: Das Viewer-SDK bietet eine Reihe JavaScript-basierter Komponenten für die benutzerdefinierte Viewer-Entwicklung. Die Viewer sind webbasierte Anwendungen, mit denen von Adobe Dynamic Media bereitgestellte Rich-Media-Inhalte in Webseiten eingebettet werden können.
solution: Experience Manager
title: Viewer-SDK-Tutorial
feature: Dynamic Media Classic,Viewers,SDK/API
role: Developer,User
exl-id: 3a798595-6c65-4a12-983d-3cdc53830d28
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '964'
ht-degree: 0%

---

# Viewer-SDK-Tutorial{#viewer-sdk-tutorial}

Das Viewer-SDK bietet eine Reihe JavaScript-basierter Komponenten für die benutzerdefinierte Viewer-Entwicklung. Die Viewer sind webbasierte Anwendungen, mit denen von Adobe Dynamic Media bereitgestellte Rich-Media-Inhalte in Webseiten eingebettet werden können.

Das SDK bietet beispielsweise interaktives Zoomen und Schwenken. Darüber hinaus erhalten Sie eine 360°-Ansicht und Videowiedergabe von Assets, die über die Backend-Anwendung Dynamic Media Classic in Adobe Dynamic Media hochgeladen wurden.

Obwohl die Komponenten auf HTML5-Funktionen basieren, sind sie für die Verwendung auf iOS-Geräten von Android und Apple sowie Desktops, einschließlich Internet Explorer und höher, entwickelt worden. Diese Art von Erlebnis bedeutet, dass Sie einen einzigen Workflow für alle unterstützten Plattformen bereitstellen können.

Das SDK besteht aus UI-Komponenten, aus denen Viewer-Inhalte bestehen. Sie können diese Komponenten über CSS gestalten und nicht über Benutzeroberflächen-Komponenten verfügen, die eine unterstützende Rolle haben, z. B. Abrufen und Analysieren von Set-Definitionen oder Tracking. Das Verhalten aller Komponenten kann mithilfe von Modifikatoren angepasst werden, die Sie auf verschiedene Weise angeben können, z. B. als `name=value`-Paare in der URL.

Dieses Tutorial enthält die folgende Reihenfolge von Aufgaben, mit denen Sie einen einfachen Zoom-Viewer erstellen können:

* [Herunterladen des neuesten Viewer-SDK aus Adobe Developer Connection](c-tutorial.md#section-84dc74c9d8e24a2380b6cf8fc28d7127)
* [Laden des Viewer-SDK](c-tutorial.md#section-98596c276faf4cf79ccf558a9f4432c6)
* [Hinzufügen von Stilen zum Viewer](c-tutorial.md#section-3783125360a1425eae5a5a334867cc32)
* [Einschließen von Container und ZoomView](c-tutorial.md#section-1a01730663154a508b88cc40c6f35539)
* [Hinzufügen von MediaSet- und Farbfeldkomponenten zum Viewer](c-tutorial.md#section-02b8c21dd842400e83eae2a48ec265b7)
* [Hinzufügen von Schaltflächen zum Viewer](c-tutorial.md#section-1fc334fa0d2b47eb9cdad461725c07be)
* [Vertikale Konfiguration der Farbfelder](c-tutorial.md#section-91a8829d5b5a4d45a35b7faeb097fcc9)

## Herunterladen des neuesten Viewer-SDK aus Adobe Developer Connection {#section-84dc74c9d8e24a2380b6cf8fc28d7127}

1. Laden Sie das neueste Viewer-SDK von Adobe Developer Connection herunter <!-- SDK NO LONGER AVAILABLE TO DOWNLOAD;DOUBLE CHECK WITH AMIT. THIS ENTIRE TOPIC IS LIKELY OBSOLETE. [here](https://marketing.adobe.com/developer/devcenter/scene7/show) -->.

   >[!NOTE]
   >
   >Sie können dieses Tutorial abschließen, ohne das Viewer-SDK-Paket herunterladen zu müssen, da das SDK tatsächlich remote geladen wird. Das Viewer-Paket enthält jedoch zusätzliche Beispiele und ein API-Referenzhandbuch, das Sie beim Erstellen Ihrer eigenen Viewer als hilfreich finden.

## Laden des Viewer-SDK {#section-98596c276faf4cf79ccf558a9f4432c6}

1. Richten Sie zunächst eine neue Seite ein, um den einfachen Zoom-Viewer zu entwickeln, den Sie erstellen werden.

   Betrachten Sie diesen Bootstrap- oder loader -Code, um eine leere SDK-Anwendung einzurichten. Öffnen Sie Ihren bevorzugten Texteditor und fügen Sie das folgende HTML-Markup ein:

   ```
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

   Fügen Sie den folgenden JavaScript-Code innerhalb des Tags `script` hinzu, um den `ParameterManager` zu initialisieren. Auf diese Weise können Sie die Erstellung und Instanziierung von SDK-Komponenten innerhalb der Funktion `initViewer` vorbereiten:

   ```
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

   Sie werden diese leere Vorlagendatei als Referenz verwenden, wenn Sie in Zukunft neue Viewer erstellen. Diese Vorlage funktioniert lokal und wenn sie von einem Webserver bereitgestellt wird.

Sie fügen Ihrem Viewer jetzt Stil hinzu.

## Hinzufügen von Stilen zum Viewer {#section-3783125360a1425eae5a5a334867cc32}

1. Für diesen vollständigen Seiten-Viewer, den Sie erstellen, können Sie einige grundlegende Stile hinzufügen.

   Fügen Sie den folgenden `style`-Block am unteren Rand von `head` hinzu:

   ```
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

Sie werden nun die Komponenten `Container` und `ZoomView` einschließen.

## Einschließen von Container und ZoomView {#section-1a01730663154a508b88cc40c6f35539}

1. Erstellen Sie einen tatsächlichen Viewer, indem Sie die Komponenten `Container` und `ZoomView` einfügen.

   Fügen Sie die folgenden `include`-Anweisungen am unteren Rand des Elements `<head>` ein - nachdem das Skript [!DNL Utils.js] geladen wurde:

   ```
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

   Fügen Sie die folgenden Variablen oben in der anonymen Hauptfunktion hinzu, direkt über `s7sdk.Util.init()`:

   ```
   var container, zoomView;
   ```

1. Fügen Sie Folgendes in die Funktion `initViewer` ein, um einige Modifikatoren zu definieren und die entsprechenden Komponenten zu instanziieren:

   ```
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

1. Damit der obige Code ordnungsgemäß ausgeführt werden kann, fügen Sie einen `containerResize`-Ereignishandler und eine Hilfsfunktion hinzu:

   ```
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

1. Zeigen Sie eine Vorschau der Seite an, damit Sie sehen können, was Sie erstellt haben. Ihre Seite sieht wie folgt aus:

   ![](assets/viewer-1.jpg)

Sie fügen nun die Komponenten `MediaSet` und `Swatches` zu Ihrem Viewer hinzu.

## Hinzufügen von MediaSet- und Farbfeldkomponenten zum Viewer {#section-02b8c21dd842400e83eae2a48ec265b7}

1. Um Benutzern die Möglichkeit zu geben, Bilder aus einem Set auszuwählen, können Sie die Komponenten `MediaSet` und `Swatches` hinzufügen.

   Fügen Sie das folgende SDK hinzu:

   ```
   s7sdk.Util.lib.include('s7sdk.set.MediaSet'); 
   s7sdk.Util.lib.include('s7sdk.set.Swatches');
   ```

1. Aktualisieren Sie die Variablenliste mit folgendem Code:

   ```
   var mediaSet, container, zoomView, swatches;
   ```

1. Instanziieren Sie die Komponenten `MediaSet` und `Swatches` innerhalb der Funktion `initViewer` .

   Stellen Sie sicher, dass Sie die `Swatches` -Instanz nach den Komponenten `ZoomView` und `Container` instanziieren. Andernfalls wird die `Swatches` durch die Stapelreihenfolge ausgeblendet:

   ```
   // Create MediaSet to manage assets and add event listener to the NOTF_SET_PARSED event 
   mediaSet = new s7sdk.set.MediaSet(null, params, "mediaSet"); 
   
   // Add MediaSet event listener 
   mediaSet.addEventListener(s7sdk.event.AssetEvent.NOTF_SET_PARSED, onSetParsed, false); 
   
   /* create Swatches component and associate event handler for swatch selection notification */ 
   swatches = new s7sdk.set.Swatches("s7container", params, "mySwatches");   
   swatches.addEventListener(s7sdk.event.AssetEvent.SWATCH_SELECTED_EVENT, swatchSelected, false);
   ```

1. Fügen Sie nun die folgenden Ereignis-Handler-Funktionen hinzu:

   ```
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

1. Positionieren Sie die Farbfelder am unteren Rand des Viewers, indem Sie dem Element `style` die folgende CSS hinzufügen:

   ```
   /* Align swatches to bottom of viewer */ 
   .s7swatches { 
       bottom: 0; 
       left: 0; 
       right: 0; 
       height: 150px; 
   }
   ```

1. Vorschau des Viewers

   Beachten Sie, dass sich die Farbfelder unten links im Viewer befinden. Damit die Farbfelder die gesamte Viewer-Breite annehmen, fügen Sie einen Aufruf hinzu, um die Größe der Farbfelder manuell zu ändern, sobald der Benutzer die Größe seines Browsers ändert. Fügen Sie der Funktion `resizeViewer` Folgendes hinzu:

   ```
   swatches.resize(width, swatches.getHeight());
   ```

   Ihr Viewer sieht nun wie das folgende Bild aus. Versuchen Sie, die Größe des Browser-Fensters des Viewers zu ändern, und beachten Sie das daraus resultierende Verhalten.

   ![](assets/viewer-2.jpg)

Sie fügen Ihrem Viewer jetzt Schaltflächen zum Vergrößern, Verkleinern und Zurücksetzen des Zooms hinzu.

## Hinzufügen von Schaltflächen zum Viewer {#section-1fc334fa0d2b47eb9cdad461725c07be}

1. Derzeit kann der Benutzer nur mit Klick- oder Berührungsgesten zoomen. Fügen Sie daher einige einfache Zoom-Steuerelement-Schaltflächen zum Viewer hinzu.

   Fügen Sie die folgenden Schaltflächenkomponenten hinzu:

   ```
   s7sdk.Util.lib.include('s7sdk.common.Button');
   ```

1. Aktualisieren Sie die Variablenliste mit folgendem Code:

   ```
   var mediaSet, container, zoomView, swatches, zoomInButton, zoomOutButton, zoomResetButton;
   ```

1. Schaltflächen am unteren Rand der Funktion `initViewer` instanziieren.

   Beachten Sie, dass die Reihenfolge wichtig ist, es sei denn, Sie geben die `z-index` in CSS an:

   ```
   /* Create Zoom In, Zoom Out and Zoom Reset buttons */ 
   zoomInButton  = new s7sdk.common.ZoomInButton("s7container", params, "zoomInBtn"); 
   zoomOutButton = new s7sdk.common.ZoomOutButton("s7container", params, "zoomOutBtn"); 
   zoomResetButton = new s7sdk.common.ZoomResetButton("s7container", params, "zoomResetBtn"); 
   
   /* Add handlers for zoom in, zoom out and zoom reset buttons inline. */ 
   zoomInButton.addEventListener("click", function() { zoomView.zoomIn(); }); 
   zoomOutButton.addEventListener("click", function() { zoomView.zoomOut(); }); 
   zoomResetButton.addEventListener("click", function() { zoomView.zoomReset(); });
   ```

1. Definieren Sie nun einige grundlegende Stile für die Schaltflächen, indem Sie dem `style` -Block oben in Ihrer Datei Folgendes hinzufügen:

   ```
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

1. Vorschau des Viewers Sie sieht wie folgt aus:

   ![](assets/viewer-3.jpg)

   Sie konfigurieren die Farbfelder jetzt so, dass sie vertikal auf der rechten Seite ausgerichtet werden.

## Vertikale Konfiguration der Farbfelder {#section-91a8829d5b5a4d45a35b7faeb097fcc9}

1. Sie können Modifikatoren direkt in der `ParameterManager`-Instanz konfigurieren.

   Fügen Sie oben in der Funktion `initViewer` Folgendes hinzu, um das `Swatches` Miniaturlayout als einzelne Zeile zu konfigurieren:

   ```
   params.push("Swatches.tmblayout", "1,0");
   ```

1. Aktualisieren Sie den folgenden Größenaufruf in `resizeViewer`:

   ```
   swatches.resize(swatches.getWidth(), height);
   ```

1. Bearbeiten Sie die folgende `s7swatches`-Regel in `ZoomViewer.css`:

   ```
   .s7swatches { 
       top:0 ; 
       bottom: 0; 
       right: 0; 
       width: 150px; 
   }
   ```

1. Vorschau des Viewers Sie sieht wie folgt aus:

   ![](assets/viewer-4.jpg)

   Ihr einfacher Zoom-Viewer ist jetzt fertig.

   Dieses Viewer-Tutorial behandelt die Grundlagen dessen, was das Dynamic Media Viewer SDK bietet. Bei der Arbeit mit dem SDK können Sie die verschiedenen Standardkomponenten verwenden, um mühelos Rich-View-Erlebnisse für Ihre Zielgruppen zu erstellen und zu gestalten.
