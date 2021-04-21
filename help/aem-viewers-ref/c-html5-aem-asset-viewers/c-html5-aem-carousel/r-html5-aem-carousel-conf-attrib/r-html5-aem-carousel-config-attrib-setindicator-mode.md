---
description: SetIndicator.mode
solution: Experience Manager
title: SetIndicator.mode
feature: Dynamic Media Classic,Viewers,SDK/API,Carousel Banners
role: Developer,Business Practitioner
exl-id: f228cf05-8b74-4f85-a02e-3bc084581529
translation-type: tm+mt
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '77'
ht-degree: 5%

---

# SetIndicator.mode{#setindicator-mode}

`[SetIndicator.|<containerId>_setIndicator.]mode=numeric|dotted`

<table id="table_0BEA0B5FFDF64E5594B534B2A87A6D88"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> numeric|dotted</span> </p> </td> 
   <td colname="col2"> <p> Konfiguriert den Renderstil des Satzindikators. </p> <p>Bei Festlegung auf <span class="codeph"> dotted</span> gibt die Komponente identische Indikatoren für alle Seiten wieder. </p> <p>Bei Festlegung auf <span class="codeph"> numerisch</span> wird in jedem Indikatorelement eine 1-basierte Seitenzahl eingefügt. </p> <p>Der Betriebsmodus <span class="codeph"> numerisch</span> wird auf Geräten, die Berührungseingabe ermöglichen, nicht unterstützt. Stattdessen verwendet die Komponente auf solchen Geräten <span class="codeph"> gepunktete</span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschaften {#section-1e637b22e8a44d759d588e47576891e6}

Optional.

## Standard {#section-71fb773f814649b2885aefee68073641}

`dotted`

## Beispiel {#section-bce98c31f08a4a0ab262fab7f95ba020}

`mode=numeric`
