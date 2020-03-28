---
description: 'null'
seo-description: 'null'
seo-title: SpinView.maxloadradius
solution: Experience Manager
title: SpinView.maxloadradius
topic: Dynamic media
uuid: 8f475fa8-92d1-4663-bc12-1e65b76076ba
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# SpinView.maxloadradius{#spinview-maxloadradius}

` [SpinView.|<containerId>_spinView.]maxloadradius= *``*[, *`valueHeighRes`*]`

<table id="table_49FFD1BC53B846F09A6D214BC8C5C3FE"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> Wert</span></span> </p> </td> 
   <td colname="col2"> <p> Stellt die maximale Anzahl von Frames dar, die im Voraus in jede Richtung geladen werden sollen, wenn die Rotationsansicht im Leerlauf ist. Der Wert <span class="codeph"> -1</span> lädt alle Frames im Satz vorab. Die vorgeladenen Frames werden immer mit der ursprünglichen Auflösung angezeigt, mit der die SpinView ursprünglich geladen wurde. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> highRes</span></span> </p> </td> 
   <td colname="col2"> <p> Steuert die Qualität von vorab geladenen Frames. Wenn die Einstellung auf <span class="codeph"> 1</span> Frames festgelegt ist, werden hochqualitative Frames geladen, die der Größe der Komponente entsprechen. Bei Festlegung auf <span class="codeph"> 0</span> wird nur die Kachel mit niedriger Auflösung geladen. </p> <p>Das Vorausladen in hoher Auflösung verbessert die Benutzerfreundlichkeit, insbesondere wenn die automatische Rotation aktiviert ist. Gleichzeitig wird die Beginn-Zeit verkürzt und der Netzwerkverbrauch steigt, daher sollten Sie vorsichtig sein. Wenn eine hochauflösende Vorladung verwendet wird, befinden sich die vorgeladenen Frames immer in der ursprünglichen Auflösung, in der die Komponente ursprünglich geladen wurde. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschaften {#section-924163cb2f6542499f49894becef7fb5}

Optional.

## Standard {#section-7a2128fd488941948aff18421f533ccf}

`6,0`

## Beispiel {#section-622348a84fbe4ff4b5dd7eb53b044d83}

`maxloadradius=12,1`
