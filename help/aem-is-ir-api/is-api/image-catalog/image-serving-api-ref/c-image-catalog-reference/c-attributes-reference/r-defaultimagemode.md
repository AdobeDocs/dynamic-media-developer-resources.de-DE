---
description: Standardbildmodus. Legt fest, wie das Standardbild angewendet wird, wenn in der Anforderung angegebene Bilder nicht gefunden werden.
seo-description: Standardbildmodus. Legt fest, wie das Standardbild angewendet wird, wenn in der Anforderung angegebene Bilder nicht gefunden werden.
seo-title: DefaultImageMode
solution: Experience Manager
title: DefaultImageMode
topic: Scene7 Image Serving - Image Rendering API
uuid: e5640f09-e1e3-473b-8fbc-84c6bfce2460
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# DefaultImageMode{#defaultimagemode}

Standardbildmodus. Legt fest, wie das Standardbild angewendet wird, wenn in der Anforderung angegebene Bilder nicht gefunden werden.

## Eigenschaften {#section-7fa8acb63540490d9f5186231b5e77c3}

Enum. &quot;0&quot;, um das gesamte Composite-Bild zu ersetzen, auch wenn das fehlende Bild nur eine von mehreren Ebenen ist; &#39;1&#39;, um jedes fehlende Ebenenquellbild durch das Standardbild zu ersetzen und das Composite wie gewohnt zurückzugeben.

## Restrictions {#section-04cb0d50e8914564a8d226d0d4663c8b}

Beim Image Serving wird wieder auf `DefaultImageMode=0` die Funktion zurückgekehrt, wenn verschachtelte Image Rendering-, FXG- oder `req=set` Anforderungen fehlschlagen.

## Standard {#section-9e318524a2a5496386901286748c7ee7}

Vererbt von, `default::DefaultImage` wenn nicht definiert oder leer.

## Verwandte Themen {#section-fddce1d27a0c43fb8b4d891f76ac5a52}

[defaultImage=](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-is-cat-defaultimage.md#reference-8e9900e129f54ed68462a3c2fc3bc433) , [attribute::DefaultImage](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-defaultimage.md#reference-209aa6ce830f490483412eb26af67fd2)
