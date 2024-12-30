---
description: Erzeugt ein neues Kennwort
solution: Experience Manager
title: generatePassword
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 80e7642f-4aec-4ff0-a090-e59b7a065c39
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '59'
ht-degree: 16%

---

# generatePassword{#generatepassword}

Erzeugt ein neues Kennwort

Syntax

## Autorisierte Benutzertypen {#section-88f7dc11e5c74be281399d8f2e3c9555}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parameter {#section-d516615c906240819a284786efb19863}

**Input (generatePasswordParam)**

Keine.

**Ausgabe (generatePasswordParam)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| Passwort | `xsd:string` | Ja | Ein neues Kennwort. |

## Beispiele {#section-f580fefdccec46fe95359e3aef0ed17f}

Dieses Code-Beispiel generiert ein Kennwort. Dies ist ungewöhnlich, da die Anfrage einfach ein Parameter ohne eingeschlossene Elemente oder Werte ist. IPS gibt ein sicheres Kennwort zurück.

**Anfrage**

```java
<generatePasswordParam xmlns="http://www.scene7.com/IpsApi/xsd">
</generatePasswordParam>
```

**Antwort**

```java
<generatePasswordReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <password>1\7aQRn]</password>
</generatePasswordReturn>
```
