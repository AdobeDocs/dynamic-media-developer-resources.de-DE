---
description: Leitet die bereitgestellte Liste von URLs an den Scene7 CDN (Content Distribution Network)-Provider weiter, um den vorhandenen Cache der HTTP-Antworten für ungültig zu erklären.
seo-description: Leitet die bereitgestellte Liste von URLs an den Scene7 CDN (Content Distribution Network)-Provider weiter, um den vorhandenen Cache der HTTP-Antworten für ungültig zu erklären.
seo-title: cdnCacheInvalidation
solution: Experience Manager
title: cdnCacheInvalidation
topic: Scene7 Image Production System API
uuid: 16cf53d4-4101-405c-b008-009b6ac62169
translation-type: tm+mt
source-git-commit: aa095022d43db4bf815aece9bc2b087c53a64e1b
workflow-type: tm+mt
source-wordcount: '490'
ht-degree: 3%

---


# cdnCacheInvalidation{#cdncacheinvalidation}

Leitet die bereitgestellte Liste von URLs an den Scene7 CDN (Content Distribution Network)-Provider weiter, um den vorhandenen Cache der HTTP-Antworten für ungültig zu erklären.

## cdnCacheInvalidation: Über {#section-4f70d2bc79d64288b961836ab17e9690}

Die CDN-Cache-Ungültigmachung zwingt dazu, dass alle HTTP-Anforderungen für diese URLs anhand der aktuellen veröffentlichten Daten im Scene7-Netzwerk erneut überprüft werden, sobald diese Ungültigmachung über das CDN-Netzwerk verarbeitet wird. Alle URLs, die nicht mit der URL-Struktur des Scene7-Dienstes verbunden sind und direkt mit der beim Erstellen der Firma zugewiesenen Scene7-Firma-Stamm-ID übereinstimmen, führen zu einem API-Fehler für die gesamte Anforderung. Ungültige URLs, die vom CDN nicht unterstützt werden und für ungültig gehalten werden, führen auch zu einem API-Fehler für die gesamte Anforderung.

**Häufigkeit der Anwendung: Regeln**

Die Regeln für die Häufigkeit der Verwendung dieser Funktion werden von den CDN-Partnern von Scene7 kontrolliert. Das CDN behält sich das Ermessen vor, die Reaktion auf diese Ungültigkeiten zu mindern, um eine optimale Leistung seines Dienstes für seine Nutzer zu gewährleisten. Sollte Scene7 über eine Übernutzung dieser Funktion informiert werden, müssen wir entweder die Funktion pro Firma oder vollständig im gesamten Service deaktivieren.

**Bestätigungs-E-Mails**

Bestätigungs-E-Mails des Scene7 CDN-Partners können an den Ersteller der Liste oder bis zu 5 weitere E-Mail-Adressen gesendet werden. Die API sendet die Bestätigung, wenn das gesamte CDN-Netzwerk benachrichtigt wurde, dass die in der E-Mail referenzierten URLs gelöscht wurden. Ein einzelner Aufruf von `cdnCacheInvalidation` kann mehrere E-Mails senden, wenn die Anzahl der bereitgestellten URLs die Anzahl übersteigt, die Scene7 dem CDN-Partner bei einer einzigen Benachrichtigung zukommen lassen kann. Derzeit würde dies der Fall sein, wenn die Anforderung 100 URLs überschreitet, aber auf Anfrage des CDN-Partners geändert werden kann.

**Unterstützt seit**

6,0

## Autorisierte Benutzertypen {#section-0d7895e733d54fb68beb8d231a04e4c9}

* `IpsAdmin`
* `IpsCompanyAdmin`

## Parameter {#section-bd1ed2b7419945d19a2ebd5668499f72}

**Eingabe** (  `cdnCacheInvalidationParam`)

