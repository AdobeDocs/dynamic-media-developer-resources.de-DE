---
description: Die responsive Bildbibliothek ist ein JavaScript-Modul, das die Qualität der von Dynamic Media bereitgestellten und in responsive Web-Seiten eingebetteten Bilder dynamisch anpasst. Darüber hinaus bietet es eine verbesserte Bildqualität auf Geräten mit High-Density-Bildschirmen. Die Bibliothek kann auch Ergebnisse aus smartem Zuschneiden und smarten Farb-/Bildmustern dynamisch rendern.
solution: Experience Manager
title: Über die Bibliothek responsiver Bilder
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: f853b9b4-917c-4744-b2a5-25fde2532356
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '804'
ht-degree: 0%

---

# Über die Bibliothek responsiver Bilder{#about-responsive-image-library}

Die responsive Bildbibliothek ist ein JavaScript-Modul, das die Qualität der von Dynamic Media bereitgestellten und in responsive Web-Seiten eingebetteten Bilder dynamisch anpasst. Darüber hinaus bietet es eine verbesserte Bildqualität auf Geräten mit High-Density-Bildschirmen. Die Bibliothek kann auch Ergebnisse aus smartem Zuschneiden und smarten Farb-/Bildmustern dynamisch rendern.

## Demo-URLs {#section-4f72c1dc38bf4e03acfa5205733a05a5}

