---
title: JSONP-Eigenschaften
description: Wenn jsonp als Antwortformat angegeben ist, werden die Antwortdaten mithilfe von JSONP (JavaScript Object Notation with Padding) formatiert, die in einen JavaScript-Funktionsaufruf eingeschlossen sind.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 2294eb37-b362-438f-94bc-eb24ca641752
TQID: 'https://experienceleague.adobe.com/pMirwhZ5n0mVuK2If4kJz3XDQZPDhORJCZBLsDf2C8I'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 212
ht-degree: 0%

---

# JSONP-Eigenschaften{#jsonp-properties}

Wenn jsonp als Antwortformat angegeben ist, werden die Antwortdaten mithilfe von JSONP (JavaScript Object Notation with Padding) formatiert, die in einen JavaScript-Funktionsaufruf eingeschlossen sind.

Der Client kann eine optionale eindeutige Anforderungskennung (*`reqId`*) angeben, die in der Antwort zurückgegeben wird und es dem Client ermöglicht, mehrere asynchron empfangene Antworten zu unterscheiden. Eine typische Antwort weist die folgende allgemeine Struktur auf:

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

Die `s7jsonResponse` JavaScript-Funktion muss vom Client definiert werden. In ihrer einfachsten Form könnte die Funktion wie folgt aussehen:

```
var responseData; 
S7jsonResponse(data, reqId) 
{ 
 responseData = eval(data); 
}
```

Bei Anfragen, die das JSONP-Antwortformat unterstützen, können Sie den Namen des JS-Callback-Handlers mithilfe der erweiterten Syntax `req=` Parameters angeben:

`req=...,json [&handler = reqHandler]`

Die `<reqHandler>` Syntax ist der Name des JS-Handlers, der in der JSONP-Antwort vorhanden ist. Nur a-z, A-Z und 0-9 Zeichen sind zulässig. Optional. Der Standardwert ist `s7jsonResponse`.

Das Paket Dynamic Media Image Serving Viewers enthält ein Dienstprogramm zum Anfordern und Analysieren von JSONP-formatierten Daten von Image Serving.

Weitere Informationen zum JSONP-](https://en.wikipedia.org/wiki/JSONP) finden Sie unter [https://en.wikipedia.org/wiki/JSONP.

Weitere Informationen zum JSON-](https://www.json.org/json-en.html) finden Sie unter [www.json.org.

Siehe auch [req](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76).
