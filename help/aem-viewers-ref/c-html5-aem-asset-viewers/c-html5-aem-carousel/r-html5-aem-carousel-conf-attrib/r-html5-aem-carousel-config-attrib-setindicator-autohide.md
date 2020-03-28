---
description: 'null'
seo-description: 'null'
seo-title: SetIndicator.autohide
solution: Experience Manager
title: SetIndicator.autohide
topic: Dynamic media
uuid: eb93ad7a-6176-47ed-92c6-2eb1afcac0eb
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# SetIndicator.autohide{#setindicator-autohide}

` [SetIndicator.|<containerId>_setIndicator.]autohide=0|1[, *`Grenze`*]`

<table id="table_0BEA0B5FFDF64E5594B534B2A87A6D88"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">0|1[,<span class="varname"> Grenze</span>]</span> </p> </td> 
   <td colname="col2"> <p> Konfiguriert das Verhalten zum automatischen Ausblenden in Abhängigkeit von der Anzahl der Seiten und der Laufzeit-Komponentengröße. </p> <p> <span class="codeph"> 0</span> deaktiviert das automatische Ausblenden. </p> <p> <span class="codeph"> 1</span> Aktiviert das automatische Ausblenden. Die Komponente blendet ihre Punkte aus, wenn mindestens eine der folgenden Bedingungen wahr wird: </p> <p> 
     <ul id="ul_A7F9C1DDC6AE44BAA348B3AD440A4EDD"> 
      <li id="li_39332158806445DF874C5A52F1331B8B">die Zeile mit Punkten breiter ist als die Laufzeit-Komponentenbreite oder </li> 
      <li id="li_E30BAC8B609147ADB8824000F5729B21">Die Anzahl der für diese Komponente festgelegten Seiten überschreitet die durch den <span class="codeph"><span class="varname"> Limit</span></span> -Parameter konfigurierte Grenze. </li> 
     </ul> </p> <p> Wenn Sie <span class="codeph"><span class="varname"> den Grenzwert</span></span> auf <span class="codeph"> -1</span> festlegen, wird die zweite Bedingung für das automatische Ausblenden deaktiviert. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschaften {#section-1e637b22e8a44d759d588e47576891e6}

Optional.

## Standard {#section-71fb773f814649b2885aefee68073641}

`1,10`

## Beispiel {#section-bce98c31f08a4a0ab262fab7f95ba020}

`autohide=0`
