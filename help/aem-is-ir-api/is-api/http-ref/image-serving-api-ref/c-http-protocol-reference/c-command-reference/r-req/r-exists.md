---
description: Bild existiert.
solution: Experience Manager
title: vorhanden
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 810453f0-7b35-4eed-8b23-6b59a8300c50
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '124'
ht-degree: 1%

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
