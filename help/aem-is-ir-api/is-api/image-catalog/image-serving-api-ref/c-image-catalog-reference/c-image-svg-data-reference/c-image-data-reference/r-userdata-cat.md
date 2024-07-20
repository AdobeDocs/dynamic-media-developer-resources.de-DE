---
description: Benutzerdaten. Der Server gibt den Inhalt dieses Felds als Antwort auf req=userdata an den Client zurück.
solution: Experience Manager
title: UserData
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 4994c91c-52d7-473d-88ee-f136c4193c40
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '123'
ht-degree: 3%

---

# UserData{#userdata}

Benutzerdaten. Der Server gibt den Inhalt dieses Felds als Antwort auf req=userdata an den Client zurück.

## Eigenschaften {#section-06f2002b77d54a64be07f12fff54ad13}

Textzeichenfolgenwert. Es wird empfohlen, die Formatierung mit [Eigenschaftsdaten](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-common-data-types/r-property-data.md) zu verwenden. Wenn die Formatierung der Eigenschaftsdaten nicht verwendet wird, darf die Textzeichenfolge das Zeichen &#39;=&#39; nicht enthalten.

Die Viewer-Clients für Zoom, Rotation und Broschüren gehen davon aus, dass dieses Feld die Formatierung der Eigenschaftsdaten verwendet. Diese Clients verwenden dieses Feld für die Viewer-Konfiguration und -Anpassung. Weitere Informationen finden Sie in der Viewer-Dokumentation .

Dieses Feld nimmt an der Lokalisierung von Textzeichenfolgen teil. Weitere Informationen finden Sie unter [Lokalisierung von Textzeichenfolgen](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-text-string-localization.md) in der *HTTP-Protokollreferenz*.

## Standard {#section-7ee879762130467199745f2abc662f1e}

Keine.

## Verwandte Themen {#section-e07a022933b2461d9c37b1f188aa8fb5}

[req=userdata](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md) , [Lokalisierung von Textzeichenfolgen](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-text-string-localization.md)
