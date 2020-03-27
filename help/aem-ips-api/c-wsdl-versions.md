---
description: Der IPS-Webdienst wird von einer Reihe von WSDL-Dokumenten (Web Services Description Language) unterstützt, auf die von jeder IPS-Installation, auf der die IPS-Webdienstkomponente installiert ist, zugegriffen wird. Jede IPS-API-Version enthält eine neue WSDL-Datei, die auf einen XML-Namensraum mit Versionsnummer verweist. Frühere WSDL Namensraum-Versionen werden ebenfalls unterstützt, um die Abwärtskompatibilität mit bestehenden Anwendungen zu gewährleisten.
seo-description: Der IPS-Webdienst wird von einer Reihe von WSDL-Dokumenten (Web Services Description Language) unterstützt, auf die von jeder IPS-Installation, auf der die IPS-Webdienstkomponente installiert ist, zugegriffen wird. Jede IPS-API-Version enthält eine neue WSDL-Datei, die auf einen XML-Namensraum mit Versionsnummer verweist. Frühere WSDL Namensraum-Versionen werden ebenfalls unterstützt, um die Abwärtskompatibilität mit bestehenden Anwendungen zu gewährleisten.
seo-title: IPS Web Service WSDL Versionen
solution: Experience Manager
title: IPS Web Service WSDL Versionen
topic: Scene7 Image Production System API
uuid: 3443bb91-1663-4686-b20a-94c372f0026e
translation-type: tm+mt
source-git-commit: aa095022d43db4bf815aece9bc2b087c53a64e1b

---


# IPS Web Service WSDL Versionen{#ips-web-service-wsdl-versions}

Der IPS-Webdienst wird von einer Reihe von WSDL-Dokumenten (Web Services Description Language) unterstützt, auf die von jeder IPS-Installation, auf der die IPS-Webdienstkomponente installiert ist, zugegriffen wird. Jede IPS-API-Version enthält eine neue WSDL-Datei, die auf einen XML-Namensraum mit Versionsnummer verweist. Frühere WSDL Namensraum-Versionen werden ebenfalls unterstützt, um die Abwärtskompatibilität mit bestehenden Anwendungen zu gewährleisten.

## WSDL-Zugriff {#section-62e69fa2c87f4dc9bca72f10ba028f6c}

Greifen Sie wie unten dargestellt auf die Scene7-WSDLs zu.

```
https://<IPS_hostname:<IPS_port>/<IPS_webapp>/ 
webservice/IpsApi[-<API_version>].wsdl 
```

Der Standardwert für `<IPS_webapp>` ist `scene7`.

**Dienststandort**

Die Dienst-URL wird im Dienstabschnitt des IPS-Webdienst-WSDL-Dokuments angegeben. Die Dienst-URL lautet im Allgemeinen wie folgt:

```
https://<IPS_hostname>:<IPS_port>/<IPS_webapp>/ 
services/IpsApiService 
```

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

Denken Sie daran, dass Sie Ihren Code möglicherweise ändern müssen, wenn Sie Funktionen in der neuesten Version der IPS-API verwenden möchten. Die IPS-API unterstützt WSDLs für die folgenden Versionen:

