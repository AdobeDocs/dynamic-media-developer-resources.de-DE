---
description: 'Zoom: Zielgruppendaten aus dem Bildkatalog. Gibt Zoom-Zieldaten für den Bildkatalogeintrag zurück, der im URL-Pfad angegeben ist.'
solution: Experience Manager
title: als Target vorsehen
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 58f7b1ad-8762-4d23-b320-6f69e75ecf63
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '186'
ht-degree: 2%

---

# als Target vorsehen{#targets}

Zoom: Zielgruppendaten aus dem Bildkatalog. Gibt Zoom-Zieldaten für den Bildkatalogeintrag zurück, der im URL-Pfad angegeben ist.

`req=targets[,text|{xml[, *``*]}|{json[&id= *`encodingreqId`*]}]`

<table id="simpletable_D64E706258FD4A9C9C8026D97B472FCC"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> encoding</span> </span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> UTF-8 | UTF-16 | UTF-16LE | UTF-16BE | ISO-8859-1</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> reqId</span></span> </p></td> 
  <td class="stentry"> <p>Eindeutige Anforderungskennung. </p></td> 
 </tr> 
</table>

Der Inhalt von `catalog::Targets` wird zurückgegeben. Wenn das Format &quot;text&quot;angefordert wird, werden alle Instanzen von `??` in `catalog::Targets` durch Zeilenende-Zeichen ersetzt und am Ende wird ein einzeiliger Zeilenende-Zeichen ( `CR/LF`) angehängt. Wenn der URL-Pfad nicht zu einem gültigen Katalogeintrag aufgelöst wird, besteht die Antwort nur aus einem einzeiligen Terminator. Wenn das Format &quot;xml&quot;oder &quot;json&quot;angefordert wird, wird eine entsprechende Formatierung angewendet.

Andere Befehle in der Anforderungszeichenfolge werden ignoriert.

Die HTTP-Antwort kann zwischengespeichert werden, wobei die TTL auf `catalog::Expiration` basiert.

Anforderungen, die das JSONP-Antwortformat unterstützen, ermöglichen es Ihnen, den Namen des JS-Callback-Handlers mit der erweiterten Syntax des Parameters `req=` anzugeben:

`req=...,json [&handler = reqHandler ]`

`<reqHandler>` ist der Name des JS-Handlers, der in der JSONP-Antwort vorhanden ist. Es sind nur a-z, A-Z und 0-9 Zeichen zulässig. Optional. Die Standardgrenze ist `s7jsonResponse`.
