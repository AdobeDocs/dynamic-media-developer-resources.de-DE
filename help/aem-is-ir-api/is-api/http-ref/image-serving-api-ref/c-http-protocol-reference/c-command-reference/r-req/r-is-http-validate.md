---
description: Überprüfung anfordern.
seo-description: Überprüfung anfordern.
seo-title: validieren
solution: Experience Manager
title: validieren
topic: Scene7 Image Serving - Image Rendering API
uuid: 5322c484-2cf5-4022-9863-73fc525beb56
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# validieren{#validate}

Überprüfung anfordern.

`req=validate[,text|javascript|xml|{json[&id= *`reqId`*]}]`

<table id="simpletable_F214CDA7580A46C0B5CF14CF13AA9B0A"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> reqId</span></span> </p> </td> 
  <td class="stentry"> <p>Eindeutige Anforderungskennung. </p></td> 
 </tr> 
</table>

Analysiert die Anforderungszeichenfolge so, als `req=img` wären sie angegeben, ohne Variablen zu ersetzen und referenzierte Objekte (Bilder, ICC-Profile, Schriftarten usw.) auszuwerten. Die standardmäßige Fehlerantwort wird zurückgegeben, wenn die Analyse fehlschlägt. Andernfalls wird die folgende Eigenschaft zurückgegeben:

`request.isValid=1`

Die HTTP-Antwort kann nicht zwischengespeichert werden.

Anforderungen, die das JSONP-Antwortformat unterstützen, können Sie den Namen des JS-Callback-Handlers mit der erweiterten Syntax des `req=` Parameters angeben:

`req=...,json [&handler = reqHandler ]`

`<reqHandler>` ist der Name des JS-Handlers, der in der JSONP-Antwort vorhanden ist. Es sind nur a-z-, A-Z- und 0-9-Zeichen zulässig. Optional. Die Standardgrenze ist `s7jsonResponse`.
