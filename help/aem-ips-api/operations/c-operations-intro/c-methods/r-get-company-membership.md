---
description: Ruft die Mitgliedschaften eines Benutzers in einem Unternehmens-Array ab.
solution: Experience Manager
title: getCompanyMembership
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 53af8a97-208c-4c44-93d6-aa36a459af51
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '86'
ht-degree: 17%

---

# getCompanyMembership{#getcompanymembership}

Ruft die Mitgliedschaften eines Benutzers in einem Unternehmens-Array ab.

Syntax

## Autorisierte Benutzertypen {#section-f8bba547e1f648648be99dc48fd72b5d}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parameter {#section-8745c360c3e1400a88e9bdb26bcb93de}

**Eingabe (getCompanyMembershipParam)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| `*`userHandle`*` | `xsd:string` | Nein | Der Handle für den Benutzer, dessen Mitgliedschaften Sie erhalten möchten. |

**Ausgabe (getCompanyMembershipReturn)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| `*`membershipArray`*` | `types:CompanyMembershipArray` | Ja | Array von Unternehmensmitgliedschaften. |

## Beispiele {#section-e4958d104ea344a4a79f57d07b46eba7}

Dieses Codebeispiel übernimmt ein Benutzerhandbuch und ruft alle Unternehmensmitgliedschaften des Benutzers in einem Array ab. Die Antwort wurde aus Gründen der Kürze abgeschnitten.

**Anforderung**

```java
<ns1:getCompanyMembershipParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:userHandle>70|kmagnusson@adobe.com</ns1:userHandle>
</ns1:getCompanyMembershipParam>
```

**Antwort**

```java
<getCompanyMembershipReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <membershipArray>
      <items>
         <companyHandle>48</companyHandle>
         <name>AIR</name>
         <rootPath>AIR/</rootPath>
         <expires>2101-01-31T23:00:00.485-08:00</expires>
      </items>
      ...
    </membershipArray>
</getCompanyMembershipReturn>
```
