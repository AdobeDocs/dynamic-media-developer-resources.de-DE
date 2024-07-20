---
description: Wird von MetadataField/type, saveMetadataFieldParam/fieldType und createMetadataField/fieldType verwendet.
solution: Experience Manager
title: Metadatenfeldtypen
feature: Dynamic Media Classic,SDK/API,Metadata
role: Developer,Admin
exl-id: cbbe55f2-bd22-44f5-9440-f58fb45b8d9a
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '94'
ht-degree: 2%

---

# Metadatenfeldtypen{#metadata-field-types}

Wird von MetadataField/type, saveMetadataFieldParam/fieldType und createMetadataField/fieldType verwendet.

Syntax

## Werte {#section-1d8f05dbeff74bfdbd5960ccc7347557}

* [!DNL `Untyped`]
* [!DNL `Boolean`]
* [!DNL `BooleanTag`]: Ein Sonderfall von [!DNL `SingleFixedTag`] mit einem nicht änderbaren Wörterbuch, das auf die Werte [!DNL `True`] und [!DNL `False`] initialisiert wurde.

* [!DNL `Color`]
* [!DNL `Date`]
* [!DNL `Dimension`]
* [!DNL `FileName`]
* [!DNL `Float`]
* [!DNL `Int`]
* [!DNL `MultiFixedTag`]: Null oder mehr Zeichenfolgenwerte aus einem geschlossenen Wörterbuch. Nur Admin-Benutzer können das Wörterbuch ändern.
* [!DNL `MultiTag`]: Null oder mehr Zeichenfolgenwerte.
* [!DNL `SingleFixedTag`]: Ein einzelner Zeichenfolgenwert aus einem geschlossenen Wörterbuch. Wenn `setAssetMetadata` oder `batchSetAssetMetadata` mit einem Wert aufgerufen werden, der nicht im Wörterbuch enthalten ist, wird ein Fehler zurückgegeben. Nur Admin-Benutzer können das Wörterbuch ändern.

* [!DNL `SingleTag`]: Jeder einzelne Zeichenfolgenwert.
* [!DNL `String`]
