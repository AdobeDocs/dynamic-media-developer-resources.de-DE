---
description: Verwendet ein Eigenschaftenarray, um einen Eigenschaftensatz zu aktualisieren.
seo-description: Verwendet ein Eigenschaftenarray, um einen Eigenschaftensatz zu aktualisieren.
seo-title: updatePropertySet
solution: Experience Manager
title: updatePropertySet
topic: Scene7 Image Production System API
uuid: 21a59c5a-7799-4af6-ab9f-b0311f5f7254
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '95'
ht-degree: 13%

---


# updatePropertySet{#updatepropertyset}

Verwendet ein Eigenschaftenarray, um einen Eigenschaftensatz zu aktualisieren.

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

**Input (updatePropertySetParam)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| ` *`setHandle`*` | `xsd:string` | Ja | Verarbeiten Sie den Eigenschaftensatz. |
| ` *`replaceProperties`*` | `xsd:string` | Nein | Auf `true` setzen, um Eigenschaften zu ersetzen. |
| ` *`propertyArray`*` | `types:PropertyArray` | Ja | Array mit aktualisierten Eigenschaften für den Eigenschaftensatz. |

**Output (updatePropertySetReturn)**

Die IPS-API gibt keine Antwort für diesen Vorgang zurück.

## Beispiele {#section-55d1c9dcd0174c6b9b52b4709f7c8bf9}

Dieses Codebeispiel aktualisiert einen Eigenschaftssatz mit Eigenschaften im Eigenschaftenarray.

**Anforderung**

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
