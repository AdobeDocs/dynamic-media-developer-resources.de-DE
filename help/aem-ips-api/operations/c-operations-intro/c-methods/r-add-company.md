---
description: Fügt dem System eine Firma hinzu.
solution: Experience Manager
title: Firma hinzufügen
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 2f834fe8-a621-4a41-9473-8ef53294b348
source-git-commit: b89ca96947f751b750623e1f18d2a5d86f0cd759
workflow-type: tm+mt
source-wordcount: '170'
ht-degree: 7%

---

# Firma hinzufügen{#addcompany}

Fügt dem System eine Firma hinzu.

Sendet den Namen des Unternehmens, das dem System hinzugefügt werden soll, und sendet optional, ob das Unternehmen abläuft.

Wenn dieser Vorgang aufgerufen wird, erhält das System einen companyInfo-Typ, der ein firmenspezifisches Handle und beschreibende Felder enthält. Wenn der angeforderte Firmenname bereits im System vorhanden ist, wird ein `ipsApiFault` ausgelöst.

## Autorisierte Benutzertypen {#section-ae926c7672984be79f6102748accab72}

* `IpsAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## Parameter {#section-c64a21b72585447880760db9e7a12ccb}

**Eingabe (addCompanyParam)**

<table id="table_AA915BAD2E8E4A1B9719725994309CE8"> 
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
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> companyName</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:string</span> </p> </td> 
   <td colname="col3"> <p>Ja </p> </td> 
   <td colname="col4"> <p>Der Name der hinzuzufügenden Firma. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> läuft </span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:dateTime</span> </p> </td> 
   <td colname="col3"> <p>Nein </p> </td> 
   <td colname="col4"> <p>Das Ablaufdatum des Unternehmens. Geben Sie die Zeitzone mit der Anfrage für dieses Feld an. Die Zeitzonen werden an die zentrale Zeit angepasst. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Ausgabe (addCompanyReturn)**

<table id="table_89EBAC0E0FB34793BD843837BB02B518"> 
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
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> companyInfo</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:string</span> </p> </td> 
   <td colname="col3"> <p>Ja </p> </td> 
   <td colname="col4"> <p>Verarbeiten von und Name, Stammpfad, Ablaufdatum und Uhrzeit des neuen Unternehmens. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Beispiele {#section-4c8f1bb40d154c77a7b410468206e52b}

Dieses Beispiel zeigt eine Anfrage zum Hinzufügen eines Unternehmens zum IPS-System und die Antwort mit detaillierten Informationen zum hinzugefügten Unternehmen, die zur Durchführung anderer Vorgänge benötigt werden.

**Anfrage**

```java {.line-numbers}
<ns1:addCompanyParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyName>Planetary</ns1:companyName>
</ns1:addCompanyParam>
```

**Antwort**

```java {.line-numbers}
<ns1:addCompanyReturn xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyInfo>
      <ns1:companyHandle>137</ns1:companyHandle>
      <ns1:name>Planetary</ns1:name>
      <ns1:rootPath>Planetary/</ns1:rootPath>
      <ns1:expires>2101-01-31T23:00:00.030Z</ns1:expires>
   </ns1:companyInfo>
</ns1:addCompanyReturn>
```
