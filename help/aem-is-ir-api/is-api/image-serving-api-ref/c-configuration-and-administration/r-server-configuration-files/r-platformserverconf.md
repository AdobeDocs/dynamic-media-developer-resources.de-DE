---
description: Enthält Plattformservereinstellungen.
seo-description: Enthält Plattformservereinstellungen.
seo-title: PlatformServer.conf
solution: Experience Manager
title: PlatformServer.conf
topic: Scene7 Image Serving - Image Rendering API
uuid: d798762b-c9ff-4e1b-b2ac-c5e40476b375
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '156'
ht-degree: 1%

---


# PlatformServer.conf{#platformserver-conf}

Enthält Plattformservereinstellungen.

Diese Datei ist eine JAVA-Eigenschaftendatei. Es ist darauf zu achten, dass die entsprechenden Konventionen eingehalten werden. Andernfalls kann es vorkommen, dass der Beginn des Plattformservers fehlschlägt. Verwenden Sie in Windows-Dateipfaden einen umgekehrten Schrägstrich (\\) oder einen einzelnen Schrägstrich (/) anstelle eines umgekehrten Schrägstrichs (\). Der umgekehrte Schrägstrich wird als Escape-Zeichen in diesem Dateityp verwendet.

Änderungen an dieser Datei werden nach dem Speichern der Datei wirksam.

Nur die unten aufgeführten Einstellungen können in [!DNL PlatformServer.conf] geändert werden. Wenn eine bestimmte Einstellung fehlt, kann sie an einer beliebigen Stelle in der Datei hinzugefügt werden. Es ist möglicherweise nur eine Instanz jeder Einstellung vorhanden.

<table id="simpletable_38244750F50A46E5B0077F5F860B125C"> 
 <tr class="strow"> 
  <td class="stentry"> <p>Allgemeine Plattformserver-Einstellungen </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> cache.rootPaths=./cache </span> </p> <p> <span class="codeph"> cache.maxEntries=1000000  </span> </p> <p> <span class="codeph"> cache.maxSize=1073741824  </span> </p> <p> <span class="codeph"> isConnection.port=27345  </span> </p> <p> <span class="codeph"> allowDefaultCatalogRequsts=true  </span> </p> <p> <span class="codeph"> saveToFile.saveTimeout=60000  </span> </p> <p> <span class="codeph"> staticContent.rootPaths=./static-content </span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>Cache-Clusterkonfiguration </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> cluster.hosts=&lt;empty&gt; </span> </p> <p> <span class="codeph"> cacheCluster.queryTimeout=50  </span> </p> <p> <span class="codeph"> cacheCluster.fetchTimeout=10000  </span> </p> <p> <span class="codeph"> cacheCluster.updateLocalCache=true  </span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>Fehler-Umleitungskonfiguration </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> errorRedirect.rootUrl=&lt;empty&gt; </span> </p> <p> <span class="codeph"> errorRedirect.connectTimeout=1000  </span> </p> <p> <span class="codeph"> errorRedirect.socketTimeout=30000  </span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>SVG-Konfiguration </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> svgProvider.rootPaths=./Bilder </span> </p> <p> <span class="codeph"> svgProvider.SVGFileSizeLimit=1024  </span> </p> <p> <span class="codeph"> svgProvider.port=8080  </span> </p> <p> <span class="codeph"> svgProvider.fontRoot=./Bilder </span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>Medienset-Antworten </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> fvctx.useCatalogRecordValidation=false  </span> </p> <p> <span class="codeph"> fvctx.nestingLimit=10  </span> </p> <p> <span class="codeph"> fvctx.brochureLimit=20  </span> </p> </td> 
 </tr> 
</table>

