---
title: ZoomView.enableHD
description: ZoomView.enableHD
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: 340a9614-b9dd-4aee-bd73-b99f6576930e
source-git-commit: ec2a15e2e76bae5da4fbabc9b6912b12dc080f66
workflow-type: tm+mt
source-wordcount: '306'
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
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> Nummer</span></span> </p> </td> 
   <td colname="col2"> <p> Bei Verwendung der Einstellung „Limit“ aktiviert die Komponente eine hohe Pixeldichte nur bis zum angegebenen Limit. </p> <p>Siehe Beispiel unten. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschaften {#section-1e637b22e8a44d759d588e47576891e6}

Optional.

## Standard {#section-71fb773f814649b2885aefee68073641}

`limit,1500`

## Beispiel {#section-bce98c31f08a4a0ab262fab7f95ba020}

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
   <td colname="col1"> <p><span class="codeph"> immer</span> </p> </td> 
   <td colname="col2"> <p>Die Pixeldichte des Bildschirms/Geräts wird immer berücksichtigt.</p> <p> 
     <ul id="ul_D8F31FDFCDB74B75A3B1BFBEE33AF2E2"> 
      <li id="li_8A1C6DCCE10545349C73029729211BB2"> <p>Wenn die Pixeldichte des Bildschirms = 1 ist, beträgt das angeforderte Bild 1000 x 1000. </p> </li> 
      <li id="li_884156A34AC64B4E9B3ACC4C25EB710F"> <p>Wenn die Pixeldichte des Bildschirms = 1,5 ist, beträgt das angeforderte Bild 1500 x 1500. </p> </li> 
      <li id="li_7EC699284A7F4E679E512C3DA8B5454F"> <p>Wenn die Pixeldichte des Bildschirms = 2 ist, beträgt das angeforderte Bild 2000 x 2000. </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> nie</span> </p> </td> 
   <td colname="col2"> <p>Es verwendet immer eine Pixeldichte von 1 und ignoriert die HD-Fähigkeit des Geräts. Daher ist das angeforderte Bild immer 1000 x 1000. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> Limit&lt;number&gt;</span> </p> </td> 
   <td colname="col2"> <p>Eine Gerätepixeldichte wird nur angefordert und bereitgestellt, wenn das resultierende Bild unter dem angegebenen Grenzwert liegt. </p> <p>Die Zahl für die Begrenzung gilt entweder für die Breite oder die Höhe. </p> <p> 
     <ul id="ul_CEC06B2280164951BA1A0ADED99E8050"> 
      <li id="li_CA7A0980ACC54690A4F212DF53E2DC8A"> <p>Wenn der Grenzwert 1600 beträgt und die Pixeldichte 1,5 beträgt, wird das Bild mit 1500 x 1500 bereitgestellt. </p> </li> 
      <li id="li_A4AAD7FBFA0347B082789511CA6768A5"> <p>Wenn der Grenzwert 1600 und die Pixeldichte 2 beträgt, wird das Bild 1000 x 1000 bereitgestellt, da das Bild 2000 x 2000 den Grenzwert überschreitet. </p> </li> 
     </ul> </p> <p><b>Best Practice</b>: Die Limit-Zahl muss mit der Unternehmenseinstellung für die maximale Bildgröße übereinstimmen. Legen Sie daher die Limit-Nummer auf die Einstellung für die maximale Bildgröße des Unternehmens fest. </p> </td> 
  </tr> 
 </tbody> 
</table>
