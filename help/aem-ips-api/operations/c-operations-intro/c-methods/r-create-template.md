---
description: Erstellt ein Bild mit mehreren Ebenen, das über mehrere Text- und Bildebenen verfügen kann.
solution: Experience Manager
title: createTemplate
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 228b4228-8c42-4e42-9fb1-d6aea61b9c4a
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '190'
ht-degree: 10%

---

# createTemplate{#createtemplate}

Erstellt ein Bild mit mehreren Ebenen, das über mehrere Text- und Bildebenen verfügen kann.

Der Parameter `urlModifier` gibt die im Bildserver-Katalog gespeicherten Protokollbefehle an, die vor vom Benutzer bereitgestellten Befehlen auf die URL angewendet wurden. Der Parameter `urlPostApplyModifier` gibt Protokollbefehle an, die nach beliebigen URL-Befehlen angewendet werden, wodurch alle vom Benutzer bereitgestellten widersprüchlichen Einstellungen außer Kraft gesetzt werden.

## Autorisierte Benutzertypen {#section-9fb615d8e75f452eab2893cc3decfbe6}

* `IpsUser`
* `IpsAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parameter {#section-f54870f07d1d48fb8749ba7a4b43b6cb}

**Input (createTemplateParam)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| companyHandle | `xsd:string` | Ja | Das Unternehmen, zu dem die Vorlage gehört. |
| folderHandle | `xsd:string` | Ja | Der Ordner-Handle, der den Ordner darstellt, in dem sich die Vorlage befindet. |
| name | `xsd:string` | Ja | Vorlagenname. |
| Typ | `xsd:string` | Ja | Vorlagentyp |
| urlModifier | `xsd:string` | Ja | Gibt die im IS-Katalog gespeicherten Image-Server-Befehle an, die vor vom Benutzer bereitgestellten Befehlen auf die URL angewendet werden. |
| urlPostApplyModifier | `xsd:string` | Nein | Gibt Protokollbefehle an, die auf beliebige URL-Befehle angewendet werden, wodurch alle vom Benutzer bereitgestellten, in Konflikt stehenden Einstellungen außer Kraft gesetzt werden. |

**Output (createTemplateParam)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| assetHandle | `xsd:string` | Ja | Der Handle für die Vorlage. |

## Beispiele {#section-09adb4d2f0c944af875c4463a461f55d}

In diesem Codebeispiel wird eine Vorlage in einem Ordner erstellt, der von einem Handle mit dem Namen `APIcreateTemplate`, `urlModifier` und `urlPostApplyModifier` angegeben wird. Die Antwort gibt den Handle an die neu erstellte Vorlage zurück.

**Anfrage**

```java
<createTemplateParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|21</companyHandle>
   <folderHandle>ApiTestCo/</folderHandle>
   <name>APIcreateTemplate</name>
   <type>Template</type>
   <urlModifier>url=Modifier</urlModifier>
   <urlPostApplyModifier>urlPostApply=Modifier</urlPostApplyModifier>
</createTemplateParam>
```

**Antwort**

```java
<createTemplateReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <assetHandle>a|153393|2|2061</assetHandle>
</createTemplateReturn>
```
