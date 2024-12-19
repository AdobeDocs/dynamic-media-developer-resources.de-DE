---
title: ControlBar.transition
description: Konfigurationsattribut für Video Viewer.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Video
role: Developer,User
exl-id: 133717c7-38d9-47b6-86bb-e23ebd8f147a
source-git-commit: 67e12fae514341137e4218ea950f34da0d9997f3
workflow-type: tm+mt
source-wordcount: '119'
ht-degree: 2%

---

# ControlBar.transition{#controlbar-transition}

Konfigurationsattribut für Video Viewer.

` [ControlBar.|<containerId>_controls.]transition=none|fade[, *`DelayToHide`*[, *`duration`*]`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|fade</span> </p> </td> 
   <td colname="col2"> <p> Gibt den Effekttyp an, mit dem die Steuerleiste und ihr Inhalt ein- oder ausgeblendet werden. </p> <p>Verwenden Sie <span class="codeph"> Keine</span> zum sofortigen Ein- und Ausblenden. Verwenden Sie <span class="codeph"> </span>, um einen allmählichen Ein- und Ausblendeffekt zu erzielen. </p> <p>Fade wird in Internet Explorer 8 nicht unterstützt. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> DelaytoHide</span> </span> </p> </td> 
   <td colname="col2"> <p>Gibt die Zeit in Sekunden an, die zwischen dem letzten von der Steuerleiste registrierten Maus-/Touch-Ereignis und der Zeit liegt, die von der Steuerleiste ausgeblendet wird. </p> <p> Trigger Bei <span class="codeph"> -1</span> ändert die Komponente ihren Effekt zum automatischen Ausblenden nicht und bleibt immer auf dem Bildschirm sichtbar. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> Dauer</span> </span> </p> </td> 
   <td colname="col2"> <p>Legt die Dauer der Ein- und Ausblendung in Sekunden fest. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschaften {#section-f42369774e2740dcb399626a0e4e930e}

Optional.

## Standard {#section-d016470e92a74f98a18c4ab3489410a5}

`fade,2,0.5`

## Beispiel {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

```
transition=none
```
