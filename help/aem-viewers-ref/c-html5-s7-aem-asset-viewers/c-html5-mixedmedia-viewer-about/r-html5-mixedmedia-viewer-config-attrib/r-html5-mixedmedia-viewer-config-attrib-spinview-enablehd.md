---
description: 'null'
seo-description: 'null'
seo-title: SpinView.enableHD
solution: Experience Manager
title: SpinView.enableHD
topic: Dynamic media
uuid: 3e7cdb44-4366-4e84-a6c7-c1cf1f5e6344
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# SpinView.enableHD{#spinview-enablehd}

` [SpinView.|<containerId>_spinView.]enableHD=always|never|limit[, *`Nummer`*]`

<table id="table_8929B59833DE4E1C89FA4BCF07309809"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> always|never|limit</span> </p> </td> 
   <td colname="col2"> <p> Aktivieren, begrenzen oder deaktivieren Sie die Optimierung für Geräte, bei denen <span class="codeph"> devicePixelRatio</span> größer als <span class="codeph"> 1</span>ist, d. h. für Geräte mit hoher Auflösung wie iPhone4 und ähnliche Geräte. Wenn diese Option aktiviert ist, schränkt die Komponente die Größe der IS-Bildanforderung so ein, als hätte das Gerät nur ein Pixelverhältnis von <span class="codeph"> 1</span> und verringert dadurch die Bandbreite. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> Nummer</span></span> </p> </td> 
   <td colname="col2"> <p> Bei Verwendung der <span class="codeph"> Limit</span> -Einstellung ermöglicht die Komponente eine hohe Pixeldichte nur bis zum angegebenen Limit. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschaften {#section-65be9301796240e38f31818229da7acc}

Optional.

## Standard {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`limit,1500`

## Beispiel {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`enableHD=always`
