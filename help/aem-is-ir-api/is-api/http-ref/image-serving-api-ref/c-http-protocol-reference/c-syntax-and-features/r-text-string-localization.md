---
title: Lokalisierung von Textzeichenfolgen
description: Bei der Lokalisierung von Textzeichenfolgen können Bildkataloge mehrere gebietsschemaspezifische Darstellungen für denselben Zeichenfolgenwert enthalten.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: f105c7f2-b544-4c08-bb91-4916e485572d
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '669'
ht-degree: 3%

---

# Lokalisierung von Textzeichenfolgen{#text-string-localization}

Bei der Lokalisierung von Textzeichenfolgen können Bildkataloge mehrere gebietsschemaspezifische Darstellungen für denselben Zeichenfolgenwert enthalten.

Der Server gibt an den Client die Darstellung zurück, die dem Gebietsschema entspricht, mit dem `locale=`, wodurch eine clientseitige Lokalisierung vermieden und Anwendungen zum Wechseln der Gebietsschemata einfach durch Senden der entsprechenden `locale=` -Wert mit den IS-Textanfragen.

## Anwendungsbereich {#section-a03f48e3bc0e4ab281909a2bd441a3c2}

Die Lokalisierung von Textzeichenfolgen wird auf alle Zeichenfolgenelemente angewendet, die das Lokalisierungstoken enthalten ` ^loc= *`locId`*^` in den folgenden Katalogfeldern:

<table id="table_83344EFCB5B5418184E0A0B43D0B23F7"> 
 <thead> 
  <tr> 
   <th class="entry"> <b>Katalogfeld</b> </th> 
   <th class="entry"> <b>Zeichenfolgenelement im Feld</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> catalog::ImageSet </span> </p> </td> 
   <td> <p>Jedes Unterelement, das eine übersetzbare Zeichenfolge enthält (getrennt durch eine beliebige Kombination von Trennzeichen ',' ';' ':' und/oder das Start-/End-Element des Felds). </p> <p> A <span class="codeph"> 0xrggbb </span> Farbwert am Anfang eines lokalisierbaren Felds wird aus der Lokalisierung ausgeschlossen und ohne Änderung weitergegeben. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> Katalog::Map </span> </p> </td> 
   <td> <p>Jeder beliebige ein- oder doppelte Anführungszeichen-Attributwert, mit Ausnahme der Werte der Variablen <span class="codeph"> coords= </span> und <span class="codeph"> shape= </span> -Attribute. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalog:Targets </span> </p> </td> 
   <td> <p>Der Wert eines <span class="codeph"> Zielgruppe.*.label </span> und <span class="codeph"> Zielgruppe.*.userdata </span> -Eigenschaft. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalog::UserData </span> </p> </td> 
   <td> <p>Der -Wert einer beliebigen Eigenschaft. </p> </td> 
  </tr> 
 </tbody> 
</table>

## String-Syntax {#section-d12320edf300409f8e17565b143acafc}

Lokalisierungsaktivierung *`string`* -Elemente im Bildkatalog bestehen aus einer oder mehreren lokalisierten Zeichenfolgen, denen jeweils ein Lokalisierungstoken vorangestellt ist.

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
  <td class="stentry"> <p>Interne Gebietsschema-ID für die <span class="varname"> localizedString </span> folgt diesem <span class="varname"> localizationToken </span>. </p> </td> 
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

Die *`locId`* muss ASCII sein und darf &quot;^&quot;nicht enthalten.

Das &quot;^&quot;kann an einer beliebigen Stelle in Unterzeichenfolgen mit oder ohne HTTP-Kodierung auftreten. Der Server stimmt mit dem gesamten *`localizationToken`* `^loc=locId^` Muster zum Trennen von Unterzeichenfolgen.

Die *`stringElements`*, die nicht mindestens ein *`localizationToken`*, werden bei der Lokalisierung nicht berücksichtigt.

## Die Übersetzungskarte {#section-f7ce3df91b724adf95cee44eac4915d4}

`attribute::LocaleStrMap` definiert die Regeln, die vom Server verwendet werden, um zu bestimmen, *`localizedStrings`* zum Client zurück. Sie besteht aus einer Liste von Eingaben *`locales`* (entspricht den Werten, die mit `locale=`), jede mit keiner oder mehreren internen Gebietsschema-IDs ( *`locId`*). Beispiel:

`attribute::LocaleStrMap= en,E|nl,N|de,D|,`

Empty *`locId`* -Werte zeigen an, dass *`defaultString`* zurückgegeben werden, falls verfügbar.

Siehe Beschreibung von `attribute::LocaleStrMap` für Details.

## Der Übersetzungsprozess {#section-a2a8a3e5850f4f7c9d2318267afe98a2}

