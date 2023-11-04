---
description: 'Zoom: Zielgruppendaten aus Bildkatalog. Gibt Zoom-Zieldaten für den Bildkatalogeintrag zurück, der im URL-Pfad angegeben ist.'
solution: Experience Manager
title: als Target vorsehen
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 58f7b1ad-8762-4d23-b320-6f69e75ecf63
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '179'
ht-degree: 2%

---

# als Target vorsehen{#targets}

Zoom: Zielgruppendaten aus Bildkatalog. Gibt Zoom-Zieldaten für den Bildkatalogeintrag zurück, der im URL-Pfad angegeben ist.

`req=targets[,text|{xml[, *`encoding`*]}|{json[&id= *`reqId`*]}]`

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

Der Inhalt von `catalog::Targets` zurückgegeben. Wenn das Format &quot;text&quot;angefordert wird, werden alle Instanzen von `??` in `catalog::Targets` durch Zeilenende-Zeichen und einen einzeiligen Abschlusszeichen ( `CR/LF`) wird an das Ende angehängt. Wenn der URL-Pfad nicht zu einem gültigen Katalogeintrag aufgelöst wird, besteht die Antwort nur aus einem einzeiligen Terminator. Wenn das Format &quot;xml&quot;oder &quot;json&quot;angefordert wird, wird eine entsprechende Formatierung angewendet.

Andere Befehle in der Anforderungszeichenfolge werden ignoriert.

Die HTTP-Antwort kann zwischengespeichert werden, wobei die TTL auf `catalog::Expiration`.

Bei Anforderungen, die das JSONP-Antwortformat unterstützen, können Sie den Namen des JS-Callback-Handlers mit der erweiterten Syntax von `req=` Parameter:

`req=...,json [&handler = reqHandler ]`

`<reqHandler>` ist der Name des JS-Handlers, der in der JSONP-Antwort vorhanden ist. Es sind nur a-z, A-Z und 0-9 Zeichen zulässig. Optional. Die Standardgrenze ist `s7jsonResponse`.
