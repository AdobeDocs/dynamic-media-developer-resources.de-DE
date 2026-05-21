---
title: ControlBar.transition
description: Gibt den Effekttyp an, mit dem die Steuerleiste und ihr Inhalt ein- oder ausgeblendet werden.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: abe8affb-cbcd-4072-b2ed-91a398b1d678
TQID: 'https://experienceleague.adobe.com/x94JmgoSMd-qMO6jWpiIpgvbecaNljMEcgq2jXKYnf4'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 139
ht-degree: 2%

---

# ControlBar.transition{#controlbar-transition}

` [ControlBar.|<containerId>_controls.]transition=none|fade[, *`DelayToHide`*[, *`duration`*]`

<table id="table_F71AA834FE494949A2D4B569EA5E721F"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|fade </span> </p> </td> 
   <td colname="col2"> <p> Gibt den Effekttyp an, mit dem die Steuerleiste und ihr Inhalt ein- oder ausgeblendet werden. Verwenden Sie <span class="codeph"> None -</span> für die sofortige Ein- und Ausblendung. <span class="codeph"> Einblendeffekt bietet </span> einen allmählichen Ein- und Ausblendeffekt (wird in Internet Explorer 8 nicht unterstützt). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> DelaytoHide </span> </span> </p> </td> 
   <td colname="col2"> <p> Gibt die Zeit in Sekunden an, die zwischen dem letzten von der Steuerleiste registrierten Maus-/Berührungsereignis und dem Ausblenden der Zeitsteuerleiste liegt. </p> <p> Bei <span class="codeph"> -1 </span> wird der automatische Ausblendeffekt der Komponente niemals Trigger und sie bleibt immer auf dem Bildschirm sichtbar. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> Dauer </span> </span> </p> </td> 
   <td colname="col2"> <p> Legt die Dauer der Ein- und Ausblendung in Sekunden fest. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschaften {#section-f42369774e2740dcb399626a0e4e930e}

Optional. Dieser Befehl wird auf Touch-Geräten ignoriert, bei denen die automatische Ausblendung der Steuerleiste deaktiviert ist.

## Standard {#section-d016470e92a74f98a18c4ab3489410a5}

`fade,2,0.5`

## Beispiel {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

`transition=none`
