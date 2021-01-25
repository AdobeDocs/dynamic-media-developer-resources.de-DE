---
description: Löscht den Eigenschaftssatztyp und den zugehörigen Eigenschaftensatz und die zugehörigen Eigenschaften.
seo-description: Löscht den Eigenschaftssatztyp und den zugehörigen Eigenschaftensatz und die zugehörigen Eigenschaften.
seo-title: deletePropertySetType
solution: Experience Manager
title: deletePropertySetType
topic: Dynamic Media Image Production System API
uuid: 7a5232cc-fa3a-4dac-bf88-8b954dd37c87
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '106'
ht-degree: 10%

---


# deletePropertySetType{#deletepropertysettype}

Löscht den Eigenschaftssatztyp und den zugehörigen Eigenschaftensatz und die zugehörigen Eigenschaften.

Syntax

## Autorisierte Benutzertypen {#section-16a17b4ebf9a4639bdb2784a2e9fe00d}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## Parameter {#section-1c8973f5d35f44b4a6a483a41609e455}

**Input (deletePropertySetTypeParam)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| `*`typeHandle`*` | `xsd:string` | Ja | Der Handle für den zu löschenden Eigenschaftssatztyp. |

**Output (deletePropertySetTypeParam)**

Die IPS-API gibt keine Antwort für diesen Vorgang zurück.

## Beispiele {#section-85faa2e3411a4e23aa6489037f7ce078}

In diesem Codebeispiel wird der Handle des Typs als Feld im Feld `deletePropertySetTypeParam` verwendet, das an den IPS-Webdienstserver gesendet wird, um den Eigenschaftssatztyp zu löschen.

**Anforderung**

```java
<deletePropertySetTypeParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <typeHandle>pt|10801</typeHandle>
</deletePropertySetTypeParam>
```

**Antwort**

Keine.
