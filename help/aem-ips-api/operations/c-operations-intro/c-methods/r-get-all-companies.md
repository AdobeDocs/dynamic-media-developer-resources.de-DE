---
description: Gibt ein Array aller Firmen zurück.
solution: Experience Manager
title: getAllCompanies
feature: Dynamic Media Classic, SDK/API
role: Entwickler, Administrator
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '77'
ht-degree: 19%

---


# getAllCompanies{#getallcompanies}

Gibt ein Array aller Firmen zurück.

Syntax

## Autorisierte Benutzertypen {#section-773db3753b4842e5a4623ad810176508}

* `IpsAdmin`

## Parameter {#section-efd74992e6904ebabe7383b577af4fdb}

**Input (getAllCompaniesParam)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| `*`includeExpired`*` | `xsd:boolean` | Ja | Auf &quot;true&quot;setzen, um abgelaufene und nicht abgelaufene Firmen zurückzugeben. |

**Output (getAllCompaniesReturn)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| `*`companyArray`*` | `types:CompanyArray` | Ja | Das Array der Firmen. |

## Beispiele {#section-3eecf4e6900b41fb92a0e3214791c6b9}

Dieses Codebeispiel gibt alle Firmen in IPS in einem Array zurück. Beachten Sie, dass die Stichprobenantwort für die Kürze abgeschnitten wird.

**Anforderung**

```java
<ns1:getAllCompaniesParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:includeExpired>false</ns1:includeExpired>
</ns1:getAllCompaniesParam>
```

**Antwort**

```java
<ns1:getAllCompaniesReturnxmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyArray>
      <ns1:items>
         <ns1:companyHandle>18</ns1:companyHandle>
         <ns1:name>00webload</ns1:name>
         <ns1:rootPath>00webload/</ns1:rootPath>
         <ns1:expires>2101-02-01T07:00:00.667Z</ns1:expires>
      </ns1:items>
      <ns1:items>
         <ns1:companyHandle>19</ns1:companyHandle>
         <ns1:name>01webload</ns1:name>
         <ns1:rootPath>01webload/</ns1:rootPath>
         <ns1:expires>2101-02-01T07:00:00.414Z</ns1:expires>
      </ns1:items>
      . . .
   </ns1:companyArray>
</ns1:getAllCompaniesReturn>
```