<table id="table_6FABCC4E7786448CB56C343E3C0B36CA"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>API Release-Version </p> </th> 
   <th colname="col2" class="entry"> <p>WSDL </p> </th> 
   <th colname="col3" class="entry"> <p>API-Namensraum </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>6.8/2014R1 </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> IpsApi-2014-04-03.wsdl </span> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> http://www.scene7.com/IpsApi/xsd/2014-04-03 </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>6.6/2013R1 </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> ipsApi-2013-02-15.wsdl </span> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> http://www.scene7.com/IpsApi/xsd/2013-02-15 </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>6.0/2012R1 </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> IpsApi-2012-02-14.wsdl </span> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> http://www.scene7.com/IpsApi/xsd/2012-02-14 </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>4.5 </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> IpsApi-2010-01-31.wsdl </span> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> http://www.scene7.com/IpsApi/xsd/2010-01-31 </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>4.4 </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> IpsApi-2009-07-31.wsdl </span> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> http://www.scene7.com/IpsApi/xsd/2009-07-31 </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>4.2 </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> IpsApi-2008-09-10.wsdl </span> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> http://www.scene7.com/IpsApi/xsd/2008-09-10 </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>4.0 </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> ipsApi-2008-01-15.wsdl </span> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> http://www.scene7.com/IpsApi/xsd/2008-01-15 </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Pre-4.0 </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> IpsApi.wsdl </span> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> http://www.scene7.com/IpsApi/xsd </span> </p> </td> 
  </tr> 
 </tbody> 
</table>

Bestehende Anwendungen, die geändert werden müssen, um neue Funktionen zu verwenden, müssen auf die neueste API-Version aktualisieren und müssen möglicherweise Änderungen am vorhandenen Code vornehmen. Weitere Informationen finden Sie im Änderungsprotokoll.

## SOAP {#section-51e7ecbd1d7f451b9e4f6bf7e1579cae}

**Bindungen**

Der IPS-API-Webdienst unterstützt nur eine SOAP-Bindung.

**Unterstützte Transporte**

Die IPS API SOAP-Bindung unterstützt nur HTTP-Transport. Nehmen Sie alle SOAP-Anforderungen mit der HTTPS POST-Methode vor.

**SOAP-Aktionsheader**

Um eine Anforderung zu verarbeiten, setzen Sie den SOAPAction-HTTP-Header auf den Namen der angeforderten Operation. Das Vorgangsnamenattribut im WSDL-Bindungsbereich gibt den Namen an.

**Nachrichtenformat**

