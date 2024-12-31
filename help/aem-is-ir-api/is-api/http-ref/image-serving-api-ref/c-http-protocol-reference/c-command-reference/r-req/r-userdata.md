---
description: Benutzerdaten aus dem Bildkatalog. Gibt Benutzerdaten für den im URL-Pfad angegebenen Bildkatalogeintrag zurück.
solution: Experience Manager
title: UserData
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: b1d85ea6-0e12-49a8-b1dc-4c64a672770b
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '189'
ht-degree: 0%

---

# UserData{#userdata}

Benutzerdaten aus dem Bildkatalog. Gibt Benutzerdaten für den im URL-Pfad angegebenen Bildkatalogeintrag zurück.

`req=userdata[,text|{xml[, *`Kodierung`*]}|json]`

<table id="simpletable_F9D94C83865F4216BCF7987C32FACC46"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> Kodierung</span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> UTF-8 | UTF-16 | UTF-16LE | UTF-16BE | ISO-8859-1</span> </p></td> 
 </tr> 
</table>

Der Inhalt von `catalog::UserData` wird zurückgegeben. Wenn das Format &#39;Text&#39; angegeben ist, werden alle Instanzen von `??` in `catalog::UserData`durch Zeilenabschlüsse ersetzt, und ein einzeiliger Abschluss (CR/LF) wird an das Ende angehängt. Wenn der URL-Pfad nicht in einen gültigen Katalogeintrag aufgelöst wird, besteht die Antwort nur aus einem einzeiligen Abschlusszeichen. Wenn das Format „xml“ oder „json“ angefordert wird, wird eine entsprechende Formatierung angewendet.

Andere Befehle in der Anfragezeichenfolge werden ignoriert.

Die HTTP-Antwort kann basierend auf `catalog::Expiration` mit der TTL zwischengespeichert werden.

>[!NOTE]
>
>Der Doppelpunkt ist in den Namen der Schlüssel der Benutzerdateneigenschaft nicht zulässig.

Bei Anfragen, die das JSONP-Antwortformat unterstützen, können Sie den Namen des JS-Callback-Handlers mithilfe der erweiterten Syntax `req=` Parameters angeben:

`req=...,json [&handler = reqHandler ]`

`<reqHandler>` ist der Name des JS-Handlers, der in der JSONP-Antwort vorhanden ist. Nur a-z, A-Z und 0-9 Zeichen sind zulässig. Optional. Der Standardwert ist `s7jsonResponse`.
