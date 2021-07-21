---
description: Ruft Zeichenfolgenwerte von Systemeigenschaften ab, die sich auf Image Portal beziehen.
solution: Experience Manager
title: getProperty
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 2297b785-28c7-49c6-8891-00986f35ea88
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '137'
ht-degree: 11%

---

# getProperty{#getproperty}

Ruft Zeichenfolgenwerte von Systemeigenschaften ab, die sich auf Image Portal beziehen.

Zu den unterstützten Systemeigenschaften gehören:

* `IpsVersion`: IPS-Versionsnummer.
* `IpsImageServerUrl`: Vollständiges, externes URL-Präfix für den IPS-Image-Server.
* `VideoRootUrl`
* `swfRootUrl`
* `SvgRenderRootUrl`: URL-Präfix zum Rendern von SVG-Assets.
* `SvgRenderEnabled`: True , wenn SVG-Assets von gerendert werden können  `SvgRenderRootUrl`.

* `UploadPostMaxFileSize`: Maximale Größe (in Byte) der bei einem Upload zulässigen Dateidaten  [!DNL POST]. Das System lehnt Dateien ab, die größer als das Limit sind.

## Autorisierte Benutzertypen {#section-2cd36bbd46ed414b8753569d5895530e}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parameter {#section-e3d389d183b244c2a5ef39c0ec331b5e}

**Eingabe (getPropertyParam)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| `*`name`*` | `xsd:string` | Ja | Der Name der abzurufenden Eigenschaft. |

**Ausgabe (getPropertyReturn)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| `*`Wert`*` | `xsd:string` | Ja | Der Eigenschaftswert. |

## Beispiele {#section-3f80a78dd60c404181b34d3a912d7a36}

In diesem Codebeispiel wird eine IPS-Eigenschaften-String-Konstante verwendet, um einen bestimmten Wert zurückzugeben. In diesem Beispiel ist die IPS-Eigenschaft die Version des IPS-Servers.

**Anforderung**

```java
<ns1:getPropertyParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:name>IpsVersion</ns1:name>
</ns1:getPropertyParam>
```

**Antwort**

```java
<getPropertyReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <value>3.8.0</value>
</getPropertyReturn>
```
