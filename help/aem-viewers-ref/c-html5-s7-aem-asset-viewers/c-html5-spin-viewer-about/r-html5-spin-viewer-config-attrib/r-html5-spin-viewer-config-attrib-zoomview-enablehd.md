---
title: ZoomView.enableHD
description: ZoomView.enableHD
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Spin Sets
role: Developer,User
exl-id: fd81cd48-9990-4659-a52c-7abdbc95a0e3
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '280'
ht-degree: 3%

---

# ZoomView.enableHD{#zoomview-enablehd}

` [ZoomView.|<containerId>_zoomView.]enableHD=always|never|limit[, *`Nummer`*]`

<table id="table_0BEA0B5FFDF64E5594B534B2A87A6D88"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> always|never|limit</span> </p> </td> 
   <td colname="col2"> <p> Aktivieren, Beschränken oder Deaktivieren der Optimierung für Geräte, auf denen <span class="codeph"> devicePixelRatio</span> größer als <span class="codeph"> 1</span>: Geräte mit hoher Dichte, wie iPhone4 und ähnliche Geräte. Wenn diese Option aktiviert ist, beschränkt die Komponente die Größe der IS-Bildanforderung so, als hätte das Gerät nur ein Pixelverhältnis von <span class="codeph"> 1</span> und so die Bandbreite zu reduzieren. </p> <p>Siehe Beispiel unten. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> Nummer</span></span> </p> </td> 
   <td colname="col2"> <p> Bei Verwendung der Grenzeinstellung ermöglicht die Komponente eine hohe Pixeldichte nur bis zum angegebenen Grenzwert. </p> <p>Siehe Beispiel unten. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschaften {#section-924163cb2f6542499f49894becef7fb5}

Optional.

## Standard {#section-7a2128fd488941948aff18421f533ccf}

`limit,1500`

## Beispiel {#section-622348a84fbe4ff4b5dd7eb53b044d83}

Die folgenden Ergebnisse werden erwartet, wenn Sie dieses Konfigurationsattribut mit dem Viewer verwenden und die Viewer-Größe 1000 x 1000 beträgt:

<table id="table_F97FEDA0EE1B4EF6AC9FF9060548ACA4"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Wenn die Variable set gleich </p> </th> 
   <th colname="col2" class="entry"> <p>Ergebnis </p> </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> immer</span> </p> </td> 
   <td colname="col2"> <p>Die Pixeldichte des Bildschirms/Geräts wird immer berücksichtigt. </p> <p> 
     <ul id="ul_D8F31FDFCDB74B75A3B1BFBEE33AF2E2"> 
      <li id="li_8A1C6DCCE10545349C73029729211BB2"> <p>Wenn die Pixeldichte des Bildschirms = 1 ist, beträgt das angeforderte Bild 1000 x 1000. </p> </li> 
      <li id="li_884156A34AC64B4E9B3ACC4C25EB710F"> <p>Wenn die Pixeldichte des Bildschirms 1,5 beträgt, beträgt das angeforderte Bild 1500 x 1500. </p> </li> 
      <li id="li_7EC699284A7F4E679E512C3DA8B5454F"> <p>Wenn die Pixeldichte des Bildschirms = 2 ist, beträgt das angeforderte Bild 2000 x 2000. </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> nie</span> </p> </td> 
   <td colname="col2"> <p>Dabei wird immer die Pixeldichte 1 verwendet und die HD-Funktion des Geräts ignoriert. Daher beträgt das angeforderte Bild immer 1000 x 1000. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> limit&lt;number&gt;</span> </p> </td> 
   <td colname="col2"> <p>Eine Geräte-Pixeldichte wird nur angefordert und bereitgestellt, wenn das resultierende Bild unter der angegebenen Grenze liegt. </p> <p>Die Begrenzungsnummer bezieht sich entweder auf die Breite oder die Höhe. </p> <p> 
     <ul id="ul_CEC06B2280164951BA1A0ADED99E8050"> 
      <li id="li_CA7A0980ACC54690A4F212DF53E2DC8A"> <p>Wenn der Grenzwert 1600 beträgt und die Pixeldichte 1,5 beträgt, wird das Bild 1500 x 1500 bereitgestellt. </p> </li> 
      <li id="li_A4AAD7FBFA0347B082789511CA6768A5"> <p>Wenn der Grenzwert 1600 beträgt und die Pixeldichte 2 beträgt, wird das Bild 1000 x 1000 bereitgestellt, da das Bild 2000 x 2000 den Grenzwert überschreitet. </p> </li> 
     </ul> </p> <p><b>Best Practice</b>: Die Begrenzungsnummer muss mit der Unternehmenseinstellung verwendet werden, um ein Bild mit der maximalen Größe zu erhalten. Stellen Sie daher die Höchstzahl so ein, dass sie der Einstellung für die maximale Bildgröße des Unternehmens entspricht. </p> </td> 
  </tr> 
 </tbody> 
</table>
