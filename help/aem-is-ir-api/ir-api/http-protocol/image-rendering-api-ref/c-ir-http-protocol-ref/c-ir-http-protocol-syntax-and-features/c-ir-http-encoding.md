---
title: Bild-Rendering HTTP-Kodierung
description: Befehlswerte müssen mit %xx Escape-Sequenzen http-kodiert sein, sodass die Wertzeichenfolgen die reservierten Zeichen '=', '&' und '%' nicht enthalten.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: a1efc4ce-a170-4bdb-8584-407e07113272
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '135'
ht-degree: 2%

---

# Bild-Rendering HTTP-Kodierung{#image-rendering-http-encoding}

Befehlswerte müssen mit %xx Escape-Sequenzen http-kodiert sein, sodass die Wertzeichenfolgen die reservierten Zeichen &#39;=&#39;, &#39;&amp;&#39; und &#39;%&#39; nicht enthalten.

Andernfalls gelten die standardmäßigen HTTP-Kodierungsregeln. Die HTTP-Spezifikation erfordert die Kodierung der unsicheren Zeichen wie &#39; (Leerzeichen), &#39;&#39; (doppeltes Anführungszeichen), &#39;#&#39;, &#39;%&#39;, &#39;&lt;&#39; und &#39;>&#39; sowie aller Steuerzeichen wie `<return>` und `<tab>`.

**Vorsicht:** Geschweifte Klammern { }, die als Trennzeichen für Anfragen-Verschachtelungen verwendet werden, dürfen nicht kodiert werden. Manche E-Mail-Clients kodieren leider geschweifte Klammern in eingebetteten HTTP-Anforderungen. Sollte es sich bei diesem Problem um ein Problem handeln, ermöglicht das Bild-Rendering die Verwendung von Klammern ( ) anstelle von geschweiften Klammern.

## Beispiel {#section-3edc5b8ee2354220a281b01722ad337a}

`…&$text=rate&weight=85% 27#&…`

Das obige Anforderungsfragment muss wie folgt kodiert werden:

`…&$text=rate%26weight%3D85%25%2027%23&…`

## Verwandte Themen {#section-d31268a02fe345e3abf0a4eb95a1dac5}

[HTTP/1.1-Spezifikation (RFC 2616)](https://www.w3.org/Protocols/rfc2616/rfc2616.html)
