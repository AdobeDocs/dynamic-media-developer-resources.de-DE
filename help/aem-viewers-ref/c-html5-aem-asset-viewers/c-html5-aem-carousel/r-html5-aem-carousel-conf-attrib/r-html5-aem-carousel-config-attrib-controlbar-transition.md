---
description: Konfigurationsattribut für Karussell-Viewer.
solution: Experience Manager
title: ControlBar.transition
feature: Dynamic Media Classic,Viewer,SDK/API,Karussellbanner
role: Developer,User
exl-id: 260a1767-e49a-46e3-9c3d-23efa5c3228e
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '130'
ht-degree: 3%

---

# ControlBar.transition{#controlbar-transition}

Konfigurationsattribut für Karussell-Viewer.

` [ControlBar.|<containerId>_controlBar.]transition=none|fade[, *``*[, *`delaytohideduration`*]`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|fade</span> </p> </td> 
   <td colname="col2"> <p> Gibt den Effekttyp an, der zum Anzeigen oder Ausblenden der Steuerleiste und ihres Inhalts verwendet wird. </p> <p>Legen Sie für sofortiges Anzeigen/Verbergen auf <span class="codeph"> none</span> fest. </p> <p>Setzen Sie sie auf <span class="codeph"> fade</span> , um einen allmählichen Ein-/Ausblendeffekt zu erzielen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> delaytohide</span></span> </p> </td> 
   <td colname="col2"> <p> Gibt die Zeit in Sekunden zwischen dem letzten Maus-/Touchereignis an, das von der Steuerleiste registriert wird, und dem ausgeblendeten Zeitkontrollbalken. </p> <p>Wenn der Wert auf <span class="codeph"> -1</span> festgelegt ist, wird der automatische Ausblendeffekt der Komponente nie Trigger und bleibt daher immer auf dem Bildschirm sichtbar. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> Dauer</span></span> </p> </td> 
   <td colname="col2"> <p> Legt die Dauer der Ein-/Ausblendung-Animation in Sekunden fest. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschaften {#section-1e637b22e8a44d759d588e47576891e6}

Optional. Dieser Befehl wird auf Touch-Geräten ignoriert, auf denen die automatische Ausblendung der Steuerleiste deaktiviert ist.

## Standard {#section-71fb773f814649b2885aefee68073641}

`fade,2,0.3`

## Beispiel {#section-bce98c31f08a4a0ab262fab7f95ba020}

```
transition=none
```
