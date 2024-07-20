---
description: Der IPS-Webdienst wird von einer Reihe von WSDL-Dokumenten (Web Services Description Language) unterstützt, auf die von jeder IPS-Installation zugegriffen wird, auf der die IPS-Webdienstkomponente installiert ist. Jede IPS-API-Version enthält eine neue WSDL-Datei, die auf einen versionierten Ziel-XML-Namespace verweist. Frühere WSDL-Namespace-Versionen werden ebenfalls unterstützt, um Abwärtskompatibilität mit bestehenden Anwendungen zu ermöglichen.
solution: Experience Manager
title: IPS Web Service WSDL-Versionen
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: d7a6079e-286e-4e62-b2ff-551ef4a5815c
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '901'
ht-degree: 1%

---

# IPS Web Service WSDL-Versionen{#ips-web-service-wsdl-versions}

Der IPS-Webdienst wird von einer Reihe von WSDL-Dokumenten (Web Services Description Language) unterstützt, auf die von jeder IPS-Installation zugegriffen wird, auf der die IPS-Webdienstkomponente installiert ist. Jede IPS-API-Version enthält eine neue WSDL-Datei, die auf einen versionierten Ziel-XML-Namespace verweist. Frühere WSDL-Namespace-Versionen werden ebenfalls unterstützt, um Abwärtskompatibilität mit bestehenden Anwendungen zu ermöglichen.

## WSDL-Zugriff {#section-62e69fa2c87f4dc9bca72f10ba028f6c}

Greifen Sie auf die Scene7-WSDLs zu, wie unten dargestellt.

```
https://<IPS_hostname:<IPS_port>/<IPS_webapp>/ 
webservice/IpsApi[-<API_version>].wsdl 
```

Der Standardwert für `<IPS_webapp>` ist `scene7`.

**Dienstspeicherort**

Die Dienst-URL wird im Dienstabschnitt des IPS Web Service-WSDL-Dokuments angegeben. Die Dienst-URL ist im Allgemeinen wie folgt:

```
https://<IPS_hostname>:<IPS_port>/<IPS_webapp>/ 
services/IpsApiService 
```

**Zugreifen auf URLs für Dynamic Media-Regionen**

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
   <td colname="col2"> <p> https://s7sps1apissl.scene7.com/scene7/ </p> </td> 
   <td colname="col3"> <p> https://s7sps1apissl-staging.scene7.com/scene7/ </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Europa, Naher Osten, Asien </p> </td> 
   <td colname="col2"> <p> https://s7sps3apissl.scene7.com/scene7/ </p> </td> 
   <td colname="col3"> <p> https://s7sps3apissl-staging.scene7.com/scene7/ </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Japan/Asien-Pazifik </p> </td> 
   <td colname="col2"> <p> https://s7sps5apissl.scene7.com/scene7/ </p> </td> 
   <td colname="col3"> <p> https://s7sps5apissl-staging.scene7.com/scene7/ </p> </td> 
  </tr> 
 </tbody> 
</table>

## Unterstützte WSDLs {#section-ebbba69880f94e9c823f1147974eb404}

Denken Sie daran, dass Sie möglicherweise Ihren Code ändern müssen, wenn Sie Funktionen in der neuesten Version der IPS-API verwenden möchten. Die IPS-API unterstützt WSDLs für die folgenden Versionen:

