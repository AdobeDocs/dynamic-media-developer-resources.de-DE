---
description: Verwenden Sie diese Server-Einstellungen für die Protokollierung des Zugriffs.
solution: Experience Manager
title: Zugriffsprotokollierung
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: e677a617-115d-4f6e-9eb5-bdc14ad7ff24
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '676'
ht-degree: 0%

---

# Zugriffsprotokollierung{#access-logging}

Verwenden Sie diese Server-Einstellungen für die Protokollierung des Zugriffs.

Syntax

## TC::directory - Protokolldateiordner {#section-5d9e2168d4504bbe9868b7d6051c9d67}

Der Ordner, in den der [!DNL Platform Server] Protokolldateien schreibt. Dies kann ein absoluter Pfad oder ein Pfad relativ zu *`install_folder`* sein. Der Standardwert lautet [!DNL  *`install_folder`*/logs].

>[!NOTE]
>
>Der neue Ordner muss erstellt werden, bevor diese Einstellung geändert werden kann. Stellen Sie sicher, dass der Ordner über die richtigen Lese-/Schreibzugriffsberechtigungen verfügt, wenn Image Serving für die Ausführung unter einem anderen Benutzerkonto als dem Stammkonto installiert ist.

## TC::maxDays - Anzahl der Tage, die Protokolldateien aufbewahrt werden {#section-45cbecffc5694c87b7d5c176a44a4885}

Die Anzahl der Tage, die Protokolldateien beibehalten werden sollen. Täglich um Mitternacht werden neue Protokolldateien erstellt. Zu diesem Zeitpunkt löscht der Server alle Dateien im Protokolldateiordner, die älter als die angegebene Anzahl von Tagen sind, einschließlich der vom Bild-Server oder Render-Server geschriebenen Dateien. Die Standardgrenze ist 10.

## TC::prefix - Zugriff auf Protokolldateiname {#section-1003856323b844049632710a5a056aa7}

Namenspräfix für die Datei, in die die Zugriffsprotokolldaten geschrieben werden. Datum und Dateiendung ( [!DNL  *`yyyy`*-*`mm`*-*`dd`*.log]) werden an die angegebene Zeichenfolge angehängt. Der Name der Zugriffsprotokolldatei muss sich von dem der Trace-Protokolldatei unterscheiden. Der Standardwert lautet &quot;`access-`&quot;.

## TC::pattern - Zugriffsprotokoll-Muster {#section-22775ea85cee444d8a7d7336a3b1feef}

Gibt das Datenmuster für [!DNL Platform Server] Zugriffsprotokolldatensätze an. Die Musterzeichenfolge gibt Variablen an, die durch ihre entsprechenden Werte ersetzt werden. Alle anderen Zeichen in der Musterzeichenfolge werden wörtlich in den Protokolldatensatz übertragen.

Um das Dienstprogramm zum Aufwärmen des Cache zu verwenden, müssen Leerzeichen als Feldtrennzeichen verwendet werden. Der [!DNL Platform Server] ersetzt alle Leerzeichen und &quot;%&quot;-Zeichen in den Feldwerten durch `%20` bzw. `%25`.

Die folgenden Mustervariablen werden unterstützt:

