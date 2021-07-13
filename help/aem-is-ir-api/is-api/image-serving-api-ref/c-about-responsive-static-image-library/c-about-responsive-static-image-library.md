---
description: Responsive Image Library ist ein JavaScript-Modul, das die Bildqualität von Dynamic Media dynamisch anpasst und in responsive Webseiten eingebettet ist. Darüber hinaus bietet es eine verbesserte Bildqualität auf Geräten mit High-Density-Bildschirmen. Die Bibliothek kann auch Ergebnisse aus smartem Zuschneiden und smartem Farb-/Bildmuster responsiv rendern.
solution: Experience Manager
title: Über die Bibliothek responsiver Bilder
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: f853b9b4-917c-4744-b2a5-25fde2532356
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '842'
ht-degree: 0%

---

# Über die Bibliothek responsiver Bilder{#about-responsive-image-library}

Responsive Image Library ist ein JavaScript-Modul, das die Bildqualität von Dynamic Media dynamisch anpasst und in responsive Webseiten eingebettet ist. Darüber hinaus bietet es eine verbesserte Bildqualität auf Geräten mit High-Density-Bildschirmen. Die Bibliothek kann auch Ergebnisse aus smartem Zuschneiden und smartem Farb-/Bildmuster responsiv rendern.

## Demo-URLs {#section-4f72c1dc38bf4e03acfa5205733a05a5}

Der einfachste Anwendungsfall der Bibliothek responsiver Bilder besteht darin, eine Liste mit Breakpoint-Werten für die Bildbreite zu definieren. Diese Liste stellt sicher, dass die entsprechende Ausgabedarstellung geladen und angezeigt wird, wenn die Größe eines Bildes geändert wird, weil sich das Layout der Webseite von einem Benutzer ändert, der die Größe des Browser-Fensters ändert oder die Ausrichtung des Geräts ändert. Die Bibliothek überwacht kontinuierlich die Bildschirmbildgröße und ruft jedes Mal, wenn eine neue Breakpoint-Breite erreicht wird, eine neue Bilddarstellung aus Dynamic Media ab.

