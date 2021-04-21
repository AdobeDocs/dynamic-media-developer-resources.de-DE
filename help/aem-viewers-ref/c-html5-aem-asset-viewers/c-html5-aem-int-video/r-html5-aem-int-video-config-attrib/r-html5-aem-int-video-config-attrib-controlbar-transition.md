---
description: Konfigurationsattribut für den interaktiven Video-Viewer.
solution: Experience Manager
title: ControlBar.transition
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,Business Practitioner
exl-id: a8bb32b4-0fd9-4887-98ef-31c3426092b6
translation-type: tm+mt
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '126'
ht-degree: 3%

---

# ControlBar.transition{#controlbar-transition}

Konfigurationsattribut für den interaktiven Video-Viewer.

` [ControlBar.|<containerId>_controls.]transition=none|fade[, *``*[, *`Delaytohidedauer`*]`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|fade</span> </p> </td> 
   <td colname="col2"> <p> Gibt den Effekttyp an, der zum Ein-/Ausblenden der Steuerleiste und ihres Inhalts verwendet wird. </p> <p>Für sofortiges Ein-/Ausblenden auf <span class="codeph"> none</span> setzen. </p> <p>Auf <span class="codeph"> Überblendung</span> setzen, um einen allmählichen Ein-/Ausblendeffekt zu erzielen. Nicht unterstützt in Internet Explorer 8. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> delaytohide</span></span> </p> </td> 
   <td colname="col2"> <p> Gibt die Zeit in Sekunden zwischen dem letzten Maus-/Touch-Ereignis an, das in der Steuerleiste registriert ist, und der Zeitsteuerungsleiste an. Wenn die Komponente auf <span class="codeph"> -1</span> eingestellt ist, wird ihr automatischer Ausblendeffekt nie Trigger und bleibt daher immer auf dem Bildschirm sichtbar. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> Dauer</span></span> </p> </td> 
   <td colname="col2"> <p> Legt die Dauer der Ein-/Ausblendeanimation in Sekunden fest. </p> </td> 
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
