---
description: Löscht einen Eigenschaftensatz und alle zugehörigen Eigenschaften.
seo-description: Löscht einen Eigenschaftensatz und alle zugehörigen Eigenschaften.
seo-title: deletePropertySet
solution: Experience Manager
title: deletePropertySet
topic: Scene7 Image Production System API
uuid: b4fdf51f-89ec-4a69-9179-078ee8e1937f
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# deletePropertySet{#deletepropertyset}

Löscht einen Eigenschaftensatz und alle zugehörigen Eigenschaften.

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
| ` *`setHandle`*` | `xsd:string` | Ja | Das Handle der zu löschenden Eigenschaft. |

**Output (deletePropertySetParam)**

Die IPS-API gibt keine Antwort für diesen Vorgang zurück.

## Beispiele {#section-cf319fc8f86a40ab9cbd838b031973fe}

In diesem Codebeispiel wird das Handle des Satzes als Feld in dem an den IPS-Webdienstserver `deletePropertySetParam` gesendeten Feld verwendet, um den Eigenschaftensatz zu löschen.

**Anforderung**

```java
<deletePropertySetParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <setHandle>ps|941</setHandle>
</deletePropertySetParam>
```

**Antwort**

Keine.
