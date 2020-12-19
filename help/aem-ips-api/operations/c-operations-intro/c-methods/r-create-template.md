---
description: Erstellt ein Bild mit Ebenen, das mehrere Text- und Bildebenen haben kann.
seo-description: Erstellt ein Bild mit Ebenen, das mehrere Text- und Bildebenen haben kann.
seo-title: createTemplate
solution: Experience Manager
title: createTemplate
topic: Scene7 Image Production System API
uuid: c54bd47c-13e1-4b0d-a24c-9829b0a6d5bf
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '205'
ht-degree: 10%

---


# createTemplate{#createtemplate}

Erstellt ein Bild mit Ebenen, das mehrere Text- und Bildebenen haben kann.

Der Parameter `urlModifier` gibt die im Image-Server-Katalog gespeicherten Protokollbefehle an, die vor den vom Benutzer bereitgestellten Befehlen in der URL angewendet wurden. Der Parameter `urlPostApplyModifier` gibt Protokollbefehle an, die nach beliebigen URL-Befehlen angewendet werden. Dadurch werden widersprüchliche benutzerdefinierte Einstellungen außer Kraft gesetzt.

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
| ` *`companyHandle`*` | `xsd:string` | Ja | Die Firma, zu der die Vorlage gehört. |
| ` *`folderHandle`*` | `xsd:string` | Ja | Der Ordner-Handle, der den Ordner darstellt, in dem sich die Vorlage befindet. |
| ` *`name`*` | `xsd:string` | Ja | Vorlagenname. |
| ` *`type`*` | `xsd:string` | Ja | Vorlagentyp. |
| ` *`urlModifier`*` | `xsd:string` | Ja | Gibt die im IS-Katalog gespeicherten Image-Server-Befehle an, die vor den vom Benutzer bereitgestellten Befehlen auf die URL angewendet werden. |
| ` *`urlPostApplyModifier`*` | `xsd:string` | Nein | Gibt Protokollbefehle an, die nach jedem URL-Befehl angewendet werden, wodurch die vom Benutzer bereitgestellten Einstellungen außer Kraft gesetzt werden. |

**Output (createTemplateParam)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| ` *`assetHandle`*` | `xsd:string` | Ja | Der Griff zur Vorlage. |

## Beispiele {#section-09adb4d2f0c944af875c4463a461f55d}

In diesem Codebeispiel wird eine Vorlage in einem von einem Handle angegebenen Ordner mit dem Namen `APIcreateTemplate`, `urlModifier` und `urlPostApplyModifier` erstellt. Die Antwort gibt den Handle an die neu erstellte Vorlage zurück.

**Anforderung**

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

