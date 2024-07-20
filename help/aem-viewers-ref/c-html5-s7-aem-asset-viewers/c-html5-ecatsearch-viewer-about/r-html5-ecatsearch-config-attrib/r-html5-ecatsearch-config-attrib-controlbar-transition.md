---
description: ControlBar.transition
solution: Experience Manager
title: ControlBar.transition
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: 2e08a62b-9499-41f8-927b-89bed972b4eb
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '118'
ht-degree: 1%

---

# ControlBar.transition{#controlbar-transition}

[!DNL ` [ControlBar.|<containerId>_controls.]transition=none|fade[, *`delaytohide`*[, *`duration`*]`]

<table id="table_F71AA834FE494949A2D4B569EA5E721F"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|fade </span> </p> </td> 
   <td colname="col2"> <p> Gibt den Effekttyp an, der zum Anzeigen oder Ausblenden der Steuerleiste und ihres Inhalts verwendet wird. Verwenden Sie <span class="codeph"> none </span> zum sofortigen Ein- und Ausblenden; <span class="codeph"> fade </span> bietet einen allmählichen Ein- und Ausblendeeffekt (wird in Internet Explorer 8 nicht unterstützt). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> delaytohide </span> </span> </p> </td> 
   <td colname="col2"> <p> Gibt die Zeit in Sekunden zwischen dem letzten Maus-/Touchereignis an, das die Steuerleiste registriert, und dem ausgeblendeten Zeitkontrollbalken. </p> <p> Wenn der Wert auf <span class="codeph"> -1 </span> festgelegt ist, wird der automatische Ausblendeffekt der Komponente nie Trigger und es wird immer auf dem Bildschirm angezeigt. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> Dauer </span> </span> </p> </td> 
   <td colname="col2"> <p> Legt die Dauer der Ein- und Ausblendung-Animation in Sekunden fest. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschaften {#section-f42369774e2740dcb399626a0e4e930e}

Optional. Dieser Befehl wird auf Touch-Geräten ignoriert, auf denen die automatische Ausblendung der Steuerleiste deaktiviert ist.

## Standard {#section-d016470e92a74f98a18c4ab3489410a5}

[!DNL `fade,2,0.5`]

## Beispiel {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

[!DNL `transition=none`]
