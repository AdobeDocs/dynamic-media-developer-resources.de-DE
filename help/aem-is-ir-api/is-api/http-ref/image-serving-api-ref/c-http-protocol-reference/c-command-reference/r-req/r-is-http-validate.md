---
description: Überprüfung anfordern.
solution: Experience Manager
title: validieren
feature: Dynamic Media Classic, SDK/API
role: Entwickler, Geschäftspraktiker
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '109'
ht-degree: 4%

---


# validieren{#validate}

Überprüfung anfordern.

`req=validate[,text|javascript|xml|{json[&id= *`reqId`*]}]`

<table id="simpletable_F214CDA7580A46C0B5CF14CF13AA9B0A"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> reqId</span> </span> </p> </td> 
  <td class="stentry"> <p>Eindeutige Anforderungskennung. </p></td> 
 </tr> 
</table>

Analysiert die Anforderungszeichenfolge so, als wäre `req=img` angegeben, ohne jedoch Variablen zu ersetzen und referenzierte Objekte (Bilder, ICC-Profile, Schriftarten usw.) auszuwerten. Die standardmäßige Fehlerantwort wird zurückgegeben, wenn die Analyse fehlschlägt. Andernfalls wird die folgende Eigenschaft zurückgegeben:

`request.isValid=1`

Die HTTP-Antwort kann nicht zwischengespeichert werden.

Anforderungen, die das JSONP-Antwortformat unterstützen, können Sie den Namen des JS-Callback-Handlers mit der erweiterten Syntax des Parameters `req=` angeben:

`req=...,json [&handler = reqHandler ]`

`<reqHandler>` ist der Name des JS-Handlers, der in der JSONP-Antwort vorhanden ist. Es sind nur a-z-, A-Z- und 0-9-Zeichen zulässig. Optional. Die Standardgrenze ist `s7jsonResponse`.
