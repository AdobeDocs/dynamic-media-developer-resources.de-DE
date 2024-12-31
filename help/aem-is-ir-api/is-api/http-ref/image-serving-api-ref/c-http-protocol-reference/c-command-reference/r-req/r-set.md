---
description: Informationen zu Mediensets.
solution: Experience Manager
title: setzen
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: bc69f094-ff21-4dd7-9e10-daddb3de0c65
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '142'
ht-degree: 1%

---

# setzen{#set}

Informationen zu Mediensets.

req=set[,xml[, *`encoding`*]|{json[&amp;id=*`reqId`*]}]

<table id="simpletable_02C955F4EBAD4251A728F0FC68F432B5"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> Kodierung</span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> UTF-8 | UTF-16 | UTF-16LE | UTF-16BE | ISO-8859-1</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> reqId</span> </p></td> 
  <td class="stentry"> <p>Eindeutige Anforderungskennung </p></td> 
 </tr> 
</table>

Gibt Informationen zu Bildern, Videos, Farbfeldern und verschiedenen Metadaten zurück, die mit „catalog:ImageSet“ für den im URL-Pfad angegebenen Bildkatalogeintrag verknüpft sind. Diese Antwort ist eine hierarchische Struktur, die durch den Typ des bereitgestellten Satzes bestimmt wird. Wenn das Format „xml“ oder „json“ angefordert wird, wird eine entsprechende Formatierung angewendet.

Die HTTP-Antwort kann basierend auf `catalog::NonImgExpiration` mit der TTL zwischengespeichert werden.

>[!NOTE]
>
>Der Doppelpunkt ist in req=set-Anforderungen nicht zulässig.

Bei Anfragen, die das JSON-Antwortformat unterstützen, können Sie den Namen des JS-Callback-Handlers mithilfe der erweiterten Syntax `req=` Parameters angeben:

`req=...,json [&handler = reqHandler ]`

`<reqHandler>` ist der Name des JS-Handlers, der in der JSONP-Antwort vorhanden ist. Nur a-z, A-Z und 0-9 Zeichen sind zulässig. Optional. Der Standardwert ist `s7jsonResponse`.