<table id="table_6FABCC4E7786448CB56C343E3C0B36CA"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>API-Versionsversion </p> </th> 
   <th colname="col2" class="entry"> <p>WSDL </p> </th> 
   <th colname="col3" class="entry"> <p>API-Namespace </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>6.8/2014R1 </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> ipsApi-2014-04-03.wsdl </span> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> http://www.scene7.com/IpsApi/xsd/2014-04-03 </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>6.6/2013R1 </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> ipsApi-2013-02-15.wsdl </span> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> http://www.scene7.com/IpsApi/xsd/2013-02-15 </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>6.0/2012R1 </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> ipsApi-2012-02-14.wsdl </span> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> http://www.scene7.com/IpsApi/xsd/2012-02-14 </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>4,5 </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> ipsApi-2010-01-31.wsdl </span> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> http://www.scene7.com/IpsApi/xsd/2010-01-31 </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>4,4 </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> ipsApi-2009-07-31.wsdl </span> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> http://www.scene7.com/IpsApi/xsd/2009-07-31 </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>4,2 </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> ipsApi-2008-09-10.wsdl </span> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> http://www.scene7.com/IpsApi/xsd/2008-09-10 </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>4,0 </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> ipsApi-2008-01-15.wsdl </span> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> http://www.scene7.com/IpsApi/xsd/2008-01-15 </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Vor 4.0 </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> ipsApi.wsdl </span> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> http://www.scene7.com/IpsApi/xsd </span> </p> </td> 
  </tr> 
 </tbody> 
</table>

Bestehende Anwendungen, die geändert werden müssen, um neue Funktionen zu verwenden, müssen auf die neueste API-Version aktualisieren und müssen möglicherweise Änderungen an vorhandenem Code vornehmen. Weitere Informationen finden Sie im Änderungsprotokoll .

## SOAP {#section-51e7ecbd1d7f451b9e4f6bf7e1579cae}

**Bindungen**

Der IPS-API-Webdienst unterstützt nur eine SOAP Bindung.

**Unterstützte Transporte**

Die IPS-API-SOAP-Bindung unterstützt nur den HTTP-Transport. Stellen Sie alle SOAP Anfragen mithilfe der HTTPS-POST-Methode.

**SOAP Aktionsheader**

Um eine Anfrage zu verarbeiten, setzen Sie den SOAPAction-HTTP-Header auf den Namen des angeforderten Vorgangs. Das Vorgangsnamenattribut im WSDL-Bindungsabschnitt gibt den Namen an.

**Nachrichtenformat**

