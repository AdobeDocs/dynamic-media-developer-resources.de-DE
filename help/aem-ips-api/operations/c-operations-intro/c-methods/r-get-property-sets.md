---
description: Ruft Eigenschaftensätze ab, die mit einem Handle-Typ verknüpft sind.
solution: Experience Manager
title: getPropertySets
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: da6923c3-9b86-4595-8205-645fb10e03b0
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '90'
ht-degree: 16%

---

# getPropertySets{#getpropertysets}

Ruft Eigenschaftensätze ab, die mit einem Handle-Typ verknüpft sind.

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

**Eingabe (getPropertySetsParam)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| typeHandle | `xsd:string` | Ja | Das Handle des Eigenschaftssatztyps. |
| primaryOwnerHandle | `xsd:string` | Ja | Der primäre Eigentümer der an das Datenbankobjekt gebundenen Daten. |
| secondaryOwnerHandle | `xsd:string` | Nein | Ein optionaler sekundärer Eigentümer der Daten. |

**Ausgabe (getPropertySetsReturn)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| setArray | `types:PropertySetArray` | Ja | Array von Eigenschaftensätzen. |

## Beispiele {#section-1358af974eab4259864910337a6f0bd2}

Dieses Codebeispiel gibt Eigenschaftssätze ihres primären Besitzers zurück, die durch ein Handle-Typ angegeben sind.

**Anfrage**

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
