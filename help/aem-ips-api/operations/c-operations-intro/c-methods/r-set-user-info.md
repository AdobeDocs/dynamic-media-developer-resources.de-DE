---
description: Legt Benutzerattribute fest (z. B. Name, E-Mail, Rolle usw.)
solution: Experience Manager
title: setUserInfo
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: d8f8fe53-a874-4b77-9084-9a369862a672
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '107'
ht-degree: 17%

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

**Eingabe (setUserInfoParam)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| userHandle | `xsd:string` | Nein | Benutzerhandbuch. |
| firstName | `xsd:string` | Ja | Vorname. |
| lastName | `xsd:string` | Ja | Nachname. |
| E-Mail | `xsd:string` | Ja | Benutzer-E-Mail. |
| defaultRole | `xsd:string` | Ja | Legt die Rolle für einen Benutzer in jedem Unternehmen fest, zu dem er gehört. Beachten Sie jedoch die `IpsAdmin` -Rolle überschreibt andere unternehmensspezifische Einstellungen. |
| passwordExpires | `xsd:dateTime` | Nein | Legen Sie das Ablaufdatum für das Kennwort fest. |
| isValid | `xsd:boolean` | Ja | Bestimmt, ob der Benutzer ein gültiger IPS-Benutzer ist. |
| membershipArray | `types:CompanyMembershipUpdateArray` | Ja | Ein Array von Unternehmens-Handles. |

**Ausgabe (setUserInfoReturn)**

Die IPS-API gibt keine Antwort für diesen Vorgang zurück.

## Beispiele {#section-272c103076fb4de0a53729e2f6bfb895}

**Anforderung**

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
