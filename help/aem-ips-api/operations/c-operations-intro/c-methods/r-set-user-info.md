---
description: Legt Benutzerattribute fest (z. B. Name, E-Mail, Rolle usw.)
solution: Experience Manager
title: setUserInfo
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: d8f8fe53-a874-4b77-9084-9a369862a672
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '113'
ht-degree: 15%

---

# setUserInfo{#setuserinfo}

Legt Benutzerattribute fest (z. B. Name, E-Mail, Rolle usw.)

Syntax

## Autorisierte Benutzertypen {#section-6c28db5d15b3449492a73749e4f981ac}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## Parameter {#section-71b457921fe74acb862a1e112e550211}

**Input (setUserInfoParam)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| userHandle | `xsd:string` | Nein | Benutzerhandbuch. |
| firstName | `xsd:string` | Ja | Vorname. |
| lastName | `xsd:string` | Ja | Nachname. |
| E-Mail | `xsd:string` | Ja | Benutzer-E-Mail. |
| defaultRole | `xsd:string` | Ja | Legt die Rolle für einen Benutzer in jedem Unternehmen fest, zu dem er gehört. Beachten Sie jedoch, dass die Rolle &quot;`IpsAdmin`&quot;andere unternehmensspezifische Einstellungen außer Kraft setzt. |
| passwordExpires | `xsd:dateTime` | Nein | Legen Sie das Ablaufdatum für das Kennwort fest. |
| isValid | `xsd:boolean` | Ja | Bestimmt, ob der Benutzer ein gültiger IPS-Benutzer ist. |
| membershipArray | `types:CompanyMembershipUpdateArray` | Ja | Ein Array von Unternehmens-Handles. |

**Output (setUserInfoReturn)**

Die IPS-API gibt keine Antwort für diesen Vorgang zurück.

## Beispiele {#section-272c103076fb4de0a53729e2f6bfb895}

**Anfrage**

```java
<setUserInfoParam xmlns="http://www.scene7.com/IpsApi/xsd">
   <firstName>test</firstName>
   <lastName>test</lastName>
   <email>test@test.test</email>
   <defaultRole>IpsAdmin</defaultRole>
   <isValid>true</isValid>
</setUserInfoParam>
```

**Antwort**

Keine.
