---
description: Bei der Lokalisierung von Textzeichenfolgen können Bildkataloge mehrere gebietsschemaspezifische Darstellungen für denselben Zeichenfolgenwert enthalten.
solution: Experience Manager
title: Lokalisierung von Textzeichenfolgen
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: f105c7f2-b544-4c08-bb91-4916e485572d
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '671'
ht-degree: 3%

---

# Lokalisierung von Textzeichenfolgen{#text-string-localization}

Bei der Lokalisierung von Textzeichenfolgen können Bildkataloge mehrere gebietsschemaspezifische Darstellungen für denselben Zeichenfolgenwert enthalten.

Der Server gibt an den Client die Darstellung zurück, die dem mit `locale=` angegebenen Gebietsschema entspricht. Dadurch wird eine clientseitige Lokalisierung vermieden und Anwendungen können die Gebietsschemata wechseln, indem sie einfach den entsprechenden `locale=` -Wert mit den IS-Textanforderungen senden.

## Ebene {#section-a03f48e3bc0e4ab281909a2bd441a3c2}

Die Lokalisierung von Textzeichenfolgen wird auf alle Zeichenfolgenelemente angewendet, die das Lokalisierungstoken ` ^loc= *`locId`*^` in den folgenden Katalogfeldern enthalten:

<table id="table_83344EFCB5B5418184E0A0B43D0B23F7"> 
 <thead> 
  <tr> 
   <th class="entry"> <b>Katalogfeld</b> </th> 
   <th class="entry"> <b>Zeichenfolgenelement im Feld</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> catalog::ImageSet  </span> </p> </td> 
   <td> <p>Jedes Unterelement, das eine übersetzbare Zeichenfolge enthält (getrennt durch eine beliebige Kombination der Trennzeichen ',' ';' ':' und/oder den Beginn/das Ende des Felds). </p> <p> Ein <span class="codeph"> 0xrggbb </span>-Farbwert am Anfang eines lokalisierbaren Felds wird aus der Lokalisierung ausgeschlossen und ohne Änderung weitergegeben. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> Katalog::Map  </span> </p> </td> 
   <td> <p>Ein- oder zweifacher Attributwert, ausgenommen die Werte der Attribute <span class="codeph"> coords= </span> und <span class="codeph"> shape= </span>. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalog:Targets  </span> </p> </td> 
   <td> <p>Der Wert eines beliebigen <span class="codeph">-Ziels.*.label </span> und <span class="codeph"> target.*.userdata </span> -Eigenschaft. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalog::UserData  </span> </p> </td> 
   <td> <p>Der -Wert einer beliebigen Eigenschaft. </p> </td> 
  </tr> 
 </tbody> 
</table>

## String-Syntax {#section-d12320edf300409f8e17565b143acafc}

Lokalisierungsaktivierte *`string`* -Elemente im Bildkatalog bestehen aus einer oder mehreren lokalisierten Zeichenfolgen, denen jeweils ein Lokalisierungstoken vorangestellt wird.

<table id="simpletable_CEFDAE8395E6493E902D58A7E5A25BC7"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> stringElement  </span> </span> </p> </td> 
  <td class="stentry"> <p>[ <span class="varname"> defaultString </span>]*{ <span class="varname"> localizationToken </span> <span class="varname"> localizedString </span>} </p> </td> 
 </tr> 
</table>

<table id="simpletable_0A687FA72C4C4C1AAFFCB43143C1AB3B"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> localizationToken  </span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> ^loc=  <span class="varname"> locStr  </span> ^  </span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> locId  </span> </span> </p> </td> 
  <td class="stentry"> <p>Interne Gebietsschema-ID für <span class="varname"> localizedString </span> nach <span class="varname"> localizationToken </span>. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> localizedString  </span> </span> </p> </td> 
  <td class="stentry"> <p>Lokalisierte Zeichenfolge. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> defaultString  </span> </span> </p> </td> 
  <td class="stentry"> <p>Zeichenfolge, die für unbekannte Gebietsschemata verwendet werden soll. </p> </td> 
 </tr> 
</table>

*`locId`* muss ASCII sein und darf &quot;^&quot;nicht enthalten.

&#39;^&#39; kann an einer beliebigen Stelle in Unterzeichenfolgen mit oder ohne HTTP-Kodierung auftreten. Der Server passt das gesamte *`localizationToken`* `^loc=locId^`-Muster an, um Unterzeichenfolgen zu trennen.

*`stringElements`* die nicht mindestens eine enthalten,  *`localizationToken`* werden bei der Lokalisierung nicht berücksichtigt.

## Die Übersetzungskarte {#section-f7ce3df91b724adf95cee44eac4915d4}

`attribute::LocaleStrMap` definiert die Regeln, die vom Server verwendet werden, um zu bestimmen, welche  *`localizedStrings`* an den Client zurückgegeben werden. Sie besteht aus einer Liste von Eingabe *`locales`* (entspricht den mit `locale=` angegebenen Werten) mit jeweils keiner oder mehreren internen Gebietsschema-IDs ( *`locId`*). Beispiel:

`attribute::LocaleStrMap= en,E|nl,N|de,D|,`

Leere *`locId`* -Werte geben an, dass *`defaultString`* zurückgegeben werden soll, sofern verfügbar.

