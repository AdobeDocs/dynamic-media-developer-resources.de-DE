---
description: Legt die Mitgliedschaft eines Benutzers in einer oder mehreren Firmen fest.
seo-description: Legt die Mitgliedschaft eines Benutzers in einer oder mehreren Firmen fest.
seo-title: setCompanyMembership
solution: Experience Manager
title: setCompanyMembership
topic: Scene7 Image Production System API
uuid: 34c9d457-bc2e-4186-8a8f-50388410640a
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# setCompanyMembership{#setcompanymembership}

Legt die Mitgliedschaft eines Benutzers in einer oder mehreren Firmen fest.

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
| ` *`userHandle`*` | `xsd:sting` | Nein | Benutzerhandle. |
| ` *`membershipArray`*` | `types:CompanyMembershipUpdateArray` | Ja | Array von Firmen. |

**Output (setCompanyMembershipParam)**

Die IPS-API gibt keine Antwort für diesen Vorgang zurück.

## Beispiele {#section-862c0cc32ce0407ab248028e690a8386}

Mit diesem Codebeispiel wird einer Firma ein Benutzer hinzugefügt. Geben Sie bei Bedarf mehrere Firmen im Firmen-Handle-Array an.

**Anforderung**

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
