---
description: Das Dienstprogramm "playlog"kann verwendet werden, um Inhalte für den HTTP-Antwort-Cache vorzugenerieren.
seo-description: Das Dienstprogramm "playlog"kann verwendet werden, um Inhalte für den HTTP-Antwort-Cache vorzugenerieren.
seo-title: Das Dienstprogramm "playlog"
solution: Experience Manager
title: Das Dienstprogramm "playlog"
topic: Scene7 Image Serving - Image Rendering API
uuid: 9044515e-7cfb-4e86-9ac4-e071b60f38d1
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '438'
ht-degree: 1%

---


# Das Dienstprogramm &#39;playlog&#39;{#the-playlog-utility}

Das Dienstprogramm &quot;playlog&quot;kann verwendet werden, um Inhalte für den HTTP-Antwort-Cache vorzugenerieren.

Der vorhandene Image Serving-HTTP-Antwort-Cache ist nach einer Aktualisierung der Hauptversion nicht mehr nutzbar (wenn die erste oder zweite Ziffer der Versionsnummer geändert wurde). Wenn der Server nach der Aktualisierung live in Vollladeregel übertragen werden soll, wird der Server möglicherweise überlastet und die ersten Stunden nach fehlenden Cache-Anforderungen übergeben, bis der Cache ausreichend gefüllt ist und die Cache-Trefferrate steigt.

Um diese anfängliche Ladespitze zu vermeiden, kann das `playlog`-Dienstprogramm verwendet werden, um Inhalte für den HTTP-Antwort-Cache vorzugenerieren. `playlog` extrahiert HTTP-Anforderungen aus einer vorhandenen Zugriffsprotokolldatei und sendet diese an den Server, um Cache-Einträge zu generieren. Für typische Verwendungsszenarien reicht es aus, eine einzelne Zugriffsprotokolldatei wiederzugeben, die den Traffic für einen ganzen Tag enthält.

Neben dem Hochladen des HTTP-Antwort-Cache nach der Installation der Aktualisierung wird das Dienstprogramm auch verwendet, um Cache-Inhalte vorzugenerieren, wenn einer Umgebung mit Lastenausgleich ein neuer Server hinzugefügt wird. einfach eine aktuelle Protokolldatei von einem der anderen Server wiedergeben.

`playlog` kann so konfiguriert werden, dass die meisten Zugriffsprotokolldateien unterstützt werden, die von früheren Versionen von Image Serving generiert wurden.

## Nutzung {#section-daa126ec469b4a9d90d59def4fdaacdd}

` playlog *[!DNL logFile]* [-n *[!DNL col]*] [-s *[!DNL separator]*] [-m *[!DNL marker]*] [-p *[!DNL prefix]*] [-x *[!DNL suffix]*] [-v] [-h] [-r *[!DNL request method]*] [-o *[!DNL position]*]`

<table id="simpletable_39B9638BCB0F4244B5155C958C044C31"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -p- <span class="varname"> Präfix  </span> </span> </p> </td> 
  <td class="stentry"> <p>Stamm-URL, der den aus der Protokolldatei extrahierten Anforderungen vorangestellt werden soll. </p> <p>Standard: <span class="filepath"> http://localhost:8080/is </span>) </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -n  <span class="varname"> col  </span> </span> </p> </td> 
  <td class="stentry"> <p>Feld (Spalte) Nummer, die die Anforderung im Protokolldatensatz enthält; 1-basiert. </p> <p>Standard: 16 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -s  <span class="varname"> Trennzeichen  </span> </span> </p> </td> 
  <td class="stentry"> <p>Feldtrennzeichen; reguläres Ausdruck. </p> <p>Standard: <span class="codeph"> [ ]+ </span>) </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -m  <span class="varname"> Marker  </span> </span> </p> </td> 
  <td class="stentry"> <p>Anforderungsmarkierung; identifiziert Anforderungen in der Protokolldatei, die wiedergegeben werden sollen; reguläres Ausdruck. </p> <p>Standard: <span class="codeph"> Anforderung: </span>) </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -x  <span class="varname"> Suffix  </span> </span> </p> </td> 
  <td class="stentry"> <p>Suffix, das an die aus der Protokolldatei extrahierte Anforderung angehängt wird; kann verwendet werden, um wiedergegebene Anfragen von Live-Anfragen in den Protokolldateien zu trennen; a '?' oder das Trennzeichen "&amp;"automatisch eingefügt wird; suffix kann jedes Protokollfeld nach Position innerhalb geschweifter Klammern referenzieren, Standard entspricht dem md5-Signaturfeld. </p> <p>Standard: <span class="codeph"> playlog={25} </span>) </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -v </span> </p> </td> 
  <td class="stentry"> <p>Im Modus "Ausführlich"werden die generierten Anforderungs-URLs nach <span class="codeph"> stdout </span> ausgegeben. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -h </span> </p> </td> 
  <td class="stentry"> <p>Drucken Sie eine Synchronisierung nach <span class="codeph"> stdout </span>. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -r </span> </p> </td> 
  <td class="stentry"> <p>request-method - Zu verwendende HTTP-Anforderungsmethode ( <span class="codeph"> get|post|head|smart </span>). </p> <p>Standard: <span class="codeph"> smart </span>) </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -o </span> </p> </td> 
  <td class="stentry"> <p>request-method-pos - pos in der Protokolldatei, um die ursprüngliche Methode zu erfassen. </p> <p>Standard: 15 </p> </td> 
 </tr> 
</table>

Bei Windows lautet der Dateiname [!DNL playlog.bat] und unter Linux [!DNL playlog.sh].

## Beispiele {#section-716e5c35e9fa4ee3a4b0687381fcea40}

Im folgenden Beispiel werden alle Anforderungen aus einer Zugriffsprotokolldatei wiedergegeben, die von Image Serving unter Linux erstellt wurde:

`> cd /usr/local/Scene7/ImageServing/logs`

`> ../bin/playlog.sh access-2007-01-01.log -n 18 -s ' ' -m . -p http://localhost:8080`

Mit dem folgenden Befehl werden alle Anforderungen wiedergegeben, die in einer von Image Serving unter Windows erstellten Ablaufverfolgungsprotokolldatei gefunden wurden:

`> "\Program Files\Scene7\ImageServing\bin\playlog.bat" d:\logs/access-2006-09-01.log`
