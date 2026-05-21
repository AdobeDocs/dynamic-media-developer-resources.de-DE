---
description: Um Manipulationsmöglichkeiten bei Anfragen zu reduzieren, ist eine einfache Sperrmöglichkeit vorgesehen.
solution: Experience Manager
title: Anforderungssperre
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 7ac727ef-3775-4884-b9db-bfae171a0f9d
TQID: 'https://experienceleague.adobe.com/9icGIK7meNSVUzYnsFBFM-GwG7KLe90bMDuqN89xmMk'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 229
ht-degree: 0%

---

# Anforderungssperre{#request-locking}

Um Manipulationsmöglichkeiten bei Anfragen zu reduzieren, ist eine einfache Sperrmöglichkeit vorgesehen.

Wenn das Attribut::RequestLock festgelegt ist, muss der Anfrage ein Sperrwert in Form von `&xxxx` angehängt werden, wobei xxxx ein vierstelliger Hexadezimalwert ist. Dieser Hexadezimalwert wird mithilfe eines einfachen Hash-Algorithmus generiert, der auf den *Modifiers*-Teil der Anfrage angewendet wird (nach dem &quot;?“, das den URL-Pfad von den *Modifiers*) trennt. Dies muss erfolgen, nachdem die Anfrage vollständig HTTP-codiert ist, aber bevor sie (optional) verschleiert wird. Nach der Deverschleierung der Anfrage verwendet der Server denselben Hash-Algorithmus für die Modifikatorzeichenfolge (mit Ausnahme der letzten 5 Zeichen, die den Sperrwert enthalten). Wenn der generierte Schlüssel nicht mit der Sperre übereinstimmt, wird die Anfrage abgelehnt.

>[!IMPORTANT]
>
>Wenn Sie diese Funktion aktivieren, beachten Sie, dass es bestimmte Einschränkungen bei ihrer Verwendung gibt, darunter die folgenden:<br>- Auf der Benutzeroberfläche von Dynamic Media werden möglicherweise nicht die richtigen Details für das Feld **[!UICONTROL Zuletzt veröffentlicht]** angezeigt. Dies wirkt sich jedoch nicht auf die Veröffentlichung aus.<br>- Derzeit funktioniert HLS-Video-Streaming nicht, wenn **[!UICONTROL Anfrageverschleierung]** und **[!UICONTROL Anfragensperrung]** aktiviert sind.<br>- Derzeit funktionieren einige Dynamic Media-Viewer nicht, wenn **[!UICONTROL Anfragenverschleierung]** und **[!UICONTROL Anfragensperrung]** aktiviert sind.

C++-Beispielcode zum Generieren des Werts der Anforderungssperre:

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

[HTTP-](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-http-encoding.md#reference-bb34dd13f316462695448acfa8f92df7), [Anfrage-](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-request-obfuscation.md#reference-895f65d6796c43bb9bad21a676ed714d), [attribute::RequestLock](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-requestlock.md#reference-8bbe2f581be847d3b9fa123e8e5e94b0)
