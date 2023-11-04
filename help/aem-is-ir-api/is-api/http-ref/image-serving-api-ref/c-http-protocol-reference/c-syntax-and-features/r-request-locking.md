---
description: Um die Möglichkeiten zur Bearbeitung von Anfragen zu reduzieren, wird eine einfache Sperreinrichtung bereitgestellt.
solution: Experience Manager
title: Sperren von Anforderungen
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 7ac727ef-3775-4884-b9db-bfae171a0f9d
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '226'
ht-degree: 0%

---

# Sperren von Anforderungen{#request-locking}

Um die Möglichkeiten zur Bearbeitung von Anfragen zu reduzieren, wird eine einfache Sperreinrichtung bereitgestellt.

Wenn attribute::RequestLock festgelegt ist, muss ein Sperrwert in Form von `&xxxx`, wobei xxxx ein vierstelliger Hexadezimalwert ist. Dieser hexadezimale Wert wird mithilfe eines einfachen Hashalgorithmus generiert, der auf den *modifiers* Teil der Anfrage (nach dem &quot;?&quot; , der den URL-Pfad vom *modifiers*). Dies muss erfolgen, nachdem die Anforderung vollständig HTTP-kodiert wurde, aber bevor sie (optional) verschleiert wird. Nach dem Deaktivieren der Anforderung verwendet der Server denselben Hashing-Algorithmus für die Modifikatorzeichenfolge (mit Ausnahme der letzten 5 Zeichen, die den Sperrwert enthalten). Wenn der generierte Schlüssel nicht mit der Sperre übereinstimmt, wird die Anforderung abgelehnt.

>[!IMPORTANT]
>
>Wenn Sie diese Funktion aktivieren, beachten Sie, dass die Verwendung dieser Funktion bestimmte Einschränkungen aufweist, die Folgendes umfassen:<br>- In der Dynamic Media-Benutzeroberfläche werden möglicherweise nicht die richtigen Details für die **[!UICONTROL Zuletzt veröffentlicht]** -Feld. Dies wirkt sich jedoch nicht auf die Veröffentlichung aus.<br>- Derzeit funktioniert das HLS-Video-Streaming nicht, wenn **[!UICONTROL Verschleierung von Anfragen]** und **[!UICONTROL Sperren von Anforderungen]** aktiviert sind.<br>- Derzeit funktionieren einige Dynamic Media-Viewer nicht, wenn **[!UICONTROL Verschleierung von Anfragen]** und **[!UICONTROL Sperren von Anforderungen]** aktiviert sind.

C++-Beispielcode zum Generieren des Anforderungssperrwerts:

```
unsigned int lockValue(const char *str) 
{ 
    unsigned int sum = 0; 
    if (str == NULL) 
        return sum; 
    for (; *str; ++str) 
        sum = (sum*131 + *str) & 0xffff; 
    return sum; 
} 
```

## Verwandte Themen {#section-a6d45406c0354669ac581793e4fa8436}

[HTTP-Kodierung](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-http-encoding.md#reference-bb34dd13f316462695448acfa8f92df7), [Verschleierung von Anfragen](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-request-obfuscation.md#reference-895f65d6796c43bb9bad21a676ed714d), [attribute::RequestLock](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-requestlock.md#reference-8bbe2f581be847d3b9fa123e8e5e94b0)
