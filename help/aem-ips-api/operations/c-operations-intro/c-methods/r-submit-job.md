---
description: Sendet einen Auftrag an das System.
solution: Experience Manager
title: submitJob
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: b1dc7a0e-da9a-4086-822b-5274bd62eadf
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '407'
ht-degree: 8%

---

# submitJob{#submitjob}

Sendet einen Auftrag an das System.

Syntax

## Autorisierte Benutzertypen {#section-eb7024277bec43c79e03f396205be16f}

* `IpsUser`
* `IpsAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parameter {#section-31a07dbccf964850883e817384499459}

**Eingabe (submitJobParam)**

<table id="table_9CB1F668E036422E8CE4E0BBA42EC44C"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Name </p> </th> 
   <th colname="col2" class="entry"> <p>Typ </p> </th> 
   <th colname="col3" class="entry"> <p>Erforderlich </p> </th> 
   <th colname="col4" class="entry"> <p>Beschreibung </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> companyHandle</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Ja </td> 
   <td colname="col4"> <p>Handle des Unternehmens. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> userHandle</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Nein </td> 
   <td colname="col4"> <p>Behandeln Sie den Benutzer, der den Auftrag gesendet hat. </p> <p> <p>Hinweis: Das System sendet eine E-Mail an den von <span class="codeph"> userHandle</span>. Wenn <span class="codeph"> userHandle</span> nicht angegeben ist, erhält die Person, die den Auftrag gesendet hat, die E-Mails. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> jobName</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Ja </td> 
   <td colname="col4"> <p>Auftragsname. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> locale</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Nein </td> 
   <td colname="col4"> <p>Das Gebietsschema, das für Auftragsprotokolldetails und die E-Mail-Lokalisierung verwendet wird. </p> <p>Gebietsschemata werden als <span class="codeph"> &lt;language_code&gt;</span> und <span class="codeph"> [&lt;country_code&gt;]</span>, wobei der Sprachcode ein aus zwei Buchstaben bestehender Code in Kleinbuchstaben ist, wie in ISO-639 angegeben, und der optionale Ländercode ein aus Großbuchstaben bestehender Code aus zwei Buchstaben gemäß ISO-3166 ist. Die Gebietsschema-Zeichenfolge für Englisch (USA) lautet beispielsweise: en-US. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> execTime</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:dateTime</span> </td> 
   <td colname="col3"> Nein </td> 
   <td colname="col4"> <p>Datum und Uhrzeit der Auftragsausführung. </p> <p>Hinweis: Geben Sie die Zeitzone mit der Anforderung an. Die Zeitzonen werden an die Zeitzone des Ziel-IPS-Servers angepasst. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> execSchedule</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Nein </td> 
   <td colname="col4"> <p>Legt fest, wann der Auftrag ausgeführt werden soll. </p> <p> Kann eine <span class="codeph"> cron</span> -Zeichenfolge, die den Auftrag wiederholt ausführt. </p> <p>Der Zeitplan ist immer relativ zur lokalen Zeitzone des Servers. Informationen zum benutzerdefinierten Zeitplanformat finden Sie in der IPS-Dokumentation . </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> description</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Nein </td> 
   <td colname="col4"> <p>Auftragsbeschreibung </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> exportJob</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> Typen:ExportJob</span> </td> 
   <td colname="col3"> Nein </td> 
   <td colname="col4"> <p>Exportieren Sie zuvor hochgeladene Dateien. </p> <p>Siehe <a href="../../../types/c-data-types/r-exportjob.md#reference-1ce423f7b2d54507b90b67233c588665" format="dita" scope="local"> ExportJob</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> imageServingPublishJob</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> Typen:ImageServingPublishJob</span> </td> 
   <td colname="col3"> Nein </td> 
   <td colname="col4"> <p>Details für einen Image Serving-Veröffentlichungsauftrag. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> imageRenderingPublishJob</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> Typen:ImageRenderingPublishJob</span> </td> 
   <td colname="col3"> Nein </td> 
   <td colname="col4"> <p>Details für einen Image Rendering-Veröffentlichungsauftrag. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> videoPublishJob</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> Typen:VideoPublishJob</span> </td> 
   <td colname="col3"> Nein </td> 
   <td colname="col4"> <p>Details für einen Video-Veröffentlichungsauftrag. </p> <p>Siehe <a href="../../../types/c-data-types/r-video-publish-job.md#reference-e99e60d38fe94a07914eefcd7beef2e0" format="dita" scope="local"> VideoPublishJob</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> serverDirectoryPublishJob</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> Typen:ServerDirectoryPublishJob</span> </td> 
   <td colname="col3"> Nein </td> 
   <td colname="col4"> <p>Details für einen Veröffentlichungsauftrag für Serververzeichnisse. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> uploadDirectoryJob</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> Typen:UploadDirectoryJob</span> </td> 
   <td colname="col3"> Nein </td> 
   <td colname="col4"> <p>Details für einen Upload-Ordnerauftrag. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> uploadUrlsJob</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> Typen:UploadUrlsJob</span> </td> 
   <td colname="col3"> Nein </td> 
   <td colname="col4"> <p>Details für einen Upload-URL-Auftrag. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> optimizeImagesJob</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> Typen:OptimizeImagesJob</span> </td> 
   <td colname="col3"> Nein </td> 
   <td colname="col4"> <p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> ripPdfsJob</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> Typen:RipPdfsJob</span> </td> 
   <td colname="col3"> Nein </td> 
   <td colname="col4"> <p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> reprocessAssetsJob</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> Typen:ReprocessAssetsJob</span> </td> 
   <td colname="col3"> Nein </td> 
   <td colname="col4"> <p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> automatedSetGenerationJob</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> Typen:AutomatedSetGenerationJob</span> </td> 
   <td colname="col3"> Nein </td> 
   <td colname="col4"> <p>Verarbeiten Sie eine Asset-Liste mithilfe von automatisierten Set-Skripten in Sets. </p> <p>Siehe <a href="../../../types/c-data-types/r-automated-set-generation-job.md#reference-ab0b3c5408eb41b98c49898b2197cf5a" format="dita" scope="local"> AutomatedSetGenerationJob</a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Ausgabe (submitJobReturn)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| jobHandle | `xsd:string` | Ja | Auftragshandle. |

## Beispiele {#section-40ac77d14adf4588ba2575be6879b2d2}

Dieses Codebeispiel sendet einen Image Serving-Veröffentlichungsauftrag an IPS und gibt einen Auftrags-Handle zurück. Wählen Sie nur einen Auftragstyp in der Anforderung aus. weil `userHandle` ausgelassen wurde, werden E-Mail-Benachrichtigungen an den Benutzer gesendet, der den Auftrag gesendet hat. Dieser Beispielauftrag wird sofort ausgeführt, weil `execTime` und `execSchedule` wurden weggelassen.

**Anforderung**

```java
<submitJobParam xmlns="http://www.scene7.com/IpsApi/xsd">
   <companyHandle>47</companyHandle>
   <jobName>My Test Job</jobName>
   <imageServingPublishJob>
      <publishType>Full</publishType>
      <emailSetting>Error</emailSetting>
   </imageServingPublishJob>
</submitJobParam>
```

**Antwort**

```java
<submitJobReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <jobHandle>47|My Test Job|</jobHandle>
</submitJobReturn>
```

## Anmerkungen {#section-0f3078e503a249aeb6f3d662a51f036a}

Sie können höchstens eines der folgenden `execTime` und `execSchedule`. Wenn keines von beiden übergeben wird, wird der Auftrag sofort ausgeführt. Sie können nur eine der folgenden Optionen verwenden:

* `imageServingPublishJob`
* `imageRenderingPublishJob`
* `videoPublishJob`
* `serverDirectoryPublishJob`
* `uploadDirectoryJob`
* `uploadUrlsJob`
