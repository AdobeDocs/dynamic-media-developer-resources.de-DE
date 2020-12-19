---
description: Verwenden Sie diese Servereinstellungen für den Zugriff auf die Protokollierung.
seo-description: Verwenden Sie diese Servereinstellungen für den Zugriff auf die Protokollierung.
seo-title: Zugriffsprotokollierung
solution: Experience Manager
title: Zugriffsprotokollierung
topic: Scene7 Image Serving - Image Rendering API
uuid: ea7d5d39-3f0a-45f0-bc28-6828a9c9da50
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '695'
ht-degree: 4%

---


# Zugriffsprotokollierung{#access-logging}

Verwenden Sie diese Servereinstellungen für den Zugriff auf die Protokollierung.

Syntax

## TC::directory - Protokolldateiordner {#section-5d9e2168d4504bbe9868b7d6051c9d67}

Der Ordner, in den der Plattformserver Protokolldateien schreibt. Dies kann ein absoluter Pfad oder ein Pfad relativ zu *`install_folder`* sein. Der Standardwert ist [!DNL  *`install_folder`*/logs].

>[!NOTE]
>
>Der neue Ordner muss erstellt werden, bevor diese Einstellung geändert werden kann. Stellen Sie sicher, dass der Ordner über die richtigen Lese-/Schreibzugriffsberechtigungen verfügt, wenn Image Serving für die Ausführung unter einem anderen Benutzerkonto als Root installiert ist.

## TC::maxDays - Anzahl der Tage zum Speichern von Protokolldateien {#section-45cbecffc5694c87b7d5c176a44a4885}

Die Anzahl der Tage der Protokolldateien sollte beibehalten werden. Neue Protokolldateien werden jeden Tag um Mitternacht erstellt. Zu diesem Zeitpunkt löscht der Server alle Dateien im Protokolldateiordner, die älter als die angegebene Anzahl von Tagen sind, einschließlich der vom Image-Server oder Render-Server geschriebenen Dateien. Der Standardwert ist „10“.

## TC::prefix - Name der Protokolldatei für Zugriff {#section-1003856323b844049632710a5a056aa7}

Namenpräfix für die Datei, in die die Protokolldaten geschrieben werden. Das Datum und das Dateisuffix ( [!DNL  *`yyyy`*-*`mm`*-*`dd`*.log]) werden an die angegebene Zeichenfolge angehängt. Der Name der Zugriffsprotokolldatei muss sich von dem der Ablaufverfolgungsprotokolldatei unterscheiden. Die Standardgrenze ist &quot; `access-`&quot;.

## TC::pattern - Access Log Pattern {#section-22775ea85cee444d8a7d7336a3b1feef}

Gibt das Datenmuster für Protokolldatensätze zum Zugriff auf den Plattformserver an. Die Musterzeichenfolge gibt Variablen an, die durch die entsprechenden Werte ersetzt werden. Alle anderen Zeichen in der Musterzeichenfolge werden wörtlich in den Protokolldatensatz übertragen.

Um das Dienstprogramm zum Aufwärmen des Zwischenspeichers verwenden zu können, müssen Leerzeichen als Feldtrenner verwendet werden. Der Plattformserver ersetzt alle Leerzeichen und &quot;%&quot;-Zeichen in Feldwerten durch `%20` bzw. `%25`.

Die folgenden Mustervariablen werden unterstützt:

