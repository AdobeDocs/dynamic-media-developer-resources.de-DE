---
title: SetIndicator.autohide
description: SetIndicator.autohide
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Carousel Banners
role: Developer,User
exl-id: 75521239-a0be-4aa0-b65d-9a1f7d902cf2
source-git-commit: 5a7af31d6788ded908a5e1630a3b1b0723e6fb4b
workflow-type: tm+mt
source-wordcount: '83'
ht-degree: 3%

---

# SetIndicator.autohide{#setindicator-autohide}

` [SetIndicator.|<containerId>_setIndicator.]autohide=0|1[, *`limit`*]`

<table id="table_0BEA0B5FFDF64E5594B534B2A87A6D88"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">0|1[,<span class="varname"> Limit</span>]</span> </p> </td> 
   <td colname="col2"> <p> Konfiguriert das Verhalten zum automatischen Ausblenden in Abhängigkeit von der Anzahl der Seiten und der Größe der Laufzeitkomponenten. </p> <p> <span class="codeph"> 0</span> Deaktiviert die automatische Ausblendung. </p> <p> <span class="codeph"> 1</span> Aktiviert die automatische Ausblendung. Die Komponente blendet ihre Punkte aus, wenn mindestens eine der folgenden Bedingungen zutrifft: </p> <p> 
     <ul id="ul_A7F9C1DDC6AE44BAA348B3AD440A4EDD"> 
      <li id="li_39332158806445DF874C5A52F1331B8B">Die Zeile mit Punkten wird breiter als die Breite der Laufzeitkomponente oder </li> 
      <li id="li_E30BAC8B609147ADB8824000F5729B21">Die Anzahl der für diese Komponente festgelegten Seiten überschreitet das mit dem Parameter "<span class="codeph"><span class="varname"> Limit“ konfigurierte </span></span>. </li> 
     </ul> </p> <p> Wenn Sie <span class="codeph"><span class="varname"> Limit</span></span> auf <span class="codeph"> -1 setzen</span> wird die zweite Bedingung für das automatische Ausblenden deaktiviert. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschaften {#section-1e637b22e8a44d759d588e47576891e6}

Optional.

## Standard {#section-71fb773f814649b2885aefee68073641}

`1,10`

## Beispiel {#section-bce98c31f08a4a0ab262fab7f95ba020}

`autohide=0`
