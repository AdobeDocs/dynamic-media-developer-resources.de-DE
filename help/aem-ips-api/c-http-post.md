---
title: Hochladen von Assets über HTTP-POSTs in das UploadFile-Servlet
description: Das Hochladen von Assets in Dynamic Media Classic umfasst eine oder mehrere HTTP-POST-Anforderungen, die einen Auftrag einrichten, um alle Protokollaktivitäten zu koordinieren, die mit den hochgeladenen Dateien verknüpft sind.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: e40293be-d00f-44c1-8ae7-521ce3312ca8
source-git-commit: b89ca96947f751b750623e1f18d2a5d86f0cd759
workflow-type: tm+mt
source-wordcount: '725'
ht-degree: 3%

---

# Hochladen von Assets über HTTP-POSTs in das UploadFile-Servlet{#uploading-assets-by-way-of-http-posts-to-the-uploadfile-servlet}

Das Hochladen von Assets in Dynamic Media Classic umfasst eine oder mehrere HTTP-POST-Anforderungen, die einen Auftrag einrichten, um alle Protokollaktivitäten zu koordinieren, die mit den hochgeladenen Dateien verknüpft sind.

Verwenden Sie die folgende URL, um auf das UploadFile-Servlet zuzugreifen:

```
https://<server>/scene7/UploadFile
```

>[!NOTE]
>
>Alle POST-Anforderungen für einen Upload-Auftrag müssen von derselben IP-Adresse stammen.

**Zugriffs-URLs für Dynamic Media-Regionen**

<table id="table_45BB314ABCDA49F38DF7BECF95CC984A"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Geografischer Standort </p> </th> 
   <th colname="col2" class="entry"> <p>Produktions-URL </p> </th> 
   <th colname="col3" class="entry"> <p>Staging-URL (zur Entwicklung und zum Testen vor der Produktion) </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Nordamerika </p> </td> 
   <td colname="col2"> <p> https://s7sps1ssl.scene7.com/scene7/UploadFile </p> </td> 
   <td colname="col3"> <p> https://s7sps1ssl-staging.scene7.com/scene7/UploadFile </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Europa, Naher Osten, Asien </p> </td> 
   <td colname="col2"> <p> https://s7sps3ssl.scene7.com/scene7/UploadFile </p> </td> 
   <td colname="col3"> <p> https://s7sps3ssl-staging.scene7.com/scene7/UploadFile </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Japan/Asien-Pazifik </p> </td> 
   <td colname="col2"> <p> https://s7sps5ssl.scene7.com/scene7/UploadFile </p> </td> 
   <td colname="col3"> <p> https://s7sps5ssl-staging.scene7.com/scene7/UploadFile </p> </td> 
  </tr> 
 </tbody> 
</table>

## Workflow des Upload-Auftrags {#section-873625b9512f477c992f5cdd77267094}

Der Upload-Auftrag besteht aus einem oder mehreren HTTP-POSTs, die einen gemeinsamen `jobHandle` , um die Verarbeitung mit demselben Auftrag zu korrelieren. Jede Anfrage ist `multipart/form-data` kodiert und besteht aus den folgenden Formularteilen:

>[!NOTE]
>
>Alle POST-Anforderungen für einen Upload-Auftrag müssen von derselben IP-Adresse stammen.

|  HTTP-POST als Teil  |  Beschreibung  |
|---|---|
| `auth`  |   Erforderlich. Ein XML authHeader-Dokument, das Authentifizierung und Client-Informationen angibt. Siehe **Authentifizierung anfordern** under [SOAP](/help/aem-ips-api/c-wsdl-versions.md). |
| `file params`  |   Optional. Sie können bei jeder POST-Anfrage eine oder mehrere Dateien zum Hochladen hinzufügen. Jeder Dateiteil kann einen Dateinamenparameter in der Kopfzeile &quot;Content-Disposition&quot;enthalten, der in IPS als Zieldateiname verwendet wird, falls nicht `uploadPostParams/fileName` festgelegt ist. |

