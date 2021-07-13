---
description: FlyoutZoomView.frametransition
solution: Experience Manager
title: FlyoutZoomView.frametransition
feature: Dynamic Media Classic,Viewer,SDK/API,Flyout
role: Developer,User
exl-id: 0b0a88a0-d736-4ab8-a25f-15d1689b0a48
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '69'
ht-degree: 10%

---

# FlyoutZoomView.frametransition{#flyoutzoomview-frametransition}

` [FlyoutZoomView.|<containerId>_flyout.]frametransition=none|fade[, *`Dauer`*]`

<table id="table_FC34B37AACFB4E92A37E1D2D93D5F0D2"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|fade</span> </p> </td> 
   <td colname="col2"> <p> Gibt den Typ des Effekts an, der auf die Hauptansicht bei der Asset-Änderung angewendet wird. Die <span class="codeph"> none</span> steht für keine Transition, die Hauptansichtsänderung erfolgt sofort. Die <span class="codeph">-Überblendung</span> aktiviert eine Überblendung, bei der das alte Bild ausgeblendet und das neue Bild eingeblendet wird. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> Dauer</span></span> </p> </td> 
   <td colname="col2"> <p> Anzahl der Sekunden, die der Abschluss der Animation dauert. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschaften {#section-5526a5d19e7e4ee2a35b1c4816ed4202}

Optional.

## Standard {#section-a08032f0fcf041c09e63c0238a339fc9}

Keine.

## Beispiel {#section-0338be21edd04ff1a3bed5c8319b61a4}

`frametransition=fade,1`
