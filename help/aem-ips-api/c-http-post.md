---
title: Hochladen von Assets über HTTP-POSTs zum UploadFile-Servlet
description: Das Hochladen von Assets in  [!DNL Dynamic Media] Classic umfasst eine oder mehrere HTTP-Dateianfragen, die einen Vorgang einrichten, um die gesamte mit den hochgeladenen POST verknüpfte Protokollaktivität zu koordinieren.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: e40293be-d00f-44c1-8ae7-521ce3312ca8
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '688'
ht-degree: 0%

---

# Hochladen von Assets über HTTP-POSTs zum UploadFile-Servlet{#uploading-assets-by-way-of-http-posts-to-the-uploadfile-servlet}

Das Hochladen von Assets in Dynamic Media Classic umfasst eine oder mehrere HTTP-Dateianfragen, die einen Vorgang einrichten, um die gesamte mit den hochgeladenen POST verknüpfte Protokollaktivität zu koordinieren.

Verwenden Sie die folgende URL, um auf das UploadFile-Servlet zuzugreifen:

```
https://<server>/scene7/UploadFile
```

>[!NOTE]
>
>Alle POST-Anfragen für einen Upload-Auftrag müssen von derselben IP-Adresse stammen.

**Zugriff auf URLs für Dynamic Media-Regionen**

<table id="table_45BB314ABCDA49F38DF7BECF95CC984A"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Geografische Lage </p> </th> 
   <th colname="col2" class="entry"> <p>Produktions-URL </p> </th> 
   <th colname="col3" class="entry"> <p>Staging-URL (für Entwicklung und Tests vor der Produktion) </p> </th> 
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
   <td colname="col1"> <p>Japan/Asien/Pazifik </p> </td> 
   <td colname="col2"> <p> https://s7sps5ssl.scene7.com/scene7/UploadFile </p> </td> 
   <td colname="col3"> <p> https://s7sps5ssl-staging.scene7.com/scene7/UploadFile </p> </td> 
  </tr> 
 </tbody> 
</table>

## Workflow des Upload-Auftrags {#section-873625b9512f477c992f5cdd77267094}

Der Upload-Auftrag besteht aus einem oder mehreren HTTP-POSTs, die eine gemeinsame `jobHandle` verwenden, um die Verarbeitung mit demselben Auftrag zu korrelieren. Jede Anfrage ist `multipart/form-data` codiert und besteht aus den folgenden Formularteilen:

>[!NOTE]
>
>Alle POST-Anfragen für einen Upload-Auftrag müssen von derselben IP-Adresse stammen.

|  HTTP-POST-Formularteil  |  Beschreibung  |
|---|---|
| `auth`  |   Erforderlich. Ein XML-AuthHeader-Dokument, das Authentifizierung und Client-Informationen angibt. Siehe **Authentifizierung anfordern** unter [SOAP](/help/aem-ips-api/c-wsdl-versions.md). |
| `file params`  |   Optional. Sie können bei jeder POST-Anfrage eine oder mehrere Dateien zum Hochladen hinzufügen. Jeder Dateiteil kann einen Dateinamenparameter in den Content-Disposition-Header aufnehmen, der als Zieldateiname in IPS verwendet wird, wenn kein `uploadPostParams/fileName` angegeben ist. |

