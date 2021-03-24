---
description: PageView.maxloadradius
solution: Experience Manager
title: PageView.maxloadradius
feature: Dynamic Media Classic, Viewer, SDK/API, E-Katalog
role: Entwickler, Geschäftspraktiker
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '75'
ht-degree: 5%

---


# PageView.maxloadradius{#pageview-maxloadradius}

` [PageView.|<containerId>_pageView.]maxloadradius=-1|0| *`preloadnbr`*`

<table id="table_985ADD6C9BD04C629A84C9C625CCCFEB"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph">-1|0|<span class="varname"> preloadnbr</span></span> </p> </td> 
   <td colname="col2"> <p>Gibt das Komponentenvorladeverhalten an. </p> <p>Bei Festlegung auf <span class="codeph"> -1</span> lädt die Komponente alle Katalograhmen im Leerlaufzustand vorab. </p> <p> Bei Festlegung auf <span class="codeph"> 0</span> lädt die Komponente nur den derzeit sichtbaren Rahmen, den vorherigen und den nächsten. </p> <p>Legen Sie <span class="codeph"><span class="varname"> preloadnbr</span></span> fest, um festzulegen, wie viele unsichtbare Rahmen um den derzeit angezeigten Rahmen im Leerlauf vorgeladen werden. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschaften {#section-4b7952997f9240e581d21bcdb173f9af}

Optional.

## Standard {#section-f0d5211aa2494f27a5a85e4a54b24ea2}

`1`

## Beispiel {#section-4e27dfc1e2ce4dd7a4996dc575ab7a93}

`maxloadradius=0`
