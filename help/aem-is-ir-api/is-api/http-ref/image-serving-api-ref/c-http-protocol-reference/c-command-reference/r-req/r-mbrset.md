---
description: Daten mit Mehrfachbit-Rate.
solution: Experience Manager
title: mbrSet
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 0568a4a1-7d6a-453e-83bc-05c0cde0c0f8
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '252'
ht-degree: 0%

---

# mbrSet{#mbrset}

Daten mit Mehrfachbit-Rate.

`req=mbrSet[,text|xml[, *`encoding`*]][&fmt= *`fmtType`*]`

<table id="simpletable_D2B8704E09B34337870A257CD7CB5C56"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> encoding</span></span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> UTF-8 | UTF-16 | UTF-16LE | UTF-16BE | ISO-8859-1</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> fmtType</span></span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> f4m | m3u8</span> </p></td> 
 </tr> 
</table>

Gibt eine Text- oder XML-Antwort zurück, die eine Liste von URLs (und entsprechenden Bitraten) enthält, die den gültigen Videoeinträgen im Videoset entsprechen, der mit der Nettopfad-ID verknüpft ist.

Die vorherige Anforderung, dass ein gültiger Videoeintrag einen Wert für `catalog::VideoBitRate` enthält, wurde jetzt gelockert. Der Eintrag kann einen Wert für `catalog::VideoBitRate`*oder* `catalog::AudioBitRate`*oder* `catalog::TotalStreamBitRate` enthalten. Damit der Videoeintrag gültig ist, muss nur einer dieser Definitionen definiert werden. Beachten Sie, dass sich die Anforderungen für `catalog::Path` und eine gültige Videodateierweiterung nicht geändert haben.

Die Antworten sind für die Nutzung durch Apple und Flash-Streaming-Server vorgesehen und entsprechen daher strukturell diesen Spezifikationen. URLs werden mit den Präfixen `attribute::HttpAppleStreamingContext` und `attribute::HttpFlashStreamingContext` generiert.

m3u8-Antworten enthalten nur MP4-Dateien, wenn im Videoset vorhanden sind. Wenn keine MP4-Dateien vorhanden sind, enthalten diese Antworten nur f4v-Dateien. Wenn keine MP4- oder f4v-Dateien vorhanden sind, ist die Antwort leer.

f4m-Antworten enthalten nur f4v-Dateien, wenn im Videoset vorhanden sind. Wenn keine f4v-Dateien vorhanden sind, enthalten diese Antworten nur MP4-Dateien. Wenn keine f4v-Dateien oder mp4-Dateien vorhanden sind, ist die Antwort leer.

Die Bitraten, die in f4m/m3u8-Antworten angezeigt werden, entsprechen den Werten in `catalog::TotalStreamBitRate` (in entsprechende Einheiten konvertiert). Wenn `catalog::TotalStreamBitRate` nicht definiert ist, wird die Summe von `catalog::VideoBitRate` und `catalog::AudioBitRate` verwendet.

Die HTTP-Antwort kann zwischengespeichert werden, wobei die TTL auf `catalog::NonImgExpiration` basiert.
