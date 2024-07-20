---
title: SetIndicator.mode
description: SetIndicator.mode
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Carousel Banners
role: Developer,User
exl-id: f228cf05-8b74-4f85-a02e-3bc084581529
source-git-commit: 5a7af31d6788ded908a5e1630a3b1b0723e6fb4b
workflow-type: tm+mt
source-wordcount: '64'
ht-degree: 4%

---

# SetIndicator.mode{#setindicator-mode}

`[SetIndicator.|<containerId>_setIndicator.]mode=numeric|dotted`

<table id="table_0BEA0B5FFDF64E5594B534B2A87A6D88"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> numeric|dotted</span> </p> </td> 
   <td colname="col2"> <p> Konfiguriert den Rendering-Stil des Set-Indikators. </p> <p>Wenn der Wert auf <span class="codeph"> gepunktete </span> festgelegt ist, rendert die Komponente identische Indikatoren für alle Seiten. </p> <p>Bei Festlegung auf <span class="codeph"> numeric</span> wird in jedem Indikatorelement eine 1-basierte Seitenzahl eingefügt. </p> <p>Der Betriebsmodus <span class="codeph"> numeric</span> wird auf Geräten mit Touch-Eingabe nicht unterstützt. Stattdessen verwendet die Komponente <span class="codeph"> gepunktete </span> auf solchen Geräten. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschaften {#section-1e637b22e8a44d759d588e47576891e6}

Optional.

## Standard {#section-71fb773f814649b2885aefee68073641}

`dotted`

## Beispiel {#section-bce98c31f08a4a0ab262fab7f95ba020}

`mode=numeric`
