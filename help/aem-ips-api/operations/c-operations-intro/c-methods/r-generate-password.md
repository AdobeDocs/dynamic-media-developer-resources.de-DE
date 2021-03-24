---
description: Erstellt ein neues Kennwort.
solution: Experience Manager
title: generatePassword
feature: Dynamic Media Classic, SDK/API
role: Entwickler, Administrator
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '66'
ht-degree: 18%

---


# generatePassword{#generatepassword}

Erstellt ein neues Kennwort.

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

**Output (generatePasswordParam)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| `*`Passwort`*` | `xsd:string` | Ja | Ein neues Kennwort. |

## Beispiele {#section-f580fefdccec46fe95359e3aef0ed17f}

Dieses Codebeispiel generiert ein Kennwort. Es ist ungewöhnlich, da die Anforderung einfach ein Parameter ohne eingeschlossene Elemente oder Werte ist. IPS gibt ein sicheres Kennwort zurück.

**Anforderung**

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

