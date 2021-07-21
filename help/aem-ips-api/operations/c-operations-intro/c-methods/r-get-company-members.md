---
description: Gibt die Benutzer eines Unternehmens zurück, die von einem Handle des Unternehmens angegeben wurden.
solution: Experience Manager
title: getCompanyMembers
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: da5e5a48-2e0b-4ccc-a71e-b5b746484d4a
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '94'
ht-degree: 17%

---

# getCompanyMembers{#getcompanymembers}

Gibt die Benutzer eines Unternehmens zurück, die von einem Handle des Unternehmens angegeben wurden.

Syntax

## Autorisierte Benutzertypen {#section-b2bc2fa0cc944cea8be82524838307cc}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## Parameter {#section-5602e4d6f2214e398e6a804e61f1a088}

**Eingabe (getCompanyMembersParam)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Ja | Der Handle für das Unternehmen, dessen Mitglieder Sie erhalten möchten. |
| `*`includeInvalid`*` | `xsd:boolean` | Ja | Schließen Sie ungültige Unternehmen ein. |

**Ausgabe (getCompanyMembersReturn)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| `*`memberArray`*` | `types:CompanyMemberArray` | Ja | Array von Benutzermitgliedschaften. |

## Beispiele {#section-39d8cf3653fd4fe8b842caabac9dedfc}

Dieses Codebeispiel gibt alle Mitglieder eines Unternehmens in einem Benutzer-Array zurück. Die Antwort wurde aus Gründen der Kürze abgeschnitten.

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
