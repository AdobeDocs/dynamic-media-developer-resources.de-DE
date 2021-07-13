---
description: SpinView.enableHD
solution: Experience Manager
title: SpinView.enableHD
feature: Dynamic Media Classic,Viewer,SDK/API,Gemischte Mediensets
role: Developer,User
exl-id: 0a2abdc6-eae5-4dda-b749-599cd8a07a98
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '90'
ht-degree: 6%

---

# SpinView.enableHD{#spinview-enablehd}

` [SpinView.|<containerId>_spinView.]enableHD=always|never|limit[, *`Nummer`*]`

<table id="table_8929B59833DE4E1C89FA4BCF07309809"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> always|never|limit</span> </p> </td> 
   <td colname="col2"> <p> Aktivieren, beschränken oder deaktivieren Sie die Optimierung für Geräte, bei denen <span class="codeph"> devicePixelRatio</span> größer ist als <span class="codeph"> 1</span>, d. h. Geräte mit einer High-Density-Anzeige wie iPhone4 und ähnliche Geräte. Wenn diese Option aktiviert ist, beschränkt die Komponente die Größe der IS-Bildanforderung so, als hätte das Gerät nur ein Pixelverhältnis von <span class="codeph"> 1</span> und reduziert daher die Bandbreite. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> Nummer</span></span> </p> </td> 
   <td colname="col2"> <p> Bei Verwendung der Einstellung <span class="codeph"> limit</span> ermöglicht die Komponente eine hohe Pixeldichte nur bis zum angegebenen Limit. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschaften {#section-65be9301796240e38f31818229da7acc}

Optional.

## Standard {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`limit,1500`

## Beispiel {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`enableHD=always`
