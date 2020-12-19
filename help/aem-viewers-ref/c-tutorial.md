---
description: Das Viewer-SDK stellt eine Reihe von JavaScript-basierten Komponenten für die benutzerdefinierte Viewer-Entwicklung bereit. Bei den Viewern handelt es sich um webbasierte Anwendungen, mit denen von Adobe Scene7 bereitgestellte Rich-Media-Inhalte in Webseiten eingebettet werden können.
seo-description: Das Viewer-SDK stellt eine Reihe von JavaScript-basierten Komponenten für die benutzerdefinierte Viewer-Entwicklung bereit. Bei den Viewern handelt es sich um webbasierte Anwendungen, mit denen von Adobe Scene7 bereitgestellte Rich-Media-Inhalte in Webseiten eingebettet werden können.
seo-title: Viewer-SDK-Tutorial
solution: Experience Manager
title: Viewer-SDK-Tutorial
topic: Dynamic media
uuid: ea331f05-0c58-4e6b-b5a1-d9b8372d8e94
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '999'
ht-degree: 0%

---


# Viewer-SDK-Tutorial{#viewer-sdk-tutorial}

Das Viewer-SDK stellt eine Reihe von JavaScript-basierten Komponenten für die benutzerdefinierte Viewer-Entwicklung bereit. Bei den Viewern handelt es sich um webbasierte Anwendungen, mit denen von Adobe Scene7 bereitgestellte Rich-Media-Inhalte in Webseiten eingebettet werden können.

Das SDK bietet beispielsweise interaktives Zoomen und Schwenken. Darüber hinaus bietet es eine 360-Grad-Ansicht und Videowiedergabe von Assets, die über die Backend-Anwendung SPS (Scene7 Publishing System) nach Adobe Scene7 hochgeladen wurden.

Obwohl die Komponenten auf HTML5-Funktionen basieren, sind sie für die Verwendung auf Android- und Apple iOS-Geräten und Desktops, einschließlich Internet Explorer und höher, ausgelegt. Diese Art von Erfahrung bedeutet, dass Sie einen einzigen Arbeitsablauf für alle unterstützten Plattformen bereitstellen können.

Das SDK besteht aus UI-Komponenten, aus denen der Viewer-Inhalt besteht. Sie können diese Komponenten mithilfe von CSS und Nicht-UI-Komponenten gestalten, die eine unterstützende Rolle haben, wie z. B. das Abrufen und Parsen von Definitionen oder Tracking. Alle Verhalten von Komponenten können mithilfe von Modifikatoren angepasst werden, die Sie auf verschiedene Weise angeben können, z. B. als `name=value`-Paare in der URL.

Dieses Lernprogramm enthält die folgende Reihenfolge der Aufgaben, mit denen Sie einen einfachen Zoom-Viewer erstellen können:

