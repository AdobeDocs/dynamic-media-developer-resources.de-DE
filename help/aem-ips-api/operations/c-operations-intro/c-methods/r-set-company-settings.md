---
description: Legt verschiedene unternehmensspezifische Konfigurationswerte fest.
solution: Experience Manager
title: setCompanySettings
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: c6b72ceb-3c86-4b13-89e9-5f1bb9846b2c
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '156'
ht-degree: 12%

---

# setCompanySettings{#setcompanysettings}

Legt verschiedene unternehmensspezifische Konfigurationswerte fest.

Syntax

## Autorisierte Benutzertypen {#section-41732fa7424b455cb458eec21a02259c}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## Parameter {#section-a472da6c57c74a94a179dda081004888}

**Eingabe (setCompanySettingsParam)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Ja | Handle des Unternehmens. |
| `*`overwriteMode`*` | `xsd:string` | Nein | Asset-Überschreibungsmodus. |
| `*`keepPublishState`*` | `xsd:boolean` | Nein | Auf `true` setzen, um den Veröffentlichungsstatus beim erneuten Hochladen eines Assets beizubehalten. |
| `*`defaultSourceProfileHandle`*` | `xsd:string` | Nein | IccProfile-Asset zur Verwendung als standardmäßiges Quellfarbprofil. |
| `*`defaultDisplayProfileHandle`*` | `xsd:string` | Nein | IccProfile-Asset zur Verwendung als standardmäßiges Anzeigefarbprofil. |
| `*`iptcExifMappingXsltHandle`*` | `xsd:string` | Nein | XSL-Asset, das für die Zuordnung von IPTC- und EXIF-Metadaten zu IPS-Metadatenfeldern verwendet wird. |
| `*`xmpMappingXsltHandle`*` | `xsd:string` | Nein | XSL-Asset, das zum Zuordnen XMP Metadaten zu IPS-Metadatenfeldern verwendet wird. |
| `*`diskSpaceWarningMin`*` | `xsd:int` | Nein | Mindestens freier Speicherplatz (in KB), der verfügbar ist, bevor eine Warnmeldung gesendet wird. |
| `*`emailTrashCleanupWarning`*` | `xsd:boolean` | Nein | Auf `true` setzen, um Unternehmensadministratoren eine Benachrichtigung zu senden, wenn Assets aus dem Papierkorb geleert werden. |

**Ausgabe (setCompanySettingsReturn)**

Die IPS-API gibt keine Antwort für diesen Vorgang zurück.

## Beispiele {#section-d10bf1d3d86f46f7bcf78dc1a2c363c5}

In diesem Codebeispiel wird die Konfiguration eines Unternehmens festgelegt.

**Anforderung**

```java
<ns1:setCompanySettingsParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <ns1:companyHandle>c|6</ns1:companyHandle>
   <ns1:overwriteMode>OverwriteFullName</ns1:overwriteMode>
   <ns1:retainPublishState>true</ns1:retainPublishState>
   <ns1:diskSpaceWarningMin>100000</ns1:diskSpaceWarningMin>
   <ns1:emailTrashCleanupWarning>true</ns1:emailTrashCleanupWarning>
</ns1:setCompanySettingsParam>
```

**Antwort**

Keine.
