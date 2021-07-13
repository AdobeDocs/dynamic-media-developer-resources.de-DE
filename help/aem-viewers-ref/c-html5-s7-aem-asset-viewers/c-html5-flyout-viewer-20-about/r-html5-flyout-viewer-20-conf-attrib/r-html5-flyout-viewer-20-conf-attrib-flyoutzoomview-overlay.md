---
description: FlyoutZoomView.overlay
solution: Experience Manager
title: FlyoutZoomView.overlay
feature: Dynamic Media Classic,Viewer,SDK/API,Flyout
role: Developer,User
exl-id: 7fbf24c6-900f-4e94-b879-3a8f95dc5c08
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '111'
ht-degree: 4%

---

# FlyoutZoomView.overlay{#flyoutzoomview-overlay}

`[FlyoutZoomView.|<containerId>_flyout.]overlay=0|1`

<table id="table_D052090D052D4273B37872C0C7E09E4B"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> 0 | 1</span> </p> </td> 
   <td colname="col2"> <p> Steuert das Erscheinungsbild der Hauptansicht-Hervorhebung bei aktivem Flyout. Wenn der Bereich auf <span class="codeph"> 0</span> gesetzt ist, wird der aktuell im Flyout-Fenster sichtbare Bereich mit Stilen hervorgehoben, die entweder von <span class="codeph"> .s7highlight</span> oder <span class="codeph"> .s7cursor</span> CSS-Klassennamen bereitgestellt werden (abhängig vom Wert des Modifikators <span class="codeph"> highlightmode</span> ). Wenn die Komponente auf <span class="codeph"> 1</span> gesetzt ist, wird der Modus "Umgekehrt"geöffnet, in dem der aktuell angezeigte Bereich entweder vollständig transparent ist (falls <span class="codeph"> markierungsmodus</span> auf <span class="codeph"> markiert ist) oder mit <span class="codeph"> .s7cursor</span> CSS-Klassenname formatiert ist (in Fall <span class="codeph"> marktmode</span> ist auf <span class="codeph"> Cursor</span> festgelegt, der umliegende Bereich wird jedoch mit Stilen gefüllt, die von <span class="codeph"> .s7overlay</span> CSS-Klassenname bereitgestellt werden.</span> </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschaften {#section-5526a5d19e7e4ee2a35b1c4816ed4202}

Optional.

## Standard {#section-a08032f0fcf041c09e63c0238a339fc9}

`0`

## Beispiel {#section-0338be21edd04ff1a3bed5c8319b61a4}

`overlay=1`
