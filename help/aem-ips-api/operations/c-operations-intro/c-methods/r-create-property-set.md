---
description: Eigenschaftensätze sind anwendungsspezifische Sätze von Name-Wert-Paaren, die je nach Eigenschaftssatz-Typ an verschiedene IPS-Objekte angehängt werden können. Wenn der Eigenschaftssatz-Typ nicht zulässt, dass mehrere Sets an ein Objekt angehängt werden (PropertySetType/allowMultipleisfalse) und das Objekt bereits über einen Satz desselben Typs verfügt, wird der neue Satz den vorhandenen ersetzen.
solution: Experience Manager
title: createPropertySet
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: e9f85e65-4a2f-4b82-b7b8-d0d60b8345cd
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '220'
ht-degree: 8%

---

# createPropertySet{#createpropertyset}

Eigenschaftensätze sind anwendungsspezifische Sätze von Name-Wert-Paaren, die je nach Eigenschaftssatz-Typ an verschiedene IPS-Objekte angehängt werden können. Wenn der Eigenschaftssatz-Typ nicht zulässt, dass mehrere Sets an ein Objekt angehängt werden (PropertySetType/allowMultipleisfalse) und das Objekt bereits über einen Satz desselben Typs verfügt, wird der neue Satz den vorhandenen ersetzen.

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
| `*`typeHandle`*` | `xsd:string` | Ja | Der Handle für den Eigenschaftssatz-Typ. |
| `*`primaryOwnerHandle`*` | `xsd:string` | Ja | Das Handle für den primären Eigentümer des Eigenschaftssatzes. |
| `*`secondaryOwnerHandle`*` | `xsd:string` | Nein | Das Handle an den sekundären Eigentümer des Eigenschaftssatzes. |
| `*`propertyArray`*` | `types:PropertyArray` | Ja | Das Array von Eigenschaften. |
| `*`permissionArray`*` | `types:PermissionUpdateArray` |  |  |

**Ausgabe (createPropertySetParam)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| `*`setHandle`*` | `xsd:string` | Ja | Der Handle für den neuen Eigenschaftssatz. |

## Beispiele {#section-4e1f5b2883664bc88f590fcd253df22b}

In diesem Codebeispiel wird ein Eigenschaftssatz erstellt, der Namen und Werte von Eigenschaften enthält. Die Antwort gibt einen Handle für den neuen Eigenschaftssatz zurück.

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
