---
description: Eigenschaftensätze sind anwendungsspezifische Sätze von Name-Wert-Paaren, die je nach Eigenschaftssatztyp an verschiedene IPS-Objekte angehängt werden können. Wenn der Eigenschaftssatztyp nicht zulässt, dass mehrere Sätze an ein Objekt angehängt werden (PropertySetType/allowMultipleisfalse) und das Objekt bereits über einen zugeordneten Satz desselben Typs verfügt, ersetzt der neue Satz den vorhandenen.
seo-description: Eigenschaftensätze sind anwendungsspezifische Sätze von Name-Wert-Paaren, die je nach Eigenschaftssatztyp an verschiedene IPS-Objekte angehängt werden können. Wenn der Eigenschaftssatztyp nicht zulässt, dass mehrere Sätze an ein Objekt angehängt werden (PropertySetType/allowMultipleisfalse) und das Objekt bereits über einen zugeordneten Satz desselben Typs verfügt, ersetzt der neue Satz den vorhandenen.
seo-title: createPropertySet
solution: Experience Manager
title: createPropertySet
topic: Scene7 Image Production System API
uuid: f0b5b951-143f-4a31-bb6b-cdeabdebbcbb
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '276'
ht-degree: 6%

---


# createPropertySet{#createpropertyset}

Eigenschaftensätze sind anwendungsspezifische Sätze von Name-Wert-Paaren, die je nach Eigenschaftssatztyp an verschiedene IPS-Objekte angehängt werden können. Wenn der Eigenschaftssatztyp nicht zulässt, dass mehrere Sätze an ein Objekt angehängt werden (PropertySetType/allowMultipleisfalse) und das Objekt bereits über einen zugeordneten Satz desselben Typs verfügt, ersetzt der neue Satz den vorhandenen.

Syntax

## Autorisierte Benutzertypen {#section-f9b6187ba636475787c997fc27bb192a}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## Parameter {#section-25258e75f5f3419bad165c797eb6cd8e}

**Input (createPropertySetParam)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| ` *`typeHandle`*` | `xsd:string` | Ja | Das Handle zum Eigenschaftssatztyp. |
| ` *`primaryOwnerHandle`*` | `xsd:string` | Ja | Das Handle für den primären Eigentümer der festgelegten Eigenschaft. |
| ` *`secondaryOwnerHandle`*` | `xsd:string` | Nein | Das Handle für den sekundären Eigentümer der festgelegten Eigenschaft. |
| ` *`propertyArray`*` | `types:PropertyArray` | Ja | Das Array der Eigenschaften. |
| ` *`permissionArray`*` | `types:PermissionUpdateArray` |  |  |

**Output (createPropertySetParam)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| ` *`setHandle`*` | `xsd:string` | Ja | Das Handle für die neue Eigenschaft. |

## Beispiele {#section-4e1f5b2883664bc88f590fcd253df22b}

Dieses Codebeispiel erstellt einen Eigenschaftensatz, der die Namen und Werte der Eigenschaften enthält. Die Antwort gibt einen Handle für den neuen Eigenschaftensatz zurück.

**Anforderung**

```java
<createPropertySetParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <typeHandle>pt|10801</typeHandle>
   <primaryOwnerHandle>u|41|strangio@adobe.com</primaryOwnerHandle>
   <propertyArray>
      <items>
         <name>application_project_whatever</name>
         <value>true</value>
      </items>
      <items>
         <name>application_server_prefix_published_test</name>
         <value>http://s7everest.macromedia.com:8080/is/image/</value>
      </items>
      <items>
         <name>application_server_prefix_origin_test</name>
         <value>http://s7everest:8080/is/image/</value>
      </items>
   </propertyArray>
</createPropertySetParam>
```

**Antwort**

```java
<createPropertySetReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <setHandle>ps|941</setHandle>
</createPropertySetReturn>
```

