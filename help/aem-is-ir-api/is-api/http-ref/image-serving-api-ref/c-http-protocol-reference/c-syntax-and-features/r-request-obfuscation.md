---
description: Der Inhalt des gesamten Modifikator-Teils der Anforderungszeichenfolge, einschließlich des optionalen Suffix "lock", kann durch die Anwendung der Standard-Base64-Kodierung verdeckt werden.
seo-description: Der Inhalt des gesamten Modifikator-Teils der Anforderungszeichenfolge, einschließlich des optionalen Suffix "lock", kann durch die Anwendung der Standard-Base64-Kodierung verdeckt werden.
seo-title: Verschleierung anfordern
solution: Experience Manager
title: Verschleierung anfordern
topic: Scene7 Image Serving - Image Rendering API
uuid: 59b12a78-c4ba-4b6d-97bc-63150298ed73
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Verschleierung anfordern{#request-obfuscation}

Der Inhalt des gesamten Modifikator-Teils der Anforderungszeichenfolge, einschließlich des optionalen Suffix &quot;lock&quot;, kann durch die Anwendung der Standard-Base64-Kodierung verdeckt werden.

Der Server versucht zu dekodieren, wenn `attribute::RequestObfuscation` festgelegt. Wenn die Dekodierung fehlschlägt, wird die Anforderung abgelehnt. Wenn sowohl die Sperrung von Anforderungen als auch die Verschleierung von Anforderungen angewendet werden, muss das Suffix &quot;Sperren&quot;vor der Base64-Kodierung generiert und angehängt werden.

## Beispiel {#section-dd4bfab19aa040f8ba3f6e397c6b0941}

`http://server/myTemplate?$txt=my text string&$img=myImage`

kodiert in:

`http://server/myTemplate?dHh0PW15IHRleHQgc3RyaW5nJiRpbWc9bXlJbWFnZQ==`

Alle Vorkommnisse von &#39;=&#39;, &#39;&amp;&#39; und &#39;%&#39; in Wertzeichenfolgen müssen mit &#39;%xx&#39;-Kodierung Escape-Zeichen ausgeführt werden, bevor die Anforderung verschleiert wird. Es ist nicht notwendig, den *Modifikator* vor oder nach der Verschleierung per HTTP zu kodieren, auch wenn eine Sperrung der Anforderung angewendet wird, da die base64-Kodierung für die HTTP-Übertragung sicher ist.

## Verwandte Themen {#section-7ea59724c97c4ee9a510dbbc1f79e564}

[HTTP-Kodierung](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-http-encoding.md#reference-bb34dd13f316462695448acfa8f92df7), [Anforderungssperrung](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-request-locking.md#reference-4177193d20774daab0dbf206a927844c), [Attribut::RequestObfuscation](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-requestobfuscation.md#reference-730a3330253343f893419ebd52baf0bd)