Der einfachste Anwendungsfall der Bibliothek Responsive Image besteht darin, eine Liste von Breakpoint-Werten für die Bildbreite zu definieren. Diese Liste stellt sicher, dass die entsprechende Ausgabedarstellung geladen und angezeigt wird, wenn die Größe eines Bildes geändert wird, weil sich das Web-Seiten-Layout ändert, nachdem ein Benutzer die Größe des Browser-Fensters geändert hat oder die Ausrichtung des Geräts geändert wurde. Die Bibliothek überwacht kontinuierlich die Bildgröße auf dem Bildschirm und ruft jedes Mal, wenn eine neue Breakpoint-Breite erreicht wird, eine neue Bildausgabe von Dynamic Media ab.

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
   <td colname="col1"> <p> <a href="https://experienceleague.adobe.com/tools/dynamic-media-demo/is-api/responsive-static-image-simple.html?lang=de" scope="external" format="https"> https://experienceleague.adobe.com/tools/dynamic-media-demo/is-api/responsive-static-image-simple.html?lang=de </a> </p> <p> 
     <!-- http://sasha.s7qa.com/jira-bugs/S7-7729/responsive-static-image-simple.htm--> </p> </td> 
   <td colname="col2"> <p>Im Folgenden finden Sie ein einfaches Beispiel, bei dem sich das responsive Bild in einem Container befindet, der 50 % der Web-Seitenbreite einnimmt. Jedes Mal, wenn die Größe des Browser-Fensters geändert wird, ändert sich die Container-Breite. Wenn die Bildbreite einen der konfigurierten Haltepunkte erreicht (die zu Illustrationszwecken auf 200, 400, 600 und 800 Pixel festgelegt sind), wird eine neue Ausgabedarstellung heruntergeladen und angezeigt. Dadurch soll das Laden unnötiger großer Bilder vermieden und Netzwerkbandbreite gespart werden. </p> <p>Klicken Sie auf die URL, um die Web-Seite zu öffnen, die Größe des Browser-Fensters zu ändern und den Netzwerk-Traffic zu überwachen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>2 </p> </td> 
   <td colname="col1"> <p> <a href="https://experienceleague.adobe.com/tools/dynamic-media-demo/is-api/responsive-static-image-bootstrap.html?lang=de" format="https" scope="external"> https://experienceleague.adobe.com/tools/dynamic-media-demo/is-api/responsive-static-image-bootstrap.html?lang=de </a> </p> <p> 
     <!-- http://sasha.s7qa.com/jira-bugs/S7-7729/responsive-static-image-bootstrap.htm--> </p> </td> 
   <td colname="col2"> <p>Das folgende Bootstrap-Beispiel veranschaulicht denselben Anwendungsfall auf einer Web-Seite. Gemäß Bootstrap-CSS kann die Layoutzelle, der das responsive Bild hinzugefügt wird, eine der folgenden Breiten annehmen: 360, 720 und 940 Pixel. Diese Werte sind genau das, was als Haltepunkte an die Bibliothek für responsive Bilder übergeben wird. Auf diese Weise stellt Dynamic Media sicher, dass die Netzwerkbandbreite des Clients effektiv genutzt wird. Außerdem wird sichergestellt, dass das Bild in der exakt erforderlichen Größe angezeigt wird - angesichts des aktuellen Web-Seiten-Layouts - ohne visuelle Artefakte durch die Skalierung des Client-seitigen Browsers. </p> <p>Klicken Sie auf die URL, um die Web-Seite zu öffnen, die Größe des Browser-Fensters zu ändern, um verschiedene Layout-Breakpoints aufzurufen, und den Netzwerk-Traffic zu überwachen. </p> <p>Zu den komplexeren Anwendungsfällen gehören die Zuordnung verschiedener Bildvorgaben, Image-Serving-Befehle oder beides zu unterschiedlichen Breakpoint-Werten. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>3 </p> </td> 
   <td colname="col1"> <p> <a href="https://experienceleague.adobe.com/tools/dynamic-media-demo/is-api/image-presets.html?lang=de" format="https" scope="external"> https://experienceleague.adobe.com/tools/dynamic-media-demo/is-api/image-presets.html?lang=de</a> </p> <p> 
     <!--http://sasha.s7qa.com/jira-bugs/S7-7729/image-presets.html--> </p> </td> 
   <td colname="col2"> <p>In diesem nächsten Beispiel werden Bildvorgaben mit unterschiedlicher Bildqualität und unterschiedlichem Format für unterschiedliche Breakpoint-Größen verwendet. Für einen kleinen Breakpoint wird eine Vorgabe von niedriger Qualität angewendet, die Image Serving zwingt, das GIF-Bild nur in sechs Farben komprimiert zurückzugeben. Ein mittlerer Breakpoint verwendet eine Bildvorgabe, die für JPEG mit hoher Komprimierung konfiguriert ist. Der größte Breakpoint ist mit einer Bildvorgabe hoher Qualität mit verlustfreiem PNG verbunden. Durch dieses Verfahren wird sichergestellt, dass diesen Geräten hochwertige Bilder bereitgestellt werden, wobei davon ausgegangen wird, dass Geräte mit größeren Bildschirmen eine größere Bandbreite und Rechenleistung aufweisen. </p> <p>Klicken Sie auf die URL, um die Web-Seite zu öffnen. Ändern Sie die Größe des Webbrowser-Fensters von größer auf kleiner und beobachten Sie eine Verschlechterung der Bildqualität. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>4 </p> </td> 
   <td colname="col1"> <p> <a href="https://experienceleague.adobe.com/tools/dynamic-media-demo/is-api/crops.html?lang=de" format="https" scope="external"> https://experienceleague.adobe.com/tools/dynamic-media-demo/is-api/crops.html?lang=de </a> </p> <p> 
     <!--http://sasha.s7qa.com/jira-bugs/S7-7729/crops.html--> </p> </td> 
   <td colname="col2"> <p>Zusätzlich zu Bildvorgaben ist es möglich, bestimmte Bildbereitstellungsbefehle Breakpoints zuzuordnen. Das folgende Beispiel zeigt, wie es möglich ist, das Bannerbild schrittweise in den gewünschten Bereich zuzuschneiden, da die Bildschirmbildgröße geringer wird. Hier verfügt der größte Breakpoint über keine Image-Serving-Befehle, sodass das Bannerbild vollständig sichtbar ist. Bei einem mittleren Breakpoint wird ein moderater Zuschnitt angewendet, sodass nur der Runner mit „Laufen“-Text sichtbar wird. Bei einem kleinen Breakpoint wird mehr Zuschnitt angewendet, sodass nur das Produkt angezeigt wird. </p> <p>Klicken Sie auf die URL, um die Web-Seite zu öffnen und die Größe des Browser-Fensters zu ändern. Beachten Sie, wie das Bild schrittweise von einer größeren zu einer kleineren Größe abgeschnitten wird. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>5 </p> </td> 
   <td colname="col1"> <p> <a href="https://experienceleague.adobe.com/tools/dynamic-media-demo/is-api/template.html?lang=de" format="https" scope="external"> https://experienceleague.adobe.com/tools/dynamic-media-demo/is-api/template.html?lang=de </a> </p> <p> 
     <!--http://sasha.s7qa.com/jira-bugs/S7-7729/template.html--> </p> </td> 
   <td colname="col2"> <p>Sie können Bildbereitstellungsbefehle auch mit Bildbereitstellungsvorlagen verwenden, um bestimmte Vorlagenparameter basierend auf der Bildgröße zu steuern. In diesem nächsten Beispiel wird eine Bildbereitstellungsvorlage verwendet, bei der die Schriftgröße der Textüberlagerung mithilfe <span class="codeph"> $fontsize-</span> parametrisiert wird. Responsives Bild ist so konfiguriert, dass bei kleineren Bildgrößen eine größere Schriftgröße verwendet wird, um sicherzustellen, dass Text immer lesbar bleibt: </p> </td> 
  </tr> 
 </tbody> 
</table>

## Systemanforderungen {#section-35ea9e9c79cc43d7bcefdc240340fba4}

**Server-Hardware und -Software**

* Dynamic Media Image Serving 6.0.1 oder höher.

**Mindestanforderungen für Client-Browser**

* Microsoft® Windows® 7 oder höher; macOS X 10.8 oder höher.
* Firefox 23, Safari 6, Chrome 29, IE 9 oder höher.
* iOS 6 oder höher.
* Zertifiziert für iPhone3GS oder höher und iPad2 oder höher (nur native Browser).
* Android™ OS 2.3 oder höher.
* Internet Explorer wird auf Mobilgeräten derzeit nicht unterstützt.
