---
description: Wird von MetadataField/type, saveMetadataFieldParam/fieldType und createMetadataField/fieldType verwendet.
seo-description: Wird von MetadataField/type, saveMetadataFieldParam/fieldType und createMetadataField/fieldType verwendet.
seo-title: Metadatenfeldtypen
solution: Experience Manager
title: Metadatenfeldtypen
uuid: 57d292bb-848a-4e6e-bd08-4e6af1f9fc72
feature: Dynamic Media Classic, SDK/API, Metadaten
role: Entwickler, Administrator
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '115'
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

