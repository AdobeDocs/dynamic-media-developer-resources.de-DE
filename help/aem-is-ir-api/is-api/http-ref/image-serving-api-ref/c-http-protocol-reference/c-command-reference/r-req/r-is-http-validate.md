---
description: Validierung anfordern.
solution: Experience Manager
title: validieren
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 88424371-45a0-43bb-af49-2e8568b7b44c
TQID: 'https://experienceleague.adobe.com/TfgOIjG2q1CKAulErZYftqmKnCocuSF-H-dQTj4xsFI'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: null
workflow-type: tm+mt
source-wordcount: 105
ht-degree: 2%

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
