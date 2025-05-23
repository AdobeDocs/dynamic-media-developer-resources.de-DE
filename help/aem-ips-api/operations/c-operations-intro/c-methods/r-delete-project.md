---
description: Löscht ein Projekt aus einer Firma. Die Verknüpfungen zwischen den Assets und dem Projekt sind fehlerhaft, aber die Assets werden nicht aus IPS gelöscht.
solution: Experience Manager
title: deleteProject
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: b42be3ef-c935-4548-8f92-4fc33af321b5
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '128'
ht-degree: 7%

---

# deleteProject{#deleteproject}

Löscht ein Projekt aus einer Firma. Die Verknüpfungen zwischen den Assets und dem Projekt sind fehlerhaft, aber die Assets werden nicht aus IPS gelöscht.

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
| companyName | `xsd:string` | Ja | Der Name der Firma, die mit dem Projekt verknüpft ist. |
| projectHandle | `xsd:string` | Ja | Das Handle des zu löschenden Projekts. |

**Ausgabe (deleteProjectReturn)**

Die IPS-API gibt keine Antwort für diesen Vorgang zurück.

## Beispiele {#section-e38507f1f7ec41b9a625f47390490254}

In diesem Codebeispiel werden das Firmen-Handle und das Projekt-Handle als Felder in deleteProjectParam verwendet, die an den IPS-Webservice-Server gesendet werden, um das Projekt zu löschen.

**Anfrage**

```java
<deleteProjectParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|6</companyHandle>
<projectHandle>p|6|ProjectTestAPI</projectHandle></deleteProjectParam>
```

**Antwort**

Keine.
