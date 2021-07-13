---
description: Bild vorhanden.
solution: Experience Manager
title: vorhanden
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 810453f0-7b35-4eed-8b23-6b59a8300c50
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '126'
ht-degree: 3%

---

# vorhanden{#exists}

Bild vorhanden.

`req=exists[,text|javascript|xml|{json[&id= *`reqId`*]}]`

*`reqId`* eindeutige Anforderungskennung

Gibt eine einzelne Eigenschaft mit dem Namen `catalogRecord.exists` zurück. Der Eigenschaftswert wird auf &quot;1&quot;gesetzt, wenn der angegebene Katalogeintrag im Bild oder Standardkatalog vorhanden ist, andernfalls auf &quot;0&quot;. `req=exists` -Anfragen für den  `/is/content` Kontext geben an, ob ein bestimmter Datensatz im statischen Inhaltskatalog vorhanden ist oder nicht.

Andere Befehle in der Anforderungszeichenfolge werden ignoriert. Die HTTP-Antwort kann zwischengespeichert werden, wobei die TTL auf `attribute::NonImgExpiration` basiert.

Anforderungen, die das JSONP-Antwortformat unterstützen, ermöglichen es Ihnen, den Namen des JS-Callback-Handlers mit der erweiterten Syntax des Parameters `req=` anzugeben:

`req=...,json [&handler = reqHandler ]`

`<reqHandler>` ist der Name des JS-Handlers, der in der JSONP-Antwort vorhanden ist. Es sind nur a-z, A-Z und 0-9 Zeichen zulässig. Optional. Die Standardgrenze ist `s7jsonResponse`.
