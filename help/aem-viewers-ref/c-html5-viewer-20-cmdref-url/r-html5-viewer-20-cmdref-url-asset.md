---
title: asset
description: Parameter, die allen Viewern gemeinsam sind.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API
role: Developer,User
exl-id: edcd18b6-5292-44da-80be-b7f75ee4c48e
source-git-commit: c99aac44711852d8ac661878e11ce0b19d3dbf60
workflow-type: tm+mt
source-wordcount: '575'
ht-degree: 2%

---

# asset{#asset}

Parameter, die allen Viewern gemeinsam sind.

` asset= *`assetId`*`

<table id="table_9B98C97485DD4DEB8A6ECBCE8DF6B886"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> assetId </span> </span> </p> </td> 
   <td colname="col2"> <p> Die Asset-ID des einzelnen Videos oder adaptiven Videosets. </p> </td> 
  </tr> 
 </tbody> 
</table>

Diese Eigenschaft ist erforderlich, es sei denn, der Parameter `video` wird verwendet. Siehe [Unterstützung für externe Videos](../c-html5-s7-aem-asset-viewers/c-html5-video-reference/r-html5-video-viewer-20-external-video-support.md#concept-22c67fee43274a29b28ee16770b1b1f3) unter Video oder [Unterstützung für externe Videos](../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-external-video-support.md#concept-66aa2784f2294794989bad2af74c3760) unter Video360.

oder

` asset= *`image`*`

<table id="table_67E18F42E97C4AAAB0A2F67B7924765D"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> Bild </span> </span> </p> </td> 
   <td colname="col2"> <p> Gibt ein einzelnes Bild oder Karussellset an. Wenden Sie eine doppelte HTTP-Kodierung auf alle nicht sicheren Zeichen an, die im Bildnamen oder im Karussellset-Namen vorhanden sind. </p> </td> 
  </tr> 
 </tbody> 
</table>

oder

` asset= *`image`* | *`imageList`* | *`imageListWithModifiers`* | *`multiDimensionalSpinSet`* [%3F *`modifiers`*]`

<table id="table_A2A0ACD942E942BC99AF0DC80FB1C670"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> Bild </span> </span> </p> </td> 
   <td colname="col2"> <p> Gibt ein Bild an. Wenden Sie eine doppelte HTTP-Kodierung auf alle nicht sicheren Zeichen an, die im Bildnamen vorhanden sind. </p> <p>Oder gibt einen Verweis auf ein Bildset an. Der Viewer ruft Bildsets vom Server ab, indem er die Anforderung <span class="codeph"> req=set IS </span> verwendet. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> imageList </span> </span> </p> </td> 
   <td colname="col2"> <p> Gibt einen expliziten Bildsatz an, der aus einer sortierten Folge von Elementen oder Rahmen besteht, getrennt durch Kommas. </p> <p> <p>Hinweis: Diese Funktion wird in Adobe Dynamic Media Classic unterstützt, nicht aber in Adobe Experience Manager Assets. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> imageListWithModifiers </span> </span> </p> </td> 
   <td colname="col2"> <p> Gibt ein explizites Bildset an, in dem jeder Frame über eigene Image Serving-Modifikatoren verfügt. In diesem Fall wird die Liste der Frames in Klammern eingeschlossen. Stellen Sie sicher, dass Sie die doppelte HTTP-Kodierung auf alle Kommas anwenden, die im frame-spezifischen Image Serving-Modifikator vorhanden sind. </p> <p> <p>Hinweis: Diese Funktion wird in Adobe Dynamic Media Classic unterstützt, nicht aber in Adobe Experience Manager Assets. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> multiDimensionalSpinSet </span> </span> </p> </td> 
   <td colname="col2"> <p>Gibt unter Verwendung der folgenden Syntax ein explizites mehrdimensionales Rotationsset an: </p> <p> <span class="codeph"> (( <span class="varname"> horizontalSpinSet </span>)[,( <span class="varname"> horizontalSpinSet </span>)] </span> </p> <p> wobei <span class="codeph"> <span class="varname"> horizontalSpinSet </span> </span> eine kommagetrennte Liste von Frames für eine bestimmte horizontale Achse ist. Alle <span class="codeph"> <span class="varname"> horizontalSpinSet </span> </span> sollten dieselbe Anzahl von Frames aufweisen. </p> <p> <p>Hinweis: Diese Funktion wird in Adobe Dynamic Media Classic unterstützt, nicht aber in Adobe Experience Manager Assets. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> Modifikatoren </span> </span> </p> </td> 
   <td colname="col2"> <p> Image Serving-Befehle; <span class="codeph"> &amp; </span> und <span class="codeph"> = </span> Trennzeichen müssen HTTP-kodiert sein als <span class="codeph"> %26 </span> bzw. <span class="codeph"> %3D </span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

oder

` asset=( *`mediaSet`* | ( *`video`*; *`swatchId`* | *`image`*; *`swatchId`* | *`setId`*; *`swatchId`*); *`ID`*;( *`video`*; *`swatchId`* | *`image`*; *`swatchId`* | *`setId`*; *`swatchId`*); *`ID`*;] [%3F *` fiers`*]`

<table id="table_D31C8507C02A4452A79DEDDEC62EF2F5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> mediaSet </span> </span> </p> </td> 
   <td colname="col2"> <p> Gibt einen Verweis auf ein Medienset an. Der Viewer ruft mithilfe der IS-Anfrage req=set Mediensets vom Server ab. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> video </span> </span> </p> </td> 
   <td colname="col2"> <p> Einzelnes Video oder adaptives Videoset. </p> <p> <p>Hinweis: Diese Funktion wird in Adobe Dynamic Media Classic unterstützt, nicht aber in Adobe Experience Manager Assets. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> Bild </span> </span> </p> </td> 
   <td colname="col2"> <p> Einzelnes Bild. </p> <p> <p>Hinweis: Diese Funktion wird in Adobe Dynamic Media Classic unterstützt, nicht aber in Adobe Experience Manager Assets. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> setId </span> </span> </p> </td> 
   <td colname="col2"> <p> Musterset. </p> <p> <p>Hinweis: Diese Funktion wird in Adobe Dynamic Media Classic unterstützt, nicht aber in Adobe Experience Manager Assets. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> swatchId </span> </span> </p> </td> 
   <td colname="col2"> <p>Musterbild. </p> <p> <p>Hinweis: Diese Funktion wird in Adobe Dynamic Media Classic unterstützt, nicht aber in Adobe Experience Manager Assets. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> ID </span> </span> </p> </td> 
   <td colname="col2"> <p> Die Elementtyp-ID für Mediensets kann eine der folgenden sein: </p> <p> 
     <ul id="ul_3100F9356628498DA820C07F6F69CC9B"> 
      <li id="li_51B649A539F14510873CFDA85A6AA714"> <p> <span class="codeph"> advanced_image </span> </p> <p>Für einzelne Bilder. </p> </li> 
      <li id="li_7E764D67294647C1A828F949E5ED1908"> <p> <span class="codeph"> advanced_swatchset </span> </p> <p>Für verschachtelte Mustersets. </p> </li> 
      <li id="li_C942CED779B54110BCDC74188995FD5B"> <p> <span class="codeph"> drehen </span> </p> <p>Für Rotationsset. </p> </li> 
      <li id="li_6EA5C54F078D4B24B44F1588BF083842"> <p> <span class="codeph"> video </span> </p> <p>Für einzelne Videos. </p> </li> 
      <li id="li_8110FA7E0CAB4681A2D8C15F2A656E69"> <p> <span class="codeph"> video_set </span> </p> <p>Für adaptive Videosets. </p> </li> 
     </ul> </p> <p> <p>Hinweis: Diese Funktion wird in Adobe Dynamic Media Classic unterstützt, nicht aber in Adobe Experience Manager Assets. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> Modifikatoren </span> </span> </p> </td> 
   <td colname="col2"> <p> Image Serving-Befehle; <span class="codeph"> &amp; </span> und <span class="codeph"> = </span> Trennzeichen müssen HTTP-kodiert sein als <span class="codeph"> %26 </span> bzw. <span class="codeph"> %3D </span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Bilder, die IR (Image Rendering) oder UGC (User-Generated Content) verwenden, werden von diesem Viewer nicht unterstützt.

## Eigenschaften {#section-10ee45d637134e0fbcd943c62578cb78}

Erforderlich.

## Standard {#section-d411e450028c460392cb8508f8ccc5d9}

Keine.

## Beispiele {#section-a8afbf76f8384aa0a83ed1feeccd5b9a}

Referenz zu einzelnen Assets:

```
asset=Scene7SharedAssets/Backpack_B
```

oder

```
asset=/content/dam/mac/aodmarketingna/shoppable-banner/shoppable-banner.jpg
```

oder

```
asset=/content/dam/mac/aodmarketingna/dm-viewers-content/video/Glacier.mp4
```

oder

```
asset=/content/dam/dm-public-facing-live-demo-page/04_shoppable_carousel/05_shoppable_banner
```

oder

```
asset=Viewers/space_station_360-AVS
```

Einzelverweis auf ein Bildset, das in einem Katalog definiert ist:

```
asset=Viewers/Pluralist
```

Explizites Bildset:

```
asset=Scene7SharedAssets/Backpack_B,Scene7SharedAssets/Backpack_C
```

Explizites Bildset mit Frame-spezifischen Image Serving-Modifikatoren:

```
asset=(Scene7SharedAssets/Backpack_B%3Fop_colorize%3D255%252C0%252C0,Scene7SharedAssets/Backpack_B%3Fop_colorize%3D0x00ff00)
```

Einzelverweis auf ein Rotationsset, das in einem Katalog definiert ist:

```
asset=Scene7SharedAssets/SpinSet-Sample
```

Explizites Rotationsset:

```
asset=Scene7SharedAssets/Frame-1,Scene7SharedAssets/Frame-2,Scene7SharedAssets/Frame-3,Scene7SharedAssets/Frame-4,Scene7SharedAssets/Frame-5,Scene7SharedAssets/Frame-6,Scene7SharedAssets/Frame-7,Scene7SharedAssets/Frame-8
```

Explizites multidimensionales Rotationsset:

```
asset=((Scene7SharedAssets/ring1-25,Scene7SharedAssets/ring1-26,Scene7SharedAssets/ring1-27,Scene7SharedAssets/ring1-28,Scene7SharedAssets/ring1-29,Scene7SharedAssets/ring1-30,Scene7SharedAssets/ring1-31,Scene7SharedAssets/ring1-32,Scene7SharedAssets/ring1-33,Scene7SharedAssets/ring1-34,Scene7SharedAssets/ring1-35,Scene7SharedAssets/ring1-36),(Scene7SharedAssets/ring1-13,Scene7SharedAssets/ring1-14,Scene7SharedAssets/ring1-15,Scene7SharedAssets/ring1-16,Scene7SharedAssets/ring1-17,Scene7SharedAssets/ring1-18,Scene7SharedAssets/ring1-19,Scene7SharedAssets/ring1-20,Scene7SharedAssets/ring1-21,Scene7SharedAssets/ring1-22,Scene7SharedAssets/ring1-23,Scene7SharedAssets/ring1-24),(Scene7SharedAssets/ring1-01,Scene7SharedAssets/ring1-02,Scene7SharedAssets/ring1-03,Scene7SharedAssets/ring1-04,Scene7SharedAssets/ring1-05,Scene7SharedAssets/ring1-06,Scene7SharedAssets/ring1-07,Scene7SharedAssets/ring1-08,Scene7SharedAssets/ring1-09,Scene7SharedAssets/ring1-10,Scene7SharedAssets/ring1-11,Scene7SharedAssets/ring1-12))
```

Referenz zu einzelnen gemischten Mediensets:

```
 asset=Scene7SharedAssets/Mixed_Media_Set_Sample
```

Explizites gemischtes Medienset:

```
asset=Scene7SharedAssets/Backpack_J;;advanced_image;,Scene7SharedAssets/Frame-6;;advanced_image;,Scene7SharedAssets/Frame-2;;advanced_image;,Scene7SharedAssets/SpinSet_Sample;;spin;,Scene7SharedAssets/ImageSet-Colors-Sample;;advanced_swatchset;,Scene7SharedAssets/Glacier_Climber_640x360;Scene7SharedAssets/Glacier_Climber_640x360;video;
```

Der Scharfzeichnungsmodifikator wurde allen Bildern im Set hinzugefügt:

```
asset=Scene7SharedAssets/Backpack_B,Scene7SharedAssets/Backpack_C%3Fop_sharpen=%3D1
```

```
asset=Scene7SharedAssets/Mixed_Media_Set_Sample%3Fop_sharpen%3D1
```

```
asset=Viewers/Pluralist%3Fop_sharpen%3D1
```
