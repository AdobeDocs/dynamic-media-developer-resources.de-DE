---
title: Lokalisierung von Textzeichenfolgen
description: Mit der Lokalisierung von Textzeichenfolgen können Bildkataloge mehrere gebietsschemaspezifische Darstellungen für denselben Zeichenfolgenwert enthalten.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: f105c7f2-b544-4c08-bb91-4916e485572d
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '644'
ht-degree: 1%

---

# Lokalisierung von Textzeichenfolgen{#text-string-localization}

Mit der Lokalisierung von Textzeichenfolgen können Bildkataloge mehrere gebietsschemaspezifische Darstellungen für denselben Zeichenfolgenwert enthalten.

Der Server gibt an den Client die Darstellung zurück, die dem mit `locale=` angegebenen Gebietsschema entspricht, wodurch eine Client-seitige Lokalisierung vermieden wird und Anwendungen Gebietsschemata wechseln können, indem einfach der entsprechende `locale=` mit den IS-Textanforderungen gesendet wird.

## Umfang {#section-a03f48e3bc0e4ab281909a2bd441a3c2}

Die Lokalisierung von Textzeichenfolgen wird auf alle Zeichenfolgenelemente angewendet, die das Lokalisierungs-Token ` ^loc= *`locId`*^` in den folgenden Katalogfeldern enthalten:

<table id="table_83344EFCB5B5418184E0A0B43D0B23F7"> 
 <thead> 
  <tr> 
   <th class="entry"> <b>Katalogfeld</b> </th> 
   <th class="entry"> <b>Zeichenfolgenelement im Feld</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph">::ImageSet-</span> </p> </td> 
   <td> <p>Beliebiges Unterelement, das eine übersetzbare Zeichenfolge enthält (durch eine beliebige Kombination von Trennzeichen ',' ';' ':' und/oder den Anfang/das Ende des Felds getrennt). </p> <p> Ein <span class="codeph"> 0xrggbb </span> Farbwert am Anfang eines lokalisierbaren Felds wird von der Lokalisierung ausgeschlossen und unverändert weitergeleitet. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph">::Map </span> </p> </td> 
   <td> <p>Jeder Attributwert in einfachen oder doppelten Anführungszeichen, mit Ausnahme der Werte der Attribute <span class="codeph"> = </span> und <span class="codeph"> Shape= </span>. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph">::Targets-</span> </p> </td> 
   <td> <p>Der Wert eines beliebigen <span class="codeph">.*.label </span> und <span class="codeph"> Target.*.UserData-</span>. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph">::UserData-</span> </p> </td> 
   <td> <p>Der Wert einer beliebigen Eigenschaft. </p> </td> 
  </tr> 
 </tbody> 
</table>

## String-Syntax {#section-d12320edf300409f8e17565b143acafc}

Lokalisierungsfähige *`string`* im Bildkatalog bestehen aus einer oder mehreren lokalisierten Zeichenfolgen, denen jeweils ein Lokalisierungs-Token vorangestellt ist.

<table id="simpletable_CEFDAE8395E6493E902D58A7E5A25BC7"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> stringElement </span> </span> </p> </td> 
  <td class="stentry"> <p>[ <span class="varname"> defaultString </span>]*{ <span class="varname"> localizationToken </span> <span class="varname"> localizedString </span>} </p> </td> 
 </tr> 
</table>

<table id="simpletable_0A687FA72C4C4C1AAFFCB43143C1AB3B"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> LocalizationToken </span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> ^loc= <span class="varname"> locStr </span> ^ </span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> locId </span> </span> </p> </td> 
  <td class="stentry"> <p>Interne Gebietsschema-ID für die <span class="varname"> localizedString </span> nach diesem <span class="varname"> localizationToken-</span>. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> localizedString </span> </span> </p> </td> 
  <td class="stentry"> <p>Lokalisierte Zeichenfolge. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> defaultString </span> </span> </p> </td> 
  <td class="stentry"> <p>Für unbekannte Gebietsschemata zu verwendender String </p> </td> 
 </tr> 
</table>

Der *`locId`* muss ASCII sein und darf nicht &#39;^&#39; enthalten.

Das &#39;^&#39; kann überall in Unterzeichenfolgen mit oder ohne HTTP-Kodierung auftreten. Der Server ordnet das gesamte *`localizationToken`*-`^loc=locId^`-Muster zu, um Teilzeichenfolgen zu trennen.

Die *`stringElements`*, die nicht mindestens eine *`localizationToken`* enthalten, werden nicht für die Lokalisierung berücksichtigt.

## Die Übersetzungskarte {#section-f7ce3df91b724adf95cee44eac4915d4}

`attribute::LocaleStrMap` definiert die Regeln, anhand derer der Server bestimmt, welche *`localizedStrings`* an den Client zurückgegeben werden sollen. Sie besteht aus einer Liste von *`locales`* (die mit den mit `locale=` angegebenen Werten übereinstimmen), von denen jede keine oder mehrere interne Gebietsschema-IDs ( *`locId`*) aufweist. Beispiel:

`attribute::LocaleStrMap= en,E|nl,N|de,D|,`

Leere *`locId`* geben an, dass die *`defaultString`* zurückgegeben werden soll, sofern verfügbar.

Weitere Informationen finden Sie in der Beschreibung von `attribute::LocaleStrMap`.

