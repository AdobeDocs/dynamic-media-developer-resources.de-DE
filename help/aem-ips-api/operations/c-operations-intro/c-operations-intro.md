---
description: Beschreibt die allgemeinen Vorgangsparameter, die von der IPS-Webservice-API verarbeitet werden.
solution: Experience Manager
title: Betriebsmethoden
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 020c8e63-ad4e-4c0d-8da6-b51efb2b89a5
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '704'
ht-degree: 0%

---

# Betriebsmethoden{#operations-methods}

In diesem Abschnitt werden die allgemeinen Vorgangsparameter beschrieben, die von der IPS-Webservice-API verarbeitet werden.

Eine vollständige Beschreibung der einzelnen Vorgangsparameter finden Sie unter [Vorgangsparameter](/help/aem-ips-api/operations/c-operations-intro/c-methods/c-methods.md).

## Handles: Info {#section-094ce1afa6244fa5b2c762f44ffdca1c}

Verarbeitet Referenz-IPS-Objekte, die von bestimmten API-Vorgängen zurückgegeben werden. Sie können auch Handles als Parameter an nachfolgende Vorgangsaufrufe übergeben. Handles sind Datentypen vom Typ „Zeichenfolge“ ( `xsd:string`).

Handles sind nur für die Verwendung während einer einzelnen Anwendungssitzung vorgesehen. Außerdem sollten Sie Handles als persistent festlegen, da sich ihr Format zwischen IPS-Versionen ändern kann. Beim Schreiben interaktiver Anwendungen werden Sitzungs-Timeouts implementiert und alle Handles zwischen Sitzungen verworfen, insbesondere nach einem IPS-Upgrade. Wenn Sie nicht interaktive Anwendungen schreiben, rufen Sie die entsprechenden Vorgänge auf, um bei jeder Ausführung der Anwendung Handles abzurufen. Die folgenden Java-/Axis2-Code-Beispiele zeigen eine falsche und korrekte Code-Ausführung:

**Fehlerhafter Handle-Code**

Dieses Codebeispiel ist falsch, da es einen hartcodierten Wert (555) für das Firmen-Handle enthält.

```
SearchAssetsParam searchParam = new SearchAssetsParam(); searchParam.setCompanyHandle("555");// INCORRECT 
searchParam.setFolder("myFolder"); 
SearchAssetsReturn retVal = ipsApi.searchAssets(searchParam, authHeader);
```

**korrekter Handle-Code**

Dieses Code-Beispiel ist korrekt, da es `getCompanyInfo` aufruft, um ein gültiges Handle zurückzugeben. Sie ist nicht auf einen hartcodierten Wert angewiesen. Verwenden Sie diese Methode - oder ein anderes IPS-API-Äquivalent - , um das erforderliche Handle zurückzugeben.

```
GetCompanyInfoParam companyInfoParam = new GetCompanyInfoParam(); 
companyInfoParam.setCompanyName("My Company"); GetCompanyInfoReturn companyInfoReturn = ipsApi.getCompanyInfo(companyInfoParam, authHeader); 
String companyHandle = companyInfoReturn.getCompanyInfo().getCompanyHandle(); 
SearchAssetsParam searchParam = new SearchAssetsParam(); searchParam.setCompanyHandle(companyHandle); //CORRECT 
searchParam.setFolder("myFolder"); 
SearchAssetsReturn retVal = ipsApi.searchAssets(searchParam, authHeader);
```

## Allgemeine Handletypen {#section-e683ac8283284f9688e63f51a494f7a0}

**companyHandle**

Bei den meisten Vorgängen müssen Sie einen Unternehmenskontext festlegen, indem Sie einen `companyHandle` übergeben. Das Firmen-Handle ist ein Zeiger, der von bestimmten Vorgängen wie `getCompanyInfo`, `addCompany` und `getCompanyMembership` zurückgegeben wird.

**userHandle**

Der `userHandle` ist ein optionaler Parameter für Vorgänge, die auf einen bestimmten Benutzer abzielen. Standardmäßig zielen diese Vorgänge auf den aufrufenden Benutzer ab (den Benutzer, dessen Anmeldeinformationen zur Authentifizierung übergeben werden). Admin-Benutzer mit den entsprechenden Berechtigungen können jedoch einen anderen Benutzer angeben. Beispielsweise legt der `setPassword` normalerweise das Kennwort des authentifizierten Benutzers fest, ein Administrator kann jedoch den `userHandle`-Parameter verwenden, um das Kennwort für einen anderen Benutzer festzulegen.

