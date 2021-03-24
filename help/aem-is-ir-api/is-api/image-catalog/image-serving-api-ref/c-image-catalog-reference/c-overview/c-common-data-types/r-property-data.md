---
description: Eigenschaftendaten bestehen aus einer Textzeichenfolge, die eine oder mehrere Eigenschaften darstellt.
solution: Experience Manager
title: Eigenschaftendaten
feature: Dynamic Media Classic, SDK/API
role: Entwickler, Geschäftspraktiker
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '118'
ht-degree: 0%

---


# Eigenschaftendaten{#property-data}

Eigenschaftendaten bestehen aus einer Textzeichenfolge, die eine oder mehrere Eigenschaften darstellt.

Eine Eigenschaft besteht aus einem Eigenschaftsnamen und einem Eigenschaftswert, die durch = voneinander getrennt sind.

Mehrere Eigenschaften werden durch Trennlinien voneinander getrennt, die entweder `??` oder `<CR><LF>` sein können. Wenn die gesamte Eigenschaftendatenzeichenfolge nicht in Anführungszeichen gesetzt ist, ersetzt der Server jedes Vorkommen von `??` durch `<CR><LF>`, bevor die Daten an den Client gesendet werden. Eigenschaftsnamen können aus Buchstaben, Zahlen, &#39;.&#39;, &#39;-&#39; und &#39;_&#39; bestehen. Bei Eigenschaftsnamen wird nicht zwischen Groß- und Kleinschreibung unterschieden.

Eigenschaftenwerte dürfen keine Trennlinien enthalten.

Weitere Regeln, die auf Eigenschaftendaten angewendet werden, finden Sie unter [Textzeichenfolge](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-common-data-types/r-text-string.md#reference-ae0a9e181b0e40c6bcdb43af7f481d63).
