---
description: Unterbreitet einen Vorgang an das System.
solution: Experience Manager
title: submitJob
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: b1dc7a0e-da9a-4086-822b-5274bd62eadf
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '407'
ht-degree: 7%

---

# submitJob{#submitjob}

Unterbreitet einen Vorgang an das System.

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
   <td colname="col4"> <p>Firmengriff. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> userHandle</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Nein </td> 
   <td colname="col4"> <p>Handle an den Benutzer, der den Auftrag gesendet hat. </p> <p> <p>Hinweis: Das System sendet E-Mails an den Benutzer, der von <span class="codeph"> userHandle</span> angegeben wird. Wenn <span class="codeph"> userHandle</span> nicht angegeben wird, erhält die Person, die den Auftrag eingereicht hat, die E-Mails. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> jobName</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Ja </td> 
   <td colname="col4"> <p>Vorgangsname. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> Gebietsschema</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Nein </td> 
   <td colname="col4"> <p>Das Gebietsschema, das für Auftragsprotokolldetails und E-Mail-Lokalisierung verwendet wird. </p> <p>Gebietsschemata werden als <span class="codeph"> &lt;language_code&gt;</span> und <span class="codeph"> [&lt;country_code&gt;]</span> angegeben, wobei der Sprach-Code ein Code mit zwei Kleinbuchstaben gemäß ISO-639 ist und der optionale Länder-Code ein Code mit zwei Großbuchstaben gemäß ISO-3166 ist. Die Gebietsschema-Zeichenfolge für Englisch (Vereinigte Staaten) wäre beispielsweise: en-US. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> execTime</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:dateTime</span> </td> 
   <td colname="col3"> Nein </td> 
   <td colname="col4"> <p>Datum und Uhrzeit der Ausführung des Auftrags. </p> <p>Hinweis: Geben Sie bei der Anfrage die Zeitzone an. Die Zeitzonen werden an die Zeitzone des Ziel-IPS-Servers angepasst. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> execSchedule</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Nein </td> 
   <td colname="col4"> <p>Legt fest, wann der Auftrag ausgeführt wird. </p> <p> Kann eine <span class="codeph"> Cron</span>-Zeichenfolge sein, die den Auftrag wiederholt ausführt. </p> <p>Der Zeitplan ist immer relativ zur lokalen Zeitzone des Servers. Informationen zum benutzerdefinierten Zeitplanformat finden Sie in der IPS-Dokumentation . </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> Beschreibung</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Nein </td> 
   <td colname="col4"> <p>Auftragsbeschreibung. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> exportJob</span> </span> </td> 
   <td colname="col2"> <span class="codeph">:ExportJob</span> </td> 
   <td colname="col3"> Nein </td> 
   <td colname="col4"> <p>Exportieren Sie zuvor hochgeladene Dateien. </p> <p>Siehe <a href="../../../types/c-data-types/r-exportjob.md#reference-1ce423f7b2d54507b90b67233c588665" format="dita" scope="local">Exportvorgang</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> imageServingPublishJob</span> </span> </td> 
   <td colname="col2"> <span class="codeph">:ImageServingPublishJob</span> </td> 
   <td colname="col3"> Nein </td> 
   <td colname="col4"> <p>Details für einen Image-Serving-Veröffentlichungsauftrag. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> imageRenderingPublishJob</span> </span> </td> 
   <td colname="col2"> <span class="codeph">:ImageRenderingPublishJob</span> </td> 
   <td colname="col3"> Nein </td> 
   <td colname="col4"> <p>Details für einen Veröffentlichungsauftrag zum Rendern von Bildern. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> videoPublishJob</span> </span> </td> 
   <td colname="col2"> <span class="codeph">:VideoPublishJob</span> </td> 
   <td colname="col3"> Nein </td> 
   <td colname="col4"> <p>Details für einen Videoveröffentlichungsauftrag. </p> <p>Siehe <a href="../../../types/c-data-types/r-video-publish-job.md#reference-e99e60d38fe94a07914eefcd7beef2e0" format="dita" scope="local"> VideoPublishJob</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> serverDirectoryPublishJob</span> </span> </td> 
   <td colname="col2"> <span class="codeph">:ServerDirectoryPublishJob</span> </td> 
   <td colname="col3"> Nein </td> 
   <td colname="col4"> <p>Details für einen Veröffentlichungsauftrag für ein Serververzeichnis. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> uploadDirectoryJob</span> </span> </td> 
   <td colname="col2"> <span class="codeph">:UploadDirectoryJob</span> </td> 
   <td colname="col3"> Nein </td> 
   <td colname="col4"> <p>Details für einen Upload-Verzeichnisauftrag. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> uploadUrlsJob</span> </span> </td> 
   <td colname="col2"> <span class="codeph">:UploadUrlsJob</span> </td> 
   <td colname="col3"> Nein </td> 
   <td colname="col4"> <p>Details für einen URL-Upload-Auftrag. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> optimizeImagesJob</span> </span> </td> 
   <td colname="col2"> <span class="codeph">:OptimizeImagesJob</span> </td> 
   <td colname="col3"> Nein </td> 
   <td colname="col4"> <p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> ripPdfsJob</span> </span> </td> 
   <td colname="col2"> <span class="codeph">:RipPdfsJob</span> </td> 
   <td colname="col3"> Nein </td> 
   <td colname="col4"> <p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> reprocessAssetsJob</span> </span> </td> 
   <td colname="col2"> <span class="codeph">:ReprocessAssetsJob</span> </td> 
   <td colname="col3"> Nein </td> 
   <td colname="col4"> <p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> automatedSetGenerationJob</span> </span> </td> 
   <td colname="col2"> <span class="codeph">:AutomatedSetGenerationJob</span> </td> 
   <td colname="col3"> Nein </td> 
   <td colname="col4"> <p>Verarbeiten Sie eine Asset-Liste mithilfe automatisierter Set-Skripte in Sets. </p> <p>Siehe <a href="../../../types/c-data-types/r-automated-set-generation-job.md#reference-ab0b3c5408eb41b98c49898b2197cf5a" format="dita" scope="local"> AutomatedSetGenerationJob</a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Ausgabe (submitJobReturn)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| jobHandle | `xsd:string` | Ja | Auftragsverarbeitung. |

## Beispiele {#section-40ac77d14adf4588ba2575be6879b2d2}

Dieses Codebeispiel übermittelt einen Image Serving-Veröffentlichungsauftrag an IPS und gibt ein Auftrags-Handle zurück. Wählen Sie in der Anfrage nur einen Vorgangstyp aus. Da `userHandle` weggelassen wurde, werden E-Mail-Benachrichtigungen an den Benutzer gesendet, der den Auftrag gesendet hat. Dieser Beispielvorgang wird sofort ausgeführt, da `execTime` und `execSchedule` weggelassen wurden.

**Anfrage**

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

Sie können höchstens eine der Optionen `execTime` und `execSchedule` angeben. Wenn keiner der Werte übergeben wird, wird der Auftrag sofort ausgeführt. Sie können nur eine der folgenden Optionen verwenden:

* `imageServingPublishJob`
* `imageRenderingPublishJob`
* `videoPublishJob`
* `serverDirectoryPublishJob`
* `uploadDirectoryJob`
* `uploadUrlsJob`
