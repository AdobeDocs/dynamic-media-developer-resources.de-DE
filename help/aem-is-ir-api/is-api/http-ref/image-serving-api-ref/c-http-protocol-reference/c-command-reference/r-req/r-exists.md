---
description: Bild vorhanden.
seo-description: Bild vorhanden.
seo-title: vorhanden
solution: Experience Manager
title: vorhanden
topic: Scene7 Image Serving - Image Rendering API
uuid: 5490e4c7-b52a-4b2e-b002-34afaa242c08
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '124'
ht-degree: 4%

---


# vorhanden{#exists}

Bild vorhanden.

`req=exists[,text|javascript|xml|{json[&id= *`reqId`*]}]`

*`reqId`* Kennung der eindeutigen Anforderung

Gibt eine einzelne Eigenschaft mit dem Namen `catalogRecord.exists` zurück. Der Eigenschaftswert wird auf &quot;1&quot;gesetzt, wenn der angegebene Katalogeintrag im Bild oder Standardkatalog vorhanden ist, andernfalls auf &quot;0&quot;. `req=exists` -Anfragen für den  `/is/content` Kontext weisen darauf hin, dass im statischen Inhaltskatalog ein bestimmter Datensatz vorhanden ist oder fehlt.

Andere Befehle in der Anforderungszeichenfolge werden ignoriert. Die HTTP-Antwort kann zwischengespeichert werden, wobei die TTL auf `attribute::NonImgExpiration` basiert.

Anforderungen, die das JSONP-Antwortformat unterstützen, können Sie den Namen des JS-Callback-Handlers mit der erweiterten Syntax des Parameters `req=` angeben:

`req=...,json [&handler = reqHandler ]`

`<reqHandler>` ist der Name des JS-Handlers, der in der JSONP-Antwort vorhanden ist. Es sind nur a-z-, A-Z- und 0-9-Zeichen zulässig. Optional. Die Standardgrenze ist `s7jsonResponse`.
