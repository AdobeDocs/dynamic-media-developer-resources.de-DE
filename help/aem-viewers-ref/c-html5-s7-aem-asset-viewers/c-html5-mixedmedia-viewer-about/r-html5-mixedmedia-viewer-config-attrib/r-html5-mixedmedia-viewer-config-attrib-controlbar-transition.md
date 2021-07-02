---
description: ControlBar.transition
solution: Experience Manager
title: ControlBar.transition
feature: Dynamic Media Classic,Viewer,SDK/API,Gemischte Mediensets
role: Developer,Business Practitioner
exl-id: c8792f02-ae15-4b47-8727-089691d5316a
source-git-commit: bfb350e68d9b7e86cec5ee75fe9280b12ce0e54e
workflow-type: tm+mt
source-wordcount: '117'
ht-degree: 3%

---

# ControlBar.transition{#controlbar-transition}

` [ControlBar.|<containerId>_controls.]transition=none|fade[, *``*[, *`delaytohideduration`*]`

<table id="table_76B7F064B9CD46BA86931A9C841F777B"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|fade</span> </p> </td> 
   <td colname="col2"> <p> Gibt den Effekttyp an, der zum Anzeigen oder Ausblenden der Steuerleiste und ihres Inhalts verwendet wird. </p> <p>Verwenden Sie <span class="codeph"> none</span> zum sofortigen Anzeigen und Verbergen. Verwenden Sie <span class="codeph"> fade</span>, um einen allmählichen Ein- und Ausblendeeffekt zu erzielen. </p> <p>Ausblenden wird in Internet Explorer 8 nicht unterstützt. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> delaytohide</span> </span> </p> </td> 
   <td colname="col2"> <p>Gibt die Zeit in Sekunden zwischen dem letzten Maus-/Touchereignis an, das die Steuerleiste registriert, und dem ausgeblendeten Zeitkontrollbalken. </p> <p> Wenn der Wert auf <span class="codeph"> -1</span> festgelegt ist, wird der automatische Ausblendeffekt der Komponente nie Trigger und bleibt immer auf dem Bildschirm sichtbar. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> duration</span> </span> </p> </td> 
   <td colname="col2"> <p>Legt die Dauer der Ein- und Ausblendung der Animation in Sekunden fest. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschaften {#section-65be9301796240e38f31818229da7acc}

Optional.

## Standard {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`fade,2,0.5`

## Beispiel {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`transition=none`
