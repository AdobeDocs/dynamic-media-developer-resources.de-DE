---
title: PageView.maxloadradius
description: PageView.maxloadradius
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: cf769b2d-be4e-4d93-9620-00a438157693
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '71'
ht-degree: 4%

---

# PageView.maxloadradius{#pageview-maxloadradius}

[!DNL `[PageView.|<containerId>_pageView.]maxloadradius=-1|0| *`preloadnbr`*`]

<table id="table_985ADD6C9BD04C629A84C9C625CCCFEB"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph">-1|0|<span class="varname"> preloadNbr</span></span> </p> </td> 
   <td colname="col2"> <p>Gibt das Verhalten beim Vorausfüllen der Komponente an. </p> <p>Bei <span class="codeph"> -1 lädt </span> Komponente alle Katalograhmen vorab, wenn sie sich im Leerlauf befindet. </p> <p> Bei <span class="codeph"> 0 lädt </span> Komponente nur den sichtbaren Rahmen, den vorherigen und den nächsten Rahmen. </p> <p>Stellen Sie <span class="codeph"><span class="varname"> preloadnbr</span></span> ein, um festzulegen, wie viele unsichtbare Frames um den aktuell angezeigten Frame im Leerlaufzustand vorgeladen werden. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschaften {#section-4b7952997f9240e581d21bcdb173f9af}

Optional.

## Standard {#section-f0d5211aa2494f27a5a85e4a54b24ea2}

[!DNL `1`]

## Beispiel {#section-4e27dfc1e2ce4dd7a4996dc575ab7a93}

[!DNL `maxloadradius=0`]
