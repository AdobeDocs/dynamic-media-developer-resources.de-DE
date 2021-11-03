---
title: ControlBar.transition
description: Konfigurationsattribut für Smart Crop Video Viewer.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop Video
role: Developer,User
exl-id: 133717c7-38d9-47b6-86bb-e23ebd8f147a
source-git-commit: b6ebc938f55117c4144ff921bed7f8742cf3a8a7
workflow-type: tm+mt
source-wordcount: '121'
ht-degree: 3%

---

# ControlBar.transition{#controlbar-transition}

Konfigurationsattribut für Smart Crop Video Viewer.

` [ControlBar.|<containerId>_controls.]transition=none|fade[, *`delaytohide`*[, *`duration`*]`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|fade</span> </p> </td> 
   <td colname="col2"> <p> Gibt den Effekttyp an, der zum Anzeigen oder Ausblenden der Steuerleiste und ihres Inhalts verwendet wird. </p> <p>Verwendung <span class="codeph"> Keine</span> zum sofortigen Einblenden und Verbergen. Verwendung <span class="codeph"> verblassen</span> eine allmähliche Ein- und Ausblendung zu bewirken. </p> <p>Ausblenden wird in Internet Explorer 8 nicht unterstützt. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> delaytohide</span> </span> </p> </td> 
   <td colname="col2"> <p>Gibt die Zeit in Sekunden zwischen dem letzten Maus-/Touchereignis an, das die Steuerleiste registriert, und dem ausgeblendeten Zeitkontrollbalken. </p> <p> Wenn auf <span class="codeph"> -1</span>, wird der automatische Ausblendeffekt der Komponente nie Trigger und bleibt immer auf dem Bildschirm sichtbar. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> duration</span> </span> </p> </td> 
   <td colname="col2"> <p>Legt die Dauer der Ein- und Ausblendung der Animation in Sekunden fest. </p> </td> 
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
