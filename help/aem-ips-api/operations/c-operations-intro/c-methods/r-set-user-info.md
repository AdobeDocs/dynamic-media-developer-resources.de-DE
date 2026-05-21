---
description: Legt Benutzerattribute fest (z. B. Name, E-Mail, Rolle usw.)
solution: Experience Manager
title: setUserInfo
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: d8f8fe53-a874-4b77-9084-9a369862a672
TQID: 'https://experienceleague.adobe.com/JzJv4nEeWfbY-Wp-qkEq883dlTqaRm9Fc-UvDa70dOg'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 114
ht-degree: 14%

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
| userHandle | `xsd:string` | Nein | Benutzerhandle. |
| firstName | `xsd:string` | Ja | Vorname. |
| lastName | `xsd:string` | Ja | Nachname. |
| E-Mail | `xsd:string` | Ja | Benutzer-E-Mail. |
| defaultRole | `xsd:string` | Ja | Legt die Rolle eines Benutzers in jedem Unternehmen fest, dem er angehört. Beachten Sie jedoch, dass die Rolle `IpsAdmin` andere Einstellungen pro Unternehmen überschreibt. |
| passwordExpires | `xsd:dateTime` | Nein | Legen Sie das Ablaufdatum des -Kennworts fest. |
| isValid | `xsd:boolean` | Ja | Bestimmt, ob der Benutzer ein gültiger IPS-Benutzer ist. |
| membershipArray | `types:CompanyMembershipUpdateArray` | Ja | Ein Array von Unternehmens-Handles. |

**Ausgabe (setUserInfoReturn)**

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
