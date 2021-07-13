---
description: Konfigurationsattribut für interaktiven Video-Viewer.
solution: Experience Manager
title: CallToAction.maxloadradius
feature: Dynamic Media Classic,Viewer,SDK/API,interaktive Videos
role: Developer,User
exl-id: db04133e-bb23-4d94-b91d-fcf34576c03f
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '76'
ht-degree: 5%

---

# CallToAction.maxloadradius{#calltoaction-maxloadradius}

Konfigurationsattribut für interaktiven Video-Viewer.

` [CallToAction.|<containerId>_callToAction.]maxloadradius=-1|0| *`preloadnbr`*`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">-1|0|<span class="varname"> preloadnbr</span></span> </p> </td> 
   <td colname="col2"> <p> Gibt das Verhalten beim Vorausfüllen der Komponente an. </p> <p>Wenn auf <span class="codeph"> -1</span> gesetzt, werden alle Miniaturen gleichzeitig geladen, wenn die Komponente initialisiert oder das Asset geändert wird. </p> <p>Wenn auf <span class="codeph"> 0</span> gesetzt, werden nur sichtbare Miniaturen geladen. </p> <p>Auf <span class="codeph"><span class="varname"> preloadnbr</span></span> setzen, um festzulegen, wie viele unsichtbare Zeilen/Spalten um den sichtbaren Bereich vorab geladen werden. </p> </td> 
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
