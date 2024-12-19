---
description: Standardbildmodus. Wählt aus, wie das Standardbild angewendet wird, wenn in der Anfrage angegebene Bilder nicht gefunden werden.
solution: Experience Manager
title: DefaultImageMode
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: b30ce72f-7c74-407c-bd4a-042b84c469e9
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '106'
ht-degree: 2%

---

# DefaultImageMode{#defaultimagemode}

Standardbildmodus. Wählt aus, wie das Standardbild angewendet wird, wenn in der Anfrage angegebene Bilder nicht gefunden werden.

## Eigenschaften {#section-7fa8acb63540490d9f5186231b5e77c3}

Aufzählung. „0“, um das gesamte zusammengesetzte Bild zu ersetzen, auch wenn das fehlende Bild nur eine von mehreren Ebenen ist; „1“, um jedes fehlende Ebenenquellbild durch das Standardbild zu ersetzen und das zusammengesetzte Bild wie gewohnt zurückzugeben.

## Einschränkungen {#section-04cb0d50e8914564a8d226d0d4663c8b}

Die Bildbereitstellung wird auf `DefaultImageMode=0` zurückgesetzt, wenn verschachtelte Bild-Rendering-, FXG- oder `req=set`-Anfragen fehlschlagen.

## Standard {#section-9e318524a2a5496386901286748c7ee7}

Von `default::DefaultImage` geerbt, wenn nicht definiert oder leer.

## Verwandte Themen {#section-fddce1d27a0c43fb8b4d891f76ac5a52}

[defaultImage=](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-is-cat-defaultimage.md#reference-8e9900e129f54ed68462a3c2fc3bc433) , [attribute::DefaultImage](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-defaultimage.md#reference-209aa6ce830f490483412eb26af67fd2)