<table id="table_3D3D3991B802461A888E1093C1217D26"> 
 <thead> 
  <tr> 
   <th colname="col01" class="entry"> </th> 
   <th colname="col1" class="entry"> <p>Demo-URL </p> </th> 
   <th colname="col2" class="entry"> <p>Beschreibung </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col01"> <p>1 </p> </td> 
   <td colname="col1"> <p> <a href="https://experienceleague.adobe.com/tools/dynamic-media-demo/is-api/responsive-static-image-simple.html" scope="external" format="https"> https://experienceleague.adobe.com/tools/dynamic-media-demo/is-api/responsive-static-image-simple.html  </a> </p> <p> 
     <!-- http://sasha.s7qa.com/jira-bugs/S7-7729/responsive-static-image-simple.htm--> </p> </td> 
   <td colname="col2"> <p>Im Folgenden finden Sie ein einfaches Beispiel, bei dem sich das responsive Bild in einem Container befindet, der 50 % der Webseitenbreite annimmt. Jedes Mal, wenn die Größe des Browser-Fensters geändert wird, ändert sich die Behälterbreite. Wenn die Bildbreite einen der konfigurierten Haltepunkte erreicht, der für Veranschaulichungszwecke auf 200, 400, 600 und 800 Pixel festgelegt ist, wird eine neue Ausgabedarstellung heruntergeladen und angezeigt. Das Ziel besteht darin, das Laden unnötiger großer Bilder zu vermeiden und Netzwerkbandbreite zu sparen. </p> <p>Klicken Sie auf die URL, um die Webseite zu öffnen, die Größe des Browser-Fensters zu ändern und den Netzwerk-Traffic zu überwachen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>2 </p> </td> 
   <td colname="col1"> <p> <a href="https://experienceleague.adobe.com/tools/dynamic-media-demo/is-api/responsive-static-image-bootstrap.html" format="https" scope="external"> https://experienceleague.adobe.com/tools/dynamic-media-demo/is-api/responsive-static-image-bootstrap.html  </a> </p> <p> 
     <!-- http://sasha.s7qa.com/jira-bugs/S7-7729/responsive-static-image-bootstrap.htm--> </p> </td> 
   <td colname="col2"> <p>Das folgende Bootstrap-Beispiel zeigt den gleichen Anwendungsfall auf einer Webseite. Gemäß Bootstrap-CSS kann die Layoutzelle, der das responsive Bild hinzugefügt wird, eine der folgenden Breiten annehmen: 360, 720 und 940 Pixel. Diese Werte werden genau als Haltepunkte an die responsive Bildbibliothek übergeben. Daher stellt Dynamic Media sicher, dass die Netzwerkbandbreite des Clients effektiv verwendet wird. Außerdem wird sichergestellt, dass das Bild in der genauen Größe angezeigt wird, die für das aktuelle Web-Seiten-Layout erforderlich ist, ohne dass visuelle Artefakte die clientseitige Browserskalierung erfordern. </p> <p>Klicken Sie auf die URL, damit Sie die Webseite öffnen, die Größe des Browser-Fensters ändern, um unterschiedliche Layout-Haltepunkte zu erreichen, und überwachen Sie den Netzwerk-Traffic. </p> <p>Erweiterte Anwendungsfälle umfassen die Zuordnung verschiedener Bildvorgaben, Image Serving-Befehle oder beides mit unterschiedlichen Breakpoint-Werten. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>3 </p> </td> 
   <td colname="col1"> <p> <a href="https://experienceleague.adobe.com/tools/dynamic-media-demo/is-api/image-presets.html" format="https" scope="external"> https://experienceleague.adobe.com/tools/dynamic-media-demo/is-api/image-presets.html</a> </p> <p> 
     <!--http://sasha.s7qa.com/jira-bugs/S7-7729/image-presets.html--> </p> </td> 
   <td colname="col2"> <p>In diesem nächsten Beispiel werden Bildvorgaben unterschiedlicher Bildqualität und -format für unterschiedliche Breakpoint-Größen verwendet. Bei einem kleinen Breakpoint wird eine Vorgabe mit niedriger Qualität angewendet, die das Image Serving zwingt, das auf sechs Farben komprimierte GIF-Bild zurückzugeben. Ein mittlerer Breakpoint verwendet eine Bildvorgabe, die für JPEG mit hoher Komprimierung konfiguriert ist. Der größte Haltepunkt wird mit einer Bildvorgabe hoher Qualität unter Verwendung verlustfreien PNG-Elements verknüpft. Diese Methode stellt sicher, dass hochwertige Bilder an solche Geräte gesendet werden, wobei davon ausgegangen wird, dass Geräte mit größeren Bildschirmen eine größere Bandbreite und Verarbeitungsleistung aufweisen. </p> <p>Klicken Sie auf die URL, damit Sie die Webseite öffnen, die Größe des Webbrowserfensters von größer zu kleiner ändern und feststellen, wie sich die Bildqualität verschlechtert. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>4 </p> </td> 
   <td colname="col1"> <p> <a href="https://experienceleague.adobe.com/tools/dynamic-media-demo/is-api/crops.html" format="https" scope="external"> https://experienceleague.adobe.com/tools/dynamic-media-demo/is-api/crops.html  </a> </p> <p> 
     <!--http://sasha.s7qa.com/jira-bugs/S7-7729/crops.html--> </p> </td> 
   <td colname="col2"> <p>Neben Bildvorgaben ist es möglich, bestimmte Image Serving-Befehle mit Haltepunkten zu verknüpfen. Das folgende Beispiel zeigt, wie es möglich ist, das Bannerbild schrittweise in den gewünschten Bereich zu beschneiden, wenn die Bildschirmbildgröße kleiner wird. Hier verfügt der größte Haltepunkt überhaupt nicht über Image Serving-Befehle, sodass das Bannerbild vollständig sichtbar ist. Beim mittleren Breakpoint wird moderates Zuschneiden angewendet, sodass nur der Runner mit dem Text "Running"sichtbar ist. An kleinen Haltepunkten wird mehr Zuschnitt angewendet, sodass nur das Produkt angezeigt wird. </p> <p>Klicken Sie auf die URL, um die Webseite zu öffnen und die Größe des Browser-Fensters zu ändern. Beachten Sie, wie das Bild schrittweise beschnitten wird, wenn Sie von einer größeren zu einer kleineren Größe wechseln. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>5 </p> </td> 
   <td colname="col1"> <p> <a href="https://experienceleague.adobe.com/tools/dynamic-media-demo/is-api/template.html" format="https" scope="external"> https://experienceleague.adobe.com/tools/dynamic-media-demo/is-api/template.html  </a> </p> <p> 
     <!--http://sasha.s7qa.com/jira-bugs/S7-7729/template.html--> </p> </td> 
   <td colname="col2"> <p>Sie können auch Image Serving-Befehle mit Image Serving-Vorlagen verwenden, um bestimmte Vorlagenparameter basierend auf der Bildgröße zu steuern. In diesem nächsten Beispiel wird eine Image Serving-Vorlage verwendet, bei der die Schriftgröße der Textüberlagerung mit dem Parameter <span class="codeph"> $fontsize </span> parametrisiert wird. Responsives Bild ist so konfiguriert, dass eine größere Schriftgröße für kleinere Bildgrößen verwendet wird, um sicherzustellen, dass Text immer lesbar bleibt: </p> </td> 
  </tr> 
 </tbody> 
</table>

## Systemanforderungen {#section-35ea9e9c79cc43d7bcefdc240340fba4}

**Serverhardware und -software**

* Dynamic Media Image Serving 6.0.1 oder höher.

**Mindestanforderungen an den Client-Browser**

* Microsoft® Windows® 7 oder höher; macOS X 10.8 oder höher.
* Firefox 23, Safari 6, Chrome 29, IE 9 oder höher.
* iOS 6 oder höher.
* Zertifiziert für iPhone3GS oder höher und iPad2 oder höher (nur native Browser).
* Android™ OS 2.3 oder höher.
* Internet Explorer auf Mobilgeräten wird derzeit nicht unterstützt.
