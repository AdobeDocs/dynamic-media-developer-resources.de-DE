---
title: JSONP-Eigenschaften
description: Wenn jsonp als Antwortformat angegeben ist, werden die Antwortdaten mit JSONP (JavaScript Object Notation with Padding) formatiert und in einen JavaScript-Funktionsaufruf eingeschlossen.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 2294eb37-b362-438f-94bc-eb24ca641752
source-git-commit: d1df6e943747f9db12c08003647aee840fdfcc0a
workflow-type: tm+mt
source-wordcount: '200'
ht-degree: 0%

---

# JSONP-Eigenschaften{#jsonp-properties}

Wenn jsonp als Antwortformat angegeben ist, werden die Antwortdaten mit JSONP (JavaScript Object Notation with Padding) formatiert und in einen JavaScript-Funktionsaufruf eingeschlossen.

Der Client kann eine optionale eindeutige Anforderungskennung ( *`reqId`*) angeben, die in der Antwort zurückgegeben wird und es dem Client ermöglicht, mehrere asynchron empfangene Antworten zu unterscheiden. Eine typische Antwort weist die folgende allgemeine Struktur auf:

```
/*jsonp*/s7jsonResponse({ 
   " 
<varname>
  objectName 
</varname>. 
<varname>
  propertyName 
</varname>" : " 
<varname>
  propertyValue 
</varname>", 
   ... 
 }, " 
<varname>
  reqId 
</varname>" );
```

Die Funktion `s7jsonResponse` JavaScript muss vom Client definiert werden. In der einfachsten Form könnte die Funktion wie folgt aussehen:

```
var responseData; 
S7jsonResponse(data, reqId) 
{ 
 responseData = eval(data); 
}
```

Bei Anforderungen, die das JSONP-Antwortformat unterstützen, können Sie den Namen des JS-Callback-Handlers mit der erweiterten Syntax des Parameters `req=` angeben:

`req=...,json [&handler = reqHandler]`

Die Syntax `<reqHandler>` ist der Name des JS-Handlers, der in der JSONP-Antwort vorhanden ist. Es sind nur a-z, A-Z und 0-9 Zeichen zulässig. Optional. Der Standardwert ist `s7jsonResponse`.

Das Dynamic Media Image Serving Viewers-Paket enthält ein Dienstprogramm zum Anfordern und Analysieren von JSONP-formatierten Daten aus Image Serving.

Weitere Informationen zum JSONP-Format finden Sie unter [https://en.wikipedia.org/wiki/JSONP](https://en.wikipedia.org/wiki/JSONP) .

Weitere Informationen zum JSON-Format finden Sie unter [www.json.org](https://www.json.org/json-en.html) .

Siehe auch [req](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76).
