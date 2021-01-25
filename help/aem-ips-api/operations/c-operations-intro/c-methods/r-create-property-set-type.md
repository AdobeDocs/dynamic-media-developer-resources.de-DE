---
description: Ein Eigenschaftssatztyp gibt verschiedene Einstellungen an, die zur Verwaltung von Eigenschaftensätzen verwendet werden.
seo-description: Ein Eigenschaftssatztyp gibt verschiedene Einstellungen an, die zur Verwaltung von Eigenschaftensätzen verwendet werden.
seo-title: createPropertySetType
solution: Experience Manager
title: createPropertySetType
topic: Dynamic Media Image Production System API
uuid: ecbaad48-d725-4f7a-a37d-5e4cde3295cb
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '172'
ht-degree: 11%

---


# createPropertySetType{#createpropertysettype}

Ein Eigenschaftssatztyp gibt verschiedene Einstellungen an, die zur Verwaltung von Eigenschaftensätzen verwendet werden.

Syntax

## Autorisierte Benutzertypen {#section-48e5f908276c4a549fd33a8828bad326}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## Parameter {#section-43dece72eb9f44df80f4a119dd2c008b}

**Input (createPropertySetTypeParam)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Nein | Das Handle der Firma, der der Eigenschaftssatztyp gehört. Wenn `companyHandle` nicht übergeben wird und der Aufrufer ein `IpsAdmin` ist, wird ein globaler Eigenschaftssatztyp erstellt. |
| `*`name`*` | `xsd:string` | Ja | Der Name des Eigenschaftssatztyps. |
| `*`propertyType`*` | `xsd:string` | Ja | Auswahl der Eigenschaftssatztypen. |
| `*`allowMultiple`*` | `xsd:boolean` | Ja | Bestimmt, ob Ihr Programm mehrere Eigenschaftensätze haben kann. |

**Output (createPropertySetTypeReturn)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| `*`typeHandle`*` | `xsd:string` | Ja | Ein Griff zum Typ. |

## Beispiele {#section-13396c9639a6475190e622eae3cdb534}

Dieses Codebeispiel erstellt einen Eigenschaftssatz mit einem Namen und einem Typ, der von der `PropertySet Types`-Konstante angegeben wird. Das Handle der Firma, der der Eigenschaftssatztyp gehört. Wenn companyHandle nicht übergeben wird und der Aufrufer ein IpsAdmin ist, wird ein globaler Eigenschaftssatztyp erstellt.

**Anforderung**

```java
<createPropertySetTypeReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <typeHandle>pt|10803</typeHandle>
</createPropertySetTypeReturn>
```

**Antwort**

```java
<createPropertySetTypeReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <typeHandle>pt|10801</typeHandle>
</createPropertySetTypeReturn>
```

