---
description: Erstellt ein Benutzerkonto und fügt dieses Konto einem oder mehreren Unternehmen hinzu.
solution: Experience Manager
title: addUser
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: aed39e73-f528-4c26-8f62-c3d796e9101a
source-git-commit: b89ca96947f751b750623e1f18d2a5d86f0cd759
workflow-type: tm+mt
source-wordcount: '176'
ht-degree: 11%

---

# addUser{#adduser}

Erstellt ein Benutzerkonto und fügt dieses Konto einem oder mehreren Unternehmen hinzu.

Wenn Sie einen Benutzer zu mehreren Unternehmen hinzufügen, geben Sie diese Unternehmen an, indem das Unternehmen sie in `companyHandleArray` verarbeitet. Dieser Vorgang gibt den Handle an den soeben hinzugefügten Benutzer zurück.

## Autorisierte Benutzertypen {#section-126ad42f844444fea11ecf8ad01fe1ec}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## Parameter {#section-40390a512e314b8d80ecffbb7729f6fb}

**Input (addUserParam)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| firstName | `xsd:string` | Ja | Der Vorname des Benutzers. |
| lastName | `xsd:string` | Ja | Der Nachname des Benutzers. |
| E-Mail | `xsd:string` | Ja | Die E-Mail-Adresse des Benutzers. |
| defaultRole | `xsd:string` | Ja | Legt die Rolle für einen Benutzer in jedem Unternehmen fest, zu dem er gehört. Beachten Sie jedoch, dass die Rolle &quot;`IpsAdmin`&quot;andere unternehmensspezifische Einstellungen außer Kraft setzt. |
| Passwort | `xsd:string` | Ja | Legt das Kennwort des Benutzers fest |
| passwordExpires | `xsd:dateTime` | Nein | Legt die Gültigkeitsdauer des Kennworts fest. Geben Sie die Zeitzone an, in der die Anforderung übergeben wird. Die Zeitzonen werden auf die &quot;Central Time&quot;eingestellt. |
| isValid | `xsd:boolean` | Ja | Bestimmt, ob der Benutzer gültig ist. |
| membershipArray | `xsd:CompanyMembershipUpdateArray` | Ja | Ein Array von Unternehmens-Handles. |

**Output (addUserParam)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| userHandle | `xsd:string` | Ja | Der Handle für den Benutzer. |

## Beispiele {#section-2547cef622734b71919eef849960b5cb}

Die IPS-API gibt ein Benutzerhandle-Element zurück, das den neuen Benutzer angibt.

**Anfrage**

```java {.line-numbers}
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

```java {.line-numbers}
<ns1:addUserReturn xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:userHandle>525s|juser@scene7.com</ns1:userHandle>
</ns1:addUserReturn>
```