Bei Vorgängen, für die ein Unternehmenskontext erforderlich ist (mithilfe des `companyHandle`-Parameters), müssen sowohl die authentifizierten als auch die Zielbenutzer Mitglieder des angegebenen Unternehmens sein. Für Vorgänge, für die kein Unternehmenskontext erforderlich ist, müssen die authentifizierten und die Zielgruppenbenutzer Mitglieder mindestens eines gemeinsamen Unternehmens sein.

Mit den folgenden Vorgängen können Benutzer-Handles abgerufen werden:

* `getUsers`
* `getAllUsers`
* `getUserInfo`
* `getCompanyMembers`
* `getGroupMembers`
* `addUser`

**accessUserHandle und accessGroupHandle**

Standardmäßig werden Vorgänge, für die Zugriffsberechtigungen (Lesen, Schreiben, Löschen) erforderlich sind, im Berechtigungskontext des aufrufenden Benutzers ausgeführt. Mit bestimmten Vorgängen können Sie diesen Kontext mit dem Parameter `accessUserHandle` oder `accessGroupHandle` ändern. Mit dem Parameter `accessUserHandle` kann ein Administrator stellvertretend für einen anderen Benutzer agieren. Der `accessGroupHandle` Parameter ermöglicht es dem Aufrufer, im Kontext einer bestimmten Benutzergruppe zu arbeiten.

**responseFieldArray und excludeFieldArray**

Bei einigen Vorgängen können Aufrufer einschränken, welche Felder in der Antwort enthalten sind. Durch die Beschränkung von Feldern können die Zeit und der Arbeitsspeicher für die Verarbeitung der Anfrage reduziert und die Größe der Antwortdaten verringert werden. Der Aufrufer kann eine bestimmte Liste von Feldern anfordern, indem er einen `responseFieldArray` übergibt, oder mit einer Auflistung einer Liste von ausgeschlossenen Feldern mithilfe des `excludeFieldArray`.

Sowohl `responseFieldArray` als auch `excludeFieldArray` geben Felder mithilfe eines Knotenpfads an, der durch `/` getrennt ist. Um beispielsweise anzugeben, dass `searchAssets` nur den Namen, das Datum der letzten Änderung und die Metadaten für jedes Asset zurückgibt, verweisen Sie auf Folgendes:

```
<responseFieldArray> 
   <items>assetArray/items/name</items> 
   <items>assetArray/items/lastModified</items> 
   <items>assetArray/items/metadataArray</items> 
</responseFieldArray>
```

Entsprechend müssen Sie alle Felder (mit Ausnahme der Berechtigungen) zurückgeben:

```
<excludeFieldArray> 
   <items>assetArray/items/permissions</items> 
</excludeFieldArray>
```

Beachten Sie, dass die Knotenpfade relativ zum Stammknoten des Rückgabeknotens sind. Wenn Sie ein Feld vom Typ „Komplex“ ohne seine Unterelemente angeben (z. B. `assetArray/items/imageInfo`), werden alle seine Unterelemente eingeschlossen. Wenn Sie ein oder mehrere Unterelemente in einem Feld vom Typ „Komplex“ angeben (z. B. `assetArray/items/imageInfo/originalPath`), werden nur diese Unterelemente einbezogen.

Wenn Sie `responseFieldArray` oder `excludeFieldArray` nicht in eine Anfrage einbeziehen, werden alle Felder zurückgegeben.

**Gebietsschema**

Seit IPS 4.0 unterstützt die IPS-API das Festlegen des Gebietsschemakontexts eines Vorgangs durch Übergeben des `authHeader` Gebietsschemaparameters. Wenn der Parameter „locale“ nicht vorhanden ist, wird der HTTP-Header `Accept-Language` verwendet. Wenn auch dieser Header nicht vorhanden ist, wird das Standardgebietsschema für den IPS-Server verwendet.

Bestimmte Vorgänge verwenden auch explizite Gebietsschemaparameter, die sich vom Kontext des Vorgangs-Gebietsschemas unterscheiden können. Der `submitJob`-Vorgang verwendet beispielsweise einen `locale`, der das Gebietsschema festlegt, das für die Auftragsprotokollierung und die E-Mail-Benachrichtigung verwendet wird.

Gebietsschema-Parameter verwenden das Format `<language_code>[-<country_code>]`

Wenn der Sprach-Code ein Code mit zwei Buchstaben in Kleinbuchstaben gemäß ISO-639 und der optionale Ländercode ein Code mit zwei Buchstaben in Großbuchstaben gemäß ISO-3266 ist. Beispielsweise ist die Gebietsschema-Zeichenfolge für US-Englisch `en-US`.
