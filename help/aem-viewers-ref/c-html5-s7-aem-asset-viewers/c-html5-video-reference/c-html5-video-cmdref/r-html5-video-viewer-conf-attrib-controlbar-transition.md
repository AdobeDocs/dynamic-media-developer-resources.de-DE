---
description: Konfigurationsattribut für Video Viewer.
seo-description: Konfigurationsattribut für Video Viewer.
seo-title: ControlBar.transition
solution: Experience Manager
title: ControlBar.transition
topic: Dynamic media
uuid: abd98898-d7d8-468f-b696-052e61e171b5
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '123'
ht-degree: 3%

---


# ControlBar.transition{#controlbar-transition}

Konfigurationsattribut für Video Viewer.

` [ControlBar.|<containerId>_controls.]transition=none|fade[, *``*[, *`Delaytohidedauer`*]`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|fade</span> </p> </td> 
   <td colname="col2"> <p> Gibt den Effekttyp an, mit dem die Steuerleiste und ihr Inhalt ein- oder ausgeblendet werden. </p> <p>Verwenden Sie <span class="codeph"> none</span> zum sofortigen Ein- und Ausblenden. Verwenden Sie &lt; a0/&gt; fade<span class="codeph">, um einen allmählichen Ein- und Ausblendeffekt zu erzielen.</span> </p> <p>Fade wird in Internet Explorer 8 nicht unterstützt. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> delaytohide</span> </span> </p> </td> 
   <td colname="col2"> <p>Gibt die Zeit in Sekunden zwischen dem letzten Maus-/Berührungsereignis an, das die Steuerleiste registriert, und der Zeitsteuerungsleiste an. </p> <p> Wenn die Komponente auf <span class="codeph"> -1</span> eingestellt ist, löst sie nie ihren automatischen Ausblendeffekt aus und bleibt immer auf dem Bildschirm sichtbar. </p> </td> 
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

