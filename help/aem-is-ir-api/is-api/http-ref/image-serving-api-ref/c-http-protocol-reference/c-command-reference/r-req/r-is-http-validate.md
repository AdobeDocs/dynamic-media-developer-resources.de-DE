---
description: Anforderungsvalidierung.
solution: Experience Manager
title: validieren
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 88424371-45a0-43bb-af49-2e8568b7b44c
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '103'
ht-degree: 1%

---

# validieren{#validate}

Anforderungsvalidierung.

`req=validate[,text|javascript|xml|{json[&id= *`reqId`*]}]`

<table id="simpletable_F214CDA7580A46C0B5CF14CF13AA9B0A"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> reqId</span> </span> </p> </td> 
  <td class="stentry"> <p>Eindeutige Anforderungskennung. </p></td> 
 </tr> 
</table>

Analysiert die Anforderungszeichenfolge so, als wäre `req=img` angegeben, ohne Variablen zu ersetzen und referenzierte Objekte (Bilder, ICC-Profile, Schriftarten usw.) zu evaluieren. Die standardmäßige Fehlerantwort wird zurückgegeben, wenn das Parsen fehlschlägt. Andernfalls wird die folgende Eigenschaft zurückgegeben:

`request.isValid=1`

Die HTTP-Antwort kann nicht zwischengespeichert werden.

Bei Anforderungen, die das JSONP-Antwortformat unterstützen, können Sie den Namen des JS-Callback-Handlers mit der erweiterten Syntax des Parameters `req=` angeben:

`req=...,json [&handler = reqHandler ]`

`<reqHandler>` ist der Name des JS-Handlers, der in der JSONP-Antwort vorhanden ist. Es sind nur a-z, A-Z und 0-9 Zeichen zulässig. Optional. Der Standardwert ist `s7jsonResponse`.
