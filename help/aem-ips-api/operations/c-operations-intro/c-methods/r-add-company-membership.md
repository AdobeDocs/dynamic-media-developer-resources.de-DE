---
description: Fügt einem oder mehreren Unternehmen einen Benutzer hinzu.
solution: Experience Manager
title: addCompanyMitgliedschaft
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 6efef4fb-f2e5-4c41-b739-a36ac2f17884
TQID: 'https://experienceleague.adobe.com/VNnc-lxt0VHsrYBfJHUVTfK7Hqb42u-P-DtxNdQvS8o'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 4185012f22b173b569d11ea4d350763a82f98710
workflow-type: tm+mt
source-wordcount: 83
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

