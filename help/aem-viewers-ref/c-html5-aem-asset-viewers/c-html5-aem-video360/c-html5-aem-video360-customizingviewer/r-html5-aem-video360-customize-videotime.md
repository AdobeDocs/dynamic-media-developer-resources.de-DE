---
title: Videodauer
description: Die Videozeit ist die numerische Anzeige, die die aktuelle Zeit und Dauer des aktuell wiedergegebenen Videos anzeigt.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,360 VR Video
role: Developer,User
exl-id: 78657fd2-e805-4047-be0a-592143025986
TQID: 'https://experienceleague.adobe.com/MTc2VW3VBM3XSUlibEAzZ48PVrQuIXfQvuqhvKsoQuc'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: null
workflow-type: tm+mt
source-wordcount: 201
ht-degree: 0%

---

# Videodauer{#video-time}

Die Videozeit ist die numerische Anzeige, die die aktuelle Zeit und Dauer des aktuell wiedergegebenen Videos anzeigt.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

Die Schriftfamilie des Videos, die Schriftgröße und die Schriftfarbe gehören zu den Eigenschaften, die CSS steuern kann. Sie kann auch relativ zur Steuerleiste, die sie enthält, per CSS positioniert werden.

Das Erscheinungsbild der Videozeit wird mit dem folgenden CSS-Klassenselektor gesteuert:

```
.s7video360viewer .s7videotime
```

## CSS-Eigenschaften der Videozeit {#css-properties-of-video-time}

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Top-</span> </p> </td> 
   <td colname="col2"> <p>Position ab dem oberen Rahmen, einschließlich Auffüllung. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> rechte </span> </p> </td> 
   <td colname="col2"> <p>Position vom rechten Rand aus, einschließlich Abstand. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Breite </span> </p> </td> 
   <td colname="col2"> <p> Die Breite der Video-Zeitsteuerung. Diese Eigenschaft ist erforderlich, damit Internet Explorer 8 oder höher ordnungsgemäß funktioniert. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">-</span> </p> </td> 
   <td colname="col2"> <p>Die Schriftfamilie, die für die Zeitanzeige verwendet werden soll. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">-</span> </p> </td> 
   <td colname="col2"> <p>Die Schriftgröße, die für den Text der Zeitanzeige verwendet werden soll. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">-</span> </p> </td> 
   <td colname="col2"> <p>Die Schriftfarbe, die für die Zeitanzeige verwendet werden soll. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Beispiel** `#BBBBBB` - Legen Sie die Videozeit auf Hellgrau (Hexadezimalzahl) fest. Die Größe beträgt 12 Pixel, die Position 15 Pixel vom oberen Rand der Steuerleiste und 80 Pixel vom oberen und rechten Rand der Steuerleiste.

```
.s7video360viewer .s7videotime { 
top:15px; 
right:80px; 
font-size:12px; 
color:#BBBBBB; 
width:60px;  
}
```
