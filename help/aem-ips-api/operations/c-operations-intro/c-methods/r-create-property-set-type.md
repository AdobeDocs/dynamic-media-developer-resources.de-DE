---
description: Ein Eigenschaftssatztyp gibt verschiedene Einstellungen an, die bei der Verwaltung von Eigenschaftssätzen verwendet werden.
solution: Experience Manager
title: createPropertySetType
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 1730ccbf-e8b0-4f92-9daf-da2fa047cbbd
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '156'
ht-degree: 10%

---

# createPropertySetType{#createpropertysettype}

Ein Eigenschaftssatztyp gibt verschiedene Einstellungen an, die bei der Verwaltung von Eigenschaftssätzen verwendet werden.

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
| companyHandle | `xsd:string` | Nein | Das Handle an das Unternehmen, dem der Eigenschaftssatztyp gehört. Wenn `companyHandle` nicht übergeben wird und der Aufrufer ein `IpsAdmin` ist, wird ein globaler Eigenschaftssatztyp erstellt. |
| name | `xsd:string` | Ja | Der Name des Eigenschaftssatztyps. |
| propertyType | `xsd:string` | Ja | Auswahl der Eigenschaftssatztypen. |
| allowMultiple | `xsd:boolean` | Ja | Bestimmt, ob Ihr Programm über mehrere Eigenschaftssätze verfügen kann. |

**Ausgabe (createPropertySetTypeReturn)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| typeHandle | `xsd:string` | Ja | Ein Handle für den Typ. |

## Beispiele {#section-13396c9639a6475190e622eae3cdb534}

Dieses Codebeispiel erstellt einen Eigenschaftssatz mit einem Namen und einem Typ, die durch die `PropertySet Types`-Konstante angegeben werden. Das Handle an das Unternehmen, dem der Eigenschaftssatztyp gehört. Wenn companyHandle nicht übergeben wird und der Aufrufer ein IpsAdmin ist, wird ein globaler Eigenschaftssatztyp erstellt.

**Anfrage**

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
