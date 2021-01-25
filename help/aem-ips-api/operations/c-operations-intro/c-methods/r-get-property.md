---
description: Ruft Zeichenfolgenwerte der Systemeigenschaften ab, die mit Image Portal zusammenhängen.
seo-description: Ruft Zeichenfolgenwerte der Systemeigenschaften ab, die mit Image Portal zusammenhängen.
seo-title: getProperty
solution: Experience Manager
title: getProperty
topic: Dynamic Media Image Production System API
uuid: 38ea08a6-c948-4a01-bc9a-d1609197224e
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '143'
ht-degree: 11%

---


# getProperty{#getproperty}

Ruft Zeichenfolgenwerte der Systemeigenschaften ab, die mit Image Portal zusammenhängen.

Zu den unterstützten Systemeigenschaften gehören:

* `IpsVersion`: IPS-Versionsnummer.
* `IpsImageServerUrl`: Vollständiges externes URL-Präfix für den IPS-Image-Server.
* `VideoRootUrl`
* `swfRootUrl`
* `SvgRenderRootUrl`: URL-Präfix zum Rendern von SVG-Assets.
* `SvgRenderEnabled`: True, wenn SVG-Assets von  `SvgRenderRootUrl`dargestellt werden können.

* `UploadPostMaxFileSize`: Maximale Größe (in Byte) der bei einem Hochladen zulässigen Dateidaten  [!DNL POST]. Das System lehnt Dateien ab, die größer als die Obergrenze sind.

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

**Input (getPropertyParam)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| `*`name`*` | `xsd:string` | Ja | Der Name der abzurufenden Eigenschaft. |

**Output (getPropertyReturn)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| `*`Wert`*` | `xsd:string` | Ja | Der Eigenschaftswert. |

## Beispiele {#section-3f80a78dd60c404181b34d3a912d7a36}

Dieses Codebeispiel verwendet eine IPS-Eigenschaftenzeichenfolgen-Konstante, um einen bestimmten Wert zurückzugeben. In diesem Beispiel ist die IPS-Eigenschaft die Version des IPS-Servers.

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

