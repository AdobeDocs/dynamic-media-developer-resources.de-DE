---
description: Löscht einen Eigenschaftssatz und alle zugehörigen Eigenschaften.
solution: Experience Manager
title: deletePropertySet
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 72429030-200d-4e13-a537-10a728998a26
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '83'
ht-degree: 10%

---

# deletePropertySet{#deletepropertyset}

Löscht einen Eigenschaftssatz und alle zugehörigen Eigenschaften.

Syntax

## Autorisierte Benutzertypen {#section-b54aa8c854de400a989b4957412ff42c}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## Parameter {#section-e5fc868f69494cf6858e03027db09101}

**Input (deletePropertySetParam)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| setHandle | `xsd:string` | Ja | Der Handle für die Eigenschaft, die gelöscht werden soll. |

**Output (deletePropertySetParam)**

Die IPS-API gibt keine Antwort für diesen Vorgang zurück.

## Beispiele {#section-cf319fc8f86a40ab9cbd838b031973fe}

In diesem Codebeispiel wird das Handle des Satzes als Feld im Feld `deletePropertySetParam` verwendet, das an den IPS-Webdienstserver gesendet wird, um den Eigenschaftssatz zu löschen.

**Anfrage**

```java
<deletePropertySetParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <setHandle>ps|941</setHandle>
</deletePropertySetParam>
```

**Antwort**

Keine.
