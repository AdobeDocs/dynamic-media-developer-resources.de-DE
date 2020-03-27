---
description: Daten mit mehreren Bitraten.
seo-description: Daten mit mehreren Bitraten.
seo-title: mbrSet
solution: Experience Manager
title: mbrSet
topic: Scene7 Image Serving - Image Rendering API
uuid: 829c44ce-c66a-49a9-ba69-9e8e94ef8921
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# mbrSet{#mbrset}

Daten mit mehreren Bitraten.

`req=mbrSet[,text|xml[, *``*]][&fmt= *`encodingfmtType`*]`

<table id="simpletable_D2B8704E09B34337870A257CD7CB5C56"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> Kodierung</span></span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> UTF-8| UTF-16| UTF-16LE| UTF-16BE| ISO-8859-1</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> fmtType</span></span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> f4m| m3u8</span> </p></td> 
 </tr> 
</table>

Gibt eine Text- oder XML-Antwort zurück, die eine Liste von URLs (und zugehörigen Bitraten) enthält, die den gültigen Videoeinträgen im Videoset entsprechen, die mit der net path-ID verknüpft sind.

Die vorherige Anforderung, dass ein gültiger Videoeintrag einen Wert für enthält, `catalog::VideoBitRate` wurde nun gelockert. Der Eintrag kann einen Wert für `catalog::VideoBitRate`*oder *`catalog::AudioBitRate`*oder* enthalten `catalog::TotalStreamBitRate`. Damit der Videoeintrag gültig ist, muss nur einer dieser Werte definiert werden. Beachten Sie, dass sich die Anforderungen für `catalog::Path` und eine gültige Videodateierweiterung nicht geändert haben.

Die Antworten sind für den Gebrauch durch Apple und Flash Streaming Server vorgesehen und entsprechen somit strukturell diesen Spezifikationen. URLs werden mit Präfixen `attribute::HttpAppleStreamingContext` und `attribute::HttpFlashStreamingContext`generiert.

m3u8-Antworten enthalten nur MP4-Dateien, wenn im Videoset vorhanden sind. Wenn keine MP4-Dateien vorhanden sind, enthalten diese Antworten nur f4v-Dateien. Wenn keine MP4- oder f4v-Dateien vorhanden sind, ist die Antwort leer.

f4m-Antworten enthalten nur f4v-Dateien, wenn im Videoset vorhanden sind. Wenn keine f4v-Dateien vorhanden sind, enthalten diese Antworten nur MP4-Dateien. Wenn keine f4v- oder mp4-Dateien vorhanden sind, ist die Antwort leer.

Bitraten, die in f4m/m3u8 Antworten angezeigt werden, entsprechen den Werten in `catalog::TotalStreamBitRate` (umgewandelt in entsprechende Einheiten). Wenn `catalog::TotalStreamBitRate` nicht definiert ist, wird die Summe von `catalog::VideoBitRate` und verwendet `catalog::AudioBitRate` .

The HTTP response is cacheable with the TTL based on `catalog::NonImgExpiration`.
