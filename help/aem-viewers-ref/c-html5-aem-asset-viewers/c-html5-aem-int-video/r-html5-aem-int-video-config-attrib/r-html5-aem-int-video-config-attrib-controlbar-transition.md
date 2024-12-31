---
title: ControlBar.transition
description: Konfigurationsattribut für den interaktiven Video-Viewer.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: a8bb32b4-0fd9-4887-98ef-31c3426092b6
source-git-commit: 17556c64af32c957ac25312e2a3288a8d86b5679
workflow-type: tm+mt
source-wordcount: '116'
ht-degree: 2%

---

# ControlBar.transition{#controlbar-transition}

Konfigurationsattribut für den interaktiven Video-Viewer.

` [ControlBar.|<containerId>_controls.]transition=none|fade[, *`DelayToHide`*[, *`duration`*]`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|fade</span> </p> </td> 
   <td colname="col2"> <p> Gibt den Effekttyp an, der zum Ein-/Ausblenden der Steuerleiste und ihres Inhalts verwendet wird. </p> <p>Auf „Keine <span class="codeph">" </span>, um sie sofort ein- oder auszublenden. </p> <p>Auf <span class="codeph"> Fade </span> eingestellt, um einen stufenweisen Ein-/Ausblendeffekt zu erzielen. Wird in Internet Explorer 8 nicht unterstützt. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> DelaytoHide</span></span> </p> </td> 
   <td colname="col2"> <p> Gibt die Zeit in Sekunden an, die zwischen dem letzten von der Steuerleiste registrierten Maus-/Touch-Ereignis und dem Ausblenden der Zeitsteuerleiste vergeht. Wenn auf <span class="codeph"> -1 festgelegt</span> wird der automatische Ausblendeffekt der Komponente niemals Trigger und bleibt daher immer auf dem Bildschirm sichtbar. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> Dauer</span></span> </p> </td> 
   <td colname="col2"> <p> Legt die Dauer der Ein-/Ausblendung in Sekunden fest. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschaften {#section-1e637b22e8a44d759d588e47576891e6}

Optional.

## Standard {#section-71fb773f814649b2885aefee68073641}

`fade,2,0.5`

## Beispiel {#section-bce98c31f08a4a0ab262fab7f95ba020}

```
transition=none
```
