---
description: Legt Benutzerattribute fest (z. B. Name, E-Mail, Rolle usw.)
seo-description: Legt Benutzerattribute fest (z. B. Name, E-Mail, Rolle usw.)
seo-title: setUserInfo
solution: Experience Manager
title: setUserInfo
topic: Scene7 Image Production System API
uuid: 52e3a21e-1dd5-4f9d-b460-506d280fff47
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '116'
ht-degree: 16%

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
| ` *`userHandle`*` | `xsd:string` | Nein | Benutzerhandle. |
| ` *`firstName`*` | `xsd:string` | Ja | Vorname. |
| ` *`lastName`*` | `xsd:string` | Ja | Nachname. |
| ` *`E-Mail`*` | `xsd:string` | Ja | Benutzer-E-Mail. |
| ` *`defaultRole`*` | `xsd:string` | Ja | Legt die Rolle eines Benutzers in jeder Firma fest, zu der er gehört. Beachten Sie jedoch, dass die `IpsAdmin`-Rolle andere Einstellungen pro Firma außer Kraft setzt. |
| ` *`passwordExpires`*` | `xsd:dateTime` | Nein | Das Ablaufdatum des Kennworts festlegen. |
| ` *`isValid`*` | `xsd:boolean` | Ja | Bestimmt, ob der Benutzer ein gültiger IPS-Benutzer ist. |
| ` *`membershipArray`*` | `types:CompanyMembershipUpdateArray` | Ja | Ein Array von Firmen-Handles. |

**Output (setUserInfoReturn)**

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
