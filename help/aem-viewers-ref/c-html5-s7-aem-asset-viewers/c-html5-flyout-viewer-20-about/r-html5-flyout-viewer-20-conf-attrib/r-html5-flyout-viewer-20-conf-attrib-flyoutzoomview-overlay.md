---
description: 'null'
seo-description: 'null'
seo-title: FlyoutZoomView.overlay
solution: Experience Manager
title: FlyoutZoomView.overlay
topic: Dynamic media
uuid: e6e9e97c-5d9b-47ca-bae3-ed3371c5ff9b
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# FlyoutZoomView.overlay{#flyoutzoomview-overlay}

`[FlyoutZoomView.|<containerId>_flyout.]overlay=0|1`

<table id="table_D052090D052D4273B37872C0C7E09E4B"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> 0 | 1</span> </p> </td> 
   <td colname="col2"> <p> Steuert das Erscheinungsbild der Hauptmarkierung der Ansicht, wenn der Flyout aktiv ist. Bei Festlegung auf <span class="codeph"> 0</span>wird der derzeit im Flyout-Fenster angezeigte Bereich mit Stilen hervorgehoben, die entweder von den CSS-Klassennamen <span class="codeph"> .s7highlight</span> oder <span class="codeph"> .s7cursor</span> bereitgestellt werden (abhängig vom Wert des Modifikators <span class="codeph"> highlightmode</span> ). Wenn die Komponente auf <span class="codeph"> 1</span> eingestellt ist, wird der Modus "inverse"geöffnet, wobei der aktuell angezeigte Bereich entweder vollständig transparent ist (falls <span class="codeph"> Highlightmode</span> auf <span class="codeph"> Highlight</span>eingestellt ist) oder mit dem CSS-Klassennamen <span class="codeph"> .s7cursor</span> formatiert ist (falls <span class="codeph"> highlightmode</span> <span class="codeph"></span><span class="codeph"></span> auf σWorkflow eingestellt ist). Der umliegende Bereich wird jedoch mit Stilen gefüllt, die von .s7overlay CSSCSS-Klassen. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschaften {#section-5526a5d19e7e4ee2a35b1c4816ed4202}

Optional.

## Standard {#section-a08032f0fcf041c09e63c0238a339fc9}

`0`

## Beispiel {#section-0338be21edd04ff1a3bed5c8319b61a4}

`overlay=1`
