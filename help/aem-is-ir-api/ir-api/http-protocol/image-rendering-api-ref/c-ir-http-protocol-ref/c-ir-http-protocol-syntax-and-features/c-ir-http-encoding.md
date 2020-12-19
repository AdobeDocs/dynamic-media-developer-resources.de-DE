---
description: Befehlswerte müssen mit %xx Escape-Sequenzen http-kodiert werden, sodass die Wertzeichenfolgen nicht die reservierten Zeichen '=', '&' und '%' enthalten.
seo-description: Befehlswerte müssen mit %xx Escape-Sequenzen http-kodiert werden, sodass die Wertzeichenfolgen nicht die reservierten Zeichen '=', '&' und '%' enthalten.
seo-title: Image Rendering HTTP-Kodierung
solution: Experience Manager
title: Image Rendering HTTP-Kodierung
topic: Scene7 Image Serving - Image Rendering API
uuid: 37bd0040-7bad-4548-ab39-7f598a217732
translation-type: tm+mt
source-git-commit: 4439103ccd0d63afdd9ec20bd475560e8f84dcba
workflow-type: tm+mt
source-wordcount: '164'
ht-degree: 1%

---


# Image Rendering HTTP encoding{#image-rendering-http-encoding}

Befehlswerte müssen mit %xx Escape-Sequenzen http-kodiert werden, sodass die Wertzeichenfolgen nicht die reservierten Zeichen &#39;=&#39;, &#39;&amp;&#39; und &#39;%&#39; enthalten.

Andernfalls gelten Standard-HTTP-Kodierungsregeln. Die HTTP-Spezifikation erfordert die Kodierung der unsicheren Zeichen wie &#39; (Leerzeichen), &#39;&#39;(Dublette-Anführungszeichen), &#39;#&#39;, &#39;%&#39;, &#39;&lt;&#39; und &#39;>&#39; sowie aller Steuerzeichen wie `<return>` und `<tab>`.

**Vorsicht:** Geschweifte Klammern { }, die als Anforderungstrennzeichen verwendet werden, dürfen nicht kodiert werden. Bestimmte E-Mail-Clients kodieren unglücklicherweise geschweifte Klammern in eingebetteter HTTP-Anforderung. Sollte dies ein Problem sein, erlaubt das Image Rendering die Verwendung von Klammern ( ) anstelle von geschweiften Klammern.

## Beispiel {#section-3edc5b8ee2354220a281b01722ad337a}

`…&$text=rate&weight=85% 27#&…`

Das obige Anforderungsfragment muss wie folgt kodiert werden:

`…&$text=rate%26weight%3D85%25%2027%23&…`

## Verwandte Themen {#section-d31268a02fe345e3abf0a4eb95a1dac5}

[HTTP/1.1-Spezifikation (RFC 2616)](https://www.w3.org/Protocols/rfc2616/rfc2616.html)
