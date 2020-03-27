---
description: Das Hochladen von Assets in das Scene7 Production System umfasst eine oder mehrere HTTP-POST-Anforderungen, mit denen ein Auftrag zur Koordination aller mit den hochgeladenen Aktivitäten verknüpften Protokolldateien eingerichtet wird.
seo-description: Das Hochladen von Assets in das Scene7 Production System umfasst eine oder mehrere HTTP-POST-Anforderungen, mit denen ein Auftrag zur Koordination aller mit den hochgeladenen Aktivitäten verknüpften Protokolldateien eingerichtet wird.
seo-title: Hochladen von Assets über HTTP POSTs zum UploadFile-Servlet
solution: Experience Manager
title: Hochladen von Assets über HTTP POSTs zum UploadFile-Servlet
topic: Scene7 Image Production System API
uuid: 8d562316-0849-4b95-a974-29732d453dc8
translation-type: tm+mt
source-git-commit: dac273f51703fd63f1d427fbb7713fcc79bfa2c4

---


# Hochladen von Assets über HTTP POSTs zum UploadFile-Servlet{#uploading-assets-by-way-of-http-posts-to-the-uploadfile-servlet}

Das Hochladen von Assets in das Scene7 Production System umfasst eine oder mehrere HTTP-POST-Anforderungen, mit denen ein Auftrag zur Koordination aller mit den hochgeladenen Aktivitäten verknüpften Protokolldateien eingerichtet wird.

Verwenden Sie die folgende URL, um auf das UploadFile-Servlet zuzugreifen:

```
https://<server>/scene7/UploadFile
```

>[!NOTE]
>
>Alle POST-Anforderungen für einen Upload-Auftrag müssen von derselben IP-Adresse stammen.

**Zugriff auf URLs für Scene7-Regionen**

<table id="table_45BB314ABCDA49F38DF7BECF95CC984A"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Geografischer Standort </p> </th> 
   <th colname="col2" class="entry"> <p>Produktions-URL </p> </th> 
   <th colname="col3" class="entry"> <p>Staging-URL (für die Entwicklung und den Test vor der Produktion) </p> </th> 
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

## Arbeitsablauf des Upload-Auftrags {#section-873625b9512f477c992f5cdd77267094}

Der Upload-Auftrag besteht aus einem oder mehreren HTTP-POSTs, die eine häufig verwendete Methode verwenden, um die Verarbeitung mit demselben Auftrag `jobHandle` zu korrelieren. Jede Anforderung ist `multipart/form-data` kodiert und besteht aus den folgenden Formularelementen:

>[!NOTE]
>
>Alle POST-Anforderungen für einen Upload-Auftrag müssen von derselben IP-Adresse stammen.

| HTTP POST form part | Description ||-|-||`auth`| Erforderlich. Ein XML-authHeader-Dokument, das Authentifizierungs- und Clientinformationen angibt. Siehe **Authentifizierung** anfordern unter [SOAP](/help/aem-ips-api/c-wsdl-versions.md). |
|`file params` |  Optional. Sie können bei jeder POST-Anforderung eine oder mehrere Dateien hochladen. Jeder Dateiteil kann einen Dateinamenparameter in der Content-Disposition-Kopfzeile enthalten, der in IPS als Dateiname für die Zielgruppe verwendet wird, wenn kein `uploadPostParams/fileName` Parameter angegeben ist. |

