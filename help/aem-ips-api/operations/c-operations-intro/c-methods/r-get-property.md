---
description: Ruft Zeichenfolgenwerte von Systemeigenschaften für das Bildportal ab.
solution: Experience Manager
title: getProperty
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 2297b785-28c7-49c6-8891-00986f35ea88
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '132'
ht-degree: 10%

---

# getProperty{#getproperty}

Ruft Zeichenfolgenwerte von Systemeigenschaften für das Bildportal ab.

Zu den unterstützten Systemeigenschaften gehören:

* `IpsVersion`: IPS-Versionsnummer.
* `IpsImageServerUrl`: Vollständiges externes URL-Präfix für den IPS-Bildserver.
* `VideoRootUrl`
* `swfRootUrl`
* `SvgRenderRootUrl`: URL-Präfix für das Rendern von SVG-Assets.
* `SvgRenderEnabled`: True, wenn SVG-Assets von `SvgRenderRootUrl` gerendert werden können.

* `UploadPostMaxFileSize`: Maximale Größe (in Byte) der in einem Upload-[!DNL POST] zulässigen Dateidaten. Das System lehnt Dateien ab, die größer sind als die Höchstgrenze.

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
| name | `xsd:string` | Ja | Der Name der abzurufenden Eigenschaft. |

**Ausgabe (getPropertyReturn)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| value | `xsd:string` | Ja | Der Wert der Eigenschaft. |

## Beispiele {#section-3f80a78dd60c404181b34d3a912d7a36}

In diesem Codebeispiel wird eine Zeichenfolgenkonstante der IPS-Eigenschaften verwendet, um einen bestimmten Wert zurückzugeben. In diesem Beispiel ist die IPS-Eigenschaft die Version des IPS-Servers.

**Anfrage**

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
