---
description: Bild existiert.
solution: Experience Manager
title: vorhanden
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 810453f0-7b35-4eed-8b23-6b59a8300c50
TQID: 'https://experienceleague.adobe.com/JyGNYH5-vW7FbZbMcMk2mQFB7rrrzYd0FpvsBbI-Zi4'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 126
ht-degree: 2%

---

# vorhanden{#exists}

Bild existiert.

`req=exists[,text|javascript|xml|{json[&id= *`reqId`*]}]`

Eindeutige Anforderungskennung *`reqId`*

Gibt eine einzelne Eigenschaft mit dem Namen `catalogRecord.exists` zurück. Der Eigenschaftswert wird auf „1“ gesetzt, wenn der angegebene Katalogeintrag im Bild oder Standardkatalog vorhanden ist. Andernfalls wird er auf „0“ gesetzt. `req=exists` Anfragen an den `/is/content` Kontext zeigen an, dass ein bestimmter Datensatz im statischen Inhaltskatalog vorhanden ist oder nicht.

Andere Befehle in der Anfragezeichenfolge werden ignoriert. Die HTTP-Antwort kann basierend auf `attribute::NonImgExpiration` mit der TTL zwischengespeichert werden.

Bei Anfragen, die das JSONP-Antwortformat unterstützen, können Sie den Namen des JS-Callback-Handlers mithilfe der erweiterten Syntax `req=` Parameters angeben:

`req=...,json [&handler = reqHandler ]`

`<reqHandler>` ist der Name des JS-Handlers, der in der JSONP-Antwort vorhanden ist. Nur a-z, A-Z und 0-9 Zeichen sind zulässig. Optional. Der Standardwert ist `s7jsonResponse`.
