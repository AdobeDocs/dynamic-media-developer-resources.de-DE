---
description: Benutzerdaten aus dem Bildkatalog. Gibt Benutzerdaten für den im URL-Pfad angegebenen Bildkatalogeintrag zurück.
solution: Experience Manager
title: userdata
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: b1d85ea6-0e12-49a8-b1dc-4c64a672770b
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '189'
ht-degree: 0%

---

# userdata{#userdata}

Benutzerdaten aus dem Bildkatalog. Gibt Benutzerdaten für den im URL-Pfad angegebenen Bildkatalogeintrag zurück.

`req=userdata[,text|{xml[, *`encoding`*]}|json]`

<table id="simpletable_F9D94C83865F4216BCF7987C32FACC46"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> encoding</span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> UTF-8 | UTF-16 | UTF-16LE | UTF-16BE | ISO-8859-1</span> </p></td> 
 </tr> 
</table>

Der Inhalt von `catalog::UserData` wird zurückgegeben. Wenn das &quot;text&quot;-Format angegeben wird, werden alle Instanzen von `??` in `catalog::UserData`durch Zeilenende-Zeichen ersetzt und ein einzeiliger Endpunkt (CR/LF) wird an das Ende angehängt. Wenn der URL-Pfad nicht zu einem gültigen Katalogeintrag aufgelöst wird, besteht die Antwort nur aus einem einzeiligen Terminator. Wenn das Format &quot;xml&quot;oder &quot;json&quot;angefordert wird, wird eine entsprechende Formatierung angewendet.

Andere Befehle in der Anforderungszeichenfolge werden ignoriert.

Die HTTP-Antwort kann zwischengespeichert werden, wobei die TTL auf `catalog::Expiration` basiert.

>[!NOTE]
>
>Das Doppelpunkt-Zeichen ist in Schlüsselnamen der Benutzerdateneigenschaft nicht zulässig.

Bei Anforderungen, die das JSONP-Antwortformat unterstützen, können Sie den Namen des JS-Callback-Handlers mit der erweiterten Syntax des Parameters `req=` angeben:

`req=...,json [&handler = reqHandler ]`

`<reqHandler>` ist der Name des JS-Handlers, der in der JSONP-Antwort vorhanden ist. Es sind nur a-z, A-Z und 0-9 Zeichen zulässig. Optional. Der Standardwert ist `s7jsonResponse`.
