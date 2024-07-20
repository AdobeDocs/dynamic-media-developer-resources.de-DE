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
   <td colname="col2"> <p> Steuert das Erscheinungsbild der Hauptansicht-Hervorhebung bei aktivem Flyout. Wenn der Wert auf <span class="codeph"> 0</span> festgelegt ist, wird der Bereich, der derzeit im Flyout-Fenster sichtbar ist, anhand von Stilen hervorgehoben, die von <span class="codeph"> .s7highlight</span> oder von <span class="codeph"> .s7cursor</span> CSS-Klassennamen bereitgestellt werden (abhängig vom Wert des Modifikators <span class="codeph"> highlightmode</span> ). Wenn die Komponente auf <span class="codeph"> 1</span> gesetzt ist, wechselt sie in den Modus "Umkehren", wobei der derzeit angezeigte Bereich entweder vollständig transparent ist (falls <span class="codeph"> markhlightMode</span> auf <span class="codeph"> highlight</span> eingestellt ist) oder mit dem CSS-Klassennamen <span class="codeph"> .s7cursor</span> formatiert ist (in dem Fall, dass <span class="codeph"> marklightMode</span> auf <span class="codeph"> Cursor</span> festgelegt ist), jedoch umgibt, -Bereich wird mit den Stilen gefüllt, die vom CSS-Klassennamen <span class="codeph"> .s7overlay</span> bereitgestellt werden. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschaften {#section-5526a5d19e7e4ee2a35b1c4816ed4202}

Optional.

## Standard {#section-a08032f0fcf041c09e63c0238a339fc9}

`0`

## Beispiel {#section-0338be21edd04ff1a3bed5c8319b61a4}

`overlay=1`
