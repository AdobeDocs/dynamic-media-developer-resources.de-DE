---
description: 'null'
seo-description: 'null'
seo-title: ZoomView.enableHD
solution: Experience Manager
title: ZoomView.enableHD
topic: Dynamic media
uuid: 5badee0b-3bbc-4306-bc60-a606775db2bd
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '78'
ht-degree: 10%

---


# ZoomView.enableHD{#zoomview-enablehd}

` [ZoomView.|<containerId>_zoomView.]enableHD=always|never|limit[, *`Nummer`*]`

<table id="table_0BEA0B5FFDF64E5594B534B2A87A6D88"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> always|never|limit</span> </p> </td> 
   <td colname="col2"> <p> Aktivieren, begrenzen oder deaktivieren Sie die Optimierung für Geräte, bei denen <span class="codeph"> devicePixelRatio</span> größer als <span class="codeph"> 1</span> ist. Betrifft Geräte mit hoher Auflösung, wie iPhone4 und ähnliche Geräte. Wenn sie aktiv ist, schränkt die Komponente die Größe der IS-Bildanforderung so ein, als hätte das Gerät ein Pixelverhältnis von <span class="codeph"> 1</span>, wodurch die Bandbreite verringert wird. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> Nummer</span></span> </p> </td> 
   <td colname="col2"> <p> Bei Verwendung der Limit-Einstellung ermöglicht die Komponente eine hohe Pixeldichte nur bis zum angegebenen Limit. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschaften {#section-1e637b22e8a44d759d588e47576891e6}

Optional.

## Standard {#section-71fb773f814649b2885aefee68073641}

`limit,1500`

## Beispiel {#section-bce98c31f08a4a0ab262fab7f95ba020}

`enableHD=always`
