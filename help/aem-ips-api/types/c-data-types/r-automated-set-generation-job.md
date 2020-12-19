---
description: Gruppieren Sie Dateien mithilfe eines Asset-Handle-Liste-Arrays in Sets.
seo-description: Gruppieren Sie Dateien mithilfe eines Asset-Handle-Liste-Arrays in Sets.
seo-title: AutomatedSetGenerationJob
solution: Experience Manager
title: AutomatedSetGenerationJob
topic: Scene7 Image Production System API
uuid: 9c664bde-a731-4d6b-ae6b-c862bda02d4c
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '187'
ht-degree: 3%

---


# AutomatedSetGenerationJob{#automatedsetgenerationjob}

Gruppieren Sie Dateien mithilfe eines Asset-Handle-Liste-Arrays in Sets.

Syntax

## Parameter {#section-939b2e6946a64238be3709fec2cd0b84}

<table id="table_0E031B2014B646BDA2A94D7E0B55DD5B"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Name </th> 
   <th colname="col2" class="entry"> Typ </th> 
   <th colname="col3" class="entry"> Beschreibung </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> assetHandleArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> Typen:HandleArray</span> </td> 
   <td colname="col3">Ein Array von Asset-Handles, mit denen der Satz erstellt wird. <p>Standardmäßig ist 1000 die maximale Anzahl von Assets, die Sie im Array haben können. </p></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> destFolder</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Pfad zu dem Ordner, in dem Sie die Sets speichern möchten. Speichert standardmäßig im Stammordner der Firma. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> readyForPublish</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> Legt ein Flag fest, das angibt, ob die Assets veröffentlicht werden sollen oder nicht. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> autoSetCreationOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> Typen:AutoSetCreationOptions</span> </td> 
   <td colname="col3">Ein Array mit Skripten zur Erzeugung von Sets, die Sie mit den hochgeladenen Dateien ausführen können. Siehe <a href="../../types/c-data-types/r-auto-set-creation-options.md#reference-58b42b39e53345aeb87cd1adc864e7ff" format="dita" scope="local"> AutoSetCreationOptions</a></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> emailSetting</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> <p>Richten Sie eine automatische E-Mail-Benachrichtigung für den Auftrag ein. </p> </td> 
  </tr> 
 </tbody> 
</table>

**emailSetting-Optionen**

Der Parameter `emailSetting` enthält die folgenden Optionen:

| Option | Rückgabe |
|---|---|
| `All` | Alle Auftragsbenachrichtigungen (Fehler, Warnungen, Abschluss) an den angegebenen Empfänger. |
| `Error` | Auftragsfehler im angegebenen Empfänger. |
| `ErrorAndWarning` | Auftragsfehler und Warnungen beim angegebenen Empfänger. |
| `JobCompletion` | Eine Auftragsabschlussbenachrichtigung an den angegebenen Empfänger. |
| `None` | Der Auftrag sendet keine Auftragsbenachrichtigungen an den angegebenen Empfänger. |

## Beispiel {#section-d01ee7671f274a1fa12737e8df91d2cf}

```
<complexType name="AutomatedSetGenerationJob">
  <sequence>
    <element name="assetHandleArray" type="types:HandleArray"/>
    <element name="destFolder" type="xsd:string" minOccurs="0"/>
    <element name="readyForPublish" type="xsd:boolean"/>
    <element name="autoSetCreationOptions" type="types:AutoSetCreationOptions"/>
    <element name="emailSetting" type="xsd:string"/>
  </sequence>
</complexType>
```

