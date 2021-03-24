---
description: VideoPlayer.progressivebitrate
solution: Experience Manager
title: VideoPlayer.progressivebitrate
feature: Dynamic Media Classic,Viewer,SDK/API,Mix-Mediensets
role: Entwickler, Geschäftspraktiker
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '95'
ht-degree: 6%

---


# VideoPlayer.progressivebitrate{#videoplayer-progressivebitrate}

` [VideoPlayer.|<containerId>_videoPlayer.]progressivebitrate= *`Wert`*`

<table id="table_678AFC7BC06F41188F820502D2014C1F"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> Wert</span></span> </p> </td> 
   <td colname="col2"> <p> Gibt (in Kbit/s oder Kbit/s) die gewünschte Video-Bitrate an, die von einem adaptiven Video-Set wiedergegeben werden soll, falls das aktuelle System die adaptive Videowiedergabe nicht unterstützt. </p> <p>Die Komponente nimmt den Videostream mit der nächstmöglichen Bitrate (jedoch nicht über dem angegebenen Wert) ab. Wenn alle Videostreams im adaptiven Video-Set eine höhere Qualität als der angegebene Wert haben, wählt die Logik die Bitrate mit der niedrigsten Qualität. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Eigenschaften {#section-65be9301796240e38f31818229da7acc}

Optional.

## Standard {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`700`

## Beispiel {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`progressivebitrate=600`
