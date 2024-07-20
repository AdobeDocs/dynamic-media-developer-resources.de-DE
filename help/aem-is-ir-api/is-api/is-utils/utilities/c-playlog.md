---
description: Mit dem Dienstprogramm "playlog"können Inhalte für den HTTP-Antwort-Cache vorab generiert werden.
solution: Experience Manager
title: Das Dienstprogramm "playlog"
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: e0213978-3a1d-44b4-82bf-4527b980b29e
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '422'
ht-degree: 0%

---

# Das Dienstprogramm &quot;playlog&quot;{#the-playlog-utility}

Mit dem Dienstprogramm &quot;playlog&quot;können Inhalte für den HTTP-Antwort-Cache vorab generiert werden.

Der vorhandene Image Serving HTTP-Antwort-Cache ist nach einem Upgrade der Hauptversion nicht mehr nutzbar (wenn die erste oder zweite Ziffer der Versionsnummer geändert wurde). Wenn der Server nach der Aktualisierung in die Bedingungen für die volle Auslastung übernommen werden soll, kann der Server überlastet sein und die ersten Stunden mit fehlenden Cache-Anforderungen verarbeiten, bis der Cache ausreichend gefüllt ist und die Cache-Trefferrate steigt.

Um diese anfängliche Ladespitze zu vermeiden, kann das Dienstprogramm `playlog` verwendet werden, um Inhalte für den HTTP-Antwort-Cache vorab zu generieren. `playlog` extrahiert HTTP-Anfragen aus einer vorhandenen Zugriffsprotokolldatei und sendet sie an den Server, um Cache-Einträge zu generieren. Für typische Nutzungsszenarien reicht es aus, eine einzelne Zugriffsprotokolldatei mit dem Traffic für einen ganzen Tag wiederzugeben.

Zusätzlich zum Hochladen des HTTP-Antwort-Cache nach der Installation wird das Dienstprogramm auch verwendet, um Cache-Inhalte vorzugenerieren, wenn ein neuer Server zu einer Umgebung mit Lastenausgleich hinzugefügt wird. Geben Sie einfach eine aktuelle Protokolldatei von einem der anderen Server zurück.

`playlog` kann so konfiguriert werden, dass die meisten Zugriffsprotokolldateien unterstützt werden, die von früheren Versionen von Image Serving generiert wurden.

## Nutzung {#section-daa126ec469b4a9d90d59def4fdaacdd}

` playlog *[!DNL logFile]* [-n *[!DNL col]*] [-s *[!DNL separator]*] [-m *[!DNL marker]*] [-p *[!DNL prefix]*] [-x *[!DNL suffix]*] [-v] [-h] [-r *[!DNL request method]*] [-o *[!DNL position]*]`

<table id="simpletable_39B9638BCB0F4244B5155C958C044C31"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -p <span class="varname"> Präfix </span> </span> </p> </td> 
  <td class="stentry"> <p>Stamm-URL, die den aus der Protokolldatei extrahierten Anforderungen vorangestellt werden soll. </p> <p>Standard: <span class="filepath"> http://localhost:8080/is </span>) </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -n <span class="varname"> col </span> </span> </p> </td> 
  <td class="stentry"> <p>Feldnummer (Spalte), die die Anforderung im Protokolldatensatz enthält; 1-basiert. </p> <p>Standard: 16 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -s <span class="varname"> Trennzeichen </span> </span> </p> </td> 
  <td class="stentry"> <p>Feldtrennzeichen; Muster für reguläre Ausdrücke. </p> <p>Standard: <span class="codeph"> [ ]+ </span>) </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -m <span class="varname"> Markierung </span> </span> </p> </td> 
  <td class="stentry"> <p>Anforderungsmarkierung; gibt Anforderungen in der Protokolldatei an, die wiedergegeben werden sollen; Muster für reguläre Ausdrücke. </p> <p>Standard: <span class="codeph"> Anfrage: </span>) </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -x <span class="varname"> Suffix </span> </span> </p> </td> 
  <td class="stentry"> <p>Suffix, das an die aus der Protokolldatei extrahierte Anfrage angehängt wird. Kann verwendet werden, um wiedergegebene Anfragen von Live-Anfragen in den Protokolldateien zu trennen; ein "?" oder "&amp;"-Trennzeichen wird automatisch eingefügt; das Suffix kann jedes Protokollfeld in geschweiften Klammern nach Position referenzieren, der Standard entspricht dem Unterschriftsfeld md5. </p> <p>Standard: <span class="codeph"> playlog={25} </span>) </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -v </span> </p> </td> 
  <td class="stentry"> <p>Verbose-Modus druckt die generierten Anfrage-URLs auf <span class="codeph"> stdout </span>. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -h </span> </p> </td> 
  <td class="stentry"> <p>Drucken Sie eine Synchronisation auf <span class="codeph"> stdout </span>. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -r </span> </p> </td> 
  <td class="stentry"> <p>request-method - HTTP request method to use ( <span class="codeph"> get|post|head|smart </span>). </p> <p>Standard: <span class="codeph"> smart </span>) </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -o </span> </p> </td> 
  <td class="stentry"> <p>request-method-pos - pos in der Protokolldatei, um die ursprüngliche Methode zu erfassen. </p> <p>Standard: 15 </p> </td> 
 </tr> 
</table>

Für Windows lautet der Dateiname [!DNL playlog.bat] und unter Linux der Dateiname [!DNL playlog.sh].

## Beispiele {#section-716e5c35e9fa4ee3a4b0687381fcea40}

Im folgenden Beispiel werden alle Anfragen aus einer von Image Serving unter Linux erstellten Zugriffsprotokolldatei wiedergegeben:

`> cd /usr/local/Scene7/ImageServing/logs`

`> ../bin/playlog.sh access-2007-01-01.log -n 18 -s ' ' -m . -p http://localhost:8080`

Mit dem folgenden Befehl werden alle Anfragen wiedergegeben, die in einer von Image Serving unter Windows erstellten Ablaufverfolgungsprotokolldatei gefunden wurden:

`> "\Program Files\Scene7\ImageServing\bin\playlog.bat" d:\logs/access-2006-09-01.log`
