---
title: ControlBar.transition
description: ControlBar.transition
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: c8792f02-ae15-4b47-8727-089691d5316a
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '109'
ht-degree: 2%

---

# ControlBar.transition{#controlbar-transition}

` [ControlBar.|<containerId>_controls.]transition=none|fade[, *`DelayToHide`*[, *`duration`*]`

<table id="table_76B7F064B9CD46BA86931A9C841F777B"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|fade</span> </p> </td> 
   <td colname="col2"> <p> Gibt den Effekttyp an, mit dem die Steuerleiste und ihr Inhalt ein- oder ausgeblendet werden. </p> <p>Verwenden Sie <span class="codeph"> Keine</span> zum sofortigen Ein- und Ausblenden. Verwenden Sie <span class="codeph"> </span>, um einen allmählichen Ein- und Ausblendeffekt zu erzielen. </p> <p>Fade wird in Internet Explorer 8 nicht unterstützt. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> DelaytoHide</span> </span> </p> </td> 
   <td colname="col2"> <p>Gibt die Zeit in Sekunden zwischen dem letzten Maus-/Touch-Ereignis an, das die Steuerleiste registriert, und der Zeit, die die Steuerleiste ausblendet. </p> <p> Trigger Bei <span class="codeph"> -1</span> ändert die Komponente ihren Effekt zum automatischen Ausblenden nicht und bleibt immer auf dem Bildschirm sichtbar. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> Dauer</span> </span> </p> </td> 
   <td colname="col2"> <p>Legt die Dauer der Ein- und Ausblendung in Sekunden fest. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschaften {#section-65be9301796240e38f31818229da7acc}

Optional.

## Standard {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`fade,2,0.5`

## Beispiel {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`transition=none`
