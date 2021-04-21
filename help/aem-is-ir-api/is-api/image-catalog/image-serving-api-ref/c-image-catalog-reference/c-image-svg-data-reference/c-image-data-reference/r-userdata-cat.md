---
description: Benutzerdaten. Der Server gibt den Inhalt dieses Felds als Antwort auf req=userdata an den Client zurück.
solution: Experience Manager
title: Benutzerdaten
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '131'
ht-degree: 8%

---


# Benutzerdaten{#userdata}

Benutzerdaten. Der Server gibt den Inhalt dieses Felds als Antwort auf req=userdata an den Client zurück.

## Eigenschaften {#section-06f2002b77d54a64be07f12fff54ad13}

Textzeichenfolgenwert. Es wird empfohlen, die Formatierung [Eigenschaftsdaten](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-common-data-types/r-property-data.md) zu verwenden. Wenn keine Formatierung der Eigenschaftsdaten verwendet wird, darf die Textzeichenfolge nicht das Zeichen &#39;=&#39; enthalten.

Die Viewer-Clients für Zoom, Rotationsset und Broschüre gehen davon aus, dass dieses Feld die Formatierung der Eigenschaftsdaten verwendet. Diese Clients verwenden dieses Feld für die Viewer-Konfiguration und -Anpassung. Weitere Informationen finden Sie in der Viewer-Dokumentation.

Dieses Feld nimmt an der lokale Anpassung der Textzeichenfolge teil. Weitere Informationen finden Sie unter [Textzeichenfolgen-Lokale Anpassung](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-text-string-localization.md) in der *HTTP-Protokollreferenz*.

## Standard {#section-7ee879762130467199745f2abc662f1e}

Keine.

## Verwandte Themen {#section-e07a022933b2461d9c37b1f188aa8fb5}

[req=userdata](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md) ,  [Textzeichenfolgen-Lokale Anpassung](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-text-string-localization.md)