* [Laden Sie das neueste Viewer-SDK von Adobe Developer Connection herunter](c-tutorial.md#section-84dc74c9d8e24a2380b6cf8fc28d7127)
* [Laden des Viewer-SDK](c-tutorial.md#section-98596c276faf4cf79ccf558a9f4432c6)
* [Hinzufügen eines Stils zum Viewer](c-tutorial.md#section-3783125360a1425eae5a5a334867cc32)
* [Einschließen von Container und ZoomView](c-tutorial.md#section-1a01730663154a508b88cc40c6f35539)
* [Hinzufügen von MediaSet- und Musterkomponenten zum Viewer](c-tutorial.md#section-02b8c21dd842400e83eae2a48ec265b7)
* [Hinzufügen von Schaltflächen zum Viewer](c-tutorial.md#section-1fc334fa0d2b47eb9cdad461725c07be)
* [Konfigurieren der Farbfelder vertikal](c-tutorial.md#section-91a8829d5b5a4d45a35b7faeb097fcc9)

## Laden Sie das neueste Viewer-SDK von Adobe Developer Connection herunter.{#section-84dc74c9d8e24a2380b6cf8fc28d7127}

1. Laden Sie das neueste Viewer-SDK von Adobe Developer Connection [hier](https://marketing.adobe.com/developer/devcenter/scene7/show) herunter.

   >[!NOTE]
   >
   >Sie können diese Übung abschließen, ohne das Viewer-SDK-Paket herunterladen zu müssen, da das SDK tatsächlich remote geladen wird. Das Viewer-Paket enthält jedoch weitere Beispiele und eine API-Referenzhandbuch, die Sie beim Erstellen Ihrer eigenen Viewer als hilfreich erachten können.

## Laden des Viewer-SDK {#section-98596c276faf4cf79ccf558a9f4432c6}

1. Beginn durch Einrichten einer neuen Seite, um den grundlegenden Zoom-Viewer zu entwickeln, den Sie erstellen werden.

   Betrachten Sie diesen Bootstrap- oder Loader-Code, um eine leere SDK-Anwendung einzurichten. Öffnen Sie Ihren bevorzugten Texteditor und fügen Sie das folgende HTML-Markup hinzu:

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
               can use a relative path if the viewer is deployed on one of the Adobe Scene7 servers and it is served  
               from the same domain. Otherwise, specify a full path to one of Adobe Scene7 servers that have the SDK  
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

   hinzufügen Sie den folgenden JavaScript-Code innerhalb des `script`-Tags, um das `ParameterManager` zu initialisieren. Auf diese Weise können Sie SDK-Komponenten innerhalb der Funktion `initViewer` erstellen und instanziieren:

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

   Sie werden diese leere Vorlagendatei als Referenz verwenden, wenn Sie in Zukunft neue Viewer erstellen. Diese Vorlage funktioniert lokal und wird von einem Webserver bereitgestellt.

Sie fügen Ihrem Viewer jetzt den Stil hinzu.

## Hinzufügen eines Stils zum Viewer {#section-3783125360a1425eae5a5a334867cc32}

1. Für diesen Vollbild-Viewer, den Sie erstellen, können Sie einige einfache Stile hinzufügen.

   hinzufügen Sie den folgenden `style`-Block am unteren Rand von `head`:

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

1. Erstellen Sie einen tatsächlichen Viewer, indem Sie die Komponenten `Container` und `ZoomView` einbeziehen.

   Fügen Sie die folgenden `include`-Anweisungen nach dem Laden des Skripts [!DNL Utils.js] am unteren Rand des Elements `<head>` ein:

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

   hinzufügen Sie die folgenden Variablen am Anfang der anonymen Hauptfunktion direkt über `s7sdk.Util.init()`:

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

1. Damit der oben genannte Code ordnungsgemäß ausgeführt werden kann, fügen Sie einen `containerResize`-Ereignis-Handler und eine Hilfsfunktion hinzu:

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

1. Vorschau der Seite, damit Sie sehen können, was Sie erstellt haben. Ihre Seite sieht wie folgt aus:

   ![](assets/viewer-1.jpg)

Sie fügen nun die Komponenten `MediaSet` und `Swatches` Ihrem Viewer hinzu.

## Hinzufügen von MediaSet- und Musterkomponenten zu Ihrem Viewer {#section-02b8c21dd842400e83eae2a48ec265b7}

1. Damit Benutzer Bilder aus einem Satz auswählen können, können Sie die Komponenten `MediaSet` und `Swatches` hinzufügen.

   hinzufügen das folgende SDK enthält:

   ```
   s7sdk.Util.lib.include('s7sdk.set.MediaSet'); 
   s7sdk.Util.lib.include('s7sdk.set.Swatches');
   ```

1. Aktualisieren Sie die Liste der Variablen wie folgt:

   ```
   var mediaSet, container, zoomView, swatches;
   ```

1. Instanziieren Sie die Komponenten `MediaSet` und `Swatches` innerhalb der Funktion `initViewer`.

   Stellen Sie sicher, dass die `Swatches`-Instanz nach den Komponenten `ZoomView` und `Container` instanziiert wird. Andernfalls wird die `Swatches`-Stapelreihenfolge ausgeblendet:

   ```
   // Create MediaSet to manage assets and add event listener to the NOTF_SET_PARSED event 
   mediaSet = new s7sdk.set.MediaSet(null, params, "mediaSet"); 
   
   // Add MediaSet event listener 
   mediaSet.addEventListener(s7sdk.event.AssetEvent.NOTF_SET_PARSED, onSetParsed, false); 
   
   /* create Swatches component and associate event handler for swatch selection notification */ 
   swatches = new s7sdk.set.Swatches("s7container", params, "mySwatches");   
   swatches.addEventListener(s7sdk.event.AssetEvent.SWATCH_SELECTED_EVENT, swatchSelected, false);
   ```

1. Fügen Sie jetzt die folgenden Ereignis-Handler-Funktionen hinzu:

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

1. Positionieren Sie die Farbfelder unten im Viewer, indem Sie dem Element `style` die folgende CSS hinzufügen:

   ```
   /* Align swatches to bottom of viewer */ 
   .s7swatches { 
       bottom: 0; 
       left: 0; 
       right: 0; 
       height: 150px; 
   }
   ```

1. Vorschau des Viewers.

   Beachten Sie, dass sich die Farbfelder unten links im Viewer befinden. Damit die Farbfelder die gesamte Viewer-Breite annehmen, müssen Sie einen Aufruf hinzufügen, um die Größe der Farbfelder manuell zu ändern, sobald der Benutzer die Größe des Browsers ändert. hinzufügen Sie Folgendes zur Funktion `resizeViewer`:

   ```
   swatches.resize(width, swatches.getHeight());
   ```

   Ihr Viewer sieht jetzt wie das folgende Bild aus. Versuchen Sie, die Größe des Browser-Fensters des Viewers zu ändern, und beachten Sie das resultierende Verhalten.

   ![](assets/viewer-2.jpg)

Sie können Ihrem Viewer jetzt Schaltflächen zum Zoomen, Herauszoomen und Zurücksetzen des Zooms hinzufügen.

## Hinzufügen von Schaltflächen zum Viewer {#section-1fc334fa0d2b47eb9cdad461725c07be}

1. Derzeit kann der Benutzer nur mit Klick- oder Berührungsgesten zoomen. Fügen Sie dem Viewer daher einige einfache Schaltflächen zur Zoomsteuerung hinzu.

   hinzufügen die folgenden Schaltflächenkomponenten:

   ```
   s7sdk.Util.lib.include('s7sdk.common.Button');
   ```

1. Aktualisieren Sie die Liste der Variablen wie folgt:

   ```
   var mediaSet, container, zoomView, swatches, zoomInButton, zoomOutButton, zoomResetButton;
   ```

1. Instanziieren Sie Schaltflächen am unteren Rand der Funktion `initViewer`.

   Beachten Sie, dass die Reihenfolge wichtig ist, es sei denn, Sie geben in CSS `z-index` an:

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

1. Definieren Sie nun einige grundlegende Stile für die Schaltflächen, indem Sie dem `style`-Block oben in Ihrer Datei Folgendes hinzufügen:

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

1. Vorschau des Viewers. Es sieht wie folgt aus:

   ![](assets/viewer-3.jpg)

   Sie konfigurieren die Muster jetzt so, dass sie vertikal auf der rechten Seite ausgerichtet werden.

## Konfigurieren der Farbfelder vertikal {#section-91a8829d5b5a4d45a35b7faeb097fcc9}

1. Sie können Modifikatoren direkt auf der `ParameterManager`-Instanz konfigurieren.

   hinzufügen Sie die folgenden Elemente oben in der Funktion `initViewer`, um das `Swatches`-Miniaturlayout als einzelne Zeile zu konfigurieren:

   ```
   params.push("Swatches.tmblayout", "1,0");
   ```

1. Aktualisieren Sie den folgenden Größenaufruf innerhalb von `resizeViewer`:

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

1. Vorschau des Viewers. Es sieht wie folgt aus:

   ![](assets/viewer-4.jpg)

   Ihr einfacher Zoom-Viewer ist jetzt abgeschlossen.

   Dieses Viewer-Tutorial gibt einen Überblick über die Grundlagen des Scene7 Viewer-SDK. Während Sie mit dem SDK arbeiten, können Sie die verschiedenen Standardkomponenten verwenden, um mühelos Rich-View-Erlebnisse für Ihre Zielgruppe-Audiencen zu erstellen und zu gestalten.