Weitere Informationen finden Sie in der Beschreibung von `attribute::LocaleStrMap` .

## Der Übersetzungsprozess {#section-a2a8a3e5850f4f7c9d2318267afe98a2}

Bei der obigen beispielhaften Übersetzungszuordnung und der Anfrage `/is/image/myCat/myItem?req=&locale=nl` sucht der Server zuerst in der Gebietsschemakarte nach &quot;`nl`&quot;. Der übereinstimmende Eintrag `nl,N` gibt an, dass für jeden *`stringElement`* der *`localizedString`* zurückgegeben werden soll, der mit `^loc=N^` markiert ist. Wenn *`localizationToken`* nicht im *`stringElement`* vorhanden ist, wird ein leerer Wert zurückgegeben.

Nehmen wir an, `catalog::UserData` für `myCat/myItem` enthält Folgendes (aus Gründen der Klarheit eingefügte Zeilenumbrüche):

`val1=111?? str1=Default1^loc=N^Dutch1^loc=D^German1?? val2=value2?? str2=^loc=E^English2^loc=N^Dutch2^loc=D^German2?? str3=Default3^loc=N^Dutch3^loc=D^German3`

Der Server gibt als Antwort auf unsere Beispielanfrage Folgendes zurück:

`val1=111 str1=Dutch1 val2=value2 str2=Dutch2 str3=Dutch3`

## Unbekannte Gebietsschemata {#section-26dfeefbd60345de94bbfeaaf7741223}

Im obigen Beispiel hat `attribute::LocaleStrMap` einen Eintrag mit einem leeren *`locale`* -Wert. Der Server verwendet diesen Eintrag, um alle `locale=`-Werte zu verarbeiten, die sonst nicht explizit in der Übersetzungskarte angegeben sind.

Die Beispielübersetzungszuordnung gibt an, dass in diesem Fall *`defaultString`* zurückgegeben werden sollte, sofern verfügbar. Daher wird Folgendes zurückgegeben, wenn diese Übersetzungszuordnung auf die Anfrage `/is/image/myCat/myItem?req=&locale=ja` angewendet wurde:

`val1=111 str1=Default1 val2=value2 str2= str3=Default3`

## Beispiele {#section-ae6ff7fb90754b839f04ed08aadffa3f}

**Sprachfamilien**

Mehrere *`locId`* -Werte können jedem *`locale`* in der Übersetzungszuordnung zugeordnet werden. Dies ermöglicht die Unterstützung länderspezifischer oder regionsspezifischer Varianten (z. B. US-Englisch vs. britisches Englisch) für die Auswahl von *`stringElements`*, während die meisten Inhalte mit gängigen Basisgebietsschemata (z. B. internationales Englisch) verarbeitet werden.

Für unser Beispiel möchten wir Unterstützung für US-spezifisches Englisch ( `*`locId`* EUS`) und britisches Englisch ( `*`locId`* EUK`) hinzufügen, um die gelegentliche alternative Rechtschreibung zu unterstützen. Wenn es EUK oder EUS nicht gibt, würden wir auf E zurückgreifen. Ebenso könnten österreichisch-spezifische deutsche Varianten ( `DAT`) bei Bedarf zur Verfügung gestellt werden, während häufig gebräuchliches Deutsch *`localizedStrings`* zurückgegeben wird (markiert mit `D`).

`attribute::LocaleStrMap` würde wie folgt aussehen:

`en,E|en_us,EUS,E|en_uk,EUK,E|de,D|de_at,DAT,D|de_de,D`

Die folgende Tabelle beschreibt die Ausgabe einiger repräsentativer *`stringElement`*- und *`locale`*-Kombinationen:

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
   <td> <p> <span class="codeph"> ^loc=E^English^loc=D^German  </span> </p> </td> 
   <td> <p> en,en_us, en_uk </p> <p> de, de_at, de_de </p> <p>alle anderen </p> </td> 
   <td> <p>Englisch </p> <p>Deutsch </p> <p>- </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> ^loc=E^English^loc=UKE^UK^English^loc=D^German^loc=DAT^Austrian  </span> </p> </td> 
   <td> <p> en, en_us </p> <p> en_uk </p> <p> de, de_de </p> <p>de_at </p> <p>alle anderen </p> </td> 
   <td> <p>Englisch </p> <p>UK-Englisch </p> <p>Deutsch </p> <p>österreichisch </p> <p>- </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> ^ loc=en^English^loc=USE^US-English^loc=D^German^loc=DDE^Deutsch  </span> </p> <p> Beachten Sie, dass für dieses Beispiel das <span class="varname"> locId </span>-DDE im <span class="codeph">-Attribut nicht vorhanden ist::LocaleStrMap </span> und daher die mit dieser <span class="varname"> locId </span> verknüpfte Unterzeichenfolge nie zurückgegeben wird. </p> </td> 
   <td> <p> en, en_uk </p> <p> en_us </p> <p> de, de_at, de_de </p> <p>alle anderen </p> </td> 
   <td> <p>Englisch </p> <p>US-Englisch </p> <p>Deutsch </p> <p>- </p> </td> 
  </tr> 
 </tbody> 
</table>