Der Dokument-/Literalstil wird für alle Eingabe- und Ausgabemeldungen mit Typen verwendet, die auf der XML-Schemadefinitionssprache ( [https://www.w3.org/TR/xmlschema-0/](https://www.w3.org/TR/xmlschema-0/)) basieren und in der WSDL-Datei angegeben sind. Für alle Typen sind qualifizierte Namen erforderlich, die den in der WSDL-Datei angegebenen Zielnamespace-Wert verwenden.

**Authentifizierung anfordern**

Die bevorzugte Methode zur Übergabe von Authentifizierungsberechtigungen in API-Anfragen besteht darin, das Element `authHeader` zu verwenden, wie in der IPS-API-WSDL definiert.

```
<element name="authHeader"> 
    <complexType> 
       <sequence> 
            <element name="user" type="xsd:string"/> 
            <element name="password" type="xsd:string"/> 
            <element name="locale" type="xsd:string" minOccurs="0"/> 
            <element name="appName" type="xsd:string" minOccurs="0"/> 
            <element name="appVersion" type="xsd:string" minOccurs="0"/> 
            <element name="gzipResponse" type="xsd:boolean" minOccurs="0"/> 
            <element name="faultHttpStatusCode" type="xsd:int" minOccurs="0"/> 
       </sequence> 
    </complexType> 
 </element>
```

**Felder**

<table id="table_B295FEB0EA584C2BA4122FC084AEF18D"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Name </p> </th> 
   <th colname="col2" class="entry"> <p>Beschreibung </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> user </span> </p> </td> 
   <td colname="col2"> <p> Gültige IPS-Benutzer-E-Mail. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> password </span> </p> </td> 
   <td colname="col2"> <p>Kennwort für das Benutzerkonto. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> locale </span> </p> </td> 
   <td colname="col2"> <p> Optionales Gebietsschema für die Anforderung. Weitere Informationen finden Sie unter <b>Gebietsschema</b> . </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> appName </span> </p> </td> 
   <td colname="col2"> <p> Anwendungsname aufrufen. Dieser Parameter ist optional. Es wird jedoch empfohlen, ihn in alle Anforderungen aufzunehmen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> appVersion </span> </p> </td> 
   <td colname="col2"> <p> Aufrufen der Anwendungsversion. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> gzipResponse </span> </p> </td> 
   <td colname="col2"> <p> Optionales Flag zum Aktivieren oder Deaktivieren der gzip-Komprimierung der Antwort-XML. Standardmäßig werden Antworten gzip-komprimiert, wenn der HTTP Accept-Encoding-Header die Unterstützung für gzip anzeigt. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> failureHttpStatusCode </span> </p> </td> 
   <td colname="col2"> <p> Optionaler Parameter zum Überschreiben des HTTP-Status-Codes für Fehlerantworten. Standardmäßig geben Fehlerantworten den HTTP-Status-Code 500 (Interner Server-Fehler) zurück. Einige Clientplattformen, einschließlich Adobe-Flash, können den Antworttext nur lesen, wenn ein Statuscode von 200 (OK) zurückgegeben wird. </p> </td> 
  </tr> 
 </tbody> 
</table>

Das Element `authHeader` wird unabhängig von der API-Version immer im Namespace `http://www.scene7.com/IpsApi/xsd` definiert.

Im Folgenden finden Sie ein Beispiel für die Verwendung des Elements `authHeader` in einer Anfrage-SOAP-Kopfzeile:

```
<soap:Header xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"> 
   <authHeader xmlns="http://www.scene7.com/IpsApi/xsd"> 
      <user>user@scene7.com</user> 
      <password>mypassword</password> 
      <appName>MyApp</appName> 
      <appVersion>1.0</appVersion> 
   </authHeader> 
 </soap:Header>
```

**Andere Anfrageauthentifizierungsmethoden**

Wenn es aus irgendeinem Grund nicht möglich ist, dass Ihre Client-Anwendung den SOAP-Header `authHeader` übergibt, können API-Anfragen auch Anmeldeinformationen mithilfe der HTTP Basic-Authentifizierung angeben (wie in RFC 2617 angegeben).

Für die HTTP Basic-Authentifizierung muss der HTTP-Header-Abschnitt jeder SOAP POST-Anfrage einen Header des Formulars enthalten:

`Authorization: Basic base64(<IPS_user_email>:<password>)`

Wobei `base64()` die standardmäßige Base64-Kodierung anwendet, ist `<IPS_user_email>` die E-Mail-Adresse eines gültigen IPS-Benutzers und `<password>` das Kennwort des Benutzers.

Senden Sie die Autorisierungs-Kopfzeile mit der ersten Anfrage vorab. Wenn keine Authentifizierungsberechtigungen in der Anfrage enthalten sind, antwortet `IpsApiService` nicht mit dem Statuscode `401 (Unauthorized)`. Stattdessen wird ein Statuscode von `500 (Internal Server Error)` mit einem SOAP Fehlertext zurückgegeben, der angibt, dass die Anfrage nicht authentifiziert werden konnte.

Vor IPS 3.8 wurde die Authentifizierung über SOAP Kopfzeile mit den Elementen `AuthUser` und `AuthPassword` im Namespace `http://www.scene7.com/IpsApi` implementiert. Beispiel:

```
<soap:Header xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"> 
   <AuthUser xmlns="http://www.scene7.com/IpsApi">user@scene7.com</AuthUser> 
   <AuthPassword xmlns="http://www.scene7.com/IpsApi">mypassword</AuthPassword> 
</soap:Header>
```

Dieser Stil wird weiterhin aus Gründen der Abwärtskompatibilität unterstützt, wird jedoch nicht mehr zugunsten des Elements `authHeader` unterstützt.

**Autorisierung anfordern**

Nachdem die Anmeldeinformationen des Anrufers authentifiziert wurden, wird die Anfrage überprüft, um sicherzustellen, dass der Anrufer zur Durchführung des angeforderten Vorgangs berechtigt ist. Die Autorisierung basiert auf der Benutzerrolle des Aufrufers und erfordert möglicherweise auch die Überprüfung des Zielunternehmens, des Zielbenutzers und anderer Vorgangsparameter. Darüber hinaus müssen Image Portal-Benutzer zu einer Gruppe gehören, die über die erforderlichen Berechtigungen zum Ausführen bestimmter Ordner- und Asset-Vorgänge verfügt. Im Abschnitt &quot;Vorgangsreferenz&quot;werden die Autorisierungsanforderungen für jeden Vorgang beschrieben.

**SOAP-Beispielanfrage und -Antwort**

Das folgende Beispiel zeigt einen vollständigen `addCompany` -Vorgang, einschließlich HTTP-Headern:

```
POST /scene7/services/IpsApiService HTTP/1.1 
User-Agent: Axis/2.0 
SOAPAction: addCompany 
Content-Type: text/xml; charset=UTF-8 
 
<?xml version='1.0' encoding='UTF-8'?> 
<soapenv:Envelope xmlns:soapenv="http://schemas.xmlsoap.org/soap/envelope/"> 
    <soapenv:Header> 
      <authHeader xmlns="http://www.scene7.com/IpsApi/xsd"> 
        <user>user@scene7.com</user> 
        <password>mypassword</password> 
        <appName>MyApp</appName> 
        <appVersion>1.0</appVersion> 
      </authHeader> 
    </soapenv:Header> 
    <soapenv:Body> 
    <ns1:addCompanyParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd/2008-01-15"> 
      <ns1:companyName>Sample Company</ns1:companyName> 
      <ns1:expires>2008-07-31T12:00:00-06:00</ns1:expires> 
    </ns1:addCompanyParam> 
    </soapenv:Body> 
 </soapenv:Envelope>
```

Und die entsprechende Antwort:

```
HTTP/1.1 200 OK 
Server: Apache-Coyote/1.1 
Content-Type: text/xml;charset=UTF-8 
Transfer-Encoding: chunked 
Date: Fri, 21 Jul 2006 20:47:55 GMT 
 
<?xml version='1.0' encoding='utf-8'?><soapenv:Envelope 
xmlns:soapenv="http://schemas.xmlsoap.org/soap/envelope/"> 
   <soapenv:Header /> 
   <soapenv:Body> 
     <ns1:addCompanyReturn xmlns:ns1="http://www.scene7.com/IpsApi/xsd/2008-01-15"> 
       <ns1:companyInfo> 
          <ns1:companyHandle>2</ns1:companyHandle> 
          <ns1:name>Sample Company</ns1:name> 
          <ns1:rootPath>SampleCompany/</ns1:rootPath> 
          <ns1:expires>2008-07-31T18:00:00.000Z</ns1:expires> 
       </ns1:companyInfo> 
     </ns1:addCompanyReturn> 
   </soapenv:Body> 
</soapenv:Envelope>
```

**SOAP faults**

Wenn bei einem Vorgang eine Ausnahmebedingung auftritt, wird anstelle der normalen Antwort ein SOAP Fehler als Textkörper der SOAP zurückgegeben. Wenn beispielsweise ein Benutzer ohne Administratorrechte versucht, die vorherige `addCompany` -Anfrage zu senden, wird die folgende Antwort zurückgegeben:

```
HTTP/1.1 500 Internal Server Error 
Server: Apache-Coyote/1.1 
Content-Type: text/xml;charset=UTF-8 
Transfer-Encoding: chunked 
Date: Fri, 21 Jul 2006 16:36:20 GMT 
Connection: close 
 
<?xml version='1.0' encoding='utf-8'?> 
<soapenv:Envelope xmlns:soapenv="http://schemas.xmlsoap.org/soap/envelope/"> 
   <soapenv:Header /> 
   <soapenv:Body> 
      <soapenv:Fault> 
         <faultcode>soapenv:Client</faultcode> 
         <faultstring>AuthorizationException</faultstring> 
         <detail> 
           <ns1:authorizationFault xmlns:ns1="http://www.scene7.com/IpsApi/xsd"> 
               <code xmlns="http://www.scene7.com/IpsApi/xsd">20003</code> 
             <reason xmlns="http://www.scene7.com/IpsApi/xsd">User does not  
             have permission to access operation 'addCompany'</reason> 
           </ns1:authorizationFault> 
         </detail> 
      </soapenv:Fault> 
   </soapenv:Body> 
</soapenv:Envelope>
```
