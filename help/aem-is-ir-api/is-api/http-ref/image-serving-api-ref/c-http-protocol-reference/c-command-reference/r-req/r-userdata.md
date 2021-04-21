---
description: Benutzerdaten aus dem Bildkatalog. Gibt Benutzerdaten für den im URL-Pfad angegebenen Bildkatalogeintrag zurück.
solution: Experience Manager
title: userdata
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '193'
ht-degree: 2%

---


# userdata{#userdata}

Benutzerdaten aus dem Bildkatalog. Gibt Benutzerdaten für den im URL-Pfad angegebenen Bildkatalogeintrag zurück.

`req=userdata[,text|{xml[, *`Kodierung`*]}|json]`

<table id="simpletable_F9D94C83865F4216BCF7987C32FACC46"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> Kodierung</span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> UTF-8 | UTF-16 | UTF-16LE | UTF-16BE | ISO-8859-1</span> </p></td> 
 </tr> 
</table>

Der Inhalt von `catalog::UserData` wird zurückgegeben. Wenn das Format &#39;text&#39; angegeben ist, werden alle Instanzen von `??` in `catalog::UserData`durch Zeilenende ersetzt und ein einzeiliger Abschlusszeichen (CR/LF) wird an das Ende angehängt. Wenn der URL-Pfad nicht zu einem gültigen Katalogeintrag aufgelöst wird, besteht die Antwort nur aus einem einzeiligen Terminator. Wenn das Format &quot;xml&quot;oder &quot;json&quot;angefordert wird, wird eine entsprechende Formatierung angewendet.

Andere Befehle in der Anforderungszeichenfolge werden ignoriert.

Die HTTP-Antwort kann zwischengespeichert werden, wobei die TTL auf `catalog::Expiration` basiert.

>[!NOTE]
>
>Der Doppelpunkt ist in Schlüsselnamen der userdata-Eigenschaft nicht zulässig.

Anforderungen, die das JSONP-Antwortformat unterstützen, können Sie den Namen des JS-Callback-Handlers mit der erweiterten Syntax des Parameters `req=` angeben:

`req=...,json [&handler = reqHandler ]`

`<reqHandler>` ist der Name des JS-Handlers, der in der JSONP-Antwort vorhanden ist. Es sind nur a-z-, A-Z- und 0-9-Zeichen zulässig. Optional. Die Standardgrenze ist `s7jsonResponse`.
