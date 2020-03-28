---
description: Um die Möglichkeiten zur Bearbeitung von Anfragen zu reduzieren, wird eine einfache Sperrfunktion bereitgestellt.
seo-description: Um die Möglichkeiten zur Bearbeitung von Anfragen zu reduzieren, wird eine einfache Sperrfunktion bereitgestellt.
seo-title: Sperren von Anforderungen
solution: Experience Manager
title: Sperren von Anforderungen
topic: Scene7 Image Serving - Image Rendering API
uuid: 03239376-1e40-48d2-a396-c276802854ed
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Sperren von Anforderungen{#request-locking}

Um die Möglichkeiten zur Bearbeitung von Anfragen zu reduzieren, wird eine einfache Sperrfunktion bereitgestellt.

Wenn attribute::RequestLock festgelegt ist, muss der Anforderung ein Sperrwert in Form von `&xxxx`xxxx als vierstelliger Hexadezimalwert angehängt werden. Dieser Hexadezimalwert wird mithilfe eines einfachen Hashing-Algorithmus generiert, der auf den *Modifikatorteil* der Anforderung angewendet wird (nach dem &#39;?&#39;) , der den URL-Pfad von den *Modifikatoren* trennt). Dies muss erfolgen, nachdem die Anforderung vollständig HTTP-kodiert wurde, aber bevor sie (optional) verschleiert wird. Nach dem Entfernen der Verschleierung der Anforderung verwendet der Server denselben Hashing-Algorithmus für die Modifiziererzeichenfolge (mit Ausnahme der letzten 5 Zeichen, die den Sperrwert enthalten). Wenn der generierte Schlüssel nicht mit der Sperre übereinstimmt, wird die Anforderung abgelehnt.

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

[HTTP-Kodierung](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-http-encoding.md#reference-bb34dd13f316462695448acfa8f92df7), [Anforderungsverschleierung](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-request-obfuscation.md#reference-895f65d6796c43bb9bad21a676ed714d), [Attribut::RequestLock](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-requestlock.md#reference-8bbe2f581be847d3b9fa123e8e5e94b0)