<table id="table_7A07AFF34B5040A5B30F5735CFE9428F"> 
 <thead> 
  <tr> 
   <th class="entry"> <b>Muster</b> </th> 
   <th class="entry"> <b>Beschreibung</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> %a </span> </p> </td> 
   <td> <p>Remote-IP-Adresse. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %A </span> </p> </td> 
   <td> <p>Lokale IP-Adresse. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %b </span> </p> </td> 
   <td> <p>Byteanzahl der Antwort ohne HTTP-Kopfzeilen oder ' ' bei null. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %B </span> </p> </td> 
   <td> <p>Byteanzahl der Antwort ohne HTTP-Kopfzeilen. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %d </span> </p> </td> 
   <td> <p>Verarbeitungszeit der Anfrage in Millisekunden. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %i </span> </p> </td> 
   <td> <p>Thread-ID (für Querverweise auf Debug-/Fehlerprotokolleinträge). </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %G </span> </p> </td> 
   <td> <p>Datum und Uhrzeit, formatiert als <span class="codeph"> <span class="varname"> JJJJ </span>- <span class="varname"> MM </span>- <span class="varname"> TT </span> <span class="varname"> HH </span>: <span class="varname"> mm </span>: <span class="varname"> ss </span>. <span class="varname"> SSS </span> Offset </span> </p> <p> (<span class="varname"> SSS-</span> sind msec, <span class="varname"> Offset </span> der GMT-Zeitversatz ist); der Zeitwert wird erfasst, wenn die Antwort an den Client gesendet wird. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %m </span> </p> </td> 
   <td> <p>Anfragemethode ( <span class="codeph"> GET </span>, <span class="codeph"> POST </span> usw.). </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %O </span> </p> </td> 
   <td> <p>Anfrageüberschneidung (Anzahl der gleichzeitig verarbeiteten Anfragen) </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %p </span> </p> </td> 
   <td> <p>Lokaler Port, an dem diese Anforderung empfangen wurde. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %q </span> </p> </td> 
   <td> <p>Abfragezeichenfolge (mit vorangestelltem "?“ falls vorhanden). </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %r </span> </p> </td> 
   <td> <p>Erste Zeile der Anfrage (Anfragemethode, URI, HTTP-Version). </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %R </span> </p> </td> 
   <td> <p>Entspricht <span class="codeph"> %r-</span>, wendet jedoch eine begrenzte HTTP-Kodierung auf den URI an, um Probleme beim Parsen von Protokollen zu vermeiden. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %s </span> </p> </td> 
   <td> <p>HTTP-Antwort-Status-Code. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %s </span> </p> </td> 
   <td> <p>Benutzer-Sitzungs-ID. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %t </span> </p> </td> 
   <td> <p>Datum und Uhrzeit im allgemeinen Protokollformat. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %u </span> </p> </td> 
   <td> <p>Remote-Benutzer, der authentifiziert wurde (falls vorhanden), andernfalls "". </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %u </span> </p> </td> 
   <td> <p>URI-Pfad. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %v </span> </p> </td> 
   <td> <p>Name des lokalen Servers. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %T </span> </p> </td> 
   <td> <p>Verarbeitungszeit der Anfrage in Sekunden. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{CacheKey}r </span> </p> </td> 
   <td> <p>[!DNL Platform Server] Cache-Schlüssel (Cache-Datei/Ordner/Name). </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{CacheUse}r </span> </p> </td> 
   <td> <p>[!DNL Platform Server] Schlüsselwort für die Cache-Verwaltung: <span class="codeph"> { REUSED | ERSTELLT | AKTUALISIERT | ENTFERNT | REMOTE_CREATED | REMOTE_UPDATED | REMOTE_CACHE | VALIDIERT | IGNORIERT | UNDEFINED } </span>. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{ContentType}r </span> </p> </td> 
   <td> <p>Der Antwort-MIME-Typ. </p> </td> 
  </tr> 
  <tr> 
   <td> <p>%{Context}r </p> </td> 
   <td> <p>Der Zielkontext, wenn ein Weiterleitungskontext auftritt. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{Digest}r </span> </p> </td> 
   <td> <p>Der <span class="codeph"> eTag </span> Antwort-Header-Wert (MD5-Signatur der Antwortdaten). </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{Exception}r </span> </p> </td> 
   <td> <p>Fehlermeldung. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{FetchTime}r </span> </p> </td> 
   <td> <p>Dauer des Abrufs des Cache-Eintrags oder der Daten vom Bild-Server. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{ParseTime}r </span> </p> </td> 
   <td> <p>Dauer der Anforderungs- und Bildkatalogsuche. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{PathBasedAccess}r </span> </p> </td> 
   <td> <p>Gibt an, ob mit dieser Anfrage versucht wurde, einen pfadbasierten Zugriff außerhalb des Katalogsystems durchzuführen. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{PeerServer}r </span> </p> </td> 
   <td> <p>IP-Adresse des Peer-Servers im Cache-Cluster, der den Cache-Eintrag bereitgestellt hat, oder '-', wenn <span class="codeph"> CacheUse-</span> weder <span class="codeph"> REMOTE_CREATED-</span> noch <span class="codeph"> REMOTE_UPDATED-</span> ist. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{ProcessingStatus}r </span> </p> </td> 
   <td> <p>Fehlerkategorie: </p> <p> 
     <ul id="ul_BA2A18337D374939AC9BF2424247E40F"> 
      <li id="li_0A2410F03E1A41078F8E8FDF34531810"> <p>0=kein Fehler. </p> </li> 
      <li id="li_CCEE27F75BD34195895428188B2C30AA"> <p>1=Bild(er) nicht auf dem Server gefunden. </p> </li> 
      <li id="li_315BBCC7B4C1443495C9C2B3F9800C1F"> <p> 2=IS-Protokollverwendungsfehler oder ein anderer Inhaltsfehler als 1. </p> </li> 
      <li id="li_E028FFF165BD4535875F8684FCAF1859"> <p>3=Anderer Server-Fehler. </p> </li> 
      <li id="li_5AFFB0EE80484885BCDACD9DF3EF58F7"> <p>4=Anfrage aufgrund temporärer Server-Überlastung abgelehnt. </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{ReqType}r </span> </p> </td> 
   <td> <p>Der Wert in Großbuchstaben <span class="codeph"> req= </span>. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{RootId}r </span> </p> </td> 
   <td> <p>Die Stamm-ID des Hauptkatalogs der Anfrage. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{SendTime}r </span> </p> </td> 
   <td> <p>Die Zeit, die [!DNL Platform Server] zum Senden der Antwort nach dem Schreiben von Daten in den Ausgabestream benötigt. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{Size}r </span> </p> </td> 
   <td> <p>Wie <span class="codeph"> %B </span>, enthält jedoch Werte für 304-Antworten (nicht modifiziert). </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{TransformedUrl}r </span> </p> </td> 
   <td> <p>Die endgültige URL nach allen Regelsatztransformationen. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{ <span class="varname"> httpRequestHeader </span>}i </span> </p> </td> 
   <td> <p>Der Wert des angegebenen HTTP-Anfrage-Headers. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{ <span class="varname"> httpResponseHeader </span>} </span> </p> </td> 
   <td> <p>Der Wert des angegebenen HTTP-Antwort-Headers. </p> </td> 
  </tr> 
 </tbody> 
</table>

Der Standardwert ist `"%G %a %s %{ProcessingStatus}r %{Size}r %D %{ParseTime}r %{FetchTime}r %O %{ReqType}r '%{RootId}r' %{CacheUse}r %R [%I] '%{Referer}i' %{Host}i %{X-Forwarded-For}i %{If-None-Match}i %{If-Match}i %{If-Modified-Since}i %{Digest}r %{ContentType}r %p %{Exception}r %{CacheKey}r %{PeerServer}" %{SendTime}r %{Context}r %{TransformedUrl}r %{PathBasedAccess}r.`
