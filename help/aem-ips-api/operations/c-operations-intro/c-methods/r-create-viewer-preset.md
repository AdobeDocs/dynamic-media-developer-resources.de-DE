---
description: Erstellt eine Vorgabenansicht, die bestimmt, was ein Benutzer sehen kann. Der Viewer kann einen beliebigen Typ aufweisen, der in IPS verfügbar ist. Die Vorgabenansicht wird angewendet, wenn die Assets veröffentlicht werden.
solution: Experience Manager
title: createViewerPreset
feature: Dynamic Media Classic,SDK/API,Viewer-Vorgaben
role: Developer,Admin
exl-id: b24536d9-df66-4c94-8467-6f46e66a1b36
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '165'
ht-degree: 13%

---

# createViewerPreset{#createviewerpreset}

Erstellt eine Vorgabenansicht, die bestimmt, was ein Benutzer sehen kann. Der Viewer kann einen beliebigen Typ aufweisen, der in IPS verfügbar ist. Die Vorgabenansicht wird angewendet, wenn die Assets veröffentlicht werden.

Syntax

## Autorisierte Benutzertypen {#section-0b8b1322ebea4a7ea24d516e080b7367}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## Parameter {#section-aa6dc37e327541ebbfed7685cd8071ff}

**Eingabe (createViewerPresetParam)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Ja | Das Handle des Unternehmens, das die Viewer-Vorgaben und Assets enthält. |
| `*`folderHandle`*` | `xsd:string` | Ja | Der Handle des Ordners, der die Assets enthält. |
| `*`name`*` | `xsd:string` | Ja | Viewer-Name. |
| `*`type`*` | `xsd:string` | Ja | Viewer-Typ. |
| `*`configSettingArray`*` | `types:ConfigSettingArray` | Nein | Ein Array, das Namen, Werte und Handles von Bildern enthält, auf die Sie Vorgaben anwenden. |

**Ausgabe (createViewerPresetReturn)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| `*`viewerPresetHandle`*` | `xsd:string` | Ja | Handhabung der Vorgabe an den Viewer. |

## Beispiele {#section-c88ea63536f3461cbe4677ba53f875dd}

In diesem Codebeispiel wird eine Videoplayer-Vorgabe erstellt. Die Antwort gibt einen Handle an die Vorgabe zurück.

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
