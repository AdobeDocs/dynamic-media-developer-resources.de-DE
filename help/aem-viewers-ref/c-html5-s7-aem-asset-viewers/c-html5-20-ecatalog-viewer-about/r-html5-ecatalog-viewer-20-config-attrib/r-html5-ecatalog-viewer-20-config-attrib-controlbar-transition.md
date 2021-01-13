---
description: ControlBar.transition
solution: Experience Manager
title: ControlBar.transition
topic: Dynamic media
uuid: e029173b-c004-4be8-b304-d6e2183314ad
translation-type: tm+mt
source-git-commit: bf5873e5a6bdb859e19b15584ba85e9c106f853b
workflow-type: tm+mt
source-wordcount: '118'
ht-degree: 3%

---


# ControlBar.transition{#controlbar-transition}

` [ControlBar.|<containerId>_controls.]transition=none|fade[, *``*[, *`Delaytohidedauer`*]`

<table id="table_F71AA834FE494949A2D4B569EA5E721F"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|fade  </span> </p> </td> 
   <td colname="col2"> <p> Gibt den Effekttyp an, mit dem die Steuerleiste und ihr Inhalt ein- oder ausgeblendet werden. Verwenden Sie <span class="codeph"> none </span> zum sofortigen Ein- und Ausblenden; <span class="codeph"> verblassen </span> bietet einen allmählichen Ein- und Ausblendeffekt (nicht unterstützt in Internet Explorer 8). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> delaytohide  </span> </span> </p> </td> 
   <td colname="col2"> <p> Gibt die Zeit in Sekunden zwischen dem letzten Maus-/Berührungsereignis an, das die Steuerleiste registriert, und der Zeitsteuerungsleiste an. </p> <p> Bei Festlegung auf <span class="codeph"> -1 </span> wird der Trigger-Ausblendeffekt nie automatisch zugewiesen und bleibt immer sichtbar. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> Dauer  </span> </span> </p> </td> 
   <td colname="col2"> <p> Legt die Dauer der Animation zum Ein- und Ausblenden in Sekunden fest. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschaften {#section-f42369774e2740dcb399626a0e4e930e}

Optional. Dieser Befehl wird auf Touch-Geräten ignoriert, auf denen die Steuerungsleiste automatisch ausgeblendet wird.

## Standard {#section-d016470e92a74f98a18c4ab3489410a5}

`fade,2,0.5`

## Beispiel {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

`transition=none`
