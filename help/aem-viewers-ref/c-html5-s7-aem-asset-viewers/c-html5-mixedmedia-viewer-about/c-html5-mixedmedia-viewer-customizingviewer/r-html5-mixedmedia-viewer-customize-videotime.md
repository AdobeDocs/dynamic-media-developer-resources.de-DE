---
title: Videodauer
description: Die Videozeit ist die numerische Anzeige, die die aktuelle Zeit und Dauer des derzeit wiedergegebenen Videos anzeigt.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: 5efae314-5f37-4afc-9b9e-3108a8529e50
source-git-commit: cdc85af782ebc492ae2303469a7f4f54b5bc09c8
workflow-type: tm+mt
source-wordcount: '197'
ht-degree: 0%

---

# Videodauer{#video-time}

Die Videozeit ist die numerische Anzeige, die die aktuelle Zeit und Dauer des derzeit wiedergegebenen Videos anzeigt.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

Die Schriftfamilie, Schriftgröße und Schriftfarbe für die Videozeit gehören zu den Eigenschaften, die CSS steuern kann. Sie kann auch relativ zur Steuerleiste, in der sie enthalten ist, durch CSS positioniert werden.

Das Erscheinungsbild der Videozeit wird mit der folgenden CSS-Klassenauswahl gesteuert:

```
.s7mixedmediaviewer .s7videotime
```

## CSS-Eigenschaften der Videodauer {#css-properties-of-video-time}

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> top </span> </p> </td> 
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
   <td colname="col1"> <p> <span class="codeph"> Schriftfamilie </span> </p> </td> 
   <td colname="col2"> <p>Die Schriftfamilie, die für die Zeitanzeige verwendet werden soll. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size </span> </p> </td> 
   <td colname="col2"> <p>Die Schriftgröße, die für die Zeitanzeige verwendet wird. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> color </span> </p> </td> 
   <td colname="col2"> <p>Die Schriftfarbe für die Zeitanzeige. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Beispiel {#section-e8caea0a303c425a8a637c2a47c06355}

Legen Sie die Videozeit auf hellgrau (hexadezimal `#BBBBBB`) fest, die auf 12 Pixel skaliert, 15 Pixel von der oberen Ecke der Steuerleiste positioniert und 80 Pixel von den rechten Kanten der Steuerleiste entfernt ist.

```
.s7mixedmediaviewer .s7videotime { 
top:15px; 
right:80px; 
font-size:12px; 
color:#BBBBBB; 
width:60px;  
}
```
