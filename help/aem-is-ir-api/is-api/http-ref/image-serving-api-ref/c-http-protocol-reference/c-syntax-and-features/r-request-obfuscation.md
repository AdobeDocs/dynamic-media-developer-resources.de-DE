---
description: Der Inhalt des gesamten Modifikatorteils der Anfragezeichenfolge, einschließlich des optionalen Sperrsuffix, kann durch Anwendung der standardmäßigen Base64-Codierung verdeckt werden.
solution: Experience Manager
title: Verschleierung anfordern
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 358d714b-703d-418b-90c0-5940f5388c7d
TQID: 'https://experienceleague.adobe.com/77Q5rV3cP4KoBz3rFKlEmBlumS0TBthuLbLQBETPitE'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 220
ht-degree: 1%

---

# Verschleierung anfordern{#request-obfuscation}

Der Inhalt des gesamten Modifikatorteils der Anfragezeichenfolge, einschließlich des optionalen Sperrsuffix, kann durch Anwendung der standardmäßigen Base64-Codierung verdeckt werden.

Der Server versucht zu decodieren, wenn `attribute::RequestObfuscation` festgelegt ist. Wenn die Decodierung fehlschlägt, wird die Anfrage abgelehnt. Wenn sowohl eine Anforderungssperre als auch eine Anforderungsverschleierung angewendet werden, muss das Sperrsuffix vor der Base64-Codierung generiert und angehängt werden.

>[!IMPORTANT]
>
>Wenn Sie diese Funktion aktivieren, beachten Sie, dass es bestimmte Einschränkungen bei ihrer Verwendung gibt, darunter die folgenden:<br>- Auf der Benutzeroberfläche von Dynamic Media werden möglicherweise nicht die richtigen Details für das Feld **[!UICONTROL Zuletzt veröffentlicht]** angezeigt. Dies wirkt sich jedoch nicht auf die Veröffentlichung aus.<br>- Derzeit funktioniert HLS-Video-Streaming nicht, wenn **[!UICONTROL Anfrageverschleierung]** und **[!UICONTROL Anfragensperrung]** aktiviert sind.<br>- Derzeit funktionieren einige Dynamic Media-Viewer nicht, wenn **[!UICONTROL Anfragenverschleierung]** und **[!UICONTROL Anfragensperrung]** aktiviert sind.

## Beispiel {#section-dd4bfab19aa040f8ba3f6e397c6b0941}

`http://server/myTemplate?$txt=my text string&$img=myImage`

Kodiert für:

`http://server/myTemplate?dHh0PW15IHRleHQgc3RyaW5nJiRpbWc9bXlJbWFnZQ==`

Alle Vorkommen von &#39;=&#39;, &#39;&amp;&#39; und &#39;%&#39; in Wertzeichenfolgen müssen mit &#39;%xx&#39;-Kodierung maskiert werden, bevor die Anfrage verschleiert wird. Es ist nicht erforderlich, den *Modifiers)-* der Anfrage vor oder nach der Verschleierung anderweitig mit HTTP zu codieren, selbst wenn eine Anforderungssperre angewendet wird, da die Base64-Codierung für die HTTP-Übertragung sicher ist.

## Verwandte Themen {#section-7ea59724c97c4ee9a510dbbc1f79e564}

[HTTP-](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-http-encoding.md#reference-bb34dd13f316462695448acfa8f92df7), [Anforderungssperrung](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-request-locking.md#reference-4177193d20774daab0dbf206a927844c), [attribute::RequestObfuscation](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-requestobfuscation.md#reference-730a3330253343f893419ebd52baf0bd)
