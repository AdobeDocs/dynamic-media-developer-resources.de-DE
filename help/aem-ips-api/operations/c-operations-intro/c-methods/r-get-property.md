---
description: Ruft Zeichenfolgenwerte von Systemeigenschaften für das Bildportal ab.
solution: Experience Manager
title: getProperty
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 2297b785-28c7-49c6-8891-00986f35ea88
TQID: 'https://experienceleague.adobe.com/loaZvP3tI8neQ6ziLR-xKkkNqGGjD8Mq1jbeC8mJEQo'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 132
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
