---
description: Um die Möglichkeiten zur Bearbeitung von Anfragen zu reduzieren, wird eine einfache Sperrfunktion bereitgestellt.
seo-description: Um die Möglichkeiten zur Bearbeitung von Anfragen zu reduzieren, wird eine einfache Sperrfunktion bereitgestellt.
seo-title: Sperren von Anforderungen
solution: Experience Manager
title: Sperren von Anforderungen
topic: Scene7 Image Serving - Image Rendering API
uuid: 03239376-1e40-48d2-a396-c276802854ed
translation-type: tm+mt
source-git-commit: 021c1d1f975083af3950775e230d4f73cbf9e0ec
workflow-type: tm+mt
source-wordcount: '242'
ht-degree: 0%

---


# Anforderungssperrung{#request-locking}

Um die Möglichkeiten zur Bearbeitung von Anfragen zu reduzieren, wird eine einfache Sperrfunktion bereitgestellt.

Wenn attribute::RequestLock festgelegt ist, muss der Anforderung ein Sperrwert in Form von `&xxxx` angehängt werden, wobei xxxx ein vierstelliger Hexadezimalwert ist. Dieser Hexadezimalwert wird mithilfe eines einfachen Hashing-Algorithmus generiert, der auf den Abschnitt *Modifikatoren* der Anforderung angewendet wird (nach dem &#39;?&#39; , der den URL-Pfad von den Modifikatoren *a1/> trennt.* Dies muss erfolgen, nachdem die Anforderung vollständig HTTP-kodiert wurde, aber bevor sie (optional) verschleiert wird. Nach dem Entfernen der Verschleierung der Anforderung verwendet der Server denselben Hashing-Algorithmus für die Modifiziererzeichenfolge (mit Ausnahme der letzten 5 Zeichen, die den Sperrwert enthalten). Wenn der generierte Schlüssel nicht mit der Sperre übereinstimmt, wird die Anforderung abgelehnt.

>[!IMPORTANT]
>
>Wenn Sie diese Funktion aktivieren, beachten Sie, dass die Verwendung bestimmter Einschränkungen eingeschränkt ist, darunter:<br>- Die Dynamic Media-Benutzeroberfläche zeigt möglicherweise nicht die richtigen Details für das Feld **[!UICONTROL Zuletzt veröffentlicht]** an. Diese Auswirkung hat jedoch keine Auswirkungen auf die Veröffentlichung.<br>- Derzeit funktioniert das HLS-Video-Streaming nicht, wenn **[!UICONTROL die]** Verschleierung der Anforderung und die  **[!UICONTROL Sperrung der]** Anforderung aktiviert sind.<br>- Derzeit funktionieren einige Dynamic Media-Viewer nicht, wenn  **[!UICONTROL Verschleierung]** der Anforderung und Sperren der  **[!UICONTROL Anforderung]** aktiviert sind.

C++-Beispielcode zum Generieren des Werts für die Anforderungssperre:

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

[HTTP-Kodierung](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-http-encoding.md#reference-bb34dd13f316462695448acfa8f92df7),  [Anforderungsverschleierung](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-request-obfuscation.md#reference-895f65d6796c43bb9bad21a676ed714d),  [Attribut::RequestLock](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-requestlock.md#reference-8bbe2f581be847d3b9fa123e8e5e94b0)
