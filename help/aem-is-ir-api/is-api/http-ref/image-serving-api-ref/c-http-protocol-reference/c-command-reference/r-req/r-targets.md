---
description: Zoomdaten zu Zielgruppen aus dem Bildkatalog. Gibt Zoomdaten für die Zielgruppe des Bildkatalogeintrags zurück, der im URL-Pfad angegeben ist.
seo-description: Zoomdaten zu Zielgruppen aus dem Bildkatalog. Gibt Zoomdaten für die Zielgruppe des Bildkatalogeintrags zurück, der im URL-Pfad angegeben ist.
seo-title: als Target vorsehen
solution: Experience Manager
title: als Target vorsehen
topic: Scene7 Image Serving - Image Rendering API
uuid: e20dcd2c-913a-4153-97c7-dfb190763e39
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# als Target vorsehen{#targets}

Zoomdaten zu Zielgruppen aus dem Bildkatalog. Gibt Zoomdaten für die Zielgruppe des Bildkatalogeintrags zurück, der im URL-Pfad angegeben ist.

`req=targets[,text|{xml[, *``*]}|{json[&id= *`encodingreqId`*]}]`

<table id="simpletable_D64E706258FD4A9C9C8026D97B472FCC"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> Kodierung</span></span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> UTF-8| UTF-16| UTF-16LE| UTF-16BE| ISO-8859-1</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> reqId</span></span> </p></td> 
  <td class="stentry"> <p>Eindeutige Anforderungskennung. </p></td> 
 </tr> 
</table>

Der Inhalt von `catalog::Targets` wird zurückgegeben. Wenn das Format &quot;text&quot;angefordert wird, `??` werden alle Instanzen von `catalog::Targets` in durch Zeilenende ersetzt und ein einzeiliger Abschlusszeichen ( `CR/LF`) wird an das Ende angehängt. Wenn der URL-Pfad nicht zu einem gültigen Katalogeintrag aufgelöst wird, besteht die Antwort nur aus einem einzeiligen Terminator. Wenn das Format &quot;xml&quot;oder &quot;json&quot;angefordert wird, wird eine entsprechende Formatierung angewendet.

Andere Befehle in der Anforderungszeichenfolge werden ignoriert.

The HTTP response is cacheable with the TTL based on `catalog::Expiration`.

Anforderungen, die das JSONP-Antwortformat unterstützen, können Sie den Namen des JS-Callback-Handlers mit der erweiterten Syntax des `req=` Parameters angeben:

`req=...,json [&handler = reqHandler ]`

`<reqHandler>` ist der Name des JS-Handlers, der in der JSONP-Antwort vorhanden ist. Es sind nur a-z-, A-Z- und 0-9-Zeichen zulässig. Optional. Die Standardgrenze ist `s7jsonResponse`.
