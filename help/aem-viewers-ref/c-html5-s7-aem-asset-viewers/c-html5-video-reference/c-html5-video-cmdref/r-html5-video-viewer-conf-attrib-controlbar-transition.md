---
description: Konfigurationsattribut für Video Viewer.
solution: Experience Manager
title: ControlBar.transition
feature: Dynamic Media Classic, Viewer, SDK/API, Video
role: Entwickler, Geschäftspraktiker
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '127'
ht-degree: 3%

---


# ControlBar.transition{#controlbar-transition}

Konfigurationsattribut für Video Viewer.

` [ControlBar.|<containerId>_controls.]transition=none|fade[, *``*[, *`Delaytohidedauer`*]`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|fade</span> </p> </td> 
   <td colname="col2"> <p> Gibt den Effekttyp an, mit dem die Steuerleiste und ihr Inhalt ein- oder ausgeblendet werden. </p> <p>Verwenden Sie <span class="codeph"> none</span> zum sofortigen Ein- und Ausblenden. Verwenden Sie &lt; a0/&gt; fade</span>, um einen allmählichen Ein- und Ausblendeffekt zu erzielen.<span class="codeph"> </span></p> <p>Fade wird in Internet Explorer 8 nicht unterstützt. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> delaytohide</span> </span> </p> </td> 
   <td colname="col2"> <p>Gibt die Zeit in Sekunden zwischen dem letzten Maus-/Berührungsereignis an, das die Steuerleiste registriert, und der Zeitsteuerungsleiste an. </p> <p> Wenn die Komponente auf <span class="codeph"> -1</span> eingestellt ist, wird ihr automatischer Ausblendeffekt nie Trigger und bleibt immer auf dem Bildschirm sichtbar. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> Dauer</span> </span> </p> </td> 
   <td colname="col2"> <p>Legt die Dauer der Animation zum Ein- und Ausblenden in Sekunden fest. </p> </td> 
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

