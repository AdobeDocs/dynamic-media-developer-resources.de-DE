---
description: Überprüft, ob sich ein Benutzer mit einem bestimmten Unternehmen (identifiziert durch Handle), einer bestimmten E-Mail-Adresse und einem bestimmten Kennwort anmelden kann.
solution: Experience Manager
title: checkLogin
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 1f96f376-574c-464b-9c89-c215f6454b81
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '145'
ht-degree: 11%

---

# checkLogin{#checklogin}

Überprüft, ob sich ein Benutzer mit einem bestimmten Unternehmen (identifiziert durch Handle), einer bestimmten E-Mail-Adresse und einem bestimmten Kennwort anmelden kann.

>[!NOTE]
>
>Wenn das Firmen-Handle weggelassen wird, prüft diese Methode die Anmeldung des Standardbenutzers.

## Autorisierte Benutzertypen {#section-df8b26b550854f899948276adaca083a}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parameter {#section-1ad4c0b4803b4388aedd655030676cb3}

**Eingabe (checkLoginParam)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| companyHandle | `xsd:string` | Nein | Das -Handle an die Firma, die den Benutzer enthält. |
| E-Mail | `xsd:string` | Ja | Die E-Mail-Adresse des Benutzers. |
| Passwort | `xsd:string` | Ja | Das Kennwort des Benutzers. |

**Ausgabe (checkLoginParam)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| status | `xsd:string` | Ja | Anmeldestatus des Benutzers. |

## Beispiele {#section-23f90100a9d94bc7b4045634cccd1b98}

Dieser Beispielcode verwendet einen Firmen-Handle-Parameter, eine E-Mail-Adresse und ein Kennwort, um zu bestimmen, ob sich ein Benutzer bei IPS anmelden kann. Wenn sich *Benutzer anmelden*, gibt diese Methode `ValidLogin` die Zeichenfolge zurück. Wenn sich *Benutzer (nicht* anmelden kann, gibt diese Methode `InvalidLogin` die Zeichenfolge zurück.

**Anfrage**

```java
<ns1:checkLoginParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>137</ns1:companyHandle>
   <ns1:email>juser3@scene7.com</ns1:email>
   <ns1:password>welcome</ns1:password>
</ns1:checkLoginParam>
```

**Antwort**

```java
<ns1:checkLoginReturn xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:status>InvalidLogin</ns1:status>
</ns1:checkLoginReturn>
```
