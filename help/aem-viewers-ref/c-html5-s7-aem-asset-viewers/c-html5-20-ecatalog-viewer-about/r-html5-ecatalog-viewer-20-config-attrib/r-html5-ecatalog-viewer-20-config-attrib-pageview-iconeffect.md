---
title: PageView.iconEffect
description: PageView.iconEffect
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: cdd96e58-d805-47d6-bf26-9ebd90afd535
TQID: 'https://experienceleague.adobe.com/BChSE62IgfhsabTf1I-XlAJLqvRhai4U48vNEg-MkQ4'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 120
ht-degree: 4%

---

# PageView.iconEffect{#pageview-iconeffect}

` [PageView.|<containerId>_pageView.]iconeffect=0|1[, *`count`*][, *`fade`*][, *`autoHide`*]`

<table id="table_DD66FFC263A34220876DD204BFE62D49"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0|1</span> </p> </td> 
   <td colname="col2"> <p> Aktiviert den <span class="codeph"> iconeffect</span>, der über dem Bild angezeigt wird, wenn das Bild zurückgesetzt wird und eine Aktion angezeigt werden kann, die mit dem Bild interagiert werden kann. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> Anzahl</span></span> </p> </td> 
   <td colname="col2"> <p> Gibt an, wie oft der <span class="codeph"> IconEffect</span> maximal angezeigt werden kann. Der Wert <span class="codeph"> -1</span> bedeutet, dass das Symbol immer unbegrenzt wieder angezeigt wird. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> verblasst</span></span> </p> </td> 
   <td colname="col2"> <p>Gibt die Dauer der Einblenden- oder Ausblenden-Animation in Sekunden an. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> automatisch ausblenden</span></span> </p> </td> 
   <td colname="col2"> <p>Legt die Anzahl der Sekunden fest, die der <span class="codeph"> iconeffect</span> vollständig sichtbar bleibt, bevor er automatisch ausgeblendet wird. Das heißt, die Zeit nach Abschluss der Einblendanimation, aber vor Beginn der Ausblendanimation. Bei einer Einstellung von <span class="codeph"> 0</span> wird das Verhalten zum automatischen Ausblenden deaktiviert. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschaften {#section-b6e5e52698d4492f9d6350e7e312bb1b}

Optional.

## Standard {#section-7d0fc8fa09b34c288ed32ef7faa84604}

`1,1,0.3,3`

## Beispiel {#section-95db1bfcccf241089654363203b19977}

`iconeffect=0`
