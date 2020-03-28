---
description: In diesem Abschnitt werden die von der IPS Web Service API bearbeiteten Parameter für allgemeine Vorgänge beschrieben.
seo-description: In diesem Abschnitt werden die von der IPS Web Service API bearbeiteten Parameter für allgemeine Vorgänge beschrieben.
seo-title: Vorgangsmethoden
solution: Experience Manager
title: Vorgangsmethoden
topic: Scene7 Image Production System API
uuid: 713646a7-1108-4f93-bec2-3fbe7e548515
translation-type: tm+mt
source-git-commit: 806e7e670ee98e1fb6adf52ffc95fb989fa69400

---


# Vorgangsmethoden{#operations-methods}

In diesem Abschnitt werden die von der IPS Web Service API bearbeiteten Parameter für allgemeine Vorgänge beschrieben.

Eine vollständige Beschreibung der einzelnen Parameter finden Sie unter [Vorgangsparameter](/help/aem-ips-api/operations/c-operations-intro/c-methods/c-methods.md).

## Handles: Info {#section-094ce1afa6244fa5b2c762f44ffdca1c}

Handles verweisen auf IPS-Objekte, die von bestimmten API-Vorgängen zurückgegeben werden. Sie können Handles auch als Parameter an nachfolgende Vorgangsaufrufe übergeben. Handles sind Zeichenfolgendatentypen ( `xsd:string`).

Handles sind nur für die Verwendung während einer einzelnen Anwendungssitzung vorgesehen. Darüber hinaus sollten Sie Handles dauerhaft machen, da sich ihr Format zwischen IPS-Versionen ändern kann. Wenn Sie interaktive Anwendungen erstellen, implementieren Sie Sitzungs-Timeouts und verwerfen alle Handles zwischen Sitzungen, insbesondere nach einer IPS-Aktualisierung. Wenn Sie nicht interaktive Anwendungen schreiben, rufen Sie die entsprechenden Vorgänge auf, um bei jeder Ausführung der Anwendung Handles abzurufen. Die folgenden Java/Axis2-Codebeispiele zeigen eine falsche und korrekte Codeausführung:

**Falscher Handle-Code**

Dieses Codebeispiel ist nicht korrekt, da es einen hartkodierten Wert (555) für den Firmen-Handle enthält.

```
SearchAssetsParam searchParam = new SearchAssetsParam(); searchParam.setCompanyHandle("555");// INCORRECT 
searchParam.setFolder("myFolder"); 
SearchAssetsReturn retVal = ipsApi.searchAssets(searchParam, authHeader);
```

**Korrekter Handle-Code**

Dieses Codebeispiel ist korrekt, da es die Rückgabe eines gültigen Handles `getCompanyInfo` erfordert. Es ist kein hartkodierter Wert erforderlich. Verwenden Sie diese Methode oder eine andere gleichwertige IPS-API, um den erforderlichen Handle zurückzugeben.

```
GetCompanyInfoParam companyInfoParam = new GetCompanyInfoParam(); 
companyInfoParam.setCompanyName("My Company"); GetCompanyInfoReturn companyInfoReturn = ipsApi.getCompanyInfo(companyInfoParam, authHeader); 
String companyHandle = companyInfoReturn.getCompanyInfo().getCompanyHandle(); 
SearchAssetsParam searchParam = new SearchAssetsParam(); searchParam.setCompanyHandle(companyHandle); //CORRECT 
searchParam.setFolder("myFolder"); 
SearchAssetsReturn retVal = ipsApi.searchAssets(searchParam, authHeader);
```

## Allgemeine Handlungstypen {#section-e683ac8283284f9688e63f51a494f7a0}

**companyHandle**

Bei den meisten Vorgängen müssen Sie einen Firma-Kontext festlegen, indem Sie einen `companyHandle` Parameter übergeben. Der Firma-Handle ist ein Zeiger, der von bestimmten Vorgängen wie `getCompanyInfo`, `addCompany`und `getCompanyMembership`zurückgegeben wird.

**userHandle**

Der `userHandle` Parameter ist ein optionaler Parameter für Vorgänge, mit denen ein bestimmter Benutzer Zielgruppe wird. Standardmäßig wird bei diesen Vorgängen der aufrufende Benutzer Zielgruppe (der Benutzer, dessen Anmeldeinformationen zur Authentifizierung übergeben werden). Admin-Benutzer mit den entsprechenden Berechtigungen können jedoch einen anderen Benutzer angeben. Beispielsweise legt der `setPassword` Vorgang normalerweise das Kennwort des authentifizierten Benutzers fest, aber ein Administrator kann den `userHandle` Parameter verwenden, um das Kennwort für einen anderen Benutzer festzulegen.