Der Stil &quot;Dokument/Literal&quot;wird für alle Eingabe- und Ausgabemeldungen verwendet, deren Typen auf der XML-Schema-Definitionssprache ( [http://www.w3.org/TR/xmlschema-0/](http://www.w3.org/TR/xmlschema-0/)) basieren und in der WSDL-Datei angegeben sind. Für alle Typen sind qualifizierte Namensraum erforderlich, die den in der WSDL-Datei angegebenen Wert für die Zielgruppe verwenden.

**Authentifizierung anfordern**

Die bevorzugte Methode zur Übergabe von Authentifizierungsberechtigungen in API-Anforderungen besteht darin, das `authHeader` Element zu verwenden, wie in der IPS-API-WSDL definiert.

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
   <td colname="col1"> <p> <span class="codeph"> Benutzer </span> </p> </td> 
   <td colname="col2"> <p> Gültige IPS-Benutzer-E-Mail. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Passwort </span> </p> </td> 
   <td colname="col2"> <p>Kennwort für Benutzerkonto. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> locale </span> </p> </td> 
   <td colname="col2"> <p> Optionales Gebietsschema für Anforderung. See <b>Locale</b> for details. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> appName </span> </p> </td> 
   <td colname="col2"> <p> Aufruf des Anwendungsnamens. Dieser Parameter ist optional, es wird jedoch empfohlen, ihn in alle Anforderungen einzubeziehen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> appVersion </span> </p> </td> 
   <td colname="col2"> <p> Aufruf der Anwendungsversion. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> gzipResponse </span> </p> </td> 
   <td colname="col2"> <p> Optionales Flag zum Aktivieren oder Deaktivieren der gzip-Komprimierung der Antwort-XML. Standardmäßig werden Antworten gzip-komprimiert, wenn der HTTP Accept-Encoding-Header die Unterstützung für gzip anzeigt. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> faultHttpStatusCode </span> </p> </td> 
   <td colname="col2"> <p> Optionaler Parameter zum Überschreiben des HTTP-Statuscodes für Fehlerantworten. Standardmäßig geben Fehlerantworten den HTTP-Statuscode 500 zurück (Interner Serverfehler). Einige Clientplattformen, einschließlich Adobe Flash, können den Antworttext nur lesen, wenn ein Statuscode von 200 (OK) zurückgegeben wird. </p> </td> 
  </tr> 
 </tbody> 
</table>

Das `authHeader` Element wird unabhängig von der API-Version immer im Namensraum definiert `http://www.scene7.com/IpsApi/xsd`.

Im Folgenden finden Sie ein Beispiel für die Verwendung des `authHeader` Elements in einem SOAP-Anforderungs-Header:

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

**Andere Methoden zur Anforderungsauthentifizierung**

Wenn es aus irgendeinem Grund nicht möglich ist, dass Ihre Clientanwendung den `authHeader` SOAP-Header übergibt, können API-Anforderungen auch Anmeldeinformationen mit der HTTP Basic-Authentifizierung angeben (wie in RFC 2617 angegeben).

Für die HTTP Basic-Authentifizierung muss der HTTP-Header-Abschnitt jeder SOAP POST-Anforderung eine Kopfzeile des Formulars enthalten:

`Authorization: Basic base64(<IPS_user_email>:<password>)`

Bei `base64()` Anwendung der standardmäßigen Base64-Kodierung ist `<IPS_user_email>` die E-Mail-Adresse eines gültigen IPS-Benutzers und `<password>` das Kennwort des Benutzers angegeben.

Senden Sie den Autorisierungs-Header mit der ursprünglichen Anforderung präventiv. Wenn keine Authentifizierungsberechtigungen in der Anforderung enthalten sind, antwortet `IpsApiService` nicht mit einem Statuscode von `401 (Unauthorized)`. Stattdessen `500 (Internal Server Error)` wird ein Statuscode mit einem SOAP-Fehlerkörper zurückgegeben, der angibt, dass die Anforderung nicht authentifiziert werden konnte.

Vor IPS 3.8 wurde die Authentifizierung über den SOAP-Header mithilfe der Elemente `AuthUser` und `AuthPassword` im Namensraum implementiert `http://www.scene7.com/IpsApi`. Beispiel:

```
<soap:Header xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"> 
   <AuthUser xmlns="http://www.scene7.com/IpsApi">user@scene7.com</AuthUser> 
   <AuthPassword xmlns="http://www.scene7.com/IpsApi">mypassword</AuthPassword> 
</soap:Header>
```

Dieser Stil wird noch aus Gründen der Abwärtskompatibilität unterstützt, wurde jedoch zugunsten des `authHeader` Elements aufgegeben.

**Autorisierung anfordern**

Nachdem die Anmeldeinformationen des Aufrufers authentifiziert wurden, wird die Anforderung überprüft, um sicherzustellen, dass der Aufrufer zur Durchführung des angeforderten Vorgangs berechtigt ist. Die Autorisierung basiert auf der Benutzerrolle des Aufrufers und erfordert möglicherweise auch die Überprüfung der Firma der Zielgruppe, der Zielgruppe und anderer Parameter. Darüber hinaus müssen Image Portal-Benutzer zu einer Gruppe gehören, die über die erforderlichen Berechtigungen zum Ausführen bestimmter Ordner- und Asset-Vorgänge verfügt. Im Abschnitt &quot;Betriebsreferenz&quot;werden die Zulassungsanforderungen für jeden Vorgang erläutert.

**Beispiel für SOAP-Anforderung und -Antwort**

Das folgende Beispiel zeigt einen vollständigen `addCompany` Vorgang, einschließlich HTTP-Kopfzeilen:

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

Wenn ein Vorgang auf eine Ausnahmebedingung trifft, wird ein SOAP-Fehler als SOAP-Nachrichtentext anstelle der normalen Antwort zurückgegeben. Wenn beispielsweise ein Benutzer ohne Administratorrechte versucht, die vorherige `addCompany` Anforderung zu senden, wird die folgende Antwort zurückgegeben:

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

