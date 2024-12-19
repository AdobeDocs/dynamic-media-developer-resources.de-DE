---
description: Verwendet ein Eigenschafts-Array zum Aktualisieren eines Eigenschaftssatzes.
solution: Experience Manager
title: updatePropertySet
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: bbe6a664-b6e1-4b46-867d-a134070b13da
source-git-commit: 67e12fae514341137e4218ea950f34da0d9997f3
workflow-type: tm+mt
source-wordcount: '85'
ht-degree: 12%

---

# updatePropertySet{#updatepropertyset}

Verwendet ein Eigenschafts-Array zum Aktualisieren eines Eigenschaftssatzes.

Syntax

## Autorisierte Benutzertypen {#section-116693bbfb5d44219e62bbb1ba19de96}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parameter {#section-98361b063e9c41e8b2f744fabc0e13ed}

**Eingabe (updatePropertySetParam)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| setHandle | `xsd:string` | Ja | Verarbeiten Sie den Eigenschaftensatz. |
| replaceProperties | `xsd:string` | Nein | Auf `true` setzen, um Eigenschaften zu ersetzen. |
| propertyArray | `types:PropertyArray` | Ja | Array von aktualisierten Eigenschaften für den Eigenschaftssatz. |

**Ausgabe (updatePropertySetReturn)**

Die IPS-API gibt keine Antwort für diesen Vorgang zurück.

## Beispiele {#section-55d1c9dcd0174c6b9b52b4709f7c8bf9}

Dieses Codebeispiel aktualisiert einen Eigenschaftssatz mit Eigenschaften im Eigenschaften-Array.

**Anfrage**

```java
<updatePropertySetParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <setHandle>ps|941</setHandle>
   <replaceProperties>true</replaceProperties>
   <propertyArray>
      <items>
         <name>application_project_whatever</name>
         <value>false</value>
      </items>
      <items>
         <name>application_server_prefix_published_test</name>
         <value>http://s7teton.macromedia.com:8080/is/image/</value>
      </items>
      <items>
         <name>application_server_prefix_origin_test</name>
         <value>http://s7teton:8080/is/image/</value>
      </items>
   </propertyArray>
</updatePropertySetParam>
```

**Antwort**

Keine.
