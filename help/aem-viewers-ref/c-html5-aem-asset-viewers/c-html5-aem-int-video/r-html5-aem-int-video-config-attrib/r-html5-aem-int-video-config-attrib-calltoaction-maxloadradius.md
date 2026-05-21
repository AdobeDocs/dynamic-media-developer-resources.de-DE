---
title: CallToAction.maxLoadRadius
description: Konfigurationsattribut für den interaktiven Video-Viewer.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: db04133e-bb23-4d94-b91d-fcf34576c03f
TQID: 'https://experienceleague.adobe.com/t8aIHpXr-5-4FhRdZkiHRKgTVLCZEdl2jdSgaSjbT7Y'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 72
ht-degree: 4%

---

# CallToAction.maxLoadRadius{#calltoaction-maxloadradius}

Konfigurationsattribut für den interaktiven Video-Viewer.

` [CallToAction.|<containerId>_callToAction.]maxloadradius=-1|0| *`preloadnbr`*`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">-1|0|<span class="varname"> preloadNbr</span></span> </p> </td> 
   <td colname="col2"> <p> Gibt das Verhalten beim Vorausfüllen der Komponente an. </p> <p>Bei <span class="codeph"> -1 </span> alle Miniaturen gleichzeitig geladen, wenn die Komponente initialisiert oder das Asset geändert wird. </p> <p>Bei Einstellung auf <span class="codeph"> 0 </span> nur sichtbare Miniaturansichten geladen. </p> <p>Legen Sie <span class="codeph"><span class="varname"> preloadnbr</span></span> fest, um festzulegen, wie viele unsichtbare Zeilen/Spalten um den sichtbaren Bereich vorgeladen werden. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschaften {#section-1e637b22e8a44d759d588e47576891e6}

Optional.

## Standard {#section-71fb773f814649b2885aefee68073641}

`-1`

## Beispiel {#section-bce98c31f08a4a0ab262fab7f95ba020}

```
maxloadradius=-1
```
