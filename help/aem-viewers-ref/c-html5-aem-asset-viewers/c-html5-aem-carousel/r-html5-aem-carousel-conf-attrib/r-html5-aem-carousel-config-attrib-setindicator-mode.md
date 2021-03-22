---
description: SetIndicator.mode
solution: Experience Manager
title: SetIndicator.mode
uuid: cfb549c2-e0cf-46c3-b5b7-219c8c1bee94
feature: Dynamic Media Classic, Viewer, SDK/API, Karussell-Banner
role: Entwickler, Geschäftspraktiker
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
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
