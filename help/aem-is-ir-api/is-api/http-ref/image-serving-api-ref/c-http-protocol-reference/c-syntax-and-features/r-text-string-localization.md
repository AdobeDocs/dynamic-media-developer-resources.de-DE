---
title: Lokalisierung von Textzeichenfolgen
description: Bei der Lokalisierung von Textzeichenfolgen können Bildkataloge mehrere gebietsschemaspezifische Darstellungen für denselben Zeichenfolgenwert enthalten.
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

Bei der Lokalisierung von Textzeichenfolgen können Bildkataloge mehrere gebietsschemaspezifische Darstellungen für denselben Zeichenfolgenwert enthalten.

Der Server gibt dem Client die Darstellung zurück, die dem mit `locale=` angegebenen Gebietsschema entspricht. Dadurch wird eine clientseitige Lokalisierung vermieden und Anwendungen können die Gebietsschemata wechseln, indem sie einfach den entsprechenden `locale=` -Wert mit den IS-Textanforderungen senden.

## Anwendungsbereich {#section-a03f48e3bc0e4ab281909a2bd441a3c2}

Die Lokalisierung von Textzeichenfolgen wird auf alle Zeichenfolgenelemente angewendet, die das Lokalisierungstoken ` ^loc= *`locId`*^` in den folgenden Katalogfeldern enthalten:

<table id="table_83344EFCB5B5418184E0A0B43D0B23F7"> 
 <thead> 
  <tr> 
   <th class="entry"> <b>Katalogfeld</b> </th> 
   <th class="entry"> <b>String element in field</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> catalog::ImageSet </span> </p> </td> 
   <td> <p>Jedes Unterelement, das eine übersetzbare Zeichenfolge enthält (getrennt durch eine beliebige Kombination von Trennzeichen ',' ';' ':' und/oder das Start-/End-Element des Felds). </p> <p> Ein <span class="codeph"> 0xrggbb </span> -Farbwert am Anfang eines lokalisierbaren Felds wird aus der Lokalisierung ausgeschlossen und ohne Änderung weitergegeben. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalog::Map </span> </p> </td> 
   <td> <p>Ein- oder zweifacher Attributwert, mit Ausnahme der Werte der Attribute <span class="codeph"> coords= </span> und <span class="codeph"> shape= </span>. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalog::Targets </span> </p> </td> 
   <td> <p>Der Wert eines beliebigen <span class="codeph"> -Ziels.*.label </span> und <span class="codeph"> target.*.userdata </span> -Eigenschaft. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalog::UserData </span> </p> </td> 
   <td> <p>Der -Wert einer beliebigen Eigenschaft. </p> </td> 
  </tr> 
 </tbody> 
</table>

## String-Syntax {#section-d12320edf300409f8e17565b143acafc}

Lokalisierungsaktivierte *`string`* -Elemente im Bildkatalog bestehen aus einer oder mehreren lokalisierten Zeichenfolgen, denen jeweils ein Lokalisierungstoken vorangestellt wird.

<table id="simpletable_CEFDAE8395E6493E902D58A7E5A25BC7"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> stringElement </span> </span> </p> </td> 
  <td class="stentry"> <p>[ <span class="varname"> defaultString </span>]*{ <span class="varname"> localizationToken </span> <span class="varname"> localizedString </span>} </p> </td> 
 </tr> 
</table>

<table id="simpletable_0A687FA72C4C4C1AAFFCB43143C1AB3B"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> localizationToken </span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> ^loc= <span class="varname"> locStr </span> ^ </span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> locId </span> </span> </p> </td> 
  <td class="stentry"> <p>Interne Gebietsschema-ID für den <span class="varname"> localizedString </span> nach diesem <span class="varname"> localizationToken </span>. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> localizedString </span> </span> </p> </td> 
  <td class="stentry"> <p>Lokalisierte Zeichenfolge. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> defaultString </span> </span> </p> </td> 
  <td class="stentry"> <p>Zeichenfolge, die für unbekannte Gebietsschemata verwendet werden soll. </p> </td> 
 </tr> 
</table>

Das *`locId`* muss ASCII sein und darf kein &#39;^&#39; enthalten.

Das &quot;^&quot;kann an einer beliebigen Stelle in Unterzeichenfolgen mit oder ohne HTTP-Kodierung auftreten. Der Server stimmt mit dem gesamten Muster *`localizationToken`* `^loc=locId^` überein, um Unterzeichenfolgen zu trennen.

Die *`stringElements`*, die nicht mindestens ein *`localizationToken`* enthalten, werden bei der Lokalisierung nicht berücksichtigt.

## Die Übersetzungskarte {#section-f7ce3df91b724adf95cee44eac4915d4}

`attribute::LocaleStrMap` definiert die Regeln, die vom Server verwendet werden, um zu bestimmen, welche *`localizedStrings`* an den Client zurückgegeben werden soll. Sie besteht aus einer Liste mit Eingabe *`locales`* (entspricht den mit `locale=` angegebenen Werten), von denen jede keine oder mehrere interne Gebietsschema-IDs ( *`locId`*) aufweist. Beispiel:

`attribute::LocaleStrMap= en,E|nl,N|de,D|,`

