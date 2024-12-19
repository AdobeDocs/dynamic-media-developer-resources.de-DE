---
description: Ruft Assets ab, die mit einem bestimmten Asset verknüpft sind, sowie Details zu ihrer Beziehung.
solution: Experience Manager
title: getAssociatedAssets
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: cf49719f-5d79-4e64-a785-bf3b2fe200c7
source-git-commit: 67e12fae514341137e4218ea950f34da0d9997f3
workflow-type: tm+mt
source-wordcount: '407'
ht-degree: 5%

---

# getAssociatedAssets{#getassociatedassets}

Ruft Assets ab, die mit einem bestimmten Asset verknüpft sind, sowie Details zu ihrer Beziehung.

Syntax

## Autorisierte Benutzertypen {#section-453cc706400345778713cda249bfac16}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parameter {#section-d11d0dab59e94e89b466123a0ebfa82e}

**Eingabe (getAssociatedAssetsParam)**

<table id="table_DBB97A6507EB48479FFFD2184FF8F07C"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Name </p> </th> 
   <th colname="col2" class="entry"> <p>Typ </p> </th> 
   <th colname="col3" class="entry"> <p>Erforderlich </p> </th> 
   <th colname="col4" class="entry"> <p>Beschreibung </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> companyHandle</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:string</span> </p> </td> 
   <td colname="col3"> <p>Ja </p> </td> 
   <td colname="col4"> <p>Handle an das Unternehmen, dem das Asset gehört. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> AssetHandle</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:string</span> </p> </td> 
   <td colname="col3"> <p>Ja </p> </td> 
   <td colname="col4"> <p>Asset-Handle. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> responseFieldArray</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph">:StringArray</span> </p> </td> 
   <td colname="col3"> <p>Nein </p> </td> 
   <td colname="col4"> <p>Das Array der gewünschten Antwortfelder. Siehe Antwort - FieldArray/excludeFieldArray in der Einführung. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> excludeFieldArray</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph">:StringArray</span> </p> </td> 
   <td colname="col3"> <p>Nein </p> </td> 
   <td colname="col4"> <p>Das Array der ausgeschlossenen Antwortfelder. Siehe Antwort - FieldArray/excludeFieldArray in der Einführung. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Ausgabe (getAssociatedAssetsReturn)**

<table id="table_B894B4B6EFA24359A0250A8A4523EA8D"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Name </p> </th> 
   <th colname="col2" class="entry"> <p>Typ </p> </th> 
   <th colname="col3" class="entry"> <p>Erforderlich </p> </th> 
   <th colname="col4" class="entry"> <p>Beschreibung </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> containerArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph">:AssetArray</span> </td> 
   <td colname="col3"> <p>Nein </p> </td> 
   <td colname="col4"> <p>Array von Satz- und Vorlagen-Assets, das das angegebene Asset enthält. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> memberArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph">:AssetArray</span> </td> 
   <td colname="col3"> <p>Nein </p> </td> 
   <td colname="col4"> <p>Array von Assets, die im angegebenen Satz oder Vorlagen-Asset enthalten sind. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> layerReferenceArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph">:AssetArray</span> </td> 
   <td colname="col3"> <p>Nein </p> </td> 
   <td colname="col4"> <p>Array von Assets, auf die in einer Ebenen- oder Vorlagen-URL verwiesen wird. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> OwnerArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph">:AssetArray</span> </td> 
   <td colname="col3"> <p>Nein </p> </td> 
   <td colname="col4"> <p>Array von Assets, denen das angegebene Asset gehört. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> DerivedArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph">:AssetArray</span> </td> 
   <td colname="col3"> <p>Nein </p> </td> 
   <td colname="col4"> <p>Array von Assets, die zum Generieren des angegebenen Assets verwendet wurden. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> generatorArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph">:GenerationInfoArray</span> </td> 
   <td colname="col3"> <p>Nein </p> </td> 
   <td colname="col4"> <p>Das <span class="codeph"> generatorArray</span> listet die Art und Weise auf, wie dieses Asset erstellt wurde. Wenn <span class="codeph"> AssetHandler</span> beispielsweise eine Bildseite einer PDF wäre, würde diese das PDF-Prozessor-Tool enthalten und auf das PDF-Datei-Asset verweisen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> generateArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph">:GenerationInfoArray</span> </td> 
   <td colname="col3"> <p>Nein </p> </td> 
   <td colname="col4"> <p>Das <span class="codeph"> generateArray</span> invertiert die Art und Weise, wie dieses Asset erstellt wurde. Beispielsweise könnte <span class="codeph"> generateArray</span> die Liste der Bilder enthalten, die aus diesem <span class="codeph"> assetHandler generiert wurden</span> wenn dies ein PDF-Datei-Asset war. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> ThumbAsset</span> </span> </td> 
   <td colname="col2"> <span class="codeph">:Asset</span> </td> 
   <td colname="col3"> <p>Nein </p> </td> 
   <td colname="col4"> <p>Die Miniatur-Asset-Informationen, die mit der Asset-Anfrage verknüpft sind. Wenn kein Miniatur-Asset zugewiesen ist, wird das Feld in der Antwort weggelassen. </p> </td> 
  </tr> 
 </tbody> 
