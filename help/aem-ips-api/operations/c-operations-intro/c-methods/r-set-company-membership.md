---
description: Legt die Mitgliedschaft eines Benutzers in einem oder mehreren Unternehmen fest.
solution: Experience Manager
title: setCompanyMembership
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 43144c75-1d83-4e1d-8319-c3275d349a2f
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '76'
ht-degree: 13%

---

# setCompanyMembership{#setcompanymembership}

Legt die Mitgliedschaft eines Benutzers in einem oder mehreren Unternehmen fest.

Syntax

## Autorisierte Benutzertypen {#section-0cbcc78cfee64c2baf66f29cce6d0a65}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## Parameter {#section-3930dc6a016140178631083563598104}

**Input (setCompanyMembershipParam)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| userHandle | `xsd:sting` | Nein | Benutzerhandbuch. |
| membershipArray | `types:CompanyMembershipUpdateArray` | Ja | Array von Unternehmen. |

**Output (setCompanyMembershipParam)**

Die IPS-API gibt keine Antwort für diesen Vorgang zurück.

## Beispiele {#section-862c0cc32ce0407ab248028e690a8386}

Mit diesem Codebeispiel wird ein Benutzer zu einem Unternehmen hinzugefügt. Geben Sie bei Bedarf mehrere Unternehmen im Handle-Array des Unternehmens an.

**Anfrage**

```java
<ns1:setCompanyMembershipParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:userHandle>3341|juser@scene7.com</ns1:userHandle>
   <ns1:companyHandleArray>
      <ns1:items>137</ns1:items>
   </ns1:companyHandleArray>
</ns1:setCompanyMembershipParam>
```

**Antwort**

Keine.
