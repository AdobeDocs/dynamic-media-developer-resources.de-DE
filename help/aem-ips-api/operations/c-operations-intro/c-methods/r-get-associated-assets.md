---
description: Ruft Assets ab, die mit einem angegebenen Asset verknüpft sind, sowie Details zu dessen Beziehung.
solution: Experience Manager
title: getAssociatedAssets
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: cf49719f-5d79-4e64-a785-bf3b2fe200c7
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '407'
ht-degree: 5%

---

# getAssociatedAssets{#getassociatedassets}

Ruft Assets ab, die mit einem angegebenen Asset verknüpft sind, sowie Details zu dessen Beziehung.

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

**Input (getAssociatedAssetsParam)**

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
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> assetHandle</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:string</span> </p> </td> 
   <td colname="col3"> <p>Ja </p> </td> 
   <td colname="col4"> <p>Asset-Handle. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> responseFieldArray</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> types:StringArray</span> </p> </td> 
   <td colname="col3"> <p>Nein </p> </td> 
   <td colname="col4"> <p>Das Array der gewünschten Antwortfelder. Siehe response- FieldArray/excludeFieldArray in der Einführung. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> excludeFieldArray</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> types:StringArray</span> </p> </td> 
   <td colname="col3"> <p>Nein </p> </td> 
   <td colname="col4"> <p>Das Array der ausgeschlossenen Antwortfelder. Siehe response- FieldArray/excludeFieldArray in der Einführung. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Output (getAssociatedAssetsReturn)**

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
   <td colname="col2"> <span class="codeph"> types:AssetArray</span> </td> 
   <td colname="col3"> <p>Nein </p> </td> 
   <td colname="col4"> <p>Array von Set- und Vorlagen-Assets, die das angegebene Asset enthalten. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> memberArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> types:AssetArray</span> </td> 
   <td colname="col3"> <p>Nein </p> </td> 
   <td colname="col4"> <p>Array von Assets, die vom angegebenen Satz oder Vorlagen-Asset enthalten sind. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> layerReferenceArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> types:AssetArray</span> </td> 
   <td colname="col3"> <p>Nein </p> </td> 
   <td colname="col4"> <p>Array von Assets, die in einer Ebene oder Vorlagen-URL referenziert werden. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> ownerArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> types:AssetArray</span> </td> 
   <td colname="col3"> <p>Nein </p> </td> 
   <td colname="col4"> <p>Array von Assets, die Eigentümer des angegebenen Assets sind. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> derivedArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> types:AssetArray</span> </td> 
   <td colname="col3"> <p>Nein </p> </td> 
   <td colname="col4"> <p>Array von Assets, mit denen das angegebene Asset generiert wurde. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> generatorArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> types:GenerationInfoArray</span> </td> 
   <td colname="col3"> <p>Nein </p> </td> 
   <td colname="col4"> <p>Das <span class="codeph"> generatorArray</span> listet auf, wie dieses Asset erstellt wurde. Wenn beispielsweise <span class="codeph"> assetHandler</span> eine Bildseite einer PDF war, würde dies das PDF-Prozessor-Tool enthalten und auf das PdfFile-Asset verweisen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> generatedArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> types:GenerationInfoArray</span> </td> 
   <td colname="col3"> <p>Nein </p> </td> 
   <td colname="col4"> <p>Das <span class="codeph"> generatedArray</span> kehrt die Art und Weise um, wie dieses Asset erstellt wurde. Beispielsweise könnte der <span class="codeph"> generatedArray</span> die Liste der Bilder enthalten, die aus diesem <span class="codeph"> assetHandler</span> generiert wurden, wenn es ein PdfFile-Asset war. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> thumbAsset</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> types:asset</span> </td> 
   <td colname="col3"> <p>Nein </p> </td> 
   <td colname="col4"> <p>Die mit dem Anfrage-Asset verknüpften Asset-Informationen. Wenn kein Miniatur-Asset zugewiesen ist, wird das Feld in der Antwort weggelassen. </p> </td> 
  </tr> 
 </tbody> 
</table>

Sie können die Parameter `responseFieldArray` oder `excludeFieldArray` verwenden, um die Antwortgröße zu begrenzen. Insbesondere enthalten die in `generatorArray` oder `generatedArray` zurückgegebenen `GenerationInfo`-Elemente standardmäßig sowohl den Originator als auch die generierten Asset-Datensätze. Bei einem PDF-Asset-Typ führt dieses Verhalten zu unerwünschten mehreren Kopien des PDF-Asset-Datensatzes &quot;originator&quot;in der Antwort. Sie können dieses Problem beheben, indem Sie `generatedArray/items/originator` zu `excludeFieldArray` hinzufügen. Sie können auch eine explizite Liste von Antwortfeldern angeben, die Sie in `responseFieldArray` einbeziehen möchten.

## Beispiele {#section-8946ea4b9cb94912a8408249c897f192}

Im folgenden Beispiel wird der Handle des Generators für ein Bild angefordert, das aus einer PDF extrahiert wird. Er enthält eine `containerArray` Länge 1 mit einem Element, das die `assetHandle` der PDF enthält.

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

Das Gegenteil des obigen Beispiels ist:

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

In diesem nächsten Beispiel wird eine Gruppe zu einem Unternehmen mit `groupHandleArray` hinzugefügt. In diesem Beispiel wird nur eine Gruppe verwendet.

**Anfrage**

```java
<ns1:addGroupMembershipParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:groupHandleArray><ns1:items>225</ns1:items></ns1:groupHandleArray>
</ns1:addGroupMembershipParam>
```

**Antwort**

Keine.
