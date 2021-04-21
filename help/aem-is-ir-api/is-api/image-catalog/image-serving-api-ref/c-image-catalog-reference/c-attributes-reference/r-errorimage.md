---
description: Fehlermeldungsbild. Image Serving gibt normalerweise einen Fehlerstatus mit einer Textmeldung zurück, wenn ein Fehler auftritt.
solution: Experience Manager
title: ErrorImage
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '283'
ht-degree: 1%

---


# ErrorImage{#errorimage}

Fehlermeldungsbild. Image Serving gibt normalerweise einen Fehlerstatus mit einer Textmeldung zurück, wenn ein Fehler auftritt.

`attribute::ErrorImage` ermöglicht die Konfiguration eines Bildes, Katalogeintrags oder einer Vorlage im Fehlerfall.

>[!NOTE]
>
>Fehlende Bilder können auch mit `attribute::DefaultImage` verarbeitet werden.

Es kann eine Image Serving-Vorlage konfiguriert werden, die den Text der Fehlermeldung im Antwortbild wiedergibt. Die folgenden vordefinierten Variablen können in die `$error.title`-Vorlage aufgenommen werden, die durch eine kurze Fehlerbeschreibung ersetzt wird, und `$error.message`, die durch eine detailliertere Fehlerbeschreibung ersetzt wird (die Detailstufe wird mit `attribute::ErrorDetail` konfiguriert).

HTTP-Status 200 wird zurückgegeben, wenn das Fehlerbild/die Fehlervorlage erfolgreich verarbeitet werden kann. Tritt während dieser Verarbeitung ein Fehler auf, werden der HTTP-Fehlerstatus und eine Textmeldung zurückgegeben.

## Eigenschaften {#section-f460c6c2dd1f46b29f9a79b093575f45}

Textzeichenfolge. Wenn angegeben, muss es sich um einen gültigen Katalog::Id-Wert in einem Bildkatalog oder um einen relativen Pfad (zu `attribute::RootPath`) oder einen absoluten Pfad zu einer Bilddatei handeln, auf die der Image-Server zugreifen kann.

## Standard {#section-2885f289e5714ddca665a6aee401967f}

Vererbt von `default::ErrorImage`, wenn nicht definiert. Wenn definiert, aber leer, ist das Verhalten des Fehlerbilds deaktiviert, auch wenn `default::ErrorImage` definiert ist, und es wird ein HTTP-Fehlerstatus und eine Textmeldung zurückgegeben.

## Beispiel {#section-c92090abe1d247529542a8dd4960c2e6}

Um Antwortbilder mit der Fehlermeldung im Bild zu erhalten, müssen wir zunächst die Vorlage im Bildkatalog definieren. In diesem Fall erstellen wir einen Eintrag in unserem Bildkatalog mit dem Namen `onError`, der Folgendes in `catalog::Modifier` enthält:

`size=300,300&bgc=ffffff&text=$error.message$`

Die Vorlage ist bei `attribute::ErrorImage` registriert:

`ErrorImage=myCatalog/onError`

In diesem Beispiel wird der Text mit der Standardschrift, der Schriftfarbe und der Schriftgröße wiedergegeben.

## Verwandte Themen {#section-bbf1f85fc0a34033bdda1dd3e4e0bbb6}

[attribute::RootPath](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md#reference-17d57e5967be403b8408fa7214017494) ,  [catalog::Id](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-id-cat.md),  [attribute::DefaultImage](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-is-cat-defaultimage.md#reference-8e9900e129f54ed68462a3c2fc3bc433),  [attribute::ErrorDetail](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-errordetail.md#reference-4987c8cddcba4c88960170e49cafc561)
