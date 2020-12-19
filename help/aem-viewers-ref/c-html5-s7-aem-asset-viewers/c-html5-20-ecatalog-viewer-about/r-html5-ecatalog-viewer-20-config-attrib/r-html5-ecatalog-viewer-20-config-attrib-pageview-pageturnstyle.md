---
description: 'null'
seo-description: 'null'
seo-title: PageView.pageturnstyle
solution: Experience Manager
title: PageView.pageturnstyle
topic: Dynamic media
uuid: 3192d810-fb30-44ae-9939-98e890c76e5c
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '122'
ht-degree: 4%

---


# PageView.pageturnstyle{#pageview-pageturnstyle}

` [PageView.|<containerId>_pageView.]pageturnstyle= *``*, *``*, *``*, *``*, *``*, *`dividerWidthdividerColordividerOpacityborderOnOffborderColorfillColor`*`

Steuert die Komponentendarstellung, wenn `PageView.frametransition` auf `turn` oder `auto` auf Desktop-Systemen eingestellt ist.

<table id="table_A8CDA1AE2680402A99BCD5DD371B225F"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> dividerWidth</span></span> </p> </td> 
   <td colname="col2"> <p> Die Breite (in Pixel) des Seitenteilschattens, der die linken und rechten Seiten im Druckbogen trennt. Sie steuert auch die Breite des laufenden Schattens, der neben der Drehseite angezeigt wird. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> dividerOpacity</span></span> </p> </td> 
   <td colname="col2"> <p> Die Schattenfarbe im RRGGBB-Format. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> dividerOpacity</span></span> </p> </td> 
   <td colname="col2"> <p>Die Schattendeckkraft im Bereich von <span class="codeph"> 0</span> bis <span class="codeph"> 1</span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> borderOnOff</span></span> </p> </td> 
   <td colname="col2"> <p> Das Flag (entweder <span class="codeph"> 0</span> oder <span class="codeph"> 1</span>), durch das der Rand um die Seite herum ein- und ausgeschaltet wird. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> borderColor</span></span> </p> </td> 
   <td colname="col2"> <p> Die Rahmenfarbe im RRGGBB-Format. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> fillColor</span></span> </p> </td> 
   <td colname="col2"> <p> Die Farbe der festen Füllung des Komponentenbereichs, der während der Seitenumblätteranimation im RRGGBB-Format verwendet wird. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschaften {#section-54c634116cfe4f17813318e07539264c}

Optional.

## Standard {#section-43fd13f639c2480c82658fafeeaf0846}

`40,909090,1,1,909090,FFFFFF`

## Beispiele {#section-bb97b2aac37a43eba11d263ce7049363}

`pageturnstyle=20,FF0000,1,1,00FF00,0000FF`
