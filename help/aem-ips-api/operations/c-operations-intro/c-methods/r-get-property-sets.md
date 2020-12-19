---
description: Ruft Eigenschaftensätze ab, die mit einem Typhandgriff verknüpft sind.
seo-description: Ruft Eigenschaftensätze ab, die mit einem Typhandgriff verknüpft sind.
seo-title: getPropertySets
solution: Experience Manager
title: getPropertySets
topic: Scene7 Image Production System API
uuid: fa3cadb3-92b3-4ffb-ac1e-87a01b98bcb2
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '99'
ht-degree: 17%

---


# getPropertySets{#getpropertysets}

Ruft Eigenschaftensätze ab, die mit einem Typhandgriff verknüpft sind.

Syntax

## Autorisierte Benutzertypen {#section-da858360b72941bfa8d9558b4da7d4da}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parameter {#section-d8da2847e77e4a95a4441d9848cac775}

**Input (getPropertySetsParam)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| ` *`typeHandle`*` | `xsd:string` | Ja | Das Handle zum Eigenschaftssatztyp. |
| ` *`primaryOwnerHandle`*` | `xsd:string` | Ja | Der primäre Eigentümer der an das Datenbankobjekt gebundenen Daten. |
| ` *`secondaryOwnerHandle`*` | `xsd:string` | Nein | Ein optionaler sekundärer Eigentümer der Daten. |

**Output (getPropertySetsReturn)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| ` *`setArray`*` | `types:PropertySetArray` | Ja | Arry of property sets. |

## Beispiele {#section-1358af974eab4259864910337a6f0bd2}

Dieses Codebeispiel gibt Eigenschaftssätze ihres primären Eigentümers zurück, die von einem Typhandle angegeben werden.

**Anforderung**

```java
<getPropertySetsParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <typeHandle>pt|10801</typeHandle>
   <primaryOwnerHandle>u|41|strangio@adobe.com</primaryOwnerHandle>
</getPropertySetsParam>
```

**Antwort**

```java
<getPropertySetsReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <setArray>
      <items>
         <setHandle>ps|941</setHandle>
         <typeHandle>pt|10801</typeHandle>
         <propertyArray>
            <items>
               <name>application_server_prefix_published_test</name>
               <value>http://s7teton.macromedia.com:8080/is/image/</value>
            </items>
            <items>
               <name>application_project_whatever</name>
               <value>false</value>
            </items>
            <items>
               <name>application_server_prefix_origin_test</name>
               <value>http://s7teton:8080/is/image</value>
            </items>
         </propertyArray>
      </items>
   </setArray>
</getPropertySetsReturn>
```

