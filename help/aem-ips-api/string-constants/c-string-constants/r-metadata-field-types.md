---
description: Wird von MetadataField/type, saveMetadataFieldParam/fieldType und createMetadataField/fieldType verwendet.
solution: Experience Manager
title: Metadatenfeldtypen
feature: Dynamic Media Classic,SDK/API,Metadata
role: Developer,Administrator
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '103'
ht-degree: 1%

---


# Metadatenfeldtypen{#metadata-field-types}

Wird von MetadataField/type, saveMetadataFieldParam/fieldType und createMetadataField/fieldType verwendet.

Syntax

## Werte {#section-1d8f05dbeff74bfdbd5960ccc7347557}

* [!DNL `Untyped`]
* [!DNL `Boolean`]
* [!DNL `BooleanTag`]: Ein Sonderfall  [!DNL `SingleFixedTag`] mit einem nicht änderbaren Wörterbuch, das in die Werte  [!DNL `True`] und  [!DNL `False`]Werte initialisiert wurde.

* [!DNL `Color`]
* [!DNL `Date`]
* [!DNL `Dimension`]
* [!DNL `FileName`]
* [!DNL `Float`]
* [!DNL `Int`]
* [!DNL `MultiFixedTag`]: Null oder mehr Zeichenfolgenwerte aus einem geschlossenen Wörterbuch. Das Wörterbuch kann nur von Administratoren geändert werden.
* [!DNL `MultiTag`]: Null oder mehr Zeichenfolgenwerte.
* [!DNL `SingleFixedTag`]: Ein einzelner Zeichenfolgenwert aus einem geschlossenen Wörterbuch. Wenn `setAssetMetadata` oder `batchSetAssetMetadata` mit einem Wert aufgerufen werden, der nicht im Wörterbuch enthalten ist, wird ein Fehler zurückgegeben. Das Wörterbuch kann nur von Administratoren geändert werden.

* [!DNL `SingleTag`]: Ein beliebiger Zeichenfolgenwert.
* [!DNL `String`]

