---
title: FlyoutZoomView.overlay
description: FlyoutZoomView.overlay
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Flyout
role: Developer,User
exl-id: 7fbf24c6-900f-4e94-b879-3a8f95dc5c08
source-git-commit: 50dddf148345d2ca5243d5d7108fefa56d23dad6
workflow-type: tm+mt
source-wordcount: '103'
ht-degree: 2%

---

# FlyoutZoomView.overlay{#flyoutzoomview-overlay}

`[FlyoutZoomView.|<containerId>_flyout.]overlay=0|1`

<table id="table_D052090D052D4273B37872C0C7E09E4B"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> 0|1</span> </p> </td> 
   <td colname="col2"> <p> Steuert die Darstellung der Hervorhebung in der Hauptansicht, wenn das Flyout aktiv ist. Bei <span class="codeph"> 0</span> wird der aktuell im Flyout-Fenster sichtbare Bereich mit Stilen hervorgehoben, die von <span class="codeph"> .s7highlightmode</span> oder <span class="codeph"> .s7cursor</span> CSS-Klassennamen bereitgestellt werden (abhängig vom Wert <span class="codeph"> Modifikators highlightmode</span>). Bei <span class="codeph"> 1 </span> die Komponente in den „inversen“ Modus, in dem der aktuell angezeigte Bereich entweder vollständig transparent ist (im Falle, <span class="codeph"> highlightmode</span> auf <span class="codeph"> highlight</span> gesetzt ist) oder mit <span class="codeph"> .s7cursor</span> CSS-Klassennamen formatiert ist (im Falle, <span class="codeph"> highlightmode</span> auf <span class="codeph"> cursor</span> gesetzt ist), aber der Umgebungsbereich mit Stilen gefüllt wird, die von <span class="codeph"> .s7overlay</span> CSS-Klassennamen bereitgestellt werden. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschaften {#section-5526a5d19e7e4ee2a35b1c4816ed4202}

Optional.

## Standard {#section-a08032f0fcf041c09e63c0238a339fc9}

`0`

## Beispiel {#section-0338be21edd04ff1a3bed5c8319b61a4}

`overlay=1`
