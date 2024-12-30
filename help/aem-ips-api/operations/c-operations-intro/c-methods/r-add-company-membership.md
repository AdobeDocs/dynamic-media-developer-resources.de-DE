---
description: Fügt einem oder mehreren Unternehmen einen Benutzer hinzu.
solution: Experience Manager
title: addCompanyMitgliedschaft
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 6efef4fb-f2e5-4c41-b739-a36ac2f17884
source-git-commit: b89ca96947f751b750623e1f18d2a5d86f0cd759
workflow-type: tm+mt
source-wordcount: '83'
ht-degree: 12%

---

# addCompanyMitgliedschaft{#addcompanymembership}

Fügt einem oder mehreren Unternehmen einen Benutzer hinzu.

Syntax

## Autorisierte Benutzertypen {#section-ae926c7672984be79f6102748accab72}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## Parameter {#section-0e925b91d63e48aa91f0b0014e6a0cab}

**Eingabe (addCompanyMembershipParam)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| userHandle | `xsd:string` | Nein | Das -Handle für den Benutzer, dessen Mitgliedschaft Sie hinzufügen möchten. |
| membershipArray | `types:CompanyMembershipUpdateArray` | Ja | Eine Reihe von Unternehmen, denen Sie die Benutzerin bzw. den Benutzer hinzufügen. |

**Ausgabe (addCompanyMembershipReturn)**

Die IPS-API gibt keine Antwort für diesen Vorgang zurück.

## Beispiele {#section-5469f88bac7047cca131faa6b021e437}

In diesem Beispiel wird companyHandleArray verwendet, um einer einzelnen Firma einen Benutzer hinzuzufügen.

**Anfrage**

```javascript {.line-numbers}
<ns1:addCompanyMembershipParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:userHandle>621|jduvar@adobe.com</ns1:userHandle>
   <ns1:companyHandleArray>
      </ns1:items>47</ns1:items>
   </ns1:companyHandleArray>
</ns1:addCompanyMembershipParam>
```

**Antwort**

Keine.
