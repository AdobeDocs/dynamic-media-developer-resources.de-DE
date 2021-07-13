---
description: Der Inhalt des gesamten Modifikatorteils der Anforderungszeichenfolge, einschließlich des optionalen Suffixes für die Sperre, kann durch Anwendung der standardmäßigen Base64-Kodierung verdeckt werden.
solution: Experience Manager
title: Verschleierung von Anfragen
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 358d714b-703d-418b-90c0-5940f5388c7d
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '224'
ht-degree: 1%

---

# Verschleierung von Anfragen{#request-obfuscation}

Der Inhalt des gesamten Modifikatorteils der Anforderungszeichenfolge, einschließlich des optionalen Suffixes für die Sperre, kann durch Anwendung der standardmäßigen Base64-Kodierung verdeckt werden.

Der Server versucht zu dekodieren, ob `attribute::RequestObfuscation` festgelegt ist. Wenn die Dekodierung fehlschlägt, wird die Anfrage abgelehnt. Wenn sowohl die Sperrung von Anforderungen als auch die Verschleierung von Anforderungen angewendet werden, muss das Suffix &quot;Sperren&quot;vor der Base64-Kodierung generiert und angehängt werden.

>[!IMPORTANT]
>
>Wenn Sie diese Funktion aktivieren, beachten Sie, dass die Verwendung dieser Funktion gewissen Einschränkungen unterliegt, darunter:<br>- Die Dynamic Media-Benutzeroberfläche zeigt möglicherweise nicht die richtigen Details für das Feld **[!UICONTROL Zuletzt veröffentlicht]** an. Dies wirkt sich jedoch nicht auf die Veröffentlichung aus.<br>- Derzeit funktioniert das HLS-Video-Streaming nicht, wenn die **[!UICONTROL Verschleierung]** von Anfragen und die  **[!UICONTROL Sperrung von]** Anfragen aktiviert sind.<br>- Derzeit funktionieren einige Dynamic Media-Viewer nicht, wenn die  **[!UICONTROL Verschleierung]** von Anfragen und die Sperrung von  **[!UICONTROL Anfragen]** aktiviert sind.

## Beispiel {#section-dd4bfab19aa040f8ba3f6e397c6b0941}

`http://server/myTemplate?$txt=my text string&$img=myImage`

kodiert in:

`http://server/myTemplate?dHh0PW15IHRleHQgc3RyaW5nJiRpbWc9bXlJbWFnZQ==`

Alle Vorkommen von &#39;=&#39;, &#39;&amp;&#39; und &#39;%&#39; in Wertzeichenfolgen müssen mit &#39;%xx&#39;-Kodierung maskiert werden, bevor die Anfrage verschleiert wird. Es ist nicht erforderlich, den *Modifikator*-Teil der Anforderung entweder vor oder nach der Verschleierung durch HTTP zu kodieren, selbst wenn die Anforderungssperrung angewendet wird, da die Base64-Kodierung für die HTTP-Übertragung sicher ist.

## Verwandte Themen {#section-7ea59724c97c4ee9a510dbbc1f79e564}

[HTTP-Kodierung](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-http-encoding.md#reference-bb34dd13f316462695448acfa8f92df7),  [Anforderungssperrung](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-request-locking.md#reference-4177193d20774daab0dbf206a927844c),  [Attribut::RequestObfuscation](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-requestobfuscation.md#reference-730a3330253343f893419ebd52baf0bd)
