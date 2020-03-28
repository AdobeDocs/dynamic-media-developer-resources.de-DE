---
description: Konfigurationsattribut für den interaktiven Video-Viewer.
seo-description: Konfigurationsattribut für den interaktiven Video-Viewer.
seo-title: ControlBar.Transition
solution: Experience Manager
title: ControlBar.Transition
topic: Dynamic media
uuid: cde4a5b9-4512-41a6-84ce-9f4fc2cc0399
translation-type: tm+mt
source-git-commit: 16838d04b005224fad6df215ab5bf8c25ef86fc7

---


# ControlBar.Transition{#controlbar-transition}

Konfigurationsattribut für den interaktiven Video-Viewer.

` [ControlBar.|<containerId>_controls.]transition=none|fade[, *``*[, *`Delaytohidedauer`*]`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|fade</span> </p> </td> 
   <td colname="col2"> <p> Gibt den Effekttyp an, der zum Ein-/Ausblenden der Steuerleiste und ihres Inhalts verwendet wird. </p> <p>Zum sofortigen Ein-/Ausblenden auf " <span class="codeph"> Ohne</span> "setzen. </p> <p>Auf <span class="codeph"> Überblenden</span> eingestellt, um einen allmählichen Ein-/Ausblendeffekt zu erzielen. Nicht unterstützt in Internet Explorer 8. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> delaytohide</span></span> </p> </td> 
   <td colname="col2"> <p> Gibt die Zeit in Sekunden zwischen dem letzten Maus-/Touch-Ereignis an, das in der Steuerleiste registriert ist, und der Zeitsteuerungsleiste an. Bei einem Wert von <span class="codeph"> -1</span> löst die Komponente nie den Effekt "Automatisch ausblenden"aus und bleibt daher immer auf dem Bildschirm sichtbar. </p> </td> 
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

