---
description: Gibt IPS-Einstellungen für ein bestimmtes Unternehmen zurück.
solution: Experience Manager
title: getCompanySettings
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: b9f41405-8a45-416c-acec-ef22c2ee119e
TQID: 'https://experienceleague.adobe.com/9ipM09frhCvBkPESJbVmPpO3IpOnW1nqmCNA9mMeVhM'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
source-git-commit: ba0745708154402d9b6c7ebf0554deb366dde11b
workflow-type: tm+mt
source-wordcount: 64
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

**Eingabe (getCompanySettingsParam)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| companyHandle | `xsd:string` | Ja | Das -Handle für die Firma, deren Einstellungen Sie abrufen möchten. |

**Ausgabe (getCompanySettingsReturn)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| Einstellungen | `types:CompanySettings` | Ja | Unternehmenseinstellungen. |

## Beispiele {#section-191f78995ecf473a95eadf7296204fd7}

Dieses Code-Beispiel gibt alle IPS-Einstellungen für eine bestimmte Firma zurück.

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

