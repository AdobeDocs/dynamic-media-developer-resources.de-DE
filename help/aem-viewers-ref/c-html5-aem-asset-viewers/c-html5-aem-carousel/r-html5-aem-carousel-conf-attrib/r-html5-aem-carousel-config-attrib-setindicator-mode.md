---
description: SetIndicator.mode
solution: Experience Manager
title: SetIndicator.mode
feature: Dynamic Media Classic,Viewer,SDK/API,Karussellbanner
role: Developer,User
exl-id: f228cf05-8b74-4f85-a02e-3bc084581529
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '74'
ht-degree: 5%

---

# SetIndicator.mode{#setindicator-mode}

`[SetIndicator.|<containerId>_setIndicator.]mode=numeric|dotted`

<table id="table_0BEA0B5FFDF64E5594B534B2A87A6D88"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> numeric|dotted</span> </p> </td> 
   <td colname="col2"> <p> Konfiguriert den Rendering-Stil des Set-Indikators. </p> <p>Wenn der Wert auf <span class="codeph"> dotted</span> festgelegt ist, rendert die Komponente identische Indikatoren für alle Seiten. </p> <p>Bei Festlegung auf <span class="codeph"> numerisch</span> wird in jedem Indikatorelement eine 1-basierte Seitenzahl eingefügt. </p> <p>Der Betriebsmodus <span class="codeph"> numeric</span> wird auf Geräten, die Touch-Eingaben vornehmen können, nicht unterstützt. Stattdessen verwendet die Komponente <span class="codeph"> gepunktete</span> auf solchen Geräten. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschaften {#section-1e637b22e8a44d759d588e47576891e6}

Optional.

## Standard {#section-71fb773f814649b2885aefee68073641}

`dotted`

## Beispiel {#section-bce98c31f08a4a0ab262fab7f95ba020}

`mode=numeric`
