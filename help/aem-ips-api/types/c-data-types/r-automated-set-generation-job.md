---
description: Gruppieren Sie Dateien mithilfe eines Listen-Arrays für das Asset-Handle in Sets.
solution: Experience Manager
title: AutomatedSetGenerationJob
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 44df6dfa-1485-40c2-8a14-bbf451b87641
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '181'
ht-degree: 3%

---

# AutomatedSetGenerationJob{#automatedsetgenerationjob}

Gruppieren Sie Dateien mithilfe eines Listen-Arrays für das Asset-Handle in Sets.

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
   <td colname="col3">Ein Array von Asset-Handles, die zum Erstellen des Sets verwendet werden. <p>Standardmäßig ist 1000 die maximale Anzahl von Assets, die Sie im Array haben können. </p></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> destFolder</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Pfad zum Ordner, in dem Sie die Sets speichern möchten. Speichert standardmäßig im Stammordner des Unternehmens. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> readyForPublish</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> Legt eine Markierung fest, die angibt, ob die Assets veröffentlicht werden sollen oder nicht. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> autoSetCreationOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> Typen:AutoSetCreationOptions</span> </td> 
   <td colname="col3">Ein Array von Skripten zur Set-Generierung, die Sie für die hochgeladenen Dateien ausführen können. Siehe <a href="../../types/c-data-types/r-auto-set-creation-options.md#reference-58b42b39e53345aeb87cd1adc864e7ff" format="dita" scope="local"> AutoSetCreationOptions</a></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> emailSetting</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> <p>Richten Sie eine automatische E-Mail-Benachrichtigung für den Auftrag ein. </p> </td> 
  </tr> 
 </tbody> 
</table>

**emailSetting Options**

Der Parameter `emailSetting` umfasst die folgenden Optionen:

| Option | Rückgabe |
|---|---|
| `All` | Alle Auftragsbenachrichtigungen (Fehler, Warnungen, Abschluss) an den angegebenen Empfänger. |
| `Error` | Auftragsfehler an den angegebenen Empfänger. |
| `ErrorAndWarning` | Auftragsfehler und -warnungen an den angegebenen Empfänger. |
| `JobCompletion` | Eine Benachrichtigung zum Abschluss eines Vorgangs an den angegebenen Empfänger. |
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
