---
description: 'null'
seo-description: 'null'
seo-title: ControlBar.Transition
solution: Experience Manager
title: ControlBar.Transition
topic: Dynamic media
uuid: 803df8d4-6fb9-49ef-a097-c883d4115fad
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# ControlBar.Transition{#controlbar-transition}

` [ControlBar.|<containerId>_controls.]transition=none|fade[, *``*[, *`Delaytohidedauer`*]`

<table id="table_76B7F064B9CD46BA86931A9C841F777B"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|fade</span> </p> </td> 
   <td colname="col2"> <p> Gibt den Effekttyp an, mit dem die Steuerleiste und ihr Inhalt ein- oder ausgeblendet werden. </p> <p>Verwenden Sie <span class="codeph"> keine</span> zum sofortigen Ein- und Ausblenden. Verwenden Sie <span class="codeph"> Fade</span> , um einen allmählichen Ein- und Ausblendeffekt zu erzielen. </p> <p>Fade wird in Internet Explorer 8 nicht unterstützt. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> delaytohide</span></span> </p> </td> 
   <td colname="col2"> <p>Gibt die Zeit in Sekunden zwischen dem letzten Maus-/Berührungsereignis an, das die Steuerleiste registriert, und der Zeitsteuerungsleiste an. </p> <p> Bei Festlegung auf <span class="codeph"> -1</span> löst die Komponente nie ihren Auto-Ausblendeffekt aus und bleibt immer auf dem Bildschirm sichtbar. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> Dauer</span></span> </p> </td> 
   <td colname="col2"> <p>Legt die Dauer der Animation zum Ein- und Ausblenden in Sekunden fest. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschaften {#section-65be9301796240e38f31818229da7acc}

Optional.

## Standard {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`fade,2,0.5`

## Beispiel {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`transition=none`
