---
description: Konfigurationsattribut für den interaktiven Video-Viewer.
solution: Experience Manager
title: CallToAction.enabledragging
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,Business Practitioner
exl-id: 21db58df-b76e-4a78-afc4-5e0188cb8896
translation-type: tm+mt
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '94'
ht-degree: 5%

---

# CallToAction.enabledragging{#calltoaction-enabledragging}

Konfigurationsattribut für den interaktiven Video-Viewer.

` [CallToAction.|<containerId>_callToAction.]enabledragging=0|1[, *`overdragvalue`*]`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0 | 1 </span> </p> </td> 
   <td colname="col2"> <p> Aktiviert bzw. deaktiviert die Möglichkeit, mit einer Maus oder mit Touch-Gesten durch die Miniaturansichten zu blättern. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> overdragvalue  </span> </span> </p> </td> 
   <td colname="col2"> <p> Befindet sich im Bereich <span class="codeph"> 0-1 </span> und ist ein Prozentwert für die Bewegung in die falsche Richtung der tatsächlichen Geschwindigkeit. </p> <p>Wenn auf <span class="codeph"> 1 </span> eingestellt, wird es mit der Maus verschoben. </p> <p>Wenn Sie auf <span class="codeph"> 0 </span> eingestellt sind, können Sie sich nicht in die falsche Richtung bewegen. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschaften {#section-1e637b22e8a44d759d588e47576891e6}

Optional.

## Standard {#section-71fb773f814649b2885aefee68073641}

`1,0.5`

## Beispiel {#section-bce98c31f08a4a0ab262fab7f95ba020}

```
enabledragging=0
```