|  HTTP-POST-Formularteil   |  uploadPostParams-Elementname   |  Typ   |  Beschreibung   |
|---|---|---|---|
| `uploadParams` (erforderlich) Ein XML-`uploadParams` (mit Angabe der Upload-Parameter)   |   `companyHandle`  |  `xsd:string`  | Erforderlich. Verarbeiten Sie das Unternehmen, in das die Datei hochgeladen wird.  |
| `uploadParams` (erforderlich) Ein XML-`uploadParams` (mit Angabe der Upload-Parameter) | `jobName`  |  `xsd:string`  | Entweder `jobName` oder `jobHandle` ist erforderlich. Name des Upload-Auftrags.  |
| `uploadParams` (erforderlich) Ein XML-`uploadParams` (mit Angabe der Upload-Parameter) | `jobHandle`  |  `xsd:string`  | Entweder `jobName` oder `jobHandle` ist erforderlich. Handhabung eines Upload-Auftrags, der mit einer vorherigen Anfrage gestartet wurde.  |
| `uploadParams` (erforderlich) Ein XML-`uploadParams` (mit Angabe der Upload-Parameter) | `locale`  |  `xsd:string`  | Optional. Sprache und Ländercode für die Lokalisierung.  |
| `uploadParams` (erforderlich) Ein XML-`uploadParams` (mit Angabe der Upload-Parameter) | `description`  |  `xsd:string`  | Optional. Beschreibung des Vorgangs.  |
| `uploadParams` (erforderlich) Ein XML-`uploadParams` (mit Angabe der Upload-Parameter) | `destFolder`  |  `xsd:string`  | Optional. Zielordnerpfad, der einer Dateinameneigenschaft das Präfix voranstellt, insbesondere für Browser und andere Clients, die möglicherweise nicht vollständige Pfade in einem Dateinamen unterstützen.  |
| `uploadParams` (erforderlich) Ein XML-`uploadParams` (mit Angabe der Upload-Parameter) | `fileName`  |  `xsd:string`  | Optional. Name der Zieldatei. Überschreibt die Eigenschaft filename . |
| `uploadParams` (erforderlich) Ein XML-`uploadParams` (mit Angabe der Upload-Parameter) | `endJob`  |  `xsd:boolean`  | Optional. Der Standardwert ist „false“. |
| `uploadParams` (erforderlich) Ein XML-`uploadParams` (mit Angabe der Upload-Parameter) | `uploadParams`  |  `types:UploadPostJob`  | Optional, wenn dies eine nachfolgende Anfrage für einen vorhandenen aktiven Auftrag ist. Wenn ein Auftrag vorhanden ist, wird `uploadParams` ignoriert und die vorhandenen Auftrags-Upload-Parameter werden verwendet. Siehe [UploadPostJob](types/c-data-types/r-upload-post-job.md#reference-bca2339b593f4637a687c33937215ef4) |

Innerhalb des `<uploadPostParams>` ist der `<uploadParams>`, der die Verarbeitung der eingeschlossenen Dateien angibt.

Siehe [UploadPostJob](types/c-data-types/r-upload-post-job.md#reference-bca2339b593f4637a687c33937215ef4).

Auch wenn Sie davon ausgehen können, dass sich der `uploadParams`-Parameter für einzelne Dateien als Teil desselben Auftrags ändern kann, ist dies nicht der Fall. Verwenden Sie dieselben `uploadParams` für den gesamten Auftrag.

In der anfänglichen POST-Anfrage für einen neuen Upload-Auftrag sollte der `jobName` angegeben werden. Vorzugsweise sollte ein eindeutiger Auftragsname verwendet werden, um nachfolgende Auftragsstatusabfragen und Vorgangslog-Abfragen zu vereinfachen. In zusätzlichen POST-Anfragen für denselben Upload-Auftrag sollte der `jobHandle`-Parameter anstelle von `jobName` angegeben werden, wobei der von der ursprünglichen Anfrage zurückgegebene `jobHandle`-Wert zu verwenden ist.

In der endgültigen Dateianforderung für einen Upload-Auftrag sollte der `endJob` auf „true“ gesetzt werden, damit keine weiteren POST für diesen Auftrag gepostet werden. Dadurch kann der Vorgang unmittelbar nach der Aufnahme aller POST-Dateien abgeschlossen werden. Andernfalls tritt ein Timeout des Auftrags auf, wenn innerhalb von 30 Minuten keine weiteren POST-Anfragen empfangen werden.

## UploadPOST-Antwort {#section-421df5cc04d44e23a464059aad86d64e}

Bei einer erfolgreichen POST-Anfrage ist der Antworttext ein XML-`uploadPostReturn`-Dokument, wie im XSD-Code im Folgenden angegeben:

```xml {.line-numbers}
<element name="uploadPostReturn"> 
        <complexType> 
            <sequence> 
                <element name="jobHandle" type="xsd:string"/> 
            </sequence> 
        </complexType> 
    </element>
```

Die zurückgegebene `jobHandle` wird für alle nachfolgenden POST-Anfragen für denselben Auftrag im `uploadPostParams`-/`jobHandle`-Parameter übergeben. Sie können damit auch den Auftragsstatus mit dem `getActiveJobs` abfragen oder die Auftragsprotokolle mit dem `getJobLogDetails` abfragen.

Wenn bei der Verarbeitung der POST-Anfrage ein Fehler auftritt, besteht der Antworttext aus einem der API-Fehlertypen, wie unter [ beschrieben](faults/c-faults/c-faults.md#concept-28c5e495f39443ecab05384d8cf8ab6b).

## Beispiel für eine POST-Anfrage {#section-810fe32abdb9426ba0fea488dffadd1e}

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

## Beispiel für eine erfolgreiche POST {#section-0d515ba14c454ed0b5196ac8d1bb156e}

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

## Beispiel für eine Fehlerantwort in POST {#section-efc32bb371554982858b8690b05090ec}

```{.line-numbers}
HTTP/1.1 200 OK 
Content-Type: text/xml;charset=utf-8 
Content-Length: 210 
Date: Mon, 25 Jul 2016 19:43:38 GMT 
Server: Unknown 
  
<?xml version='1.0' encoding='UTF-8'?><tns:authenticationFault xmlns:tns="http://www.scene7.com/IpsApi/xsd"><tns:code>10001</tns:code><tns:reason>Invalid username/password</tns:reason></tns:authenticationFault> 
 
```
