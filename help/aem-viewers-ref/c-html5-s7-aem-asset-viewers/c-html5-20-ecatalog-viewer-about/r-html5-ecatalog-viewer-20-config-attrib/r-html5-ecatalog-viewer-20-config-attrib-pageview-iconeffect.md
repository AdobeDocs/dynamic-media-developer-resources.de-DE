---
description: 'null'
seo-description: 'null'
seo-title: PageView.iconEffect
solution: Experience Manager
title: PageView.iconEffect
topic: Dynamic media
uuid: c8adabf9-ccbf-4a46-b1e7-b4cb58d4e606
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '119'
ht-degree: 6%

---


# PageView.iconEffect{#pageview-iconeffect}

` [PageView.|<containerId>_pageView.]iconeffect=0|1[, *``*][, *``*][, *`countfadeautoHide`*]`

<table id="table_DD66FFC263A34220876DD204BFE62D49"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0 | 1</span> </p> </td> 
   <td colname="col2"> <p> Aktiviert die Anzeige des <span class="codeph">-Iconeffect</span> oben im Bild, wenn sich das Bild in einem Reset-Status befindet und eine verfügbare Aktion für die Interaktion mit dem Bild angezeigt werden soll. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> Zähler</span></span> </p> </td> 
   <td colname="col2"> <p> Gibt an, wie oft <span class="codeph"> der Iconeffect</span> maximal angezeigt und erneut angezeigt wird. Der Wert <span class="codeph"> -1</span> gibt an, dass das Symbol immer unbegrenzt angezeigt wird. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> verblassen</span></span> </p> </td> 
   <td colname="col2"> <p>Gibt die Dauer der Ein- oder Ausblenden-Animation in Sekunden an. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> autoHide</span></span> </p> </td> 
   <td colname="col2"> <p>Legt die Anzahl der Sekunden fest, in denen der <span class="codeph">-Iconeffect</span> vollständig sichtbar bleibt, bevor er automatisch ausgeblendet wird. Das heißt, die Zeit nach Abschluss der Einblendeanimation, aber vor dem Ausblenden der Beginn. Die Einstellung <span class="codeph"> 0</span> deaktiviert das automatische Ausblenden. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschaften {#section-b6e5e52698d4492f9d6350e7e312bb1b}

Optional.

## Standard {#section-7d0fc8fa09b34c288ed32ef7faa84604}

`1,1,0.3,3`

## Beispiel {#section-95db1bfcccf241089654363203b19977}

`iconeffect=0`
