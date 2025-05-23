---
description: Enthält [!DNL Platform Server] Einstellungen.
solution: Experience Manager
title: PlatformServer.conf
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 00d55453-e7e6-4242-be83-7efa12764e5d
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '155'
ht-degree: 0%

---

# PlatformServer.conf{#platformserver-conf}

Enthält [!DNL Platform Server].

Diese Datei ist eine JAVA-Eigenschaftendatei. Es muss darauf geachtet werden, dass die entsprechenden Konventionen eingehalten werden. Andernfalls kann es sein, dass der [!DNL Platform Server] nicht startet. Verwenden Sie in Windows-Dateipfaden einen doppelten umgekehrten Schrägstrich &quot;\\&quot; oder einen einzelnen Schrägstrich &quot;/&quot; anstelle eines umgekehrten Schrägstrichs &quot;\&quot;. Der umgekehrte Schrägstrich wird in diesem Dateityp als Escape-Zeichen verwendet.

Änderungen an dieser Datei werden wirksam, nachdem die Datei gespeichert wurde.

Nur die unten aufgeführten Einstellungen können in [!DNL PlatformServer.conf] geändert werden. Wenn eine bestimmte Einstellung fehlt, kann sie an einer beliebigen Stelle in der Datei hinzugefügt werden. Es kann nur eine Instanz jeder Einstellung vorhanden sein.

<table id="simpletable_38244750F50A46E5B0077F5F860B125C"> 
 <tr class="strow"> 
  <td class="stentry"> <p>Allgemeine [!DNL Platform Server] </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> cache.rootPaths=./cache </span> </p> <p> <span class="codeph"> cache.maxEntries=1000000 </span> </p> <p> <span class="codeph"> cache.maxSize=1073741824 </span> </p> <p> <span class="codeph"> isConnection.port=27345 </span> </p> <p> <span class="codeph"> allowDefaultCatalogRequests=true </span> </p> <p> <span class="codeph"> saveToFile.saveTimeout=60000 </span> </p> <p> <span class="codeph"> staticContent.rootPaths="/static-content-</span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>Cache-Cluster-Konfiguration </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> cluster.hosts=&lt;empty&gt; </span> </p> <p> <span class="codeph"> cacheCluster.queryTimeout=50 </span> </p> <p> <span class="codeph"> cacheCluster.fetchTimeout=10000 </span> </p> <p> <span class="codeph"> cacheCluster.updateLocalCache=true </span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>Konfiguration der Fehlerumleitung </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> errorRedirect.rootUrl=&lt;empty&gt; </span> </p> <p> <span class="codeph"> errorRedirect.connectTimeout=1000 </span> </p> <p> <span class="codeph"> errorRedirect.socketTimeout=30000 </span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>SVG-Konfiguration </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> svgProvider.rootPaths="/images </span> </p> <p> <span class="codeph"> svgProvider.SVGFileSizeLimit=1024 </span> </p> <p> <span class="codeph"> svgProvider.port=8080 </span> </p> <p> <span class="codeph"> svgProvider.fontRoot=./images </span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>Medienset-Antworten </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> fvctx.useCatalogRecordValidation=false </span> </p> <p> <span class="codeph"> fvctx.nestingLimit=10 </span> </p> <p> <span class="codeph"> fvctx.broschureLimit=20 </span> </p> </td> 
 </tr> 
</table>
