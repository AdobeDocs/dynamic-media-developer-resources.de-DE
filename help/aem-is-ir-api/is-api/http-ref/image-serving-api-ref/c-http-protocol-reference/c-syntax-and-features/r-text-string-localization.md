---
description: Bei der lokale Anpassung von Textzeichenfolgen können Bildkataloge mehrere Gebietsschema-spezifische Darstellungen für denselben Zeichenfolgenwert enthalten.
seo-description: Bei der lokale Anpassung von Textzeichenfolgen können Bildkataloge mehrere Gebietsschema-spezifische Darstellungen für denselben Zeichenfolgenwert enthalten.
seo-title: Lokale Anpassung von Textzeichenfolgen
solution: Experience Manager
title: Lokale Anpassung von Textzeichenfolgen
topic: Dynamic Media Image Serving - Image Rendering API
uuid: bdff2403-e3bb-4b3f-a8d7-bb108c1fbee8
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '685'
ht-degree: 3%

---


# Textzeichenfolgen-lokale Anpassung{#text-string-localization}

Bei der lokale Anpassung von Textzeichenfolgen können Bildkataloge mehrere Gebietsschema-spezifische Darstellungen für denselben Zeichenfolgenwert enthalten.

Der Server gibt an den Client die Darstellung zurück, die mit dem mit `locale=` angegebenen Gebietsschema übereinstimmt. Dadurch wird eine clientseitige lokale Anpassung vermieden und es Anwendungen ermöglicht, Gebietsschemata zu wechseln, indem einfach der entsprechende `locale=`-Wert mit den IS-Textanforderungen gesendet wird.

## Ebene {#section-a03f48e3bc0e4ab281909a2bd441a3c2}

Die lokale Anpassung der Textzeichenfolge wird auf alle Zeichenfolgenelemente angewendet, die das lokale Anpassungen-Token ` ^loc= *`locId`*^` in den folgenden Katalogfeldern enthalten:

<table id="table_83344EFCB5B5418184E0A0B43D0B23F7"> 
 <thead> 
  <tr> 
   <th class="entry"> <b>Katalogfeld</b> </th> 
   <th class="entry"> <b>String-Element im Feld</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> Katalog::ImageSet  </span> </p> </td> 
   <td> <p>Jedes Unterelement, das eine übersetzbare Zeichenfolge enthält (durch eine beliebige Kombination von Trennzeichen ',' ';' ':' und/oder den Beginn/das Feldende getrennt). </p> <p> Ein <span class="codeph"> 0xrggbb </span>-Farbwert am Anfang eines lokalisierbaren Felds wird von der lokale Anpassung ausgeschlossen und ohne Änderung weitergegeben. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> Katalog::Map  </span> </p> </td> 
   <td> <p>Ein beliebiger Attributwert mit einem oder mehreren Dubletten, mit Ausnahme der Werte der Attribute <span class="codeph"> coords= </span> und <span class="codeph"> shape= </span>. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> Katalog: Zielgruppen  </span> </p> </td> 
   <td> <p>Der Wert einer beliebigen <span class="codeph">-Zielgruppe.*.label </span> und <span class="codeph"> Zielgruppe.*.userdata </span>-Eigenschaft. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> Katalog::UserData  </span> </p> </td> 
   <td> <p>Der Wert einer beliebigen Eigenschaft. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Zeichenfolgensyntax {#section-d12320edf300409f8e17565b143acafc}

*`string`*-lokale Anpassungen im Bildkatalog bestehen aus einer oder mehreren lokalisierten Zeichenfolgen, denen jeweils ein lokale Anpassungen-Token vorangestellt wird.

<table id="simpletable_CEFDAE8395E6493E902D58A7E5A25BC7"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> stringElement  </span> </span> </p> </td> 
  <td class="stentry"> <p>[ <span class="varname"> defaultString </span>]*{ <span class="varname"> localizationToken </span> <span class="varname"> localizedString </span>} </p> </td> 
 </tr> 
</table>

<table id="simpletable_0A687FA72C4C4C1AAFFCB43143C1AB3B"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> localizationToken  </span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> ^ loc=  <span class="varname"> locStr  </span> ^  </span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> locId  </span> </span> </p> </td> 
  <td class="stentry"> <p>Interne Gebietsschema-ID für <span class="varname"> localizedString </span> nach diesem <span class="varname"> localizationToken </span>. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> localizedString  </span> </span> </p> </td> 
  <td class="stentry"> <p>Lokalisierte Zeichenfolge. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> defaultString  </span> </span> </p> </td> 
  <td class="stentry"> <p>Für unbekannte Gebietsschemata zu verwendende Zeichenfolge. </p> </td> 
 </tr> 
</table>

*`locId`* muss ASCII sein und darf kein &#39;^&#39; enthalten.

&#39;^&#39; kann an einer beliebigen Stelle in Unterzeichenfolgen mit oder ohne HTTP-Kodierung auftreten. Der Server stimmt mit dem gesamten *`localizationToken`* `^loc=locId^`-Muster überein, um Unterzeichenfolgen zu trennen.

*`stringElements`* die nicht mindestens einen enthalten,  *`localizationToken`* werden für die lokale Anpassung nicht berücksichtigt.

## Die Übersetzungszuordnung {#section-f7ce3df91b724adf95cee44eac4915d4}

`attribute::LocaleStrMap` definiert die Regeln, die vom Server verwendet werden, um zu bestimmen, welche an den Client zurückgegeben  *`localizedStrings`* werden. Es besteht aus einer Liste von input *`locales`* (Übereinstimmung mit den Werten, die mit `locale=` angegeben werden), wobei jede Eingabe keine oder mehrere interne Gebietsschema-IDs ( *`locId`*) enthält. Beispiel:

`attribute::LocaleStrMap= en,E|nl,N|de,D|,`

Leere *`locId`*-Werte geben an, dass *`defaultString`* zurückgegeben werden soll, falls verfügbar.

Weitere Informationen finden Sie in der Beschreibung von `attribute::LocaleStrMap`.

## Der Übersetzungsprozess {#section-a2a8a3e5850f4f7c9d2318267afe98a2}

Bei der obigen Beispielübersetzungszuordnung und der Anforderung `/is/image/myCat/myItem?req=&locale=nl` sucht der Server zuerst in der Gebietsschemakarte nach &quot;`nl`&quot;. Der übereinstimmende Eintrag `nl,N` gibt an, dass für jedes *`stringElement`* das *`localizedString`*, das mit `^loc=N^` gekennzeichnet ist, zurückgegeben werden soll. Wenn *`localizationToken`* nicht im *`stringElement`* vorhanden ist, wird ein leerer Wert zurückgegeben.

Beispiel: `catalog::UserData` für `myCat/myItem` enthält Folgendes (aus Gründen der Klarheit eingefügte Zeilenumbrüche):

`val1=111?? str1=Default1^loc=N^Dutch1^loc=D^German1?? val2=value2?? str2=^loc=E^English2^loc=N^Dutch2^loc=D^German2?? str3=Default3^loc=N^Dutch3^loc=D^German3`

Der Server gibt als Antwort auf unsere Beispielanforderung Folgendes zurück:

`val1=111 str1=Dutch1 val2=value2 str2=Dutch2 str3=Dutch3`

## Unbekannte Gebietsschemata {#section-26dfeefbd60345de94bbfeaaf7741223}

Im obigen Beispiel hat `attribute::LocaleStrMap` einen Eintrag mit einem leeren *`locale`*-Wert. Der Server verwendet diesen Eintrag, um alle `locale=`-Werte zu verarbeiten, die sonst in der Übersetzungszuordnung nicht explizit angegeben sind.

In der Übersetzungskarte für das Beispiel wird angegeben, dass in diesem Fall *`defaultString`* zurückgegeben werden soll, wenn verfügbar. Daher würde Folgendes zurückgegeben, wenn diese Übersetzungszuordnung auf die Anforderung `/is/image/myCat/myItem?req=&locale=ja` angewendet würde:

`val1=111 str1=Default1 val2=value2 str2= str3=Default3`

## Beispiele {#section-ae6ff7fb90754b839f04ed08aadffa3f}

**Sprachfamilien**

Mehrere *`locId`*-Werte können mit jedem *`locale`* in der Übersetzungszuordnung verknüpft werden. Dies ermöglicht die Unterstützung länderspezifischer oder regionsspezifischer Variationen (z.B. Englisch in den USA oder Englisch in Großbritannien) für die Auswahl von *`stringElements`*, während die meisten Inhalte mit gängigen Basisgebietsschemata (z.B. internationales Englisch) verarbeitet werden.

In unserem Beispiel möchten wir Unterstützung für US-spezifisches Englisch ( `*`locId`* EUS`) und für britisches Englisch ( `*`locId`* EUK`) hinzufügen, um die gelegentliche alternative Schreibweise zu unterstützen. Wenn es EUK oder EUS nicht gibt, würden wir auf E zurückgreifen. Auch österreichisch-spezifische deutsche Varianten ( `DAT`) könnten bei Bedarf zur Verfügung gestellt werden, während häufig gebräuchliches Deutsch *`localizedStrings`* (gekennzeichnet mit `D`) zurückgegeben wird.

`attribute::LocaleStrMap` würde wie folgt aussehen:

`en,E|en_us,EUS,E|en_uk,EUK,E|de,D|de_at,DAT,D|de_de,D`

Die folgende Tabelle beschreibt die Ausgabe für einige repräsentative Kombinationen *`stringElement`* und *`locale`*:

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
   <td> <p> <span class="codeph"> ^loc=E^English^loc=UKE^UK-English^loc=D^German^loc=DAT^Austrian  </span> </p> </td> 
   <td> <p> en, en_us </p> <p> en_uk </p> <p> de, de_de </p> <p>de_at </p> <p>alle anderen </p> </td> 
   <td> <p>Englisch </p> <p>UK-Englisch </p> <p>Deutsch </p> <p>österreichisch </p> <p>- </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> ^ loc=en^English^loc=USE^DE-English^loc=D^German^loc=DDE^Deutsch  </span> </p> <p> Beachten Sie, dass in diesem Beispiel das <span class="varname"> locId </span>-DDE in <span class="codeph">-Attribut::LocaleStrMap </span> nicht vorhanden ist und daher die mit dieser <span class="varname"> locId </span> verknüpfte Unterzeichenfolge nie zurückgegeben wird. </p> </td> 
   <td> <p> en, en_uk </p> <p> en_us </p> <p> de, de_at, de_de </p> <p>alle anderen </p> </td> 
   <td> <p>Englisch </p> <p>US-Englisch </p> <p>Deutsch </p> <p>- </p> </td> 
  </tr> 
 </tbody> 
</table>

