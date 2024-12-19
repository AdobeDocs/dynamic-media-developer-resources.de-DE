---
description: Erstellt ein mehrschichtiges Bild, das mehrere Text- und Bildebenen haben kann.
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

Erstellt ein mehrschichtiges Bild, das mehrere Text- und Bildebenen haben kann.

Der Parameter `urlModifier` gibt die im Image-Server-Katalog gespeicherten Image-Server-Protokollbefehle an, die vor allen vom Benutzer über die URL bereitgestellten Befehlen angewendet werden. Der `urlPostApplyModifier`-Parameter gibt Protokollbefehle an, die nach allen URL-Befehlen angewendet werden, wodurch alle widersprüchlichen von Benutzenden bereitgestellten Einstellungen überschrieben werden.

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
| folderHandle | `xsd:string` | Ja | Das Ordner-Handle, das den Ordner darstellt, in dem sich die Vorlage befindet. |
| name | `xsd:string` | Ja | Name der Vorlage. |
| Typ | `xsd:string` | Ja | Vorlagentyp. |
| urlModifier | `xsd:string` | Ja | Gibt die im IMS-Katalog gespeicherten Image-Server-Befehle an, die vor allen vom Benutzer bereitgestellten Befehlen auf der URL angewendet werden. |
| urlPostApplyModifier | `xsd:string` | Nein | Gibt Protokollbefehle an, die nach allen URL-Befehlen angewendet werden, wodurch alle konfliktbehafteten, von Benutzenden bereitgestellten Einstellungen überschrieben werden. |

**Ausgabe (createTemplateParam)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| assetHandle | `xsd:string` | Ja | Der Handler zur Vorlage. |

## Beispiele {#section-09adb4d2f0c944af875c4463a461f55d}

In diesem Codebeispiel wird eine Vorlage in einem durch ein Handle angegebenen Ordner mit dem Namen `APIcreateTemplate`, einer `urlModifier` und einer `urlPostApplyModifier` erstellt. Die Antwort gibt das Handle an die neu erstellte Vorlage zurück.

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
