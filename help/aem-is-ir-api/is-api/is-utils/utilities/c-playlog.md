---
description: Das Dienstprogramm „playlog“ kann verwendet werden, um Inhalte für den HTTP-Antwort-Cache vorab zu generieren.
solution: Experience Manager
title: Das Dienstprogramm „playlog“
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: e0213978-3a1d-44b4-82bf-4527b980b29e
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '422'
ht-degree: 0%

---

# Das Dienstprogramm „playlog“{#the-playlog-utility}

Das Dienstprogramm „playlog“ kann verwendet werden, um Inhalte für den HTTP-Antwort-Cache vorab zu generieren.

Der vorhandene Image Serving-HTTP-Antwort-Cache ist nach einem Hauptversions-Upgrade (wenn die erste oder zweite Ziffer der Versionsnummer geändert wird) nicht garantiert verwendbar. Wenn der Server nach dem Upgrade in den Volllastzustand versetzt werden soll, kann der Server durch die Verarbeitung der ersten Stunden mit Cache-Fehlanfragen überlastet werden, bis der Cache ausreichend gefüllt ist und die Cache-Trefferrate steigt.

Um diese anfängliche Lastspitze zu vermeiden, kann das `playlog`-Dienstprogramm verwendet werden, um Inhalte für den HTTP-Antwort-Cache vorab zu generieren. `playlog` extrahiert HTTP-Anfragen aus einer vorhandenen Zugriffsprotokolldatei und sendet sie an den Server, um Cache-Einträge zu generieren. In typischen Nutzungsszenarien reicht es aus, eine einzige Zugriffsprotokolldatei mit einem Traffic von einem ganzen Tag abzuspielen.

Zusätzlich zum Vorbereiten des HTTP-Antwort-Caches nach der Upgrade-Installation wird das Dienstprogramm auch verwendet, um Cache-Inhalte vorab zu generieren, wenn ein neuer Server zu einer Umgebung mit Lastenausgleich hinzugefügt wird; geben Sie einfach eine aktuelle Protokolldatei von einem der anderen Server wieder.

`playlog` kann so konfiguriert werden, dass die meisten Zugriffsprotokolldateien unterstützt werden, die von früheren Versionen von Image Serving generiert wurden.

## Nutzung {#section-daa126ec469b4a9d90d59def4fdaacdd}

` playlog *[!DNL logFile]* [-n *[!DNL col]*] [-s *[!DNL separator]*] [-m *[!DNL marker]*] [-p *[!DNL prefix]*] [-x *[!DNL suffix]*] [-v] [-h] [-r *[!DNL request method]*] [-o *[!DNL position]*]`

<table id="simpletable_39B9638BCB0F4244B5155C958C044C31"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -p <span class="varname"> Präfix </span> </span> </p> </td> 
  <td class="stentry"> <p>Stamm-URL, der die aus der Protokolldatei extrahierten Anfragen vorangestellt werden. </p> <p>Standard: <span class="filepath"> http://localhost:8080/is </span>) </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -n <span class="varname"> col </span> </span> </p> </td> 
  <td class="stentry"> <p>Feldnummer (Spalte), die die Anforderung im Protokolldatensatz enthält; 1-basiert. </p> <p>Standardwert: 16 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -s <span class="varname"> Trennzeichen </span> </span> </p> </td> 
  <td class="stentry"> <p>Feldtrennzeichen; Muster regulärer Ausdrücke. </p> <p>Standard: <span class="codeph"> [ ]+ </span>) </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -M <span class="varname"> Markierung </span> </span> </p> </td> 
  <td class="stentry"> <p>Anforderungsmarkierung; kennzeichnet Anforderungen in der Protokolldatei, die wiedergegeben werden sollen; Muster regulärer Ausdrücke. </p> <p>Standard: <span class="codeph"> Anfrage: </span>) </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -x <span class="varname"> Suffix </span> </span> </p> </td> 
  <td class="stentry"> <p>Suffix, der an die aus der Protokolldatei extrahierte Anfrage angehängt werden soll. Kann verwendet werden, um die wiedergegebenen Anforderungen von den Live-Anforderungen in den Protokolldateien zu trennen. Ein "?“ oder das Trennzeichen '&amp;' wird automatisch eingefügt. Das Suffix kann innerhalb geschweifter Klammern positionsbezogen auf jedes Protokollfeld verweisen. Standard entspricht dem MD5-Signaturfeld. </p> <p>Standard: <span class="codeph"> playlog={25} </span>) </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -v </span> </p> </td> 
  <td class="stentry"> <p>Im Verbose-Modus werden die generierten Anfrage-URLs in <span class="codeph"> stdout-</span> gedruckt. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -h </span> </p> </td> 
  <td class="stentry"> <p>Drucken Sie eine Zusammenfassung in <span class="codeph"> stdout-</span>. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -r </span> </p> </td> 
  <td class="stentry"> <p>request-method - Zu verwendende HTTP-Anfragemethode ( <span class="codeph"> get|post|head|smart </span>). </p> <p>Standard: <span class="codeph"> Smart </span>) </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -o </span> </p> </td> 
  <td class="stentry"> <p>request-method-pos - POS in der Protokolldatei zum Abrufen der ursprünglichen Methode von. </p> <p>Standardwert: 15 </p> </td> 
 </tr> 
</table>

Unter Windows lautet der Dateiname [!DNL playlog.bat] und unter Linux [!DNL playlog.sh].

## Beispiele {#section-716e5c35e9fa4ee3a4b0687381fcea40}

Im folgenden Beispiel werden alle Anfragen aus einer Zugriffsprotokolldatei wiedergegeben, die von Image Serving unter Linux erstellt wurde:

`> cd /usr/local/Scene7/ImageServing/logs`

`> ../bin/playlog.sh access-2007-01-01.log -n 18 -s ' ' -m . -p http://localhost:8080`

Mit dem folgenden Befehl werden alle Anforderungen wiedergegeben, die in einer von Image Serving unter Windows erstellten Trace-Protokolldatei enthalten sind:

`> "\Program Files\Scene7\ImageServing\bin\playlog.bat" d:\logs/access-2006-09-01.log`
