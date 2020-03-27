---
description: 'null'
seo-description: 'null'
seo-title: PageView.enableHD
solution: Experience Manager
title: PageView.enableHD
topic: Dynamic media
uuid: 34c0e59f-4ed0-4b62-b661-aff20ff64ec4
translation-type: tm+mt
source-git-commit: 2bd5b17e473ec53844b4bbcb4f13580b2d6bfaf4

---


# PageView.enableHD{#pageview-enablehd}

[!DNL `[PageView.|<containerId>_pageView.]enableHD=always|never|limit[, *`Nummer`*]`]

<table id="table_0BEA0B5FFDF64E5594B534B2A87A6D88"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> always|never|limit</span> </p> </td> 
   <td colname="col2"> <p> Aktivieren, begrenzen oder deaktivieren Sie die Optimierung für Geräte, bei denen <span class="codeph"> devicePixelRatio</span> größer als <span class="codeph"> 1</span>ist, d. h. Geräte mit hoher Auflösung wie iPhone4 und ähnliche Geräte. Wenn die Komponente aktiv ist, beschränkt sie die Größe der IS-Bildanforderung so, als hätte das Gerät nur ein Pixel-Verhältnis von <span class="codeph"> 1</span> und verringert so die Bandbreite. </p> <p>Siehe Beispiel unten </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> Nummer</span></span> </p> </td> 
   <td colname="col2"> <p> Bei Verwendung der Limit-Einstellung ermöglicht die Komponente eine hohe Pixeldichte nur bis zum angegebenen Limit. </p> <p>Siehe Beispiel unten. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschaften {#section-38b878e38caa439bb462d4fa637afdaa}

Optional.

## Standard {#section-50b22de303c1432094530e6583132c02}

[!DNL `limit,1500`

## Beispiel {#section-09433488774245d985acef6c0341ece0}

Die folgenden Ergebnisse werden erwartet, wenn Sie dieses Konfigurationsattribut mit dem Viewer verwenden und die Viewer-Größe 1000 x 1000 beträgt:

<table id="table_F97FEDA0EE1B4EF6AC9FF9060548ACA4"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Wenn die set-Variable gleich </p> </th> 
   <th colname="col2" class="entry"> <p>Ergebnis </p> </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> immer</span> </p> </td> 
   <td colname="col2"> <p>Die Pixeldichte des Bildschirms/Geräts wird stets berücksichtigt. </p> <p> 
     <ul id="ul_D8F31FDFCDB74B75A3B1BFBEE33AF2E2"> 
      <li id="li_8A1C6DCCE10545349C73029729211BB2"> <p>Wenn die Pixeldichte des Bildschirms 1 ist, beträgt das angeforderte Bild 1000 x 1000. </p> </li> 
      <li id="li_884156A34AC64B4E9B3ACC4C25EB710F"> <p>Wenn die Pixeldichte des Bildschirms 1,5 beträgt, beträgt das angeforderte Bild 1500 x 1500. </p> </li> 
      <li id="li_7EC699284A7F4E679E512C3DA8B5454F"> <p>Wenn die Pixeldichte des Bildschirms 2 ist, beträgt das angeforderte Bild 2000 x 2000. </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> nie</span> </p> </td> 
   <td colname="col2"> <p>Es wird immer eine Pixeldichte von 1 verwendet und ignoriert die HD-Fähigkeit des Geräts. Das angeforderte Bild ist daher immer 1000 x 1000. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> limit&lt;number&gt;</span> </p> </td> 
   <td colname="col2"> <p>Eine Pixeldichte des Geräts wird nur dann angefordert und bereitgestellt, wenn das resultierende Bild unter der angegebenen Grenze liegt. </p> <p>Die Limit-Zahl bezieht sich entweder auf die Breite oder Höhe. </p> <p> 
     <ul id="ul_CEC06B2280164951BA1A0ADED99E8050"> 
      <li id="li_CA7A0980ACC54690A4F212DF53E2DC8A"> <p>Wenn die maximale Anzahl 1600 beträgt und die Pixeldichte 1,5 beträgt, wird das Bild mit 1500 x 1500 angezeigt. </p> </li> 
      <li id="li_A4AAD7FBFA0347B082789511CA6768A5"> <p>Wenn die Grenzwert-Zahl 1600 beträgt und die Pixeldichte 2 beträgt, wird das Bild mit 1000 x 1000 Pixel bereitgestellt, da das Bild mit 2000 x 2000 Pixel die Grenze überschreitet. </p> </li> 
     </ul> </p> <p><b>Best Practice</b>: Die Limit-Zahl muss mit der Einstellung für die Firma für die maximale Bildgröße kombiniert werden. Stellen Sie daher die maximale Anzahl so ein, dass sie der maximalen Bildgrößeneinstellung für die Firma entspricht. </p> </td> 
  </tr> 
 </tbody> 
</table>

