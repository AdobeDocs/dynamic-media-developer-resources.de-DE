---
title: ZoomView.enableHD
description: ZoomView.enableHD
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: 321ca7e2-e3f9-4b0e-8bde-41d8478e1a0b
source-git-commit: 61e3a1fd0e21d336eaf5232096f5b1b54f2a6353
workflow-type: tm+mt
source-wordcount: '305'
ht-degree: 1%

---

# ZoomView.enableHD{#zoomview-enablehd}

` [ZoomView.|<containerId>_zoomView.]enableHD=always|never|limit[, *`Zahl`*]`

<table id="table_0BEA0B5FFDF64E5594B534B2A87A6D88"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> Immer <span class="codeph">|Nie|Limit</span> </p> </td> 
   <td colname="col2"> <p> Aktivieren, beschränken oder deaktivieren Sie die Optimierung für Geräte, bei denen <span class="codeph"> devicePixelRatio</span> größer als <span class="codeph"> 1</span> ist, d. h. Geräte mit hoher Anzeigedichte wie iPhone4 und ähnliche Geräte. Wenn aktiv, dann begrenzt die Komponente die Größe der IS-Bildanforderung so, als ob das Gerät nur ein Pixelverhältnis von <span class="codeph"> 1</span> hätte und reduziert so die Bandbreite. </p> <p>Siehe Beispiel unten. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> Zahl</span> </span> </p> </td> 
   <td colname="col2"> <p> Bei Verwendung der Einstellung „Limit“ aktiviert die Komponente eine hohe Pixeldichte nur bis zum angegebenen Limit. </p> <p>Siehe Beispiel unten. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschaften {#section-50bcd15223174bb79ce08b31ea03d682}

Optional.

## Standard {#section-7564169749ff4a4996049ea1148cb2a5}

`limit,1500`

## Beispiel {#section-96e69b70365f461dae4399e49044ea2f}

Im Folgenden finden Sie die erwarteten Ergebnisse, wenn Sie dieses Konfigurationsattribut mit dem Viewer verwenden und die Viewer-Größe 1000 x 1000 beträgt:

<table id="table_F97FEDA0EE1B4EF6AC9FF9060548ACA4"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Wenn die Variable set gleich ist </p> </th> 
   <th colname="col2" class="entry"> <p>Ergebnis </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> immer</span> </p> </td> 
   <td colname="col2"> <p>Die Pixeldichte des Bildschirms/Geräts wird immer berücksichtigt.</p> <p> 
     <ul id="ul_D8F31FDFCDB74B75A3B1BFBEE33AF2E2"> 
      <li id="li_8A1C6DCCE10545349C73029729211BB2"> <p>Wenn die Pixeldichte des Bildschirms = 1 ist, beträgt das angeforderte Bild 1000 x 1000. </p> </li> 
      <li id="li_884156A34AC64B4E9B3ACC4C25EB710F"> <p>Wenn die Pixeldichte des Bildschirms = 1,5 ist, beträgt das angeforderte Bild 1500 x 1500. </p> </li> 
      <li id="li_7EC699284A7F4E679E512C3DA8B5454F"> <p>Wenn die Pixeldichte des Bildschirms = 2 ist, beträgt das angeforderte Bild 2000 x 2000. </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> nie</span> </p> </td> 
   <td colname="col2"> <p>Es verwendet immer eine Pixeldichte von 1 und ignoriert die HD-Fähigkeit des Geräts. Daher ist das angeforderte Bild immer 1000 x 1000. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Limit&lt;number&gt;</span> </p> </td> 
   <td colname="col2"> <p>Eine Gerätepixeldichte wird nur angefordert und bereitgestellt, wenn das resultierende Bild unter dem angegebenen Grenzwert liegt. </p> <p>Die Zahl für die Begrenzung gilt entweder für die Breite oder die Höhe. </p> <p> 
     <ul id="ul_CEC06B2280164951BA1A0ADED99E8050"> 
      <li id="li_CA7A0980ACC54690A4F212DF53E2DC8A"> <p>Wenn der Grenzwert 1600 beträgt und die Pixeldichte 1,5 beträgt, wird das Bild mit 1500 x 1500 bereitgestellt. </p> </li> 
      <li id="li_A4AAD7FBFA0347B082789511CA6768A5"> <p>Wenn der Grenzwert 1600 und die Pixeldichte 2 beträgt, wird das Bild 1000 x 1000 bereitgestellt, da das Bild 2000 x 2000 den Grenzwert überschreitet. </p> </li> 
     </ul> </p> <p> <b>Best Practice</b>: Die Limit-Zahl muss mit der Unternehmenseinstellung für die maximale Bildgröße übereinstimmen. Legen Sie daher die Limit-Nummer auf die Einstellung für die maximale Bildgröße des Unternehmens fest. </p> </td> 
  </tr> 
 </tbody> 
</table>
