---
description: Fügt einer oder mehreren Firmen einen Benutzer hinzu.
solution: Experience Manager
title: addCompanyMembership
feature: Dynamic Media Classic, SDK/API
role: Entwickler, Administrator
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '90'
ht-degree: 13%

---


# addCompanyMembership{#addcompanymembership}

Fügt einer oder mehreren Firmen einen Benutzer hinzu.

Syntax

## Autorisierte Benutzertypen {#section-ae926c7672984be79f6102748accab72}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## Parameter {#section-0e925b91d63e48aa91f0b0014e6a0cab}

**Input (addCompanyMembershipParam)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| `*`userHandle`*` | `xsd:string` | Nein | Das Handle des Benutzers, dessen Mitgliedschaft Sie hinzufügen möchten. |
| `*`membershipArray`*` | `types:CompanyMembershipUpdateArray` | Ja | Eine Reihe von Firmen, denen Sie den Benutzer hinzufügen. |

**Output (addCompanyMembershipReturn)**

Die IPS-API gibt keine Antwort für diesen Vorgang zurück.

## Beispiele {#section-5469f88bac7047cca131faa6b021e437}

In diesem Beispiel wird `*`companyHandleArray`*` verwendet, um einen Benutzer einer einzelnen Firma hinzuzufügen.

**Anforderung**

```java
<ns1:addCompanyMembershipParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:userHandle>621|jduvar@adobe.com</ns1:userHandle>
   <ns1:companyHandleArray>
      </ns1:items>47</ns1:items>
   </ns1:companyHandleArray>
</ns1:addCompanyMembershipParam>
```

**Antwort**

Keine.
