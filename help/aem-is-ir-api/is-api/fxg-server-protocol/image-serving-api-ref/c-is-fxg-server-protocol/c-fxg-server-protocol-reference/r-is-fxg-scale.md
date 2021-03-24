---
description: Bild skalieren. Skaliert ein Bild nach Faktor relativ zum Bild mit voller Auflösung.
solution: Experience Manager
title: scale
feature: Dynamic Media Classic, SDK/API
role: Entwickler, Geschäftspraktiker
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '50'
ht-degree: 8%

---


# scale{#scale}

Bild skalieren. Skaliert ein Bild nach Faktor relativ zum Bild mit voller Auflösung.

`scale= *`factor`*`

<table id="simpletable_AC0974B79E064BA99C1F76461BDE808A"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> factor</span></span> </p> </td> 
  <td class="stentry"> <p>Skalierungsfaktor (real, &gt;0). </p></td> 
 </tr> 
</table>

## Standard {#section-e9e53959b35844579f0f1d7721b71f8e}

Wenn kein Wert angegeben ist, wird das Bild ohne Skalierung verwendet.

## Beispiel {#section-d5526953d6434c58bb2388bd936c13b5}

[!DNL http://server/is/agm/myRootId/myImageId?scale=.5]
