---
description: SearchPanel.maxloadradius
solution: Experience Manager
title: SearchPanel.maxloadradius
topic: Dynamic media
uuid: 37d58c88-3d45-44d9-9f2c-d616d1077906
translation-type: tm+mt
source-git-commit: bf5873e5a6bdb859e19b15584ba85e9c106f853b
workflow-type: tm+mt
source-wordcount: '53'
ht-degree: 7%

---


# SearchPanel.maxloadradius{#searchpanel-maxloadradius}

[!DNL `[SearchPanel.|<containerId>_searchPanel.]maxloadradius=-1|0| *`preloadnbr`*`]

<table id="table_985ADD6C9BD04C629A84C9C625CCCFEB"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph">-1|0|<span class="varname"> preloadnbr</span></span> </p> </td> 
   <td colname="col2"> <p>Gibt das Komponentenvorladeverhalten an. </p> <p>Bei Festlegung auf <span class="codeph"> -1</span> werden alle Miniaturansichten gleichzeitig geladen, wenn die Komponente initialisiert wird oder sich das Asset ändert. </p> <p> Bei Festlegung auf <span class="codeph"> 0</span> werden nur sichtbare Miniaturansichten geladen. </p> <p>Legen Sie <span class="codeph"><span class="varname"> preloadnbr</span></span> fest, um festzulegen, wie viele unsichtbare Zeilen um den sichtbaren Bereich vorgeladen werden. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschaften {#section-4b7952997f9240e581d21bcdb173f9af}

Optional.

## Standard {#section-f0d5211aa2494f27a5a85e4a54b24ea2}

[!DNL `1`]

## Beispiel {#section-4e27dfc1e2ce4dd7a4996dc575ab7a93}

[!DNL `maxloadradius=0`]
