---
description: Ruft alle Systemeigenschaften in einer einzigen Anfrage ab.
solution: Experience Manager
title: getSystemProperties
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: b0ef16fd-1645-4e22-99bb-8c9269623168
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '55'
ht-degree: 20%

---

# getSystemProperties{#getsystemproperties}

Ruft alle Systemeigenschaften in einer einzigen Anfrage ab.

Syntax

## Autorisierte Benutzertypen {#section-fc311ce90a54400fa95b9dd36b756e23}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`
* `ImagePortalUser`
* `TrialSiteAdmin`
* `TrialSiteUser`

## Parameter {#section-b2a4fb7068424223aec87c50f0586d73}

**Eingabe (getSystemPropertiesParam)**

Keine.

**Ausgabe (getSystemPropertiesReturn)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| propertyArray | `types:PropertyArray` | Ja | Ein Array von Systemeigenschaften. |

## Beispiele {#section-728cc16fe9954b2daa035b4d4d4b4ce6}

Dieses Codebeispiel gibt ein Array von Systemeigenschaften zurück. Die Antwort wurde wegen der Kürze gekürzt.

**Anforderung**

```java
<getSystemPropertiesParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-09-10"/>
```

**Antwort**

```java
<getSystemPropertiesReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-09-10"> 
   <propertyArray> 
      <items> 
         <name>SvgRenderEnabled</name> 
         <value>true</value> 
      </items> 
      <items> 
         <name>SwfRootUrl</name> 
         <value>/SWFs/</value> 
      </items> 
      ... 
   </propertyArray> 
</getSystemPropertiesReturn>
```
