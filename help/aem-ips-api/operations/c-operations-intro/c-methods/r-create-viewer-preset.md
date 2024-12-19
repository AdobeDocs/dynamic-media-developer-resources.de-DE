---
description: Erstellt eine Vorgabenansicht, die bestimmt, was ein Benutzer sehen kann. Der Viewer kann von jedem in IPS verfügbaren Typ sein. Die Vorgabenansicht wird bei der Veröffentlichung der Assets angewendet.
solution: Experience Manager
title: createViewerPreset
feature: Dynamic Media Classic,SDK/API,Viewer Presets
role: Developer,Admin
exl-id: b24536d9-df66-4c94-8467-6f46e66a1b36
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '158'
ht-degree: 12%

---

# createViewerPreset{#createviewerpreset}

Erstellt eine Vorgabenansicht, die bestimmt, was ein Benutzer sehen kann. Der Viewer kann von jedem in IPS verfügbaren Typ sein. Die Vorgabenansicht wird bei der Veröffentlichung der Assets angewendet.

Syntax

## Autorisierte Benutzertypen {#section-0b8b1322ebea4a7ea24d516e080b7367}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## Parameter {#section-aa6dc37e327541ebbfed7685cd8071ff}

**Input (createViewerPresetParam)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| companyHandle | `xsd:string` | Ja | Das Handle des Unternehmens, das die Viewer-Vorgaben und Assets enthält. |
| folderHandle | `xsd:string` | Ja | Das Handle des Ordners, der die Assets enthält. |
| name | `xsd:string` | Ja | Viewer-Name. |
| Typ | `xsd:string` | Ja | Viewer-Typ. |
| configSettingArray | `types:ConfigSettingArray` | Nein | Ein Array, das Namen, Werte und Handles von Bildern enthält, auf die Sie Vorgaben anwenden. |

**Ausgabe (createViewerPresetReturn)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| viewerPresetHandle | `xsd:string` | Ja | Verarbeiten Sie die Vorgabe mit dem Viewer. |

## Beispiele {#section-c88ea63536f3461cbe4677ba53f875dd}

Dieses Codebeispiel erstellt eine Video-Player-Vorgabe. Die Antwort gibt ein Handle für die Voreinstellung zurück.

```java
<createViewerPresetParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|0</companyHandle>
   <folderHandle>Scene7SharedAssets/</folderHandle>
   <name>eVideo4</name>
   <type>VideoPlayer</type>
   <configSettingArray>
      <items>
         <name>Video Bit Rate</name>
         <value>393334.6508779093</value>
      </items>
      <items>
         <name>Audio Sample Rate</name>
         <value>44100</value>
      </items>
      ...
      <items>
         <name>vidPaneWidth</name>
         <value>0</value>
      </items>
   </configSettingArray>
</createViewerPresetParam>
```

**Antwort**

```java
<createViewerPresetReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <viewerPresetHandle>a|151760|40|151760</viewerPresetHandle>
</createViewerPresetReturn>
```
