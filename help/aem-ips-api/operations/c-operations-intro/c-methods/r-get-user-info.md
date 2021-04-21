---
description: Ruft Informationen zu einem Benutzer ab. Verwenden Sie die E-Mail-Adresse und das Kennwort eines Systembenutzers als Anmeldeinformationen für die Autorisierung der Anforderung. Andernfalls ruft der Vorgang Informationen zum Standardbenutzer ab.
solution: Experience Manager
title: getUserInfo
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '146'
ht-degree: 11%

---


# getUserInfo{#getuserinfo}

Ruft Informationen zu einem Benutzer ab. Verwenden Sie die E-Mail-Adresse und das Kennwort eines Systembenutzers als Anmeldeinformationen für die Autorisierung der Anforderung. Andernfalls ruft der Vorgang Informationen zum Standardbenutzer ab.

Syntax

## Autorisierte Benutzertypen {#section-1c42d78e914a4b84a946b3480f29b36a}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parameter {#section-e87b3cb743494719925c9458eed433b6}

**Input (getUserInfoParam)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| `*`userHandle`*` | `xsd:string` | Nein | Behandeln Sie den Benutzer, dessen Informationen Sie zurückgeben möchten. |
| `*`E-Mail`*` | `xsd:string` | Nein | Benutzer-E-Mail-Adresse. |

**Output (getUserInfoReturn)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| `*`userInfo`*` | `types:User` | Ja | Vorname, Nachname, E-Mail-Adresse und Rolle eines Benutzers sowie Angabe, ob der Benutzer gültig ist und wann das Kennwort des Benutzers abläuft. |

## Beispiele {#section-98d77a2e360a438dbe240099bea26a65}

Dieses Codebeispiel gibt Informationen für den standardmäßigen IPS-Benutzer zurück.

**Anforderung**

```java
<getUserInfoParam xmlns="http://www.scene7.com/IpsApi/xsd" /></getUserInfoParam>
```

**Antwort**

```java
<ns1:getUserInfoReturn xmlns:ns1="http://www.scene7.com/IpsApi/xsd"> 
   <ns1:userInfo> 
      <ns1:userHandle>3261|user@scene7.com</ns1:userHandle> 
      <ns1:firstName>FirstName</ns1:firstName> 
      <ns1:lastName>LastName</ns1:lastName> 
      <ns1:email>user@scene7.com</ns1:email> 
      <ns1:role>IpsAdmin</ns1:role> 
      <ns1:isValid>true</ns1:isValid> 
      <ns1:passwordExpires>2107-04-22T18:35:41.995Z</ns1:passwordExpires> 
   </ns1:userInfo> 
</ns1:getUserInfoReturn>
```

