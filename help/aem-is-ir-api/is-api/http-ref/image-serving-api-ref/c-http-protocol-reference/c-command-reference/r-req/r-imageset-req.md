---
description: Bildsatzdaten aus dem Bildkatalog. Gibt Bildsatzdaten für den im URL-Pfad angegebenen Bildkatalogeintrag zurück.
solution: Experience Manager
title: imageset
feature: Dynamic Media Classic,SDK/API,Image Sets
role: Developer,User
exl-id: 730e7db9-47f0-4e96-8948-18b8185a5b7a
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '166'
ht-degree: 0%

---

# imageset{#imageset}

Bildsatzdaten aus dem Bildkatalog. Gibt Bildsatzdaten für den im URL-Pfad angegebenen Bildkatalogeintrag zurück.

`req=imageset[,text|javascript|{xml[, *`encoding`*]}|{json[&id= *`reqId`*]}]`

<table id="simpletable_86FF9E59B11D4C408F0D932D46CC2F8E"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> encoding</span></span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> UTF-8 | UTF-16 | UTF-16LE | UTF-16BE | ISO-8859-1</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> requestId</span></span> </p></td> 
  <td class="stentry"> <p>Eindeutige Anforderungskennung. </p></td> 
 </tr> 
</table>

Der Inhalt von `catalog::ImageSet` wird ohne weitere Änderung zurückgegeben (außer der Zeichenfolgenlokalisierung, sofern zutreffend), gefolgt von einem einzeiligen Terminator (CR/LF). Wenn der URL-Pfad nicht zu einem gültigen Katalogeintrag aufgelöst wird, besteht die Antwort nur aus einem einzeiligen Terminator.

Andere Befehle in der Anforderungszeichenfolge werden ignoriert. Die HTTP-Antwort kann zwischengespeichert werden, wobei die TTL auf `catalog::NonImgExpiration` basiert.

Bei Anforderungen, die das JSONP-Antwortformat unterstützen, können Sie den Namen des JS-Callback-Handlers mit der erweiterten Syntax des Parameters `req=` angeben:

`req=...,json [&handler = reqHandler ]`

`<reqHandler>` ist der Name des JS-Handlers, der in der JSONP-Antwort vorhanden ist. Es sind nur a-z, A-Z und 0-9 Zeichen zulässig. Optional. Der Standardwert ist `s7jsonResponse`.