<table id="table_7A07AFF34B5040A5B30F5735CFE9428F"> 
 <thead> 
  <tr> 
   <th class="entry"> <b>Mehrfeld</b> </th> 
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
   <td> <p>Anzahl der Antwortbyte ohne HTTP-Header oder '', wenn Null. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %B </span> </p> </td> 
   <td> <p>Anzahl der Antwortbyte ohne HTTP-Header. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %D </span> </p> </td> 
   <td> <p>Anforderungsverarbeitungszeit in Millisekunden. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %I </span> </p> </td> 
   <td> <p>thread-ID (für Querverweise zu Debug-/Fehlerprotokolleinträgen). </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %G </span> </p> </td> 
   <td> <p>Datum und Uhrzeit, formatiert als <span class="codeph"> <span class="varname"> yyy </span>- <span class="varname"> MM </span>- <span class="varname"> dd </span> <span class="varname"> HH </span>: <span class="varname"> mm </span>: <span class="varname"> ss </span>. <span class="varname"> SSS- </span> Offset  </span> </p> <p> ( <span class="varname"> SSS </span> sind msec, <span class="varname"> offset </span> ist der GMT-Zeitversatz); der Zeitwert wird erfasst, wenn die Antwort an den Client gesendet wird. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %m </span> </p> </td> 
   <td> <p>Anforderungsmethode ( <span class="codeph"> GET </span>, <span class="codeph"> POST </span> usw.). </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %O </span> </p> </td> 
   <td> <p>Anforderungsüberschneidung (Anzahl der gleichzeitig verarbeiteten Anforderungen). </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %p </span> </p> </td> 
   <td> <p>Lokaler Port, an dem diese Anforderung eingegangen ist. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %q </span> </p> </td> 
   <td> <p>Zeichenfolge der Abfrage (mit vorangestelltem "?" sofern vorhanden). </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %r </span> </p> </td> 
   <td> <p>Erste Anforderungszeile (Anforderungsmethode, URI, HTTP-Version). </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %R </span> </p> </td> 
   <td> <p>Entspricht <span class="codeph"> %r </span>, wendet jedoch eine eingeschränkte HTTP-Kodierung auf den URI an, um Probleme bei der Protokollanalyse zu vermeiden. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %s </span> </p> </td> 
   <td> <p>HTTP-Antwortstatuscode. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %S </span> </p> </td> 
   <td> <p>Benutzer-Sitzungs-ID. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %t </span> </p> </td> 
   <td> <p>Datum und Uhrzeit im allgemeinen Protokollformat. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %u </span> </p> </td> 
   <td> <p>Remote-Benutzer, der authentifiziert wurde (falls vorhanden), andernfalls ''. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %U </span> </p> </td> 
   <td> <p>URI-Pfad. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %v </span> </p> </td> 
   <td> <p>Lokaler Servername. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %T </span> </p> </td> 
   <td> <p>Verarbeitungszeit der Anforderung in Sekunden </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{CacheKey}r  </span> </p> </td> 
   <td> <p>Cache-Schlüssel für den Plattformserver (Cache-Dateiordner/Name). </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{CacheUse}r  </span> </p> </td> 
   <td> <p>Platform Server Cache Management-Schlüsselwort: <span class="codeph"> { REUSED | ERSTELLT | AKTUALISIERT | REMOTE | REMOTE_CREATED | REMOTE_UPDATED | REMOTE_CACHE | ÜBERPRÜFT | IGNORIERT | UNDEFINED } </span>. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{ContentType}r  </span> </p> </td> 
   <td> <p>Der MIME-Typ der Antwort. </p> </td> 
  </tr> 
  <tr> 
   <td> <p>%{context}r </p> </td> 
   <td> <p>Der Zielkontext, wenn ein Kontext nach vorne auftritt. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{Digest}r  </span> </p> </td> 
   <td> <p>Der Antwortkopfwert <span class="codeph"> etag </span> (MD5-Signatur der Antwortdaten). </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{Exception}r  </span> </p> </td> 
   <td> <p>Fehlermeldung. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{FetchTime}r  </span> </p> </td> 
   <td> <p>Zeit zum Abrufen des Cache-Eintrags oder der Daten vom Image-Server. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{ParseTime}r  </span> </p> </td> 
   <td> <p>Zeit für die Anforderungsanalyse und die Suche nach Bildkatalogen. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{PathBasedAccess}r  </span> </p> </td> 
   <td> <p>Gibt an, ob mit dieser Anforderung ein pfadbasierter Zugriff außerhalb des Katalogsystems versucht wurde. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{PeerServer}r  </span> </p> </td> 
   <td> <p>IP-Adresse des Peer-Servers im Cache-Cluster, der den Cache-Eintrag bereitgestellt hat, oder '-', wenn <span class="codeph"> CacheUse </span> weder <span class="codeph"> noch <span class="codeph"> REMOTE_CREATED </span> noch &lt;a4/&gt; REMOTE_UPDATED &lt;a5/&gt; ist.</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{ProcessingStatus}r  </span> </p> </td> 
   <td> <p>Fehler-Kategorie: </p> <p> 
     <ul id="ul_BA2A18337D374939AC9BF2424247E40F"> 
      <li id="li_0A2410F03E1A41078F8E8FDF34531810"> <p>0 = kein Fehler. </p> </li> 
      <li id="li_CCEE27F75BD34195895428188B2C30AA"> <p>1 = Bild(e) nicht auf dem Server gefunden. </p> </li> 
      <li id="li_315BBCC7B4C1443495C9C2B3F9800C1F"> <p> 2 = IS-Protokollverwendungsfehler oder ein Inhaltsfehler, der nicht 1 ist. </p> </li> 
      <li id="li_E028FFF165BD4535875F8684FCAF1859"> <p>3 = sonstiger Serverfehler. </p> </li> 
      <li id="li_5AFFB0EE80484885BCDACD9DF3EF58F7"> <p>4 = Anfrage wegen vorübergehender Serverüberlastung abgelehnt. </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{ReqType}r  </span> </p> </td> 
   <td> <p>Der Wert in der oberen Leiste von <span class="codeph"> req= </span>. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{RootId}r  </span> </p> </td> 
   <td> <p>Die Stamm-ID des Hauptkatalogs der Anforderung. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{SendTime}r  </span> </p> </td> 
   <td> <p>Die Zeit, die Platform Server benötigt, um eine Antwort zu senden, nachdem Daten in den Ausgabestream geschrieben wurden. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{Size}r  </span> </p> </td> 
   <td> <p>Wie <span class="codeph"> %B </span>, enthält aber Werte für 304 (nicht modifizierte) Antworten. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{TransformierteUrl}r  </span> </p> </td> 
   <td> <p>Die endgültige URL nach allen Regeltransformationen. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{  <span class="varname"> httpRequestHeader  </span>}i  </span> </p> </td> 
   <td> <p>Der Wert des angegebenen HTTP-Anforderungsheaders. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{  <span class="varname"> httpResponseHeader  </span>}  </span> </p> </td> 
   <td> <p>Der Wert des angegebenen HTTP-Antwort-Headers. </p> </td> 
  </tr> 
 </tbody> 
</table>

Der Standardwert ist „`"%G %a %s %{ProcessingStatus}r %{Size}r %D %{ParseTime}r %{FetchTime}r %O %{ReqType}r '%{RootId}r' %{CacheUse}r %R [%I] '%{Referer}i' %{Host}i %{X-Forwarded-For}i %{If-None-Match}i %{If-Match}i %{If-Modified-Since}i %{Digest}r %{ContentType}r %p %{Exception}r %{CacheKey}r %{PeerServer}" %{SendTime}r %{Context}r %{TransformedUrl}r %{PathBasedAccess}r.`
