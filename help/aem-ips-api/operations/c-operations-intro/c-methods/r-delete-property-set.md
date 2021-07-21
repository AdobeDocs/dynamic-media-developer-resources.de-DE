---
description: Löscht einen Eigenschaftssatz und alle zugehörigen Eigenschaften.
solution: Experience Manager
title: deletePropertySet
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 72429030-200d-4e13-a537-10a728998a26
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '88'
ht-degree: 12%

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

**Eingabe (deletePropertySetParam)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| `*`setHandle`*` | `xsd:string` | Ja | Der Handle für die Eigenschaft, die gelöscht werden soll. |

**Ausgabe (deletePropertySetParam)**

Die IPS-API gibt keine Antwort für diesen Vorgang zurück.

## Beispiele {#section-cf319fc8f86a40ab9cbd838b031973fe}

In diesem Codebeispiel wird das Handle des Satzes als Feld im `deletePropertySetParam` verwendet, das an den IPS-Webdienstserver gesendet wird, um den Eigenschaftssatz zu löschen.

**Anforderung**

```java
<deletePropertySetParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <setHandle>ps|941</setHandle>
</deletePropertySetParam>
```

**Antwort**

Keine.
