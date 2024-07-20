---
title: ControlBar.transition
description: Konfigurationsattribut für Smart Crop Video Viewer.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop,Video
role: Developer,User
exl-id: 7b4db11b-e9ac-4a52-9206-083989128bc6
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '121'
ht-degree: 2%

---

# ControlBar.transition{#controlbar-transition}

Konfigurationsattribut für Smart Crop Video Viewer.

` [ControlBar.|<containerId>_controls.]transition=none|fade[, *`delaytohide`*[, *`duration`*]`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|fade</span> </p> </td> 
   <td colname="col2"> <p> Gibt den Effekttyp an, der zum Anzeigen oder Ausblenden der Steuerleiste und ihres Inhalts verwendet wird. </p> <p>Verwenden Sie <span class="codeph"> none</span> zum sofortigen Anzeigen und Verbergen. Verwenden Sie <span class="codeph"> fade</span> , um einen allmählichen Ein- und Ausblendeeffekt zu erzielen. </p> <p>Ausblenden wird in Internet Explorer 8 nicht unterstützt. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> delaytohide</span> </span> </p> </td> 
   <td colname="col2"> <p>Gibt die Zeit in Sekunden zwischen dem letzten Maus-/Touchereignis an, das die Steuerleiste registriert, und dem ausgeblendeten Zeitkontrollbalken. </p> <p> Wenn der Wert auf <span class="codeph"> -1</span> festgelegt ist, wird der automatische Ausblendeffekt der Komponente nie Trigger und bleibt immer auf dem Bildschirm sichtbar. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> Dauer</span> </span> </p> </td> 
   <td colname="col2"> <p>Legt die Dauer der Ein- und Ausblendung-Animation in Sekunden fest. </p> </td> 
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