</table>

Sie können die Parameter `responseFieldArray` oder `excludeFieldArray` verwenden, um die Antwortgröße zu begrenzen. Insbesondere enthalten die in `generatorArray` oder `generatedArray` zurückgegebenen `GenerationInfo` standardmäßig sowohl die ursprünglichen als auch die generierten Asset-Datensätze. Bei einem PDF-Asset-Typ führt dieses Verhalten zu unerwünschten mehreren Kopien des PDF-Asset-Originator-Datensatzes in der Antwort. Sie können dieses Problem beheben, indem Sie `generatedArray/items/originator` zu `excludeFieldArray` hinzufügen. Sie können auch eine explizite Liste von Antwortfeldern angeben, die Sie in `responseFieldArray` einbeziehen möchten.

## Beispiele {#section-8946ea4b9cb94912a8408249c897f192}

Das folgende grundlegende Beispiel ist eine Anfrage für das Handle des Generators für ein Bild, das von einer PDF extrahiert wird. Es enthält eine `containerArray` von der Länge eins mit einem Element einschließlich der `assetHandle` der PDF.

**Anfrage**

```java
<soap:Envelope xmlns:soap="http://www.w3.org/2003/05/soap-envelope" xmlns:beta="http://www.scene7.com/IpsApi/xsd/2013-08-29-beta">
   <soap:Body>
      <beta:getAssociatedAssetsParam>
         <beta:companyHandle>c|11</beta:companyHandle>
         <beta:assetHandle>a|197</beta:assetHandle>
         <beta:responseFieldArray>
            <beta:items>containerArray/items/assetHandle</beta:items>
         </beta:responseFieldArray>
      </beta:getAssociatedAssetsParam>
   </soap:Body>
</soap:Envelope>
```

**Antwort**

```java
<soapenv:Envelope xmlns:soapenv="http://www.w3.org/2003/05/soap-envelope">
   <soapenv:Body>
      <getAssociatedAssetsReturn xmlns="http://www.scene7.com/IpsApi/xsd/2013-08-29-beta">
         <containerArray>
            <items>
               <assetHandle>a|207</assetHandle>
            </items>
         </containerArray>
      </getAssociatedAssetsReturn>
   </soapenv:Body>
</soapenv:Envelope>
```

Im obigen Beispiel sieht es umgekehrt wie folgt aus:

**Anfrage**

```java
<soap:Envelope xmlns:soap="http://www.w3.org/2003/05/soap-envelope" xmlns:beta="http://www.scene7.com/IpsApi/xsd/2013-08-29-beta">
   <soap:Body>
      <beta:getAssociatedAssetsParam>
         <beta:companyHandle>c|11</beta:companyHandle>
         <beta:assetHandle>a|177</beta:assetHandle>
        <beta:responseFieldArray>
           <beta:items>generatedArray/items/originator/assetHandle</beta:items>
         </beta:responseFieldArray>
      </beta:getAssociatedAssetsParam>
   </soap:Body>
</soap:Envelope>
```

**Antwort**

```java
<soapenv:Envelope xmlns:soapenv="http://www.w3.org/2003/05/soap-envelope">
   <soapenv:Body>
      <getAssociatedAssetsReturn xmlns="http://www.scene7.com/IpsApi/xsd/2013-08-29-beta">
         <generatedArray>
            <items>
               <originator>
                  <assetHandle>a|177</assetHandle>
               </originator>
            </items>
            <items>
               <originator>
                  <assetHandle>a|177</assetHandle>
               </originator>
            </items>
            <items>
               <originator>
                  <assetHandle>a|177</assetHandle>
               </originator>
            </items>
            <items>
               <originator>
                  <assetHandle>a|177</assetHandle>
               </originator>
            </items>
            <items>
               <originator>
                  <assetHandle>a|177</assetHandle>
               </originator>
            </items>
            <items>
               <originator>
                  <assetHandle>a|177</assetHandle>
               </originator>
            </items>
            <items>
               <originator>
                  <assetHandle>a|177</assetHandle>
               </originator>
            </items>
            <items>
               <originator>
                  <assetHandle>a|177</assetHandle>
               </originator>
            </items>
            <items>
               <originator>
                  <assetHandle>a|177</assetHandle>
               </originator>
            </items>
            <items>
               <originator>
                  <assetHandle>a|177</assetHandle>
               </originator>
            </items>
         </generatedArray>
      </getAssociatedAssetsReturn>
   </soapenv:Body>
</soapenv:Envelope>
```

In diesem nächsten Beispiel wird eine Gruppe zu einer Firma mit `groupHandleArray` hinzugefügt. In diesem Beispiel wird nur eine Gruppe verwendet.

**Anfrage**

```java
<ns1:addGroupMembershipParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:groupHandleArray><ns1:items>225</ns1:items></ns1:groupHandleArray>
</ns1:addGroupMembershipParam>
```

**Antwort**

Keine.
