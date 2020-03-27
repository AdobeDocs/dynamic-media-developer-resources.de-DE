---
description: Erstellt ein Benutzerkonto und fügt dieses einer oder mehreren Firmen hinzu.
seo-description: Erstellt ein Benutzerkonto und fügt dieses einer oder mehreren Firmen hinzu.
seo-title: addUser
solution: Experience Manager
title: addUser
topic: Scene7 Image Production System API
uuid: b8c5ada6-470e-4795-a4f3-20750da709a9
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# addUser{#adduser}

Erstellt ein Benutzerkonto und fügt dieses einer oder mehreren Firmen hinzu.

Wenn Sie einen Benutzer zu mehreren Firmen hinzufügen, geben Sie diese Firmen an ihren Firmen-Handles in `companyHandleArray`. Dieser Vorgang gibt das Handle an den soeben hinzugefügten Benutzer zurück.

## Autorisierte Benutzertypen {#section-126ad42f844444fea11ecf8ad01fe1ec}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## Parameter {#section-40390a512e314b8d80ecffbb7729f6fb}

**Input (addUserParam)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| ` *`firstName`*` | `xsd:string` | Ja | Der Vorname des Benutzers. |
| ` *`lastName`*` | `xsd:string` | Ja | Der Nachname des Benutzers. |
| ` *`E-Mail`*` | `xsd:string` | Ja | Die E-Mail-Adresse des Benutzers. |
| ` *`defaultRole`*` | `xsd:string` | Ja | Legt die Rolle eines Benutzers in jeder Firma fest, zu der er gehört. Beachten Sie jedoch, dass die `IpsAdmin` Rolle andere Einstellungen pro Firma außer Kraft setzt. |
| ` *`Passwort`*` | `xsd:string` | Ja | Legt das Kennwort des Benutzers fest |
| ` *`passwordExpires`*` | `xsd:dateTime` | Nein | Legt den Ablauf des Kennworts fest. Geben Sie die Zeitzone beim Übergeben der Anforderung an. Die Zeitzonen werden auf &quot;Central Time&quot;eingestellt. |
| ` *`isValid`*` | `xsd:boolean` | Ja | Bestimmt, ob der Benutzer gültig ist. |
| ` *`membershipArray`*` | `xsd:CompanyMembershipUpdateArray` | Ja | Ein Array von Firmen-Handles. |

**Output (addUserParam)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| ` *`userHandle`*` | `xsd:string` | Ja | Das Handle für den Benutzer. |

## Beispiele {#section-2547cef622734b71919eef849960b5cb}

Die IPS-API gibt ein Benutzerhandbuchelement zurück, das den neuen Benutzer angibt.

**Anforderung**

```java
<ns1:addUserParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:firstName>Joe</ns1:firstName>
   <ns1:lastName>User</ns1:lastName>
   <ns1:email>juser@adobe.com</ns1:email>
   <ns1:defaultRole>TrialSiteUser</ns1:role>
   <ns1:password>passw0rd</ns1:password>
   <ns1:isValid>true</ns1:isValid>
   <ns1:companyHandleArray>
      <ns1:items>47</ns1:items>
   </ns1:companyHandleArray>
</ns1:addUserParam>
```

**Antwort**

```java
<ns1:addUserReturn xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:userHandle>525s|juser@scene7.com</ns1:userHandle>
</ns1:addUserReturn>
```