Bei der obigen beispielhaften Übersetzungszuordnung und der Anfrage `/is/image/myCat/myItem?req=&locale=nl`sucht der Server zuerst nach &quot; `nl`&quot;in der Gebietsschema-Zuordnung. Der übereinstimmende Eintrag `nl,N` gibt an, dass *`stringElement`*, die *`localizedString`* markiert mit `^loc=N^` zurückgegeben werden. Wenn dies *`localizationToken`* nicht im *`stringElement`*, wird ein leerer Wert zurückgegeben.

Sagen wir mal: `catalog::UserData` für `myCat/myItem` enthält Folgendes (aus Gründen der Klarheit eingefügte Zeilenumbrüche):

`val1=111?? str1=Default1^loc=N^Dutch1^loc=D^German1?? val2=value2?? str2=^loc=E^English2^loc=N^Dutch2^loc=D^German2?? str3=Default3^loc=N^Dutch3^loc=D^German3`

Der Server gibt als Antwort auf die Beispielanfrage Folgendes zurück:

`val1=111 str1=Dutch1 val2=value2 str2=Dutch2 str3=Dutch3`

## Unbekannte Gebietsschemata {#section-26dfeefbd60345de94bbfeaaf7741223}

Im obigen Beispiel `attribute::LocaleStrMap` einen Eintrag mit einer leeren *`locale`* -Wert. Der Server verwendet diesen Eintrag, um alle `locale=` Werte, die nicht explizit in der Übersetzungskarte angegeben sind.

Die beispielhafte Übersetzungszuordnung gibt an, dass in diesem Fall die *`defaultString`* zurückgegeben werden, falls verfügbar. Daher wird Folgendes zurückgegeben, wenn diese Übersetzungszuordnung auf die Anfrage angewendet wird `/is/image/myCat/myItem?req=&locale=ja`:

`val1=111 str1=Default1 val2=value2 str2= str3=Default3`

## Beispiele {#section-ae6ff7fb90754b839f04ed08aadffa3f}

**Sprachfamilien**

Mehrere *`locId`* -Werte mit jedem *`locale`* in der Übersetzungskarte. Der Grund dafür ist, dass es ermöglicht, länderspezifische oder regionsspezifische Varianten (z. B. US-Englisch oder UK-Englisch) für die Auswahl von *`stringElements`* bei der Handhabung der meisten Inhalte mit gängigen Basisgebietsschemas (z. B. Internationales Englisch).

Beispielsweise wird Unterstützung für US-spezifisches Englisch ( `*`locId`* EUS`) und britisch-spezifisches Englisch ( `*`locId`* EUK`), um die gelegentliche alternative Rechtschreibung zu unterstützen. Existiert EUK oder EUS nicht, so wird auf E zurückgegriffen. Ebenso werden österreichisch-spezifische deutsche Varianten ( `DAT`) bei Bedarf zur Verfügung gestellt werden, während das gemeinsame Deutsch zurückgegeben wird *`localizedStrings`* (markiert mit `D`) meistens.

Die `attribute::LocaleStrMap` würde wie folgt aussehen:

`en,E|en_us,EUS,E|en_uk,EUK,E|de,D|de_at,DAT,D|de_de,D`

In der folgenden Tabelle wird die Ausgabe für einige Vertreter beschrieben. *`stringElement`* und *`locale`* Kombinationen:

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
   <td> <p> en,en_us, en_uk </p> <p> de, de_at, de_de </p> <p>alle anderen </p> </td> 
   <td> <p>Englisch </p> <p>Deutsch </p> <p>- </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> ^loc=E^English^loc=UKE^UK^English^loc=D^German^loc=DAT^Austrian </span> </p> </td> 
   <td> <p> en, en_us </p> <p> en_uk </p> <p> de, de_de </p> <p>de_at </p> <p>alle anderen </p> </td> 
   <td> <p>Englisch </p> <p>UK-Englisch </p> <p>Deutsch </p> <p>österreichisch </p> <p>- </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> ^ loc=en^English^loc=USE^US-English^loc=D^German^loc=DDE^Deutsch </span> </p> <p> In diesem Beispiel wird die Variable <span class="varname"> locId </span> DDE ist nicht in vorhanden <span class="codeph"> attribute::LocaleStrMap </span>und somit die mit diesem verknüpfte Unterzeichenfolge <span class="varname"> locId </span> wird nie zurückgegeben. </p> </td> 
   <td> <p> en, en_uk </p> <p> en_us </p> <p> de, de_at, de_de </p> <p>alle anderen </p> </td> 
   <td> <p>Englisch </p> <p>US-Englisch </p> <p>Deutsch </p> <p>- </p> </td> 
  </tr> 
 </tbody> 
</table>
