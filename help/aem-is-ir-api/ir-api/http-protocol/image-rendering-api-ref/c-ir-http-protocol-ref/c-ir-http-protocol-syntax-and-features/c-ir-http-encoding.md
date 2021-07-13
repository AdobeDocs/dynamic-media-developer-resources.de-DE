---
description: Befehlswerte müssen mit %xx Escape-Sequenzen http-kodiert sein, sodass die Wertzeichenfolgen die reservierten Zeichen '=', '&' und '%' nicht enthalten.
solution: Experience Manager
title: Bild-Rendering HTTP-Kodierung
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: a1efc4ce-a170-4bdb-8584-407e07113272
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '144'
ht-degree: 2%

---

# Bild-Rendering HTTP-Kodierung{#image-rendering-http-encoding}

Befehlswerte müssen mit %xx Escape-Sequenzen http-kodiert sein, sodass die Wertzeichenfolgen die reservierten Zeichen &#39;=&#39;, &#39;&amp;&#39; und &#39;%&#39; nicht enthalten.

Andernfalls gelten die standardmäßigen HTTP-Kodierungsregeln. Die HTTP-Spezifikation erfordert die Kodierung der unsicheren Zeichen wie &#39; (Leerzeichen), &#39;&#39; (doppeltes Anführungszeichen), &#39;#&#39;, &#39;%&#39;, &#39;&lt;&#39; und &#39;>&#39; sowie aller Steuerzeichen wie `<return>` und `<tab>`.

**Vorsicht:** Geschweifte Klammern { }, die als Trennzeichen für Anforderungsverschachtelungen verwendet werden, dürfen nicht kodiert werden. Manche E-Mail-Clients kodieren leider geschweifte Klammern in eingebetteten HTTP-Anforderungen. Sollte dies ein Problem sein, können beim Rendern von Bildern Klammern ( ) anstelle von geschweiften Klammern verwendet werden.

## Beispiel {#section-3edc5b8ee2354220a281b01722ad337a}

`…&$text=rate&weight=85% 27#&…`

Das obige Anforderungsfragment muss wie folgt kodiert werden:

`…&$text=rate%26weight%3D85%25%2027%23&…`

## Verwandte Themen {#section-d31268a02fe345e3abf0a4eb95a1dac5}

[HTTP/1.1-Spezifikation (RFC 2616)](https://www.w3.org/Protocols/rfc2616/rfc2616.html)
