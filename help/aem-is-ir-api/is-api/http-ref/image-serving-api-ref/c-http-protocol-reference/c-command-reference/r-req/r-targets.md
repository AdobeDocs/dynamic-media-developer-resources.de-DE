---
description: Zoom richtet sich an Daten aus dem Bildkatalog. Gibt Zoom-Zieldaten für den im URL-Pfad angegebenen Bildkatalogeintrag zurück.
solution: Experience Manager
title: als Target vorsehen
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 58f7b1ad-8762-4d23-b320-6f69e75ecf63
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '185'
ht-degree: 1%

---

# als Target vorsehen{#targets}

Zoom richtet sich an Daten aus dem Bildkatalog. Gibt Zoom-Zieldaten für den im URL-Pfad angegebenen Bildkatalogeintrag zurück.

`req=targets[,text|{xml[, *`encoding`*]}|{json[&id= *`reqId`*]}]`

<table id="simpletable_D64E706258FD4A9C9C8026D97B472FCC"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> Kodierung</span> </span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> UTF-8 | UTF-16 | UTF-16LE | UTF-16BE | ISO-8859-1</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> reqId</span></span> </p></td> 
  <td class="stentry"> <p>Eindeutige Anforderungskennung. </p></td> 
 </tr> 
</table>

Der Inhalt von `catalog::Targets` wird zurückgegeben. Wenn das Format „Text“ angefordert wird, werden alle `??` in `catalog::Targets` durch Zeilenabschlüsse ersetzt, und am Ende wird ein einzeiliger Abschluss ( `CR/LF`) angehängt. Wenn der URL-Pfad nicht in einen gültigen Katalogeintrag aufgelöst wird, besteht die Antwort nur aus einem einzeiligen Abschlusszeichen. Wenn das Format „xml“ oder „json“ angefordert wird, wird eine entsprechende Formatierung angewendet.

Andere Befehle in der Anfragezeichenfolge werden ignoriert.

Die HTTP-Antwort kann basierend auf `catalog::Expiration` mit der TTL zwischengespeichert werden.

Bei Anfragen, die das JSONP-Antwortformat unterstützen, können Sie den Namen des JS-Callback-Handlers mithilfe der erweiterten Syntax `req=` Parameters angeben:

`req=...,json [&handler = reqHandler ]`

`<reqHandler>` ist der Name des JS-Handlers, der in der JSONP-Antwort vorhanden ist. Nur a-z, A-Z und 0-9 Zeichen sind zulässig. Optional. Der Standardwert ist `s7jsonResponse`.
