---
description: Medienset-Informationen.
seo-description: Medienset-Informationen.
seo-title: setzen
solution: Experience Manager
title: setzen
topic: Scene7 Image Serving - Image Rendering API
uuid: ebd78249-45ea-47cd-8845-786070f92f21
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '140'
ht-degree: 5%

---


# setzen{#set}

Medienset-Informationen.

req=set[,xml[, *`encoding`*]|{json[&amp;id=*`reqId`*]}]

<table id="simpletable_02C955F4EBAD4251A728F0FC68F432B5"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> Kodierung</span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> UTF-8 | UTF-16 | UTF-16LE | UTF-16BE | ISO-8859-1</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> reqId</span> </p></td> 
  <td class="stentry"> <p>Spezifische Anforderungskennung </p></td> 
 </tr> 
</table>

Gibt Informationen zu Bildern, Videos, Farbfeldern und verschiedenen Metadaten zurück, die mit catalog:ImageSet für den im URL-Pfad angegebenen Bildkatalogeintrag verknüpft sind. Diese Antwort ist eine hierarchische Struktur, die vom Typ des bereitgestellten Satzes bestimmt wird. Wenn das Format &quot;xml&quot;oder &quot;json&quot;angefordert wird, wird eine entsprechende Formatierung angewendet.

Die HTTP-Antwort kann zwischengespeichert werden, wobei die TTL auf `catalog::NonImgExpiration` basiert.

>[!NOTE]
>
>Das Doppelpunkt-Zeichen ist in Anforderungen von &quot;req=set&quot;nicht zulässig.

Anforderungen, die das JSON-Antwortformat unterstützen, können Sie den Namen des JS-Callback-Handlers mit der erweiterten Syntax des Parameters `req=` angeben:

`req=...,json [&handler = reqHandler ]`

`<reqHandler>` ist der Name des JS-Handlers in der JSONP-Antwort. Es sind nur a-z-, A-Z- und 0-9-Zeichen zulässig. Optional. Die Standardgrenze ist `s7jsonResponse`.