Leere *`locId`* -Werte geben an, dass der *`defaultString`* zurückgegeben werden soll, sofern verfügbar.

Weitere Informationen finden Sie in der Beschreibung von `attribute::LocaleStrMap` .

## Der Übersetzungsprozess {#section-a2a8a3e5850f4f7c9d2318267afe98a2}

Bei der obigen beispielhaften Übersetzungszuordnung und der Anfrage &quot;`/is/image/myCat/myItem?req=&locale=nl`&quot; sucht der Server zuerst in der Gebietsschema-Zuordnung nach &quot;`nl`&quot;. Der übereinstimmende Eintrag `nl,N` gibt an, dass für jeden *`stringElement`* die mit `^loc=N^` markierten *`localizedString`* zurückgegeben werden sollen. Wenn dieser *`localizationToken`* nicht im *`stringElement`* vorhanden ist, wird ein leerer Wert zurückgegeben.

Angenommen, `catalog::UserData` für `myCat/myItem` enthält Folgendes (aus Gründen der Klarheit werden Zeilenumbrüche eingefügt):

`val1=111?? str1=Default1^loc=N^Dutch1^loc=D^German1?? val2=value2?? str2=^loc=E^English2^loc=N^Dutch2^loc=D^German2?? str3=Default3^loc=N^Dutch3^loc=D^German3`

Der Server gibt als Antwort auf die Beispielanfrage Folgendes zurück:

`val1=111 str1=Dutch1 val2=value2 str2=Dutch2 str3=Dutch3`

## Unbekannte Gebietsschemata {#section-26dfeefbd60345de94bbfeaaf7741223}

Im obigen Beispiel hat `attribute::LocaleStrMap` einen Eintrag mit einem leeren *`locale`* -Wert. Der Server verwendet diesen Eintrag für die Verarbeitung aller `locale=` -Werte, die sonst nicht explizit in der Übersetzungskarte angegeben sind.

Die beispielhafte Übersetzungszuordnung gibt an, dass in einem solchen Fall die *`defaultString`* zurückgegeben werden sollte, sofern verfügbar. Daher wird Folgendes zurückgegeben, wenn diese Übersetzungszuordnung auf die Anfrage `/is/image/myCat/myItem?req=&locale=ja` angewendet wird:

`val1=111 str1=Default1 val2=value2 str2= str3=Default3`

## Beispiele {#section-ae6ff7fb90754b839f04ed08aadffa3f}

**Sprachfamilien**

Mehrere *`locId`* -Werte können jedem *`locale`* in der Übersetzungszuordnung zugeordnet werden. Der Grund dafür ist, dass es die Unterstützung länderspezifischer oder regionsspezifischer Varianten (z. B. US-Englisch oder UK-Englisch) für die Auswahl von *`stringElements`* ermöglicht, während die meisten Inhalte mit gängigen Basisgebietsschemata (z. B. Internationales Englisch) verarbeitet werden.

Beispielsweise wird Unterstützung für US-spezifisches Englisch ( `*`locId`* EUS`) und britisches Englisch ( `*`locId`* EUK`) hinzugefügt, um die gelegentliche alternative Rechtschreibung zu unterstützen. Wenn EUK oder EUS nicht vorhanden ist, wird auf E zurückgegriffen. Ebenso können österreichisch-spezifische deutsche Varianten ( `DAT`) bei Bedarf zur Verfügung gestellt werden, während meist gebräuchliche deutsche *`localizedStrings`* (mit `D` markiert) zurückgegeben werden.

Der `attribute::LocaleStrMap` würde wie folgt aussehen:

`en,E|en_us,EUS,E|en_uk,EUK,E|de,D|de_at,DAT,D|de_de,D`

In der folgenden Tabelle wird die Ausgabe für einige repräsentative *`stringElement`* - und *`locale`* -Kombinationen beschrieben:

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
   <td> <p> <span class="codeph"> ^loc=E^English^loc=D^German </span> </p> </td> 
   <td> <p> en, en_us, en_uk </p> <p> de, de_at, de_de </p> <p>alle anderen </p> </td> 
   <td> <p>Englisch </p> <p>Deutsch </p> <p>- </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> ^loc=E^English^loc=UKE^UK-English^loc=D^German^loc=DAT^Austrian </span> </p> </td> 
   <td> <p> en, en_us </p> <p> en_uk </p> <p> de, de_de </p> <p>de_at </p> <p>alle anderen </p> </td> 
   <td> <p>Englisch </p> <p>UK-Englisch </p> <p>Deutsch </p> <p>österreichisch </p> <p>- </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> ^ loc=en^English^loc=USE^US-English^loc=D^German^loc=DDE^Deutsch </span> </p> <p> In diesem Beispiel ist das DDE <span class="varname"> locId </span> im Attribut <span class="codeph"> nicht vorhanden::LocaleStrMap </span> und daher wird die mit dieser <span class="varname"> locId </span> verknüpfte Unterzeichenfolge nie zurückgegeben. </p> </td> 
   <td> <p> en, en_uk </p> <p> en_us </p> <p> de, de_at, de_de </p> <p>alle anderen </p> </td> 
   <td> <p>Englisch </p> <p>US-Englisch </p> <p>Deutsch </p> <p>- </p> </td> 
  </tr> 
 </tbody> 
</table>
