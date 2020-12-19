---
description: Stellt die maximale Anzahl von Frames dar, die im Voraus in jede Richtung geladen werden sollen, wenn die Rotationsansicht im Leerlauf ist.
seo-description: Stellt die maximale Anzahl von Frames dar, die im Voraus in jede Richtung geladen werden sollen, wenn die Rotationsansicht im Leerlauf ist.
seo-title: SpinView.maxloadradius
solution: Experience Manager
title: SpinView.maxloadradius
topic: Dynamic media
uuid: e1b9fa84-837c-465e-8d37-0b6867404cae
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '169'
ht-degree: 2%

---


# SpinView.maxloadradius{#spinview-maxloadradius}

Stellt die maximale Anzahl von Frames dar, die im Voraus in jede Richtung geladen werden sollen, wenn die Rotationsansicht im Leerlauf ist.

` [SpinView.|<containerId>_spinView.]maxloadradius= *``*[, *`valueHeighRes`*]`

<table id="table_06BEA037FA82467CAA88D1CA62AE972E"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> Wert</span></span> </p> </td> 
   <td colname="col2"> <p> Der Wert <span class="codeph"> -1</span> lädt alle Frames im Satz vorab. Die vorgeladenen Frames werden immer mit der ursprünglichen Auflösung angezeigt, mit der die SpinView ursprünglich geladen wurde. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> highRes</span></span> </p> </td> 
   <td colname="col2"> <p> Steuert die Qualität von vorab geladenen Frames. </p> <p>Bei Festlegung auf <span class="codeph"> 1</span> werden die Frames in hoher Qualität geladen und entsprechen der Größe der Komponente. </p> <p>Bei Festlegung auf <span class="codeph"> 0</span> wird nur die Kachel mit niedriger Auflösung geladen. </p> <p>Das Vorausladen in hoher Auflösung verbessert die Benutzerfreundlichkeit, insbesondere wenn die automatische Rotation aktiviert ist. Gleichzeitig wird die Beginn-Zeit verkürzt und der Netzwerkverbrauch erhöht, daher sollte er mit Vorsicht verwendet werden. Wenn eine hochauflösende Vorladung verwendet wird, befinden sich die vorab geladenen Frames immer in der ursprünglichen Auflösung, in der die Komponente ursprünglich geladen wurde. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschaften {#section-65be9301796240e38f31818229da7acc}

Optional.

## Standard {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`6,0`

## Beispiel {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`maxloadradius=12,1`
