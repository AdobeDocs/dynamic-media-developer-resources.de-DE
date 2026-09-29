---
title: Videodauer
description: Die Videozeit ist die numerische Anzeige, die die aktuelle Zeit und Dauer des aktuell wiedergegebenen Videos anzeigt.
solution: Experience Manager, Experience Manager Assets
feature-set: Experience Manager, Experience Manager Assets
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop,Video
role: Developer,User
exl-id: 0ef09f06-c2d5-4c84-8ff9-4e94e9e54d40
TQID: 'https://experienceleague.adobe.com/Ln-FEgGu-vFMAL25NbhWYqoBm7NSN1waCeQE85xdxOk'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
    internal-label: Experience Manager
  - id: d09181b5-a36a-43de-ba01-36641440bc43
    internal-label: Experience Manager Assets
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
    internal-label: APIs
  - id: fe490c45-63fa-5b99-b5b4-d8cfeda8aa7d
    internal-label: SDK/API
  - id: bd0d2470-932c-4269-8eca-6d939b72d9ef
    internal-label: Dynamic Media
  - id: d4b6216b-4a89-4ff0-8ac0-5a699ba23100
    internal-label: Images and videos
subfeature_v2:
  - id: c12bda38-aa1a-4647-b62e-42cd4537dac6
    internal-label: Dynamic Media Classic
  - id: d17d085a-e808-49dd-b9a6-85a996b999bd
    internal-label: Viewers
  - id: a0cde32c-c339-4649-bd06-f1111bc952fc
    internal-label: Smart Crop
  - id: cb04d42d-1b70-43b0-9951-45998eb6e842
    internal-label: Video
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
    internal-label: Developer
source-git-commit: 0e24e07f8c91d3e7fda5510ed4252f9953e27467
workflow-type: tm+mt
source-wordcount: '199'
ht-degree: 0%
---
# Videodauer{#video-time}

Die Videozeit ist die numerische Anzeige, die die aktuelle Zeit und Dauer des aktuell wiedergegebenen Videos anzeigt.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

Die Schriftfamilie des Videos, die Schriftgröße und die Schriftfarbe gehören zu den Eigenschaften, die CSS steuern kann. Sie kann auch relativ zur Steuerleiste, die sie enthält, per CSS positioniert werden.

Das Erscheinungsbild der Videozeit wird mit dem folgenden CSS-Klassenselektor gesteuert:

```
.s7smartcropvideoviewer .s7videotime
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

## Beispiel {#section-e8caea0a303c425a8a637c2a47c06355}

Stellen Sie die Zeit für das Video auf Hellgrau (`#BBBBBB`) ein. Die Größe beträgt 12 Pixel, die Position 15 Pixel vom oberen Rand der Steuerleiste und 80 Pixel vom rechten Rand der Steuerleiste.

```
.s7smartcropvideoviewer .s7videotime { 
top:15px; 
right:80px; 
font-size:12px; 
color:#BBBBBB; 
width:60px;  
}
```
