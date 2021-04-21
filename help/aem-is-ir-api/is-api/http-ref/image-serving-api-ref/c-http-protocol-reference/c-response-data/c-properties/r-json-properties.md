---
description: Wenn jsonp als Antwortformat angegeben ist, werden die Antwortdaten mithilfe von JSONP (JavaScript Object Notation with Padding) formatiert und in einen JavaScript-Funktionsaufruf eingeschlossen.
solution: Experience Manager
title: JSONP-Eigenschaften
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '211'
ht-degree: 1%

---


# JSONP-Eigenschaften{#jsonp-properties}

Wenn jsonp als Antwortformat angegeben ist, werden die Antwortdaten mithilfe von JSONP (JavaScript Object Notation with Padding) formatiert und in einen JavaScript-Funktionsaufruf eingeschlossen.

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

Die JavaScript-Funktion `s7jsonResponse` muss vom Client definiert werden. In seiner einfachsten Form könnte die Funktion wie folgt aussehen:

```
var responseData; 
S7jsonResponse(data, reqId) 
{ 
 responseData = eval(data); 
}
```

Anforderungen, die das JSONP-Antwortformat unterstützen, können Sie den Namen des JS-Callback-Handlers mit der erweiterten Syntax des Parameters `req=` angeben:

`req=...,json [&handler = reqHandler]`

`<reqHandler>` ist der Name des JS-Handlers, der in der JSONP-Antwort vorhanden ist. Es sind nur a-z-, A-Z- und 0-9-Zeichen zulässig. Optional. Die Standardgrenze ist `s7jsonResponse`.

Das Dynamic Media Image Serving Viewers-Paket enthält ein Dienstprogramm zum Anfordern und Parsen von JSONP-formatierten Daten aus Image Serving.

Weitere Informationen zum JSONP-Format finden Sie unter [http://en.wikipedia.org/wiki/JSONP](http://en.wikipedia.org/wiki/JSONP).

Weitere Informationen zum JSON-Format finden Sie unter [www.json.org](http://www.json.org).

Siehe auch [req](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76).