Bei Vorgängen, für die ein Firma-Kontext erforderlich ist (unter Verwendung des `companyHandle` Parameters), müssen sowohl der authentifizierte Benutzer als auch die Zielgruppe Mitglieder der angegebenen Firma sein. Bei Vorgängen, die keinen Kontext für die Firma erfordern, müssen sowohl die authentifizierten Benutzer als auch die Zielgruppe Mitglieder von mindestens einer gemeinsamen Firma sein.

Die folgenden Vorgänge können Benutzergriffe abrufen:

* `getUsers`
* `getAllUsers`
* `getUserInfo`
* `getCompanyMembers`
* `getGroupMembers`
* `addUser`

**accessUserHandle und accessGroupHandle**

Vorgänge, für die Zugriffsberechtigungen erforderlich sind (Lesen, Schreiben, Löschen), werden standardmäßig im Berechtigungskontext des aufrufenden Benutzers ausgeführt. Bestimmte Vorgänge ermöglichen es Ihnen, diesen Kontext mit dem `accessUserHandle` oder- `accessGroupHandle` Parameter zu ändern. Mit dem `accessUserHandle` Parameter kann ein Administrator die Identität eines anderen Benutzers annehmen. Der `accessGroupHandle` Parameter ermöglicht es dem Aufrufer, im Kontext einer bestimmten Benutzergruppe zu arbeiten.

**responseFieldArray und excludeFieldArray**

Einige Vorgänge ermöglichen es dem Aufrufer, einzuschränken, welche Felder in der Antwort enthalten sind. Die Einschränkung von Feldern kann dazu beitragen, die für die Verarbeitung der Anforderung erforderliche Zeit und Arbeitsspeicher zu reduzieren und die Größe der Antwortdaten zu reduzieren. Der Aufrufer kann eine bestimmte Liste von Feldern anfordern, indem er einen `responseFieldArray` Parameter übergibt oder eine Liste ausgeschlossener Felder über den `excludeFieldArray` Parameter aufzählt.

Sowohl `responseFieldArray` als auch `excludeFieldArray` geben Sie Felder mithilfe eines Knotenpfads getrennt durch `/`. Um beispielsweise anzugeben, dass für jedes Asset nur der Name, das Datum der letzten Änderung und die Metadaten `searchAssets` zurückgegeben werden, verweisen Sie auf Folgendes:

```
<responseFieldArray> 
   <items>assetArray/items/name</items> 
   <items>assetArray/items/lastModified</items> 
   <items>assetArray/items/metadataArray</items> 
</responseFieldArray>
```

So geben Sie alle Felder zurück (mit Ausnahme der Berechtigungen):

```
<excludeFieldArray> 
   <items>assetArray/items/permissions</items> 
</excludeFieldArray>
```

Beachten Sie, dass die Knotenpfade relativ zum Stammordner des Rückgabeknotens sind. Wenn Sie ein komplexes Typfeld ohne Unterelemente (z. B. `assetArray/items/imageInfo`) angeben, werden alle zugehörigen Unterelemente eingeschlossen. Wenn Sie ein oder mehrere Unterelemente in einem Feld eines komplexen Typs angeben (z. B. `assetArray/items/imageInfo/originalPath`), werden nur diese Unterelemente einbezogen.

Wenn Sie keine `responseFieldArray` oder keine Anforderung `excludeFieldArray` angeben, werden alle Felder zurückgegeben.

**Gebietsschema**

Seit IPS 4.0 unterstützt die IPS-API das Festlegen des Gebietsschemakontexts eines Vorgangs durch Übergabe des `authHeader` Gebietsschemaparameters. Wenn der Parameter locale nicht vorhanden ist, `Accept-Language` wird der HTTP-Header verwendet. Wenn dieser Header ebenfalls nicht vorhanden ist, wird das Standardgebietsschema für den IPS-Server verwendet.

Bestimmte Vorgänge erfordern auch explizite Gebietsschema-Parameter, die sich vom Gebietsschema-Kontext für Vorgänge unterscheiden können. Der `submitJob` Vorgang nimmt beispielsweise einen `locale` Parameter, der das Gebietsschema für die Auftragsprotokollierung und E-Mail-Benachrichtigung festlegt.

Gebietsschemaparameter verwenden das Format `<language_code>[-<country_code>]`

Ist der Sprachencode ein Kleinbuchstabe, ist der nach ISO-639 spezifizierte Zweibuchstaben-Code und der optionale Ländercode ein nach ISO-3266 spezifizierter Großbuchstabe-Zweibuchstabe-Code. Beispielsweise lautet die Zeichenfolge für Englisch (USA) `en-US`.