<table id="table_EDD1875264C846BE951869D528A90D73"> 
 <thead> 
  <tr> 
   <th class="entry"> <b> Name</b> </th> 
   <th class="entry"> <b> Typ</b> </th> 
   <th class="entry"> <b> Erforderlich</b> </th> 
   <th class="entry"> <b> Beschreibung</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> <span class="varname"> companyHandle</span> </span> </p> </td> 
   <td> <p> <span class="codeph"> xsd:string</span> </p> </td> 
   <td> <p> Ja </p> </td> 
   <td> <p> Das Handle der Firma, die mit den zu ungültigen URLs verbunden ist. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> <span class="varname"> urlArray</span> </span> </p> </td> 
   <td> <p> <span class="codeph"> Typen:UrlArray</span> </p> </td> 
   <td> <p> Ja </p> </td> 
   <td> <p> Liste von bis zu 1000 URLs, die aus dem CDN-Cache ungültig gemacht werden. Alle URLS müssen die Scene7-Firma-Stamm-ID enthalten, damit sie ungültig wird. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Output**(  `cdnCacheInvalidationReturn`)

<table id="table_1D947C1BF8864820AD7BA0CDC0F076F9"> 
 <thead> 
  <tr> 
   <th class="entry"> <b> Name</b> </th> 
   <th class="entry"> <b> Typ</b> </th> 
   <th class="entry"> <b> Erforderlich</b> </th> 
   <th class="entry"> <b> Beschreibung</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr valign="top"> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> invalidationHandle</span></span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:string</span> </p> </td> 
   <td colname="col3"> <p>Ja </p> </td> 
   <td colname="col4"> <p>Ein Handle, das auf die Bereinigungsanforderung verweist. </p> <p>Die API <span class="codeph"> cdnCacheInvalidation</span> macht den Cache jetzt fast sofort ungültig (~5 Sekunden). Daher ist die Abfrage des Status der Ungültigerklärung im Allgemeinen nicht mehr erforderlich. </p> 
    <!--<p>The next three paragraphs were added as per CQDOC-13840 With the migration from Akamai v2 API's to fast purge, purging time is now approximately 5 seconds. You are no longer required to poll on the purge URL to find out the status of the purge request.</p>--> 
    <!--<p>The cache invalidation handle used to contained the company ID, the user account type used (small or large), and the purge url. With the release of 2019R1, <codeph>invalidationHandle</codeph> now contains just the company ID and the purge ID. </p>--> 
    <!--<p>Prior to 2019R1, two different Akamai users were being used for each geography (for example, <codeph>cdninvalidatesmallemea</codeph> and <codeph>cdninvalidatelargeemea</codeph>) to invalidate requests, depending on the number of URLs in each request. This functionality was done so that a small request was not blocked because of a large request. Now, with fast purge in 2019R1, the purge is nearly instantaneous, two users are no longer needed, and only one account is used. </p>--> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> effectiveSeconds</span></span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:int</span> </p> </td> 
   <td colname="col3"> <p>Ja </p> </td> 
   <td colname="col4"> <p>Geschätzte Sekunden bis zum Abschluss der Bereinigungsanfrage. Kunden sollten auf diese Zeit warten, bevor sie den Abrufestatus erhalten. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Beispiel {#section-f414361a58e84dfcbbac30a358d02125}

In diesem Beispiel wird gefordert, dass vier URLs im CDN-Cache ungültig gemacht werden. Die Antwort enthält zusammenfassende Zahlen zum Erfolg der Vorgänge und eine Liste mit Fehlerdetails, die direkt vom CDN bereitgestellt werden, um den Kunden bei der Verwendung dieser Funktion zu unterstützen.

`getCdnCacheInvalidationStatus` Betrieb.

**Anforderung**

```java
<cdnCacheInvalidationParam xmlns="http://www.scene7.com/IpsApi/xsd/2012-02-14">
   <companyHandle>c|6</companyHandle>
   <urlArray>
       <items>http://s7d7.scene7.com/is/image/JJEsquire/11008047?$thumbnail$</items>
       <items>http://s7d7.scene7.com/is/image/JJEsquire/11008047?$product$</items>
       <items>http://s7d7.scene7.com/is/image/JJEsquire/11008047?$large$</items>
       <items>http://s7d7.scene7.com/is/image/JJEsquire/ImageSetConfigDefaults?req=userdata</items>
    </urlArray>
</cdnCacheInvalidationParam>
```

**Antwort**

```java
<cdnCacheInvalidationReturn xmlns="http://www.scene7.com/IpsApi/xsd/2012-02-14">
   <successCount>4</successCount>
   <warningCount>0</warningCount>
   <errorCount>0</errorCount>
</cdnCacheInvalidationReturn>
```

