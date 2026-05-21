---
title: HTTP-Kodierung zum Rendern von Bildern
description: Befehlswerte müssen mit %xx Escape-Sequenzen http-kodiert sein, sodass die Wertzeichenfolgen die reservierten Zeichen '=', '&' und '%' nicht enthalten.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: a1efc4ce-a170-4bdb-8584-407e07113272
TQID: 'https://experienceleague.adobe.com/TNB9NbrGzMGS64CxHgj7aXlSHz8-KPBB0hMxB36mKvI'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 145
ht-degree: 2%

---

# HTTP-Kodierung zum Rendern von Bildern{#image-rendering-http-encoding}

Befehlswerte müssen mit %xx Escape-Sequenzen http-kodiert sein, sodass die Wertzeichenfolgen die reservierten Zeichen &#39;=&#39;, &#39;&amp;&#39; und &#39;%&#39; nicht enthalten.

Andernfalls gelten die standardmäßigen HTTP-Kodierungsregeln. Die HTTP-Spezifikation erfordert die Codierung der unsicheren Zeichen wie &#39; &#39; (Leerzeichen), &#39;&quot; (doppeltes Anführungszeichen), &#39;#&#39;, &#39;%&#39;, &#39;&lt;&#39; und &#39;>&#39; sowie aller Steuerzeichen wie `<return>` und `<tab>`.

**Achtung:** geschweifte Klammern { }, die als Trennzeichen für Anforderungsverschachtelungen verwendet werden, dürfen nicht kodiert werden. Einige E-Mail-Clients kodieren geschweifte Klammern in eingebetteten HTTP-Anfragen. Sollte dieses Problem auftreten, ermöglicht das Rendern von Bildern die Verwendung von Klammern ( ) anstelle von geschweiften Klammern.

## Beispiel {#section-3edc5b8ee2354220a281b01722ad337a}

`…&$text=rate&weight=85% 27#&…`

Das obige Anfragefragment muss wie folgt kodiert werden:

`…&$text=rate%26weight%3D85%25%2027%23&…`

## Verwandte Themen {#section-d31268a02fe345e3abf0a4eb95a1dac5}

[HTTP/1.1 Spezifikation (RFC 2616)](https://www.w3.org/Protocols/rfc2616/rfc2616.html)
