---
description: Wenn eine Anfrage nicht erfolgreich abgeschlossen werden kann, gibt der Server entweder ein Fehlerbild oder einen anderen HTTP-Antwortstatus als 200 zusammen mit einer Fehlermeldung zurück.
solution: Experience Manager
title: Fehler
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 9314782f-703b-4e9c-a026-62970d1c752f
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '202'
ht-degree: 1%

---

# Fehler{#errors}

Wenn eine Anfrage nicht erfolgreich abgeschlossen werden kann, gibt der Server entweder ein Fehlerbild oder einen anderen HTTP-Antwortstatus als 200 zusammen mit einer Fehlermeldung zurück.

Der Wert für den Antwortstatus hängt vom Typ des Fehlers ab. Bei den häufigsten Fehlern ist er „403“. Fehlerantworten für Nicht-Bildanforderungstypen entsprechen dem Format, das mit `req=` angegeben wurde. (Kann derzeit möglicherweise nicht konsistent implementiert werden.)

Die in der Fehlermeldung enthaltene Menge an Details kann mit `attribute::ErrorDetail` konfiguriert werden.

## Fehlerbilder {#section-92e9b20b2507433daa96923abc95f777}

Die Bildbereitstellung kann so konfiguriert werden, dass in einem Bild gerenderte Fehlermeldungen zurückgegeben werden.

Weitere Informationen finden Sie [attribute::ErrorImage](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-errorimage.md#reference-c494d5d8b2584fe3800f35baabd0292c) in der Referenz zum Bildkatalog.

Wenn das Fehlerbild erfolgreich generiert wurde, ist der HTTP-Antwortstatus 200. Wenn bei der Verarbeitung des Fehlerbilds ein Fehler auftritt, wird die standardmäßige HTTP-Fehlerantwort und Textmeldung an den Client zurückgegeben.

## Standardbild {#section-66bf25fe6b434081bfae96d38d9be25e}

Die Bildbereitstellung kann so konfiguriert werden, dass ein fehlendes Bild durch ein Standardbild ersetzt wird. Das Standardbild kann entweder mit `attribute::DefaultImage` oder mit dem Befehl `defaultImage=` angegeben werden.

## Verwandte Themen {#section-e261d7f224ca4546bb64bf8cb909db08}

[attribute::ErrorDetail](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-errordetail.md#reference-4987c8cddcba4c88960170e49cafc561) , [attribute::ErrorImage](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-errorimage.md#reference-c494d5d8b2584fe3800f35baabd0292c), [attribute::DefaultImage](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-is-cat-defaultimage.md#reference-8e9900e129f54ed68462a3c2fc3bc433), [defaultImage=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-defaultimage.md#reference-209aa6ce830f490483412eb26af67fd2)
