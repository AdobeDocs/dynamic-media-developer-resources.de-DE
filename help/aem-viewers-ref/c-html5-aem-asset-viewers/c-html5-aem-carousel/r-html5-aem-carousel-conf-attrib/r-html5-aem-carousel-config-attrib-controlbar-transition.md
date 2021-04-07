---
description: Konfigurationsattribut für Karussell-Viewer.
solution: Experience Manager
title: ControlBar.transition
feature: Dynamic Media Classic, Viewer, SDK/API, Karussell-Banner
role: Entwickler, Geschäftspraktiker
exl-id: 260a1767-e49a-46e3-9c3d-23efa5c3228e
translation-type: tm+mt
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '133'
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
   <td colname="col2"> <p> Gibt die Zeit in Sekunden zwischen dem letzten Maus-/Touch-Ereignis an, das in der Steuerleiste registriert ist, und der Zeitsteuerungsleiste an. </p> <p>Wenn die Komponente auf <span class="codeph"> -1</span> eingestellt ist, wird ihr automatischer Ausblendeffekt nie Trigger und bleibt daher immer auf dem Bildschirm sichtbar. </p> </td> 
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