| HTTP POST form part | uploadPostParams element name | Type | Description ||-|-|-|-||`uploadParams` (Erforderlich) Ein XML- `uploadParams` Dokument, das die Upload-Parameter angibt) | `companyHandle`|`xsd:string`| Erforderlich. Behandeln Sie die Firma, in die die Datei hochgeladen wird. |
|`uploadParams` (Erforderlich. Ein XML- `uploadParams` Dokument, das die Upload-Parameter angibt)|`jobName`|`xsd:string`| Entweder `jobName` oder `jobHandle` ist erforderlich. Name des Upload-Auftrags. |
|`uploadParams` (Erforderlich. Ein XML- `uploadParams` Dokument, das die Upload-Parameter angibt)|`jobHandle`|`xsd:string`| Entweder `jobName` oder `jobHandle` ist erforderlich. Bearbeiten Sie einen Upload-Auftrag, der in einer vorherigen Anforderung gestartet wurde. |
|`uploadParams` (Erforderlich. Ein XML- `uploadParams` Dokument, das die Upload-Parameter angibt)|`locale`|`xsd:string`| Optional. Sprach- und Ländercode für die lokale Anpassung. |
|`uploadParams` (Erforderlich. Ein XML- `uploadParams` Dokument, das die Upload-Parameter angibt)|`description`|`xsd:string`| Optional. Beschreibung des Auftrags. |
|`uploadParams` (Erforderlich. Ein XML- `uploadParams` Dokument, das die Upload-Parameter angibt)|`destFolder`|`xsd:string`| Optional. Pfad des Ordners für Zielgruppen zum Präfix einer Eigenschaft &quot;Dateiname&quot;, insbesondere für Browser und andere Clients, die eventuell keine vollständigen Pfade in einem Dateinamen unterstützen. |
|`uploadParams` (Erforderlich. Ein XML- `uploadParams` Dokument, das die Upload-Parameter angibt)|`fileName`|`xsd:string`| Optional. Name der Zielgruppe Überschreibt die Eigenschaft filename. |
|`uploadParams` (Erforderlich. Ein XML- `uploadParams` Dokument, das die Upload-Parameter angibt)|`endJob`|`xsd:boolean`| Optional. Der Standardwert ist „false“. |
|`uploadParams` (Erforderlich. Ein XML- `uploadParams` Dokument, das die Upload-Parameter angibt)|`uploadParams`|`types:UploadPostJob`| Optional, wenn es sich um eine nachfolgende Anforderung für einen vorhandenen aktiven Auftrag handelt. Wenn ein bestehender Auftrag vorhanden ist, `uploadParams` wird er ignoriert und die vorhandenen Parameter zum Hochladen von Aufträgen werden verwendet. Siehe [UploadPostJob](types/c-data-types/r-upload-post-job.md#reference-bca2339b593f4637a687c33937215ef4) |

Innerhalb des `<uploadPostParams>` Blocks befindet sich der `<uploadParams>` Block, der die Verarbeitung der eingeschlossenen Dateien kennzeichnet.

Siehe [UploadPostJob](types/c-data-types/r-upload-post-job.md#reference-bca2339b593f4637a687c33937215ef4).

Sie können davon ausgehen, dass sich der `uploadParams` Parameter für einzelne Dateien im Rahmen desselben Auftrags ändern kann, aber das ist nicht der Fall. Verwenden Sie dieselben `uploadParams` Parameter für den gesamten Auftrag.

Die ursprüngliche POST-Anforderung für einen neuen Upload-Auftrag sollte den `jobName` Parameter angeben, vorzugsweise mithilfe eines eindeutigen Auftragsnamens, um die anschließende Auftragsstatusabfrage und die Auftragsprotokollabierung zu vereinfachen. Zusätzliche POST-Anforderungen für denselben Upload-Auftrag sollten den `jobHandle` Parameter anstelle `jobName`des `jobHandle` Wertes angeben, der von der ursprünglichen Anforderung zurückgegeben wurde.

Die letzte POST-Anforderung für einen Upload-Auftrag sollte den `endJob` Parameter auf true setzen, damit für diesen Auftrag keine weiteren Dateien POST-Tests durchgeführt werden. Dies wiederum ermöglicht es dem Auftrag, sofort nach der Erfassung aller POSTed-Dateien abzuschließen. Andernfalls wird die Auftragsdauer verkürzt, wenn innerhalb von 30 Minuten keine weiteren POST-Anforderungen empfangen werden.

## UploadPOST-Antwort {#section-421df5cc04d44e23a464059aad86d64e}

Bei einer erfolgreichen POST-Anforderung ist der Antworttext ein XML- `uploadPostReturn` Dokument, wie die XSD im Folgenden angibt:

```
<element name="uploadPostReturn"> 
        <complexType> 
            <sequence> 
                <element name="jobHandle" type="xsd:string"/> 
            </sequence> 
        </complexType> 
    </element>
```

Der `jobHandle` zurückgegebene Wert wird für alle nachfolgenden POST-Anforderungen für denselben Auftrag im Parameter `uploadPostParams`/ `jobHandle` weitergegeben. Sie können ihn auch verwenden, um den Auftragsstatus mit dem `getActiveJobs` Vorgang abzufragen oder um die Auftragsprotokolle mit dem `getJobLogDetails` Vorgang Abfrage.

Wenn bei der Verarbeitung der POST-Anforderung ein Fehler auftritt, besteht der Antworttext aus einem der API-Fehlertypen, wie unter [Fehler](faults/c-faults/c-faults.md#concept-28c5e495f39443ecab05384d8cf8ab6b)beschrieben.

## Beispiel für eine POST-Anforderung {#section-810fe32abdb9426ba0fea488dffadd1e}

```
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

```
HTTP/1.1 200 OK 
Content-Type: text/xml;﻿charset=utf-8 
Content-Length: 204 
Date: Mon, 25 Jul 2016 19:43:38 GMT 
Server: Unknown 
  
'1.0' encoding='UTF-8'?><uploadPostReturn xmlns="http://www.scene7.com/IpsApi/xsd/2014-04-03"> 
  <jobHandle>j|2101||uploadFileServlet-1376682217351|54091</jobHandle> 
</uploadPostReturn>
```

## Beispiel für eine POST-Antwort - Fehler {#section-efc32bb371554982858b8690b05090ec}

```
HTTP/1.1 200 OK 
Content-Type: text/xml;charset=utf-8 
Content-Length: 210 
Date: Mon, 25 Jul 2016 19:43:38 GMT 
Server: Unknown 
  
<?xml version='1.0' encoding='UTF-8'?><tns:authenticationFault xmlns:tns="http://www.scene7.com/IpsApi/xsd"><tns:code>10001</tns:code><tns:reason>Invalid username/password</tns:reason></tns:authenticationFault> 
 
```

