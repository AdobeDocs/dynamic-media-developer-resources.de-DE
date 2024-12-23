---
description: Der IPS-Webdienst wird von einer Reihe von WSDL-Dokumenten (Web Services Description Language) unterstützt, auf die von jeder IPS-Installation zugegriffen wird, auf der die IPS-Webdienstkomponente installiert ist. Jede IPS-API-Version enthält eine neue WSDL-Datei, die auf einen versionierten Ziel-XML-Namespace verweist. Frühere WSDL-Namespace-Versionen werden ebenfalls unterstützt, um die Abwärtskompatibilität mit vorhandenen Anwendungen zu ermöglichen.
solution: Experience Manager
title: WSDL-Versionen des IPS-Webdienstes
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: d7a6079e-286e-4e62-b2ff-551ef4a5815c
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '901'
ht-degree: 1%

---

# WSDL-Versionen des IPS-Webdienstes{#ips-web-service-wsdl-versions}

Der IPS-Webdienst wird von einer Reihe von WSDL-Dokumenten (Web Services Description Language) unterstützt, auf die von jeder IPS-Installation zugegriffen wird, auf der die IPS-Webdienstkomponente installiert ist. Jede IPS-API-Version enthält eine neue WSDL-Datei, die auf einen versionierten Ziel-XML-Namespace verweist. Frühere WSDL-Namespace-Versionen werden ebenfalls unterstützt, um die Abwärtskompatibilität mit vorhandenen Anwendungen zu ermöglichen.

## WSDL-Zugriff {#section-62e69fa2c87f4dc9bca72f10ba028f6c}

Greifen Sie auf die Scene7-WSDLs zu, wie unten dargestellt.

```
https://<IPS_hostname:<IPS_port>/<IPS_webapp>/ 
webservice/IpsApi[-<API_version>].wsdl 
```

Der Standardwert für `<IPS_webapp>` ist `scene7`.

**Service-Speicherort**

Die Service-URL wird im Abschnitt Service des WSDL-Dokuments des IPS-Webservices angegeben. Die Service-URL hat im Allgemeinen folgende Form:

```
https://<IPS_hostname>:<IPS_port>/<IPS_webapp>/ 
services/IpsApiService 
```

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
   <td colname="col2"> <p> https://s7sps1apissl.scene7.com/scene7/ </p> </td> 
   <td colname="col3"> <p> https://s7sps1apissl-staging.scene7.com/scene7/ </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Europa, Naher Osten, Asien </p> </td> 
   <td colname="col2"> <p> https://s7sps3apissl.scene7.com/scene7/ </p> </td> 
   <td colname="col3"> <p> https://s7sps3apissl-staging.scene7.com/scene7/ </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Japan/Asien/Pazifik </p> </td> 
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
   <th colname="col1" class="entry"> <p>API-Release-Version </p> </th> 
   <th colname="col2" class="entry"> <p>WSDL </p> </th> 
   <th colname="col3" class="entry"> <p>API-Namespace </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>6.8/2014R1 </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> IpsAPI-2014-04-03.wsdl </span> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> http://www.scene7.com/IpsApi/xsd/2014-04-03 </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>6.6/2013R1 </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> IpsAPI-2013-02-15.wsdl </span> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> http://www.scene7.com/IpsApi/xsd/2013-02-15 </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>6.0/2012R1 </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> IpsAPI-2012-02-14.wsdl </span> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> http://www.scene7.com/IpsApi/xsd/2012-02-14 </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>4,5 </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> IpsAPI-2010-01-31.wsdl </span> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> http://www.scene7.com/IpsApi/xsd/2010-01-31 </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>4,4 </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> IpsAPI-2009-07-31.wsdl </span> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> http://www.scene7.com/IpsApi/xsd/2009-07-31 </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>4,2 </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> IpsAPI-2008-09-10.wsdl </span> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> http://www.scene7.com/IpsApi/xsd/2008-09-10 </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>4,0 </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> IpsAPI-2008-01-15.wsdl </span> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> http://www.scene7.com/IpsApi/xsd/2008-01-15 </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>vor 4.0 </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> IpsApi.wsdl-</span> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> http://www.scene7.com/IpsApi/xsd </span> </p> </td> 
  </tr> 
 </tbody> 
</table>

Bestehende Anwendungen, die geändert werden müssen, um neue Funktionen zu verwenden, müssen auf die neueste API-Version aktualisieren und müssen möglicherweise Änderungen am vorhandenen Code vornehmen. Einzelheiten finden Sie im Änderungsprotokoll .

## SOAP {#section-51e7ecbd1d7f451b9e4f6bf7e1579cae}

**Bindungen**

Der IPS-API-Webservice unterstützt nur eine SOAP-Bindung.

**Unterstützte Transporte**

Die SOAP-Bindung der IPS-API unterstützt nur den HTTP-Transport. Stellen Sie alle SOAP-Anfragen mithilfe der HTTPS-POST-Methode.

**SOAP-Aktionskopfzeile**

Um eine Anfrage zu verarbeiten, legen Sie den SOAPAction-HTTP-Header auf den Namen des angeforderten Vorgangs fest. Das Attribut „Vorgangsname“ im Abschnitt „WSDL-Bindung“ gibt den Namen an.

**Nachrichtenformat**

