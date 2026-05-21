---
description: Bild der Fehlerantwort. Image Serving gibt normalerweise einen Fehlerstatus mit einer Textmeldung zurück, wenn ein Fehler auftritt.
solution: Experience Manager
title: ErrorImage
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: f412a379-525e-42fc-97bf-b10e00da6a20
TQID: 'https://experienceleague.adobe.com/eV8TNAf3uQZgspn0DjSE463ltmCNL0xwl7Kd2hT7gHk'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 275
ht-degree: 1%

---

# ErrorImage{#errorimage}

Bild der Fehlerantwort. Image Serving gibt normalerweise einen Fehlerstatus mit einer Textmeldung zurück, wenn ein Fehler auftritt.

`attribute::ErrorImage` können Sie ein Bild, einen Katalogeintrag oder eine Vorlage konfigurieren, die im Fehlerfall zurückgegeben werden soll.

>[!NOTE]
>
>Fehlende Bilder können auch mit `attribute::DefaultImage` verarbeitet werden.

Es kann eine Bildbereitstellungsvorlage konfiguriert werden, die den Fehlermeldungstext im Antwortbild rendert. Die folgenden vordefinierten Variablen können in der `$error.title`-Vorlage, die durch eine kurze Fehlerbeschreibung ersetzt wird, und in `$error.message`, die durch eine detailliertere Fehlerbeschreibung ersetzt wird (die Detailgenauigkeit wird mit `attribute::ErrorDetail` konfiguriert), enthalten sein.

Der HTTP-Status 200 wird zurückgegeben, wenn das Fehlerbild/die Fehlervorlage erfolgreich verarbeitet werden kann. Wenn während dieser Verarbeitung ein Fehler auftritt, werden der HTTP-Fehlerstatus und eine Textmeldung zurückgegeben.

## Eigenschaften {#section-f460c6c2dd1f46b29f9a79b093575f45}

Text-String Wenn angegeben, muss ein gültiger Wert für catalog:id in einem Bildkatalog oder ein relativer (zu `attribute::RootPath`) oder absoluter Pfad zu einer Bilddatei sein, auf den der Bildserver zugreifen kann.

## Standard {#section-2885f289e5714ddca665a6aee401967f}

Von `default::ErrorImage` geerbt, wenn nicht definiert. Wenn das Fehlerbildverhalten definiert, aber leer ist, wird es deaktiviert, selbst wenn `default::ErrorImage` definiert ist, und ein HTTP-Fehlerstatus und eine Textmeldung werden zurückgegeben.

## Beispiel {#section-c92090abe1d247529542a8dd4960c2e6}

Um Antwortbilder mit der im Bild gerenderten Fehlermeldung zu erhalten, müssen wir zunächst die Vorlage im Bildkatalog definieren. In diesem Fall erstellen wir einen Eintrag in unserem Bildkatalog namens `onError`, der Folgendes in `catalog::Modifier` enthält:

`size=300,300&bgc=ffffff&text=$error.message$`

Die Vorlage ist registriert bei `attribute::ErrorImage`:

`ErrorImage=myCatalog/onError`

In diesem Beispiel wird der Text mit der Standardschriftart, der Schriftfarbe und der Schriftgröße gerendert.

## Verwandte Themen {#section-bbf1f85fc0a34033bdda1dd3e4e0bbb6}

[attribute::RootPath](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md#reference-17d57e5967be403b8408fa7214017494) , [catalog::Id](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-id-cat.md), [attribute::DefaultImage](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-is-cat-defaultimage.md#reference-8e9900e129f54ed68462a3c2fc3bc433), [attribute::ErrorDetail](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-errordetail.md#reference-4987c8cddcba4c88960170e49cafc561)
