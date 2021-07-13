---
description: Die Videozeit ist die numerische Anzeige, die die aktuelle Zeit und Dauer des derzeit wiedergegebenen Videos anzeigt.
solution: Experience Manager
title: Videodauer
feature: Dynamic Media Classic,Viewer,SDK/API,interaktive Videos
role: Developer,User
exl-id: 90ec189e-6de4-44b3-8760-1e8636b919ba
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '203'
ht-degree: 2%

---

# Videodauer{#video-time}

Die Videozeit ist die numerische Anzeige, die die aktuelle Zeit und Dauer des derzeit wiedergegebenen Videos anzeigt.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

Die Schriftfamilie, Schriftgröße und Schriftfarbe für die Videozeit gehören zu den Eigenschaften, die CSS steuern kann. Sie kann auch relativ zur Steuerleiste, in der sie enthalten ist, durch CSS positioniert werden.

Das Erscheinungsbild der Videozeit wird mit der folgenden CSS-Klassenauswahl gesteuert:

```
.s7interactivevideoviewer .s7videotime
```

## CSS-Eigenschaften der Videodauer {#css-properties-of-video-time}

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Anfang </span> </p> </td> 
   <td colname="col2"> <p>Position vom oberen Rand, einschließlich Abstand. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> rechts </span> </p> </td> 
   <td colname="col2"> <p>Position vom rechten Rand, einschließlich Abstand. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p> Die Breite der Zeitsteuerung für Videos. Diese Eigenschaft ist erforderlich, damit Internet Explorer 8 oder höher ordnungsgemäß funktioniert. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Schriftfamilie  </span> </p> </td> 
   <td colname="col2"> <p>Die Schriftfamilie, die für die Zeitanzeige verwendet werden soll. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Schriftgröße  </span> </p> </td> 
   <td colname="col2"> <p>Die Schriftgröße, die für die Zeitanzeige verwendet werden soll. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> color </span> </p> </td> 
   <td colname="col2"> <p>Die Schriftfarbe für die Zeitanzeige. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Beispiel {#section-e8caea0a303c425a8a637c2a47c06355}

Legen Sie die Videozeit auf hellgrau (hexadezimal `#BBBBBB`) fest, die auf 12 Pixel skaliert, 15 Pixel von der oberen Ecke der Steuerleiste und 80 Pixel von der oberen und rechten Kante der Steuerleiste entfernt ist.

```
.s7interactivevideoviewer .s7videotime { 
top:15px; 
right:80px; 
font-size:12px; 
color:#BBBBBB; 
width:60px;  
}
```
