---
description: Eigenschaftendaten bestehen aus einer Textzeichenfolge, die eine oder mehrere Eigenschaften darstellt.
seo-description: Eigenschaftendaten bestehen aus einer Textzeichenfolge, die eine oder mehrere Eigenschaften darstellt.
seo-title: Eigenschaftendaten
solution: Experience Manager
title: Eigenschaftendaten
topic: Scene7 Image Serving - Image Rendering API
uuid: 7fa6ae70-8d70-41d6-9e47-7df3d616874c
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Eigenschaftendaten{#property-data}

Eigenschaftendaten bestehen aus einer Textzeichenfolge, die eine oder mehrere Eigenschaften darstellt.

Eine Eigenschaft besteht aus einem Eigenschaftsnamen und einem Eigenschaftswert, die durch = voneinander getrennt sind.

Mehrere Eigenschaften werden durch Trennlinien voneinander getrennt, die entweder `??` oder `<CR><LF>`. Wenn die gesamte Eigenschaftendatenzeichenfolge nicht in Anführungszeichen eingeschlossen ist, ersetzt der Server jedes Vorkommen von `??` durch, `<CR><LF>` bevor die Daten an den Client gesendet werden. Eigenschaftsnamen können aus Buchstaben, Zahlen, &#39;.&#39;, &#39;-&#39; und &#39;_&#39; bestehen. Bei Eigenschaftsnamen wird nicht zwischen Groß- und Kleinschreibung unterschieden.

Eigenschaftenwerte dürfen keine Trennlinien enthalten.

Weitere Regeln, die auf Eigenschaftendaten angewendet werden, finden Sie unter [Textzeichenfolge](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-common-data-types/r-text-string.md#reference-ae0a9e181b0e40c6bcdb43af7f481d63) .