Der Dokument-/Literalstil wird für alle Eingabe- und Ausgabemeldungen mit Typen verwendet, die auf der XML-Schemadefinitionssprache ( [https://www.w3.org/TR/xmlschema-0/](https://www.w3.org/TR/xmlschema-0/)) basieren und in der WSDL-Datei angegeben sind. Für alle Typen sind qualifizierte Namen erforderlich, die den in der WSDL-Datei angegebenen Namespace-Zielwert verwenden.

**Authentifizierung anfordern**

Die bevorzugte Methode zum Übergeben von Authentifizierungsdaten in API-Anfragen besteht darin, das `authHeader`-Element zu verwenden, wie es in der IPS-API-WSDL definiert ist.

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
   <td colname="col1"> <p> <span class="codeph">-</span> </p> </td> 
   <td colname="col2"> <p> Gültige IP-Benutzer-E-Mail. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> </span> <span class="codeph"> </p> </td> 
   <td colname="col2"> <p>Kennwort für Benutzerkonto. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">-</span> </p> </td> 
   <td colname="col2"> <p> Optionales Gebietsschema für die Anfrage. Siehe <b>Gebietsschema</b> für Details. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> AppName-</span> <span class="codeph"> </p> </td> 
   <td colname="col2"> <p> Aufrufender Anwendungsname. Dieser Parameter ist optional, es wird jedoch empfohlen, ihn in alle Anfragen aufzunehmen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> appVersion-</span> </p> </td> 
   <td colname="col2"> <p> Aufrufende Anwendungsversion. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> gzipResponse-</span> </p> </td> 
   <td colname="col2"> <p> Optionales Flag zum Aktivieren oder Deaktivieren der gzip-Komprimierung der Antwort-XML. Standardmäßig sind Antworten gzip-komprimiert, wenn der HTTP Accept-Encoding-Header Unterstützung für gzip anzeigt. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">-</span> </p> </td> 
   <td colname="col2"> <p> Optionaler Parameter zum Überschreiben des HTTP-Status-Codes für Fehlerantworten. Standardmäßig geben Fehlerantworten den HTTP-Status-Code 500 zurück (Interner Server-Fehler). Einige Client-Plattformen, einschließlich Adobe-Flash, können den Antworttext nur lesen, wenn der Statuscode 200 (OK) zurückgegeben wird. </p> </td> 
  </tr> 
 </tbody> 
</table>

Das `authHeader`-Element wird unabhängig von der API-Version immer im Namespace-`http://www.scene7.com/IpsApi/xsd` definiert.

Im Folgenden finden Sie ein Beispiel für die Verwendung des `authHeader`-Elements in einem Anfrage-SOAP-Header:

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

**Andere Authentifizierungsmethoden für Anfragen**

Wenn es aus irgendeinem Grund für Ihre Client-Anwendung nicht möglich ist, den `authHeader`-SOAP-Header zu übergeben, können API-Anfragen auch Anmeldeinformationen mithilfe der HTTP-Standardauthentifizierung angeben (wie in RFC 2617 angegeben).

Für die HTTP-Standardauthentifizierung muss der HTTP-Header-Abschnitt jeder SOAP-POST-Anfrage eine Kopfzeile des Formulars enthalten:

`Authorization: Basic base64(<IPS_user_email>:<password>)`

Wenn `base64()` die standardmäßige Base64-Codierung anwendet, ist `<IPS_user_email>` die E-Mail-Adresse eines gültigen IPS-Benutzers und `<password>` das Kennwort des Benutzers.

Senden Sie die Autorisierungs-Kopfzeile präventiv mit der ursprünglichen Anfrage. Wenn in der Anfrage keine Authentifizierungs-Anmeldeinformationen enthalten sind, antwortet `IpsApiService` nicht mit dem Status-Code `401 (Unauthorized)`. Stattdessen wird ein Status-Code von `500 (Internal Server Error)` mit einem SOAP-Fehlertext zurückgegeben, der angibt, dass die Anfrage nicht authentifiziert werden konnte.

Vor IPS 3.8 wurde die Authentifizierung über den SOAP-Header mithilfe der `AuthUser`- und `AuthPassword` im Namespace-`http://www.scene7.com/IpsApi` implementiert. Beispiel:

```
<soap:Header xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"> 
   <AuthUser xmlns="http://www.scene7.com/IpsApi">user@scene7.com</AuthUser> 
   <AuthPassword xmlns="http://www.scene7.com/IpsApi">mypassword</AuthPassword> 
</soap:Header>
```

Dieser Stil wird aus Gründen der Abwärtskompatibilität weiterhin unterstützt, wurde jedoch zugunsten des `authHeader` Elements eingestellt.

**Autorisierung anfordern**

Nachdem die Anmeldeinformationen des Aufrufers authentifiziert wurden, wird die Anfrage überprüft, um sicherzustellen, dass der Aufrufer berechtigt ist, den angeforderten Vorgang auszuführen. Die Autorisierung basiert auf der Benutzerrolle der Aufrufenden und erfordert möglicherweise auch die Überprüfung des Zielunternehmens, des Zielbenutzers und anderer Vorgangsparameter. Darüber hinaus müssen Image Portal-Benutzer einer Gruppe mit den erforderlichen Berechtigungen angehören, um bestimmte Ordner- und Asset-Vorgänge auszuführen. Im Abschnitt Operations Reference werden die Autorisierungsanforderungen für jeden Vorgang beschrieben.

**Beispiel für SOAP-Anfrage und -Antwort**

Das folgende Beispiel zeigt einen vollständigen `addCompany` einschließlich HTTP-Kopfzeilen:

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

**SOAP-Fehler**

Wenn bei einem Vorgang eine Ausnahmebedingung auftritt, wird anstelle der normalen -Antwort ein SOAP-Fehler als Text der SOAP-Nachricht zurückgegeben. Wenn beispielsweise ein Benutzer ohne Administratorrechte versucht, die vorherige `addCompany`-Anfrage zu senden, wird die folgende Antwort zurückgegeben:

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
