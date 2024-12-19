---
description: Bildset-Daten aus dem Bildkatalog. Gibt Bildsatzdaten für den im URL-Pfad angegebenen Bildkatalogeintrag zurück.
solution: Experience Manager
title: Bildsatz
feature: Dynamic Media Classic,SDK/API,Image Sets
role: Developer,User
exl-id: 730e7db9-47f0-4e96-8948-18b8185a5b7a
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '166'
ht-degree: 0%

---

# Bildsatz{#imageset}

Bildset-Daten aus dem Bildkatalog. Gibt Bildsatzdaten für den im URL-Pfad angegebenen Bildkatalogeintrag zurück.

`req=imageset[,text|javascript|{xml[, *`encoding`*]}|{json[&id= *`reqId`*]}]`

<table id="simpletable_86FF9E59B11D4C408F0D932D46CC2F8E"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> Kodierung</span></span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> UTF-8 | UTF-16 | UTF-16LE | UTF-16BE | ISO-8859-1</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> requestId</span></span> </p></td> 
  <td class="stentry"> <p>Eindeutige Anforderungskennung. </p></td> 
 </tr> 
</table>

Der Inhalt von `catalog::ImageSet` wird ohne weitere Änderungen zurückgegeben (mit Ausnahme der Zeichenfolgenlokalisierung, falls zutreffend), gefolgt von einem einzeiligen Abschlusszeichen (CR/LF). Wenn der URL-Pfad nicht in einen gültigen Katalogeintrag aufgelöst wird, besteht die Antwort nur aus einem einzeiligen Abschlusszeichen.

Andere Befehle in der Anfragezeichenfolge werden ignoriert. Die HTTP-Antwort kann basierend auf `catalog::NonImgExpiration` mit der TTL zwischengespeichert werden.

Bei Anfragen, die das JSONP-Antwortformat unterstützen, können Sie den Namen des JS-Callback-Handlers mithilfe der erweiterten Syntax `req=` Parameters angeben:

`req=...,json [&handler = reqHandler ]`

`<reqHandler>` ist der Name des JS-Handlers, der in der JSONP-Antwort vorhanden ist. Nur a-z, A-Z und 0-9 Zeichen sind zulässig. Optional. Der Standardwert ist `s7jsonResponse`.
