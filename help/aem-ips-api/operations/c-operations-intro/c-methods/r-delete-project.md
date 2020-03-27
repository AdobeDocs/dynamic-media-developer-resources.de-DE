---
description: Löscht ein Projekt aus einer Firma. Die Verknüpfungen zwischen den Assets und dem Projekt sind beschädigt, aber die Assets werden nicht aus dem IPS gelöscht.
seo-description: Löscht ein Projekt aus einer Firma. Die Verknüpfungen zwischen den Assets und dem Projekt sind beschädigt, aber die Assets werden nicht aus dem IPS gelöscht.
seo-title: deleteProject
solution: Experience Manager
title: deleteProject
topic: Scene7 Image Production System API
uuid: 0915066f-2106-4cbc-a68a-f149810c24f8
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# deleteProject{#deleteproject}

Löscht ein Projekt aus einer Firma. Die Verknüpfungen zwischen den Assets und dem Projekt sind beschädigt, aber die Assets werden nicht aus dem IPS gelöscht.

Syntax

## Autorisierte Benutzertypen {#section-d8a70e23c68d426e9af1357b978ae2f0}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parameter {#section-00d1e00dd5014513a52b4e6b4f61de62}

**Eingabe (deleteProjectParam)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| ` *`companyName`*` | `xsd:string` | Ja | Der Name der mit dem Projekt verknüpften Firma. |
| ` *`projectHandle`*` | `xsd:string` | Ja | Das zu löschende Handle des Projekts. |

**Output (deleteProjectReturn)**

Die IPS-API gibt keine Antwort für diesen Vorgang zurück.

## Beispiele {#section-e38507f1f7ec41b9a625f47390490254}

In diesem Codebeispiel werden das Firmen-Handle und das Projekthandle als an den IPS-Webdienstserver gesendete Felder im deleteProjectParam verwendet, um das Projekt zu löschen.

**Anforderung**

```java
<deleteProjectParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|6</companyHandle>
<projectHandle>p|6|ProjectTestAPI</projectHandle></deleteProjectParam>
```

**Antwort**

Keine.
