---
description: Die interaktive Bildbibliothek ist ein JavaScript-Modul, mit dem die Qualität der von Scene7 bereitgestellten und in responsive Webseiten eingebetteten Bilder dynamisch angepasst wird. Darüber hinaus bietet es eine verbesserte Bildqualität auf Geräten mit hochauflösenden Bildschirmen. Die Bibliothek kann auch Ergebnisse aus Smart-Zuschneiden und Smart-Muster responsiv rendern.
seo-description: Die interaktive Bildbibliothek ist ein JavaScript-Modul, mit dem die Qualität der von Scene7 bereitgestellten und in responsive Webseiten eingebetteten Bilder dynamisch angepasst wird. Darüber hinaus bietet es eine verbesserte Bildqualität auf Geräten mit hochauflösenden Bildschirmen. Die Bibliothek kann auch Ergebnisse aus Smart-Zuschneiden und Smart-Muster responsiv rendern.
seo-title: Info zur Bibliothek mit interaktiven Bildern
solution: Experience Manager
title: Info zur Bibliothek mit interaktiven Bildern
topic: Scene7 Image Serving - Image Rendering API
uuid: 0906a940-59ff-45b0-b509-57bd02f2da57
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Info zur Bibliothek mit interaktiven Bildern{#about-responsive-image-library}

Die interaktive Bildbibliothek ist ein JavaScript-Modul, mit dem die Qualität der von Scene7 bereitgestellten und in responsive Webseiten eingebetteten Bilder dynamisch angepasst wird. Darüber hinaus bietet es eine verbesserte Bildqualität auf Geräten mit hochauflösenden Bildschirmen. Die Bibliothek kann auch Ergebnisse aus Smart-Zuschneiden und Smart-Muster responsiv rendern.

## Demo-URLs {#section-4f72c1dc38bf4e03acfa5205733a05a5}

Der einfachste Anwendungsfall der Bibliothek für interaktives Bild besteht darin, eine Liste von Haltepunktwerten für die Bildbreite zu definieren. Diese Liste stellt sicher, dass die entsprechende Darstellung geladen und angezeigt wird, wenn die Größe eines Bildes geändert wird, da sich das Layout einer Webseite ändert, indem der Benutzer die Größe des Browserfensters ändert oder die Ausrichtung des Geräts ändert. Die Bibliothek überwacht kontinuierlich die Bildgröße auf dem Bildschirm. Jedes Mal, wenn eine neue Haltepunktbreite erreicht wird, ruft sie eine neue Bilddarstellung aus Scene7 ab.

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
   <td colname="col1"> <p> <a href="https://marketing.adobe.com/resources/help/en_US/s7/is_ir_api/is_api/samples/responsive-static-image-simple.html" scope="external" format="https"> https://marketing.adobe.com/resources/help/en_US/s7/is_ir_api/is_api/samples/responsive-static-image-simple.html </a> </p> <p> 
     <!-- http://sasha.s7qa.com/jira-bugs/S7-7729/responsive-static-image-simple.htm--> </p> </td> 
   <td colname="col2"> <p>Im Folgenden wird ein einfaches Beispiel dargestellt, bei dem sich das interaktive Bild in einem Container befindet, der 50 % der Webseitenbreite beträgt. Jedes Mal, wenn die Größe des Browserfensters geändert wird, ändert sich die Breite des Containers. Wenn die Bildbreite einen der konfigurierten Haltepunkte erreicht, die zu Veranschaulichungszwecken auf 200, 400, 600 und 800 Pixel eingestellt sind, wird eine neue Darstellung heruntergeladen und angezeigt. Das Ziel ist es, unnötige große Bilder zu vermeiden und Netzwerkbandbreite zu sparen. </p> <p>Klicken Sie auf die URL, um die Webseite zu öffnen, die Größe des Browser-Fensters zu ändern und den Netzwerkverkehr zu überwachen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>2 </p> </td> 
   <td colname="col1"> <p> <a href="https://marketing.adobe.com/resources/help/en_US/s7/is_ir_api/is_api/samples/responsive-static-image-bootstrap.html" format="https" scope="external"> https://marketing.adobe.com/resources/help/en_US/s7/is_ir_api/is_api/samples/responsive-static-image-bootstrap.html </a> </p> <p> 
     <!-- http://sasha.s7qa.com/jira-bugs/S7-7729/responsive-static-image-bootstrap.htm--> </p> </td> 
   <td colname="col2"> <p>Im folgenden Bootstrap-Beispiel wird der gleiche Verwendungsfall auf einer Webseite veranschaulicht. Gemäß Bootstrap CSS kann die Layoutzelle, der das interaktive Bild hinzugefügt wird, eine der folgenden Breiten annehmen: 360, 720 und 940 Pixel. Dies sind die genauen Werte, die als Haltepunkte an die Bibliothek für interaktives Bild übergeben werden. Somit stellt Scene7 sicher, dass die Netzwerkbandbreite des Clients effektiv genutzt wird. Darüber hinaus wird sichergestellt, dass das Bild in der exakten Größe angezeigt wird, die angesichts des aktuellen Webseitenlayouts erforderlich ist, ohne dass visuelle Artefakte durch Skalieren des clientseitigen Browsers entstehen. </p> <p>Klicken Sie auf die URL, um die Webseite zu öffnen, die Größe des Browser-Fensters zu ändern, um auf unterschiedliche LayoutHaltepunkte zuzugreifen und den Netzwerkverkehr zu überwachen. </p> <p>Zu den erweiterten Verwendungsbeispielen zählen die Zuweisung verschiedener Bildvorgaben oder Bildserstellungs-Befehle oder beides mit unterschiedlichen Haltepunktwerten. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>3 </p> </td> 
   <td colname="col1"> <p> <a href="https://marketing.adobe.com/resources/help/en_US/s7/is_ir_api/is_api/samples/image-presets.html" format="https" scope="external"> https://marketing.adobe.com/resources/help/en_US/s7/is_ir_api/is_api/samples/image-presets.html </a> </p> <p> 
     <!--http://sasha.s7qa.com/jira-bugs/S7-7729/image-presets.html--> </p> </td> 
   <td colname="col2"> <p>In diesem nächsten Beispiel werden Bildvorgaben unterschiedlicher Bildqualität und -formate für unterschiedliche Haltepunktgrößen verwendet. Bei einem kleinen Haltepunkt wird eine Vorgabe mit niedriger Qualität angewendet, die Image Serving zwingt, das GIF-Bild, das auf nur sechs Farben komprimiert wurde, zurückzugeben. Ein mittlerer Haltepunkt verwendet eine Bildvorgabe, die für JPEG mit hoher Komprimierung konfiguriert ist. Der größte Haltepunkt wird mit einer hochwertigen Bildvorgabe unter Verwendung verlustfreier PNG-Datei verknüpft. Diese Methode stellt sicher, dass hochqualitative Bilder an solche Geräte gesendet werden, wobei davon ausgegangen wird, dass Geräte mit größeren Bildschirmen eine größere Bandbreite und Verarbeitungsleistung haben. </p> <p>Klicken Sie auf die URL, um die Webseite zu öffnen, die Größe des Webbrowserfensters von größer zu kleiner zu ändern und zu erkennen, wie die Bildqualität abnimmt. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>4 </p> </td> 
   <td colname="col1"> <p> <a href="https://marketing.adobe.com/resources/help/en_US/s7/is_ir_api/is_api/samples/crops.html" format="https" scope="external"> https://marketing.adobe.com/resources/help/en_US/s7/is_ir_api/is_api/samples/crops.html </a> </p> <p> 
     <!--http://sasha.s7qa.com/jira-bugs/S7-7729/crops.html--> </p> </td> 
   <td colname="col2"> <p>Zusätzlich zu Bildvorgaben ist es möglich, bestimmte Image Serving-Befehle mit Haltepunkten zu verknüpfen. Das folgende Beispiel zeigt, wie das Bannerbild schrittweise in den Interessensbereich beschnitten werden kann, wenn die Bildschirmgröße kleiner wird. Hier verfügt der größte Haltepunkt über keine Image Serving-Befehle, sodass das Bannerbild vollständig sichtbar ist. Beim mittleren Haltepunkt wird moderater Zuschnitt angewendet, sodass nur der Läufer mit dem Text "Läuft"sichtbar ist. An einem kleinen Haltepunkt werden mehr Zuschnitte angewendet, sodass nur das Produkt angezeigt wird. </p> <p>Klicken Sie auf die URL, um die Webseite zu öffnen und die Größe des Browserfensters zu ändern. Beachten Sie, wie das Bild allmählich abgeschnitten wird, wenn Sie von einer größeren zu einer kleineren Größe wechseln. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>5 </p> </td> 
   <td colname="col1"> <p> <a href="https://marketing.adobe.com/resources/help/en_US/s7/is_ir_api/is_api/samples/template.html" format="https" scope="external"> https://marketing.adobe.com/resources/help/en_US/s7/is_ir_api/is_api/samples/template.html </a> </p> <p> 
     <!--http://sasha.s7qa.com/jira-bugs/S7-7729/template.html--> </p> </td> 
   <td colname="col2"> <p>Sie können auch Bildservierungsbefehle mit Image Serving-Vorlagen verwenden, um bestimmte Vorlagenparameter basierend auf der Bildgröße zu steuern. In diesem nächsten Beispiel wird eine Image Serving-Vorlage verwendet, bei der die Schriftgröße der Textüberlagerung mithilfe des <span class="codeph"> Parameters $fontsize parametrisiert </span> wird. Das interaktive Bild ist so konfiguriert, dass es eine größere Schriftgröße für kleinere Bildgrößen verwendet, um sicherzustellen, dass Text immer lesbar bleibt: </p> </td> 
  </tr> 
 </tbody> 
</table>

## Systemanforderungen {#section-35ea9e9c79cc43d7bcefdc240340fba4}

**Serverhardware und -software**

* Scene7 Image Serving 6.0.1 oder höher.

**Mindestanforderungen an den Client-Browser**

* Microsoft® Windows® 7 oder höher; Mac OS X 10.8 oder höher.
* Firefox 23, Safari 6, Chrome 29, IE 9 oder höher.
* iOS 6 oder höher.
* Zertifiziert für iPhone3GS oder höher und iPad2 oder höher (nur native Browser).
* Android OS 2.3 oder höher.
* Internet Explorer auf Mobilgeräten wird derzeit nicht unterstützt.

