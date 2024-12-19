---
description: Löscht das Metadatenfeld eines Unternehmens.
solution: Experience Manager
title: deleteMetadataField
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 1922fc1b-2abc-4d31-985a-65c788af4d46
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '98'
ht-degree: 9%

---

# deleteMetadataField{#deletemetadatafield}

Löscht das Metadatenfeld eines Unternehmens.

Syntax

## Autorisierte Benutzertypen {#section-63e7d17f4b434995a872838bfff7f9ff}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## Parameter {#section-73f12a30cc4340b6b32dd11effd5195e}

**Eingabe (deleteMetadataFieldParam)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| companyHandle | `xsd:string` | Ja | Das Handle für das Unternehmen, das das zu löschende Metadatenfeld enthält. |
| fieldHandle | `xsd:string` | Ja | Der Handle zum Metadatenfeld, das gelöscht werden soll. |

**Ausgabe (deleteMetadataFieldParam)**

Die IPS-API gibt keine Antwort für diesen Vorgang zurück.

## Beispiele {#section-e1c474ea91a040609ecd7c2400f4fa3c}

Dieses Codebeispiel löscht das Metadatenfeld eines Unternehmens. Es verwendet das Unternehmens-Handle und das Metadaten-Handle als Felder in den `deleteMetadataFieldParam`, die an den IPS-Webservice-Server übergeben werden, um diese Aktion durchzuführen.

**Anfrage**

```java
<deleteMetadataFieldParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|6</companyHandle>
   <fieldHandle>m|6|IMAGE|saveMetadataField</fieldHandle>
</deleteMetadataFieldParam>
```

**Antwort**

none.0
