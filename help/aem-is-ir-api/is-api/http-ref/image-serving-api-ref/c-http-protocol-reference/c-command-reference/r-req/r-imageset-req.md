---
description: Bildsatzdaten aus dem Bildkatalog. Gibt Bildsatzdaten für den Bildkatalogeintrag zurück, der im URL-Pfad angegeben ist.
seo-description: Bildsatzdaten aus dem Bildkatalog. Gibt Bildsatzdaten für den Bildkatalogeintrag zurück, der im URL-Pfad angegeben ist.
seo-title: imageset
solution: Experience Manager
title: imageset
topic: Scene7 Image Serving - Image Rendering API
uuid: 8854e903-a85f-403a-ae3d-b7281a236262
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '183'
ht-degree: 2%

---


# imageset{#imageset}

Bildsatzdaten aus dem Bildkatalog. Gibt Bildsatzdaten für den Bildkatalogeintrag zurück, der im URL-Pfad angegeben ist.

`req=imageset[,text|javascript|{xml[, *``*]}|{json[&id= *`encodingreqId`*]}]`

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

Der Inhalt von `catalog::ImageSet` wird ohne weitere Änderungen zurückgegeben (außer der String-lokale Anpassung, falls zutreffend), gefolgt von einem einzeiligen Abschlusszeichen (CR/LF). Wenn der URL-Pfad nicht zu einem gültigen Katalogeintrag aufgelöst wird, besteht die Antwort nur aus einem einzeiligen Terminator.

Andere Befehle in der Anforderungszeichenfolge werden ignoriert. Die HTTP-Antwort kann zwischengespeichert werden, wobei die TTL auf `catalog::NonImgExpiration` basiert.

Anforderungen, die das JSONP-Antwortformat unterstützen, können Sie den Namen des JS-Callback-Handlers mit der erweiterten Syntax des Parameters `req=` angeben:

`req=...,json [&handler = reqHandler ]`

`<reqHandler>` ist der Name des JS-Handlers, der in der JSONP-Antwort vorhanden ist. Es sind nur a-z-, A-Z- und 0-9-Zeichen zulässig. Optional. Die Standardgrenze ist `s7jsonResponse`.
