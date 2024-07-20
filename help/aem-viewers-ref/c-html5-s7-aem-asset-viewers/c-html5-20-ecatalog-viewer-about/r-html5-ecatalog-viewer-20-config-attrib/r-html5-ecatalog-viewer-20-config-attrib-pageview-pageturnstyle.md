---
title: PageView.pageturnstyle
description: PageView.pageturnstyle
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: 00706c64-c051-4b62-8194-61d0a1c565e9
source-git-commit: a919130f0940d81a221b79563b6b3e41533ba788
workflow-type: tm+mt
source-wordcount: '124'
ht-degree: 2%

---

# PageView.pageturnstyle{#pageview-pageturnstyle}

` [PageView.|<containerId>_pageView.]pageturnstyle= *`dividerWidth`*, *`dividerColor`*, *`dividerOpacity`*, *`borderOnOff`*, *`borderColor`*, *`fillColor`*`

Steuert das Erscheinungsbild der Komponente, wenn auf Desktop-Systemen `PageView.frametransition` auf `turn` oder `auto` gesetzt ist.

<table id="table_A8CDA1AE2680402A99BCD5DD371B225F"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> dividerWidth</span></span> </p> </td> 
   <td colname="col2"> <p> Die Breite des Seitenspaltenschattens in Pixel, der die linken und rechten Seiten im Druckbogen trennt. Sie steuert auch die Breite des laufenden Shadow, der neben der Drehseite angezeigt wird. </p> </td> 
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
   <td colname="col2"> <p> Die Markierung (entweder <span class="codeph"> 0</span> oder <span class="codeph"> 1</span>), die den Rahmen um die sich drehende Seite ein- und ausschaltet. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> borderColor</span></span> </p> </td> 
   <td colname="col2"> <p> Die Rahmenfarbe im RRGGBB-Format. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> fillColor</span></span> </p> </td> 
   <td colname="col2"> <p> Die Farbe der durchgehenden Füllung des Komponentenbereichs, der während der Seitenumkehranimation verwendet wird, im RRGGBB-Format. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschaften {#section-54c634116cfe4f17813318e07539264c}

Optional.

## Standard {#section-43fd13f639c2480c82658fafeeaf0846}

`40,909090,1,1,909090,FFFFFF`

## Beispiele {#section-bb97b2aac37a43eba11d263ce7049363}

`pageturnstyle=20,FF0000,1,1,00FF00,0000FF`
