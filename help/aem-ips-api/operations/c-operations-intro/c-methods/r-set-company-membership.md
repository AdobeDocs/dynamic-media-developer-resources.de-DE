---
description: Legt die Mitgliedschaft eines Benutzers in einer oder mehreren Firmen fest.
seo-description: Legt die Mitgliedschaft eines Benutzers in einer oder mehreren Firmen fest.
seo-title: setCompanyMembership
solution: Experience Manager
title: setCompanyMembership
uuid: 34c9d457-bc2e-4186-8a8f-50388410640a
feature: Dynamic Media Classic, SDK/API
role: Entwickler, Administrator
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '93'
ht-degree: 12%

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
| `*`userHandle`*` | `xsd:sting` | Nein | Benutzerhandle. |
| `*`membershipArray`*` | `types:CompanyMembershipUpdateArray` | Ja | Array von Firmen. |

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
