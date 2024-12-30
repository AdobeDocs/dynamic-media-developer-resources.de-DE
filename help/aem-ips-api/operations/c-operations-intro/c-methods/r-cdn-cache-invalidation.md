---
description: Leitet die bereitgestellte Liste der URLs an den Dynamic Media CDN-Provider (Content Distribution Network) weiter, um den vorhandenen Cache mit HTTP-Antworten ungültig zu machen.
solution: Experience Manager
title: cdnCacheInvalidation
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 65b758f2-b49a-4616-b657-a64808c9202a
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '476'
ht-degree: 1%

---

# cdnCacheInvalidation{#cdncacheinvalidation}

Leitet die bereitgestellte Liste der URLs an den Dynamic Media CDN-Provider (Content Distribution Network) weiter, um den vorhandenen Cache mit HTTP-Antworten ungültig zu machen.

## cdnCacheInvalidation: Über {#section-4f70d2bc79d64288b961836ab17e9690}

Die CDN-Cache-Invalidierung erzwingt, dass alle HTTP-Anfragen für diese URLs anhand der aktuell im Dynamic Media-Netzwerk veröffentlichten Daten erneut überprüft werden, nachdem diese Invalidierungsanfrage über das CDN-Netzwerk verarbeitet wurde. Alle URLs, die nicht mit der Dynamic Media-Service-URL-Struktur verbunden sind und direkt mit der beim Erstellen des Unternehmens zugewiesenen Dynamic Media-Unternehmens-Stamm-ID übereinstimmen, führen zu einem API-Fehler für die gesamte Anfrage. Alle ungültigen URLs, die das CDN nicht unterstützt und die es als ungültig erachtet, führen ebenfalls zu einem API-Fehler für die gesamte Anfrage.

**Häufigkeit der Verwendung: Regeln**

Die Regeln für die Häufigkeit der Verwendung dieser Funktion werden von den CDN-Partnern von Dynamic Media gesteuert. Das CDN behält sich das Ermessen vor, die Reaktionsfähigkeit dieser Invalidierungen zu verringern, um die optimale Leistung seines Service für seine Benutzer aufrechtzuerhalten. Sollte Dynamic Media über eine übermäßige Nutzung dieser Funktion informiert werden, muss Adobe diese Funktion entweder unternehmensübergreifend oder im gesamten Service deaktivieren.

**Bestätigungs-E-Mails**

Bestätigungs-E-Mails vom Dynamic Media CDN-Partner können an den Ersteller der Liste oder an bis zu 5 andere E-Mail-Adressen gesendet werden. Die API sendet die Bestätigung, wenn das gesamte CDN-Netzwerk darüber informiert wurde, dass die in der E-Mail referenzierten URLs gelöscht wurden. Ein einziger Aufruf an `cdnCacheInvalidation` kann mehrere E-Mails senden, wenn die Anzahl der bereitgestellten URLs die Anzahl überschreitet, die Dynamic Media mit einer einzigen Benachrichtigung an den CDN-Partner senden kann. Derzeit wäre dies der Fall, wenn die Anfrage 100 URLs überschreitet, aber auf Anfrage des CDN-Partners geändert werden kann.

**Unterstützt seit**

6,0

## Autorisierte Benutzertypen {#section-0d7895e733d54fb68beb8d231a04e4c9}

* `IpsAdmin`
* `IpsCompanyAdmin`

## Parameter {#section-bd1ed2b7419945d19a2ebd5668499f72}

**Eingabe** ( `cdnCacheInvalidationParam`)

<table id="table_EDD1875264C846BE951869D528A90D73"> 
 <thead> 
  <tr> 
   <th class="entry"> <b> Name</b> </th> 
   <th class="entry"> <b> Typ</b> </th> 
   <th class="entry"> <b> erforderlich</b> </th> 
   <th class="entry"> <b> Beschreibung</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> <span class="varname"> companyHandle</span> </span> </p> </td> 
   <td> <p> <span class="codeph"> xsd:string</span> </p> </td> 
   <td> <p> Ja </p> </td> 
   <td> <p> Das Handle an das Unternehmen, das mit den zu invalidierenden URLs verbunden ist. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> <span class="varname"> urlArray</span> </span> </p> </td> 
   <td> <p> <span class="codeph">:UrlArray</span> </p> </td> 
   <td> <p> Ja </p> </td> 
   <td> <p> Liste von bis zu 1.000 URLs, die im CDN-Cache ungültig gemacht werden sollen. Alle URLs müssen die Stamm-ID des Dynamic Media-Unternehmens enthalten, damit sie ungültig werden. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Ausgabe**( `cdnCacheInvalidationReturn`)

<table id="table_1D947C1BF8864820AD7BA0CDC0F076F9"> 
 <thead> 
  <tr> 
   <th class="entry"> <b> Name</b> </th> 
   <th class="entry"> <b> Typ</b> </th> 
   <th class="entry"> <b> erforderlich</b> </th> 
   <th class="entry"> <b> Beschreibung</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr valign="top"> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> invalidationHandle</span></span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:string</span> </p> </td> 
   <td colname="col3"> <p>Ja </p> </td> 
   <td colname="col4"> <p>Ein -Handle, das auf die Bereinigungsanfrage verweist. </p> <p>Die <span class="codeph"> cdnCacheInvalidation</span>-API macht den Cache jetzt fast sofort ungültig (~5 Sekunden). Daher ist das Abrufen des Invalidierungsstatus im Allgemeinen nicht mehr erforderlich. </p> 
    <!--<p>The next three paragraphs were added as per CQDOC-13840 With the migration from Akamai v2 API's to fast purge, purging time is now approximately 5 seconds. You are no longer required to poll on the purge URL to find out the status of the purge request.</p>--> 
    <!--<p>The cache invalidation handle used to contained the company ID, the user account type used (small or large), and the purge url. With the release of 2019R1, <codeph>invalidationHandle</codeph> now contains just the company ID and the purge ID. </p>--> 
    <!--<p>Prior to 2019R1, two different Akamai users were being used for each geography (for example, <codeph>cdninvalidatesmallemea</codeph> and <codeph>cdninvalidatelargeemea</codeph>) to invalidate requests, depending on the number of URLs in each request. This functionality was done so that a small request was not blocked because of a large request. Now, with fast purge in 2019R1, the purge is nearly instantaneous, two users are no longer needed, and only one account is used. </p>--> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> estimatedSeconds</span></span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:int</span> </p> </td> 
   <td colname="col3"> <p>Ja </p> </td> 
   <td colname="col4"> <p>Geschätzte Sekunden bis zum Abschluss der Bereinigungsanfrage. Clients sollten auf diesen Zeitpunkt warten, bevor sie den Status abfragen. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Beispiel {#section-f414361a58e84dfcbbac30a358d02125}

In diesem Beispiel werden vier URLs im CDN-Cache ungültig gemacht. Die Antwort enthält eine Zusammenfassung des Erfolgs der Vorgänge und eine Liste der Fehlerdetails, die direkt vom CDN bereitgestellt werden, um den Client bei der Verwendung dieser Funktion zu unterstützen.

`getCdnCacheInvalidationStatus`.

**Anfrage**

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
