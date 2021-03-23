---
description: Gibt die Benutzer einer Firma zurück, die von einem Firmen-Handle angegeben wurde.
seo-description: Gibt die Benutzer einer Firma zurück, die von einem Firmen-Handle angegeben wurde.
seo-title: getCompanyMembers
solution: Experience Manager
title: getCompanyMembers
uuid: 45e2d040-a70a-46f4-863a-633ddabcbcf6
feature: Dynamic Media Classic, SDK/API
role: Entwickler, Administrator
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '108'
ht-degree: 14%

---


# getCompanyMembers{#getcompanymembers}

Gibt die Benutzer einer Firma zurück, die von einem Firmen-Handle angegeben wurde.

Syntax

## Autorisierte Benutzertypen {#section-b2bc2fa0cc944cea8be82524838307cc}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## Parameter {#section-5602e4d6f2214e398e6a804e61f1a088}

**Input (getCompanyMembersParam)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Ja | Der Griff zu der Firma, deren Mitglieder Sie abrufen möchten. |
| `*`includeInvalid`*` | `xsd:boolean` | Ja | Schließen Sie ungültige Firmen ein. |

**Output (getCompanyMembersReturn)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| `*`memberArray`*` | `types:CompanyMemberArray` | Ja | Array von Benutzermitgliedschaften. |

## Beispiele {#section-39d8cf3653fd4fe8b842caabac9dedfc}

Dieses Codebeispiel gibt alle Member einer Firma in einem Benutzerarray zurück. Die Antwort wurde wegen ihrer Kürze abgeschnitten.

**Anforderung**

```java
<ns1:getCompanyMembersParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:includeInvalid>false</ns1:includeInvalid>
</ns1:getCompanyMembersParam>
```

**Antwort**

```java
<getCompanyMembersReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <memberArray>
      <items>
         <userHandle>66|pbayol@adobe.com</userHandle>
         <firstName>Peter</firstName>
         <lastName>Bayol</lastName>
         <email>pbayol@adobe.com</email>
         <role>IpsAdmin</role>
         <isValid>true</isValid>
         <passwordExpires>2107-07-25T23:12:49.472-07:00</passwordExpires>
      </items>
      ...
   </memberArray>
</getCompanyMembersReturn>
```

