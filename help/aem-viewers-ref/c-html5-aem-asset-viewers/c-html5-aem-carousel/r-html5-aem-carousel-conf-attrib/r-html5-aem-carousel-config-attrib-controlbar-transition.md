---
description: Konfigurationsattribut für Karussell-Viewer.
seo-description: Konfigurationsattribut für Karussell-Viewer.
seo-title: ControlBar.transition
solution: Experience Manager
title: ControlBar.transition
topic: Dynamic media
uuid: 80053511-f0e2-49f6-a1db-cd96c7788703
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '128'
ht-degree: 3%

---


# ControlBar.transition{#controlbar-transition}

Konfigurationsattribut für Karussell-Viewer.

` [ControlBar.|<containerId>_controlBar.]transition=none|fade[, *``*[, *`Delaytohidedauer`*]`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|fade</span> </p> </td> 
   <td colname="col2"> <p> Gibt den Effekttyp an, mit dem die Steuerleiste und ihr Inhalt ein- oder ausgeblendet werden. </p> <p>Für sofortiges Ein-/Ausblenden auf <span class="codeph"> none</span> setzen. </p> <p>Auf <span class="codeph"> Überblendung</span> setzen, um einen allmählichen Ein-/Ausblendeffekt zu erzielen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> delaytohide</span></span> </p> </td> 
   <td colname="col2"> <p> Gibt die Zeit in Sekunden zwischen dem letzten Maus-/Touch-Ereignis an, das in der Steuerleiste registriert ist, und der Zeitsteuerungsleiste an. </p> <p>Wenn die Komponente auf <span class="codeph"> -1</span> eingestellt ist, löst sie nie ihren Auto-Ausblendeffekt aus und bleibt daher immer auf dem Bildschirm sichtbar. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> Dauer</span></span> </p> </td> 
   <td colname="col2"> <p> Legt die Dauer der Ein-/Ausblendeanimation in Sekunden fest. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschaften {#section-1e637b22e8a44d759d588e47576891e6}

Optional. Dieser Befehl wird auf Touch-Geräten ignoriert, auf denen die Steuerungsleiste automatisch ausgeblendet wird.

## Standard {#section-71fb773f814649b2885aefee68073641}

`fade,2,0.3`

## Beispiel {#section-bce98c31f08a4a0ab262fab7f95ba020}

```
transition=none
```

