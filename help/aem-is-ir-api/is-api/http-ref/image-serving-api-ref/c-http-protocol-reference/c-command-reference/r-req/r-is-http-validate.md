---
description: Validierung anfordern.
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

Validierung anfordern.

`req=validate[,text|javascript|xml|{json[&id= *`reqId`*]}]`

<table id="simpletable_F214CDA7580A46C0B5CF14CF13AA9B0A"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> reqId</span> </span> </p> </td> 
  <td class="stentry"> <p>Eindeutige Anforderungskennung. </p></td> 
 </tr> 
</table>

Analysiert die Anforderungszeichenfolge so, als ob `req=img` angegeben wäre, jedoch ohne Variablen zu ersetzen und referenzierte Objekte (Bilder, ICC-Profile, Schriftarten usw.) zu bewerten. Die Standardfehlerantwort wird zurückgegeben, wenn das Parsen fehlschlägt, andernfalls wird die folgende Eigenschaft zurückgegeben:

`request.isValid=1`

Die HTTP-Antwort kann nicht zwischengespeichert werden.

Bei Anfragen, die das JSONP-Antwortformat unterstützen, können Sie den Namen des JS-Callback-Handlers mithilfe der erweiterten Syntax `req=` Parameters angeben:

`req=...,json [&handler = reqHandler ]`

`<reqHandler>` ist der Name des JS-Handlers, der in der JSONP-Antwort vorhanden ist. Nur a-z, A-Z und 0-9 Zeichen sind zulässig. Optional. Der Standardwert ist `s7jsonResponse`.
