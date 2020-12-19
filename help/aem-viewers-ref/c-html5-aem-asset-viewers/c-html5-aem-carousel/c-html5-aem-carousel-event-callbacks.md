---
description: 'null'
seo-description: 'null'
seo-title: Ereignis-Rückrufe
solution: Experience Manager
title: Ereignis-Rückrufe
topic: Dynamic media
uuid: 7280a391-3ead-470b-89e9-5faa082e0202
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '215'
ht-degree: 2%

---


# Ereignis-Rückrufe{#event-callbacks}

Der Viewer unterstützt JavaScript-Ereignis-Rückrufe, die die Webseite zur Verfolgung des Viewer-Initialisierungsprozesses oder -Laufzeitverhaltens verwendet.

Callback-Handler werden zugewiesen, indem Ereignis und entsprechende Handler-Funktionen mit der Eigenschaft `handlers` an das JSON-Objekt `config` im Konstruktor des Viewers übergeben werden. Alternativ kann die API-Methode `setHandlers()` verwendet werden.

Folgende Viewer-Ereignis werden unterstützt:

<table id="table_D4A2035B65B140F882F550B711BD3160"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Viewer-Ereignis </p> </th> 
   <th colname="col2" class="entry"> <p>Beschreibung </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> initComplete  </span> </p> </td> 
   <td colname="col2"> <p>Wird ausgelöst, wenn die Viewer-Initialisierung abgeschlossen ist und alle internen Komponenten erstellt wurden, sodass die API <span class="codeph"> getComponent() </span> verwendet werden kann. Der Callback-Handler nimmt keine Argumente an. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> trackEvent </span> </p> </td> 
   <td colname="col2"> <p> Wird jedes Mal ausgelöst, wenn ein Ereignis im Viewer auftritt, das von einem Ereignis-Verfolgungssystem wie Adobe Analytics verarbeitet werden kann. Der Callback-Handler akzeptiert die folgenden Argumente: </p> <p> 
     <ul id="ul_8A5F409E32E94063AE8D3AB158A0E13D"> 
      <li id="li_1311D5DDD4454FBC9116BA8E2CB003B1"> <p> <span class="codeph"> objID {String}  </span> - aktuell nicht verwendet. </p> </li> 
      <li id="li_C2ABD13097FA40A7B9801C0B7592FB59"> <p> <span class="codeph"> compClass {String}  </span> - aktuell nicht verwendet. </p> </li> 
      <li id="li_3BE8001365714C3FAC32C9B2CFFD5DCE"> <p> <span class="codeph"> instName {String}  </span> - Instanzname der Viewer-SDK-Komponente, die das Ereignis ausgelöst hat. </p> </li> 
      <li id="li_755DDE84B1CC4B4D8A3FA0C774CBA666"> <p> <span class="codeph"> timeStamp {Number}  </span> - Zeitstempel des Ereignisses. </p> </li> 
      <li id="li_05A1C45826AC4D1192CB72FE07EE4C29"> <p> <span class="codeph"> eventInfo {String}  </span> - Ereignis-Nutzlast. </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> quickViewActivate  </span> </p> </td> 
   <td colname="col2"> <p> Wird ausgelöst, wenn der Benutzer einen Hotspot mit zugehörigen Quick-Ansicht-Daten aktiviert. Der Callback-Handler akzeptiert das folgende Argument: </p> <p> 
     <ul id="ul_171110934BD54839B371FAD8D2AD467B"> 
      <li id="li_7B14C3BA432B43E392AC103926807E88"> <p> <span class="codeph"> data {Object}  </span> - ein JSON-Objekt, das Daten aus der Hotspot-Definition enthält. Das Feld <span class="codeph"> sku </span> ist obligatorisch, während andere Felder optional sind und von der Source Hotspot-Definition abhängen. </p> </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

Siehe auch [KarussellViewer**](../../c-html5-aem-asset-viewers/c-html5-aem-carousel/c-html5-aem-carousel-javascriptapiref/r-html5-aem-carousel-javascriptapiref-carouselviewer.md#reference-bd16cadc0c054fafb0db4994741d47cd) und [setHandlers**](../../c-html5-aem-asset-viewers/c-html5-aem-carousel/c-html5-aem-carousel-javascriptapiref/r-html5-aem-carousel-javascriptapiref-sethandlers.md#reference-d76f126ac4354dc282e56afd49a0c643).
