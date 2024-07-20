---
description: Gibt IPS-Einstellungen für ein bestimmtes Unternehmen zurück.
solution: Experience Manager
title: getCompanySettings
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: b9f41405-8a45-416c-acec-ef22c2ee119e
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '64'
ht-degree: 21%

---

# getCompanySettings{#getcompanysettings}

Gibt IPS-Einstellungen für ein bestimmtes Unternehmen zurück.

Syntax

## Autorisierte Benutzertypen {#section-3378c9c67029473a87d5f5d8c616b1f3}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## Parameter {#section-e146f479c2744baa8f68be8c8848c97f}

**Input (getCompanySettingsParam)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| companyHandle | `xsd:string` | Ja | Das Handle für das Unternehmen, dessen Einstellungen Sie abrufen möchten. |

**Output (getCompanySettingsReturn)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| Einstellungen | `types:CompanySettings` | Ja | Unternehmenseinstellungen. |

## Beispiele {#section-191f78995ecf473a95eadf7296204fd7}

Dieses Codebeispiel gibt alle IPS-Einstellungen für ein bestimmtes Unternehmen zurück.

**Anfrage**

```java
<ns1:getCompanySettingsParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <ns1:companyHandle>c|6</ns1:companyHandle>
</ns1:getCompanySettingsParam>
```

**Antwort**

```java
<getCompanySettingsReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <settings>
      <metadataArray>
         <items>
            <name>Profile Class</name>
            <value>1</value>
            <longVal>1</longVal>
         </items>
         <items>
             <name>Default Color Profile</name>
             <value>1</value>
         </items>
      </metadataArray>
      <iccProfileInfo>
         <originalPath>Scene7SharedAssets/ICCColorProfiles/Adobe ICC Profiles/RGB Profiles/</originalPath>
         <originalFile>sRGB Color Space Profile.icm</originalFile>
         <fileSize>0</fileSize>
      </iccProfileInfo>
      </defaultDisplayProfile>
      <diskSpaceWarningMin>100000</diskSpaceWarningMin>
      <emailTrashCleanupWarning>true</emailTrashCleanupWarning>
   </settings>
</getCompanySettingsReturn>
```