## Der Übersetzungsprozess {#section-a2a8a3e5850f4f7c9d2318267afe98a2}

Angesichts der obigen beispielhaften Übersetzungszuordnung und der Anfrage-`/is/image/myCat/myItem?req=&locale=nl` sucht der Server zunächst in der Gebietsschema-Zuordnung nach &quot;`nl`&quot;. Der übereinstimmende `nl,N` gibt an, dass für jeden *`stringElement`* der mit `^loc=N^` markierte *`localizedString`* zurückgegeben werden soll. Wenn diese *`localizationToken`* nicht in der *`stringElement`* vorhanden ist, wird ein leerer Wert zurückgegeben.

Nehmen wir an, `catalog::UserData` für `myCat/myItem` enthält Folgendes (Zeilenumbrüche wurden aus Gründen der Klarheit eingefügt):

`val1=111?? str1=Default1^loc=N^Dutch1^loc=D^German1?? val2=value2?? str2=^loc=E^English2^loc=N^Dutch2^loc=D^German2?? str3=Default3^loc=N^Dutch3^loc=D^German3`

Der Server gibt als Antwort auf die Beispielanfrage Folgendes zurück:

`val1=111 str1=Dutch1 val2=value2 str2=Dutch2 str3=Dutch3`

## Unbekannte Gebietsschemata {#section-26dfeefbd60345de94bbfeaaf7741223}

Im obigen Beispiel hat `attribute::LocaleStrMap` einen Eintrag mit einem leeren *`locale`*. Der Server verwendet diesen Eintrag, um alle `locale=` zu verarbeiten, die nicht explizit anders in der Übersetzungszuordnung angegeben sind.

Die beispielhafte Übersetzungszuordnung gibt an, dass in einem solchen Fall die *`defaultString`* zurückgegeben werden soll, sofern verfügbar. Daher wird Folgendes zurückgegeben, wenn diese Übersetzungszuordnung auf die Anfrage-`/is/image/myCat/myItem?req=&locale=ja` angewendet wird:

`val1=111 str1=Default1 val2=value2 str2= str3=Default3`

## Beispiele {#section-ae6ff7fb90754b839f04ed08aadffa3f}

**Sprachfamilien**

Jedem *`locale`* in der Übersetzungs-Map können mehrere *`locId`* Werte zugeordnet werden. Der Grund dafür ist, dass es die Unterstützung länder- oder regionsspezifischer Variationen (z. B. US-Englisch versus britisches Englisch) für ausgewählte *`stringElements`* ermöglicht, während die meisten Inhalte mit gängigen Basisgebietsschemata (z. B. internationales Englisch) verarbeitet werden.

Im Beispiel werden US-spezifisches Englisch ( `*`locId`* EUS`) und UK-spezifisches Englisch ( `*`locId`* EUK`) unterstützt, um die gelegentliche alternative Rechtschreibung zu unterstützen. Wenn es kein EUK oder EUS gibt, so fällt es auf E zurück. Ebenso könnten österreichische spezifische deutsche Varianten ( `DAT`) bei Bedarf zur Verfügung gestellt werden, während die meisten Zeit gemeinsame deutsche *`localizedStrings`* (mit `D` gekennzeichnet) zurückgegeben werden.

Die `attribute::LocaleStrMap` würde wie folgt aussehen:

`en,E|en_us,EUS,E|en_uk,EUK,E|de,D|de_at,DAT,D|de_de,D`

In der folgenden Tabelle wird die Ausgabe für einige repräsentative *`stringElement`*- und *`locale`* beschrieben:

<table id="table_A6B67587C5F44B5E9CD0E7ED29A81198"> 
 <thead> 
  <tr> 
   <th class="entry"> <i>stringElement</i> </th> 
   <th class="entry"> <i>locale</i> </th> 
   <th class="entry"> <p>Ausgabezeichenfolge </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> ^loc=E^Englisch^loc=D^Deutsch </span> </p> </td> 
   <td> <p> en, en_us, en_uk </p> <p> de, de_at, de_de </p> <p>Alle anderen </p> </td> 
   <td> <p>Englisch </p> <p>Deutsch </p> <p>- </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> ^loc=E^English^loc=UKE^UK-English^loc=D^German^loc=DAT^Österreichische </span> </p> </td> 
   <td> <p> en, en_us </p> <p> en_uk </p> <p> de, de_de </p> <p>de_at </p> <p>Alle anderen </p> </td> 
   <td> <p>Englisch </p> <p>Englisch (Vereinigtes Königreich) </p> <p>Deutsch </p> <p>Österreicherin </p> <p>- </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> ^ loc=en^English^loc=USE^US-English^loc=D^German^loc=DDE^Deutsch </span> </p> <p> In diesem Beispiel ist die <span class="varname"> locId </span> DDE nicht in <span class="codeph"> Attribut::LocaleStrMap </span> vorhanden, sodass die mit dieser <span class="varname"> locId-</span> verknüpfte Teilzeichenfolge nie zurückgegeben wird. </p> </td> 
   <td> <p> en, en_uk </p> <p> en_us </p> <p> de, de_at, de_de </p> <p>Alle anderen </p> </td> 
   <td> <p>Englisch </p> <p>US-Englisch </p> <p>Deutsch </p> <p>- </p> </td> 
  </tr> 
 </tbody> 
</table>
