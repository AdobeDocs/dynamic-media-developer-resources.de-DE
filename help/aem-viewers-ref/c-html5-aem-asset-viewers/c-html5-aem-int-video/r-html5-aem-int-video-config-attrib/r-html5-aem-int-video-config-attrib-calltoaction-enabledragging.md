---
description: Konfigurationsattribut für interaktiven Video-Viewer.
solution: Experience Manager
title: CallToAction.enabledragging
feature: Dynamic Media Classic,Viewer,SDK/API,interaktive Videos
role: Developer,User
exl-id: 21db58df-b76e-4a78-afc4-5e0188cb8896
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '91'
ht-degree: 5%

---

# CallToAction.enabledragging{#calltoaction-enabledragging}

Konfigurationsattribut für interaktiven Video-Viewer.

` [CallToAction.|<containerId>_callToAction.]enabledragging=0|1[, *`overdragvalue`*]`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0 | 1 </span> </p> </td> 
   <td colname="col2"> <p> Aktiviert oder deaktiviert die Möglichkeit für einen Benutzer, mit einer Maus oder durch Berührungsgesten in den Miniaturansichten zu blättern. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> overdragvalue  </span> </span> </p> </td> 
   <td colname="col2"> <p> Befindet sich im Bereich <span class="codeph"> 0-1 </span> und ist ein Prozentwert für die Bewegung in die falsche Richtung der tatsächlichen Geschwindigkeit. </p> <p>Wenn auf <span class="codeph"> 1 </span> gesetzt, wird es mit der Maus verschoben. </p> <p>Wenn auf <span class="codeph"> 0 </span> gesetzt, können Sie sich nicht in die falsche Richtung bewegen. </p> </td> 
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
