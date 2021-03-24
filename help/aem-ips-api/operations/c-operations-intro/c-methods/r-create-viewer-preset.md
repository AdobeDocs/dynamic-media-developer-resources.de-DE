---
description: Erstellt eine voreingestellte Ansicht, die bestimmt, was ein Benutzer sehen kann. Der Viewer kann von jedem in IPS verfügbaren Typ sein. Die voreingestellte Ansicht wird angewendet, wenn die Assets veröffentlicht werden.
solution: Experience Manager
title: createViewerPreset
feature: Dynamic Media Classic,SDK/API,Viewer-Vorgaben
role: Entwickler, Administrator
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '167'
ht-degree: 13%

---


# createViewerPreset{#createviewerpreset}

Erstellt eine voreingestellte Ansicht, die bestimmt, was ein Benutzer sehen kann. Der Viewer kann von jedem in IPS verfügbaren Typ sein. Die voreingestellte Ansicht wird angewendet, wenn die Assets veröffentlicht werden.

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
| `*`companyHandle`*` | `xsd:string` | Ja | Das Handle der Firma, die die Viewer-Vorgaben und -Elemente enthält. |
| `*`folderHandle`*` | `xsd:string` | Ja | Das Handle des Ordners, der die Assets enthält. |
| `*`name`*` | `xsd:string` | Ja | Viewer-Name. |
| `*`type`*` | `xsd:string` | Ja | Viewer-Typ. |
| `*`configSettingArray`*` | `types:ConfigSettingArray` | Nein | Ein Array, das Namen, Werte und Griffe von Bildern enthält, auf die Sie Vorgaben anwenden. |

**Output (createViewerPresetReturn)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| `*`viewerPresetHandle`*` | `xsd:string` | Ja | Handhabung der Vorgabe für den Viewer. |

## Beispiele {#section-c88ea63536f3461cbe4677ba53f875dd}

In diesem Codebeispiel wird eine Video-Player-Vorgabe erstellt. Die Antwort gibt einen Griff zur Vorgabe zurück.

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