|  HTTP-POST als Teil   |  Elementname uploadPostParams   |  Typ   |  Beschreibung   |
|---|---|---|---|
| `uploadParams` (Erforderlich. Eine XML `uploadParams` Dokument, das die Upload-Parameter angibt)   |   `companyHandle`  |  `xsd:string`  | Erforderlich. Handle an das Unternehmen, in das die Datei hochgeladen wird.  |
| `uploadParams` (Erforderlich. Eine XML `uploadParams` Dokument, das die Upload-Parameter angibt) | `jobName`  |  `xsd:string`  | Entweder `jobName` oder `jobHandle` ist erforderlich. Name des Upload-Auftrags.  |
| `uploadParams` (Erforderlich. Eine XML `uploadParams` Dokument, das die Upload-Parameter angibt) | `jobHandle`  |  `xsd:string`  | Entweder `jobName` oder `jobHandle` ist erforderlich. Handle mit einem in einer vorherigen Anfrage gestarteten Upload-Auftrag.  |
| `uploadParams` (Erforderlich. Eine XML `uploadParams` Dokument, das die Upload-Parameter angibt) | `locale`  |  `xsd:string`  | Optional. Sprach- und Ländercode für die Lokalisierung.  |
| `uploadParams` (Erforderlich. Eine XML `uploadParams` Dokument, das die Upload-Parameter angibt) | `description`  |  `xsd:string`  | Optional. Beschreibung des Auftrags.  |
| `uploadParams` (Erforderlich. Eine XML `uploadParams` Dokument, das die Upload-Parameter angibt) | `destFolder`  |  `xsd:string`  | Optional. Geben Sie den Ordnerpfad als Präfix für eine Dateinameneigenschaft an, insbesondere für Browser und andere Clients, die möglicherweise keine vollständigen Pfade in einem Dateinamen unterstützen.  |
| `uploadParams` (Erforderlich. Eine XML `uploadParams` Dokument, das die Upload-Parameter angibt) | `fileName`  |  `xsd:string`  | Optional. Name der Zieldatei. Überschreibt die Eigenschaft &quot;filename&quot;. |
| `uploadParams` (Erforderlich. Eine XML `uploadParams` Dokument, das die Upload-Parameter angibt) | `endJob`  |  `xsd:boolean`  | Optional. Der Standardwert ist „false“. |
| `uploadParams` (Erforderlich. Eine XML `uploadParams` Dokument, das die Upload-Parameter angibt) | `uploadParams`  |  `types:UploadPostJob`  | Optional, wenn es sich um eine nachfolgende Anfrage für einen vorhandenen aktiven Auftrag handelt. Wenn ein vorhandener Auftrag vorhanden ist, `uploadParams` wird ignoriert und die vorhandenen Auftrags-Upload-Parameter werden verwendet. Siehe [UploadPostJob](types/c-data-types/r-upload-post-job.md#reference-bca2339b593f4637a687c33937215ef4) |

Innerhalb der `<uploadPostParams>` -Block ist `<uploadParams>` -Block, der die Verarbeitung der enthaltenen Dateien bezeichnet.

Siehe [UploadPostJob](types/c-data-types/r-upload-post-job.md#reference-bca2339b593f4637a687c33937215ef4).

Während Sie davon ausgehen, dass die Variable `uploadParams` kann sich für einzelne Dateien im Rahmen desselben Auftrags ändern, was nicht der Fall ist. Verwenden Sie dasselbe `uploadParams` Parameter für den gesamten Auftrag.

Die anfängliche POST-Anfrage für einen neuen Upload-Auftrag sollte die `jobName` -Parameter, vorzugsweise mithilfe eines eindeutigen Auftragsnamens, um die nachfolgenden Auftragsstatusabfragen und Auftragsprotokollabfragen zu vereinfachen. Zusätzliche POST-Anforderungen für denselben Upload-Auftrag sollten die `jobHandle` Parameter anstelle von `jobName`, wobei `jobHandle` -Wert, der von der ursprünglichen Anfrage zurückgegeben wurde.

Die endgültige POST für einen Upload-Auftrag sollte die Variable `endJob` auf &quot;true&quot;, sodass keine zukünftigen Dateien für diesen Auftrag POSTed werden. Dadurch kann der Auftrag sofort abgeschlossen werden, nachdem alle POSTed-Dateien erfasst wurden. Andernfalls tritt eine Zeitüberschreitung für den Auftrag auf, wenn innerhalb von 30 Minuten keine weiteren POST empfangen werden.

## UploadPOST-Antwort {#section-421df5cc04d44e23a464059aad86d64e}

Bei einer erfolgreichen POST-Anfrage ist der Antworttext ein XML-Code `uploadPostReturn` -Dokument, wie die XSD im Folgenden angibt:

```xml {.line-numbers}
<element name="uploadPostReturn"> 
        <complexType> 
            <sequence> 
                <element name="jobHandle" type="xsd:string"/> 
            </sequence> 
        </complexType> 
    </element>
```

Die `jobHandle` zurückgegeben wird, wird im `uploadPostParams`/ `jobHandle` für alle nachfolgenden POST-Anforderungen für denselben Auftrag. Sie können es auch verwenden, um den Auftragsstatus mit der `getActiveJobs` oder um die Auftragsprotokolle mit der `getJobLogDetails` Vorgang.

Wenn bei der Verarbeitung der POST-Anfrage ein Fehler auftritt, besteht der Antworttext aus einem der API-Fehlertypen, wie unter [Fehler](faults/c-faults/c-faults.md#concept-28c5e495f39443ecab05384d8cf8ab6b).

## Beispielhafte POST-Anfrage {#section-810fe32abdb9426ba0fea488dffadd1e}

```{.line-numbers}
POST /scene7/UploadFile HTTP/1.1 
User-Agent: Jakarta Commons-HttpClient/3.1 
Host: localhost 
Content-Length: 362630 
Content-Type: multipart/form-data; boundary=O9-ba7tieRtqA4QRSaVk-eDq6658SPrYfvUcJ 
  
--O9-ba7tieRtqA4QRSaVk-eDq6658SPrYfvUcJ 
Content-Disposition: form-data; name="auth" 
Content-Type: text/plain; charset=US-ASCII 
Content-Transfer-Encoding: 8bit 
  
            <authHeader xmlns="http://www.scene7.com/IpsApi/xsd/2014-04-03">  
                   <user>sampleuser@test.com</user>  
                   <password>*</password>  
                   <locale>en-US</locale>  
                   <appName>MyUploadServletTest</appName>  
                   <appVersion>1.0</appVersion>  
                   <faultHttpStatusCode>200</faultHttpStatusCode>  
           </authHeader>                   
        
--O9-ba7tieRtqA4QRSaVk-eDq6658SPrYfvUcJ 
Content-Disposition: form-data; name="uploadParams" 
Content-Type: text/plain; charset=US-ASCII 
Content-Transfer-Encoding: 8bit 
  
            <uploadPostParam xmlns="http://www.scene7.com/IpsApi/xsd/2014-04-03"> 
                <companyHandle>c|2101</companyHandle> 
                <jobName>uploadFileServlet-1376682217351</jobName> 
                <uploadParams> 
                    <overwrite>true</overwrite> 
                    <readyForPublish>true</readyForPublish> 
                    <preservePublishState>true</preservePublishState> 
                    <createMask>true</createMask> 
                    <preserveCrop>true</preserveCrop> 
                    <manualCropOptions> 
                      <left>500</left> 
                      <right>500</right> 
                      <top>500</top> 
                      <bottom>500</bottom> 
                    </manualCropOptions> 
                    <photoshopOptions> 
                      <process>MaintainLayers</process> 
                      <layerOptions> 
                        <layerNaming>AppendNumber</layerNaming> 
                        <anchor>Northwest</anchor> 
                        <createTemplate>true</createTemplate> 
                        <extractText>true</extractText> 
                        <extendLayers>false</extendLayers> 
                      </layerOptions> 
                    </photoshopOptions> 
                    <emailSetting>None</emailSetting> 
                </uploadParams> 
            </uploadPostParam>        
        
--O9-ba7tieRtqA4QRSaVk-eDq6658SPrYfvUcJ-- 
Content-Disposition: form-data; name="file1"; filename="ApiTestCo1/UploadFileServlet1376682217351//1376682217351-1.jpg" 
Content-Type: application/octet-stream; charset=ISO-8859-1 
Content-Transfer-Encoding: binary 
<file bytes ... > 
--O9-ba7tieRtqA4QRSaVk-eDq6658SPrYfvUcJ-- 
Content-Disposition: form-data; name="file2"; filename="ApiTestCo1/UploadFileServlet1376682217351//1376682217351-2.jpg" 
Content-Type: application/octet-stream; charset=ISO-8859-1 
Content-Transfer-Encoding: binary 
<file bytes ... > 
--O9-ba7tieRtqA4QRSaVk-eDq6658SPrYfvUcJ--
```

## Beispiel für eine POST-Antwort - Erfolg {#section-0d515ba14c454ed0b5196ac8d1bb156e}

```{.line-numbers}
HTTP/1.1 200 OK 
Content-Type: text/xml;﻿charset=utf-8 
Content-Length: 204 
Date: Mon, 25 Jul 2016 19:43:38 GMT 
Server: Unknown 
  
'1.0' encoding='UTF-8'?><uploadPostReturn xmlns="http://www.scene7.com/IpsApi/xsd/2014-04-03"> 
  <jobHandle>j|2101||uploadFileServlet-1376682217351|54091</jobHandle> 
</uploadPostReturn>
```

## POST-Antwort - Fehler {#section-efc32bb371554982858b8690b05090ec}

```{.line-numbers}
HTTP/1.1 200 OK 
Content-Type: text/xml;charset=utf-8 
Content-Length: 210 
Date: Mon, 25 Jul 2016 19:43:38 GMT 
Server: Unknown 
  
<?xml version='1.0' encoding='UTF-8'?><tns:authenticationFault xmlns:tns="http://www.scene7.com/IpsApi/xsd"><tns:code>10001</tns:code><tns:reason>Invalid username/password</tns:reason></tns:authenticationFault> 
 
```
