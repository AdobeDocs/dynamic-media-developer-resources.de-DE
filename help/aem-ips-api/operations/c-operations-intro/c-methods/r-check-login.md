---
description: Überprüft, ob sich ein Benutzer mit einer bestimmten Firma (anhand von Handle identifiziert), E-Mail-Adresse und Kennwort anmelden kann.
seo-description: Überprüft, ob sich ein Benutzer mit einer bestimmten Firma (anhand von Handle identifiziert), E-Mail-Adresse und Kennwort anmelden kann.
seo-title: checkLogin
solution: Experience Manager
title: checkLogin
topic: Scene7 Image Production System API
uuid: 69f9e5f6-50c2-403d-93b2-b84a01f512a9
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '164'
ht-degree: 11%

---


# checkLogin{#checklogin}

Überprüft, ob sich ein Benutzer mit einer bestimmten Firma (anhand von Handle identifiziert), E-Mail-Adresse und Kennwort anmelden kann.

>[!NOTE]
>
>Wenn der Firma-Handle weggelassen wird, prüft diese Methode die Anmeldung des Standardbenutzers.

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

**Input (checkLoginParam)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | Nein | Das Handle der Firma, in der sich der Benutzer befindet. |
| ` *`E-Mail`*` | `xsd:string` | Ja | Die E-Mail-Adresse des Benutzers. |
| ` *`Passwort`*` | `xsd:string` | Ja | Das Kennwort des Benutzers. |

**Output (checkLoginParam)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| ` *`status`*` | `xsd:string` | Ja | Anmeldestatus des Benutzers. |

## Beispiele {#section-23f90100a9d94bc7b4045634cccd1b98}

Dieser Beispielcode verwendet einen Firmen-Handle-Parameter, eine E-Mail-Adresse und ein Kennwort, um zu ermitteln, ob sich ein Benutzer beim IPS anmelden kann. Wenn sich der Benutzer *can* anmeldet, gibt diese Methode die Zeichenfolge `ValidLogin` zurück. Wenn sich der Benutzer *nicht* anmelden kann, gibt diese Methode die Zeichenfolge `InvalidLogin` zurück.

**Anforderung**

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

