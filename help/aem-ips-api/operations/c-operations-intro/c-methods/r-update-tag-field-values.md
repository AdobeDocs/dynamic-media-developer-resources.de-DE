---
description: Aktualisiert Tag-Wörterbuchwerte für ein Tag-Feld.
solution: Experience Manager
title: updateTagFieldValues
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 6de49217-2d15-49d9-9357-b058b2564686
TQID: 'https://experienceleague.adobe.com/ELmOHY1OW3c3AteQOjludnMS4jRLcJX9KezAhFkQj-Q'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 154
ht-degree: 12%

---

# updateTagFieldValues{#updatetagfieldvalues}

Aktualisiert Tag-Wörterbuchwerte für ein Tag-Feld.

Syntax

## Autorisierte Benutzertypen {#section-0372b742b1344979b0668faacb36fcc6}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## Parameter {#section-0a3a4bab026746238c9d4009caf42e94}

**Eingabe (updateTagFieldValuesParam)**

<table id="table_15F354FBC043464080BC975AE35E03A4"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Name </th> 
   <th colname="col2" class="entry"> Typ </th> 
   <th colname="col3" class="entry"> Erforderlich </th> 
   <th colname="col4" class="entry"> Beschreibung </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> companyHandle</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Ja </td> 
   <td colname="col4"> Firmengriff. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> fieldHandle</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Ja </td> 
   <td colname="col4"> Handle des Tag-Felds. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> updateArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph">:TagValueUpdateArray</span> </td> 
   <td colname="col3"> Ja </td> 
   <td colname="col4">Array von Tag-Feldwerten, die Sie aktualisieren möchten. <p>Hinweis: Aktualisiert nur Tag-Zeichenfolgenwerte. Wirkt sich nicht auf Asset-Zuordnungen aus. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Ausgabe (updateTagFieldValuesReturn)**

| Name | Typ | Erforderlich | Beschreibung |
|---|---|---|---|
| successCount | `xsd:int` | Ja | Die Anzahl der erfolgreich aktualisierten Tag-Felder. |
| warningCount | `xsd:int` | Ja | Die Anzahl der Warnhinweise, die generiert wurden, wenn der Vorgang versucht hat, Tag-Felder zu aktualisieren. |
| errorCount | `xsd:int` | Ja | Die Anzahl der Fehler, die generiert wurden, als der Vorgang versucht hat, Tag-Felder zu aktualisieren. |
| warningDetailArray | `types:TagValueUpdateFaultArray` | Nein | Das Array von Details, die mit den Assets verknüpft sind und Warnungen generiert haben, wenn der Vorgang versucht hat, Tag-Felder zu aktualisieren. |
| errorDetailArray | `types:TagValueUpdateFaultArray` | Nein | Das Array von Details, die mit den Assets verknüpft sind und Fehler erzeugt haben, wenn der Vorgang versucht hat, Tag-Felder zu aktualisieren. |

## Beispiele {#section-bb4dcf97044c4675974c9b8d27674001}

**Anfrage**

```java
<updateTagFieldValuesParam xmlns="http://www.scene7.com/IpsApi/xsd/2010-01-31">
   <companyHandle>c|3</companyHandle>
   <fieldHandle>m|3|ASSET|SingleFixedTag</fieldHandle>
   <updateArray>
      <items>
         <oldValue>Nurth</oldValue>
         <newValue>North</newValue>
      </items>
      <items>
         <oldValue>Suth</oldValue>
         <newValue>South</newValue>
      </items>
      <items>
         <oldValue>East</oldValue>
         <newValue>West</newValue>
      </items>
      <items>
         <oldValue>Banana</oldValue>
         <newValue>Pear</newValue>
      </items>
   </updateArray>
</updateTagFieldValuesParam>
```

**Antwort**

```java {.line-numbers}
<updateTagFieldValuesReturn xmlns="http://www.scene7.com/IpsApi/xsd/2010-01-31">
   <successCount>2</successCount>
   <warningCount>0</warningCount>
   <errorCount>2</errorCount>
   <errorDetailArray>
      <items>
         <value>East</value>
         <code>30001</code>
         <reason>New tag value 'West' already exists.</reason>
      </items>
      <items>
         <value>Banana</value>
         <code>30001</code>
         <reason>Tag value 'Banana' not found.</reason>
      </items>
   </errorDetailArray>
</updateTagFieldValuesReturn>
```
