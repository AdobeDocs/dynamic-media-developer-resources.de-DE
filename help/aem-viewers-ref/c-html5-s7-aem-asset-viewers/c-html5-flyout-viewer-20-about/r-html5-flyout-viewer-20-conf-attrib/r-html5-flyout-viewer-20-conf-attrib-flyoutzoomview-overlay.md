---
title: FlyoutZoomView.overlay
description: FlyoutZoomView.overlay
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Flyout
role: Developer,User
exl-id: 7fbf24c6-900f-4e94-b879-3a8f95dc5c08
source-git-commit: 50dddf148345d2ca5243d5d7108fefa56d23dad6
workflow-type: tm+mt
source-wordcount: '104'
ht-degree: 4%

---

# FlyoutZoomView.overlay{#flyoutzoomview-overlay}

`[FlyoutZoomView.|<containerId>_flyout.]overlay=0|1`

<table id="table_D052090D052D4273B37872C0C7E09E4B"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> 0 | 1</span> </p> </td> 
   <td colname="col2"> <p> Steuert das Erscheinungsbild der Hauptansicht-Hervorhebung bei aktivem Flyout. Wenn auf <span class="codeph"> 0</span>, wird der Bereich, der derzeit im Flyout-Fenster sichtbar ist, mithilfe von Stilen hervorgehoben, die von <span class="codeph"> .s7highlight</span> oder <span class="codeph"> .s7cursor</span> CSS-Klassennamen (abhängig vom Wert von <span class="codeph"> highlightmode</span> -Modifikator). Wenn auf <span class="codeph"> 1</span> Komponente wird in den "umgekehrten"Modus versetzt, in dem der aktuell angezeigte Bereich entweder vollständig transparent ist (in dem Fall <span class="codeph"> highlightmode</span> auf <span class="codeph"> highlight</span>) oder mit <span class="codeph"> .s7cursor</span> CSS-Klassenname (in diesem Fall) <span class="codeph"> highlightmode</span> auf <span class="codeph"> Cursor</span>), der umliegende Bereich jedoch mit Stilen gefüllt wird, die von <span class="codeph"> .s7overlay</span> CSS-Klassenname. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschaften {#section-5526a5d19e7e4ee2a35b1c4816ed4202}

Optional.

## Standard {#section-a08032f0fcf041c09e63c0238a339fc9}

`0`

## Beispiel {#section-0338be21edd04ff1a3bed5c8319b61a4}

`overlay=1`
