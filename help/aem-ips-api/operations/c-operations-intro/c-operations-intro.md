---
description: Beschreibt die allgemeinen Vorgangsparameter, die von der IPS Web Service-API verarbeitet werden.
solution: Experience Manager
title: Vorgangsmethoden
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 020c8e63-ad4e-4c0d-8da6-b51efb2b89a5
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '700'
ht-degree: 0%

---

# Vorgangsmethoden{#operations-methods}

In diesem Abschnitt werden die allgemeinen Vorgangsparameter beschrieben, die von der IPS Web Service-API verarbeitet werden.

Eine vollständige Beschreibung der einzelnen Vorgangsparameter finden Sie unter [Aktionsparameter](/help/aem-ips-api/operations/c-operations-intro/c-methods/c-methods.md).

## Handles: Info {#section-094ce1afa6244fa5b2c762f44ffdca1c}

Handles verweisen auf IPS-Objekte, die von bestimmten API-Vorgängen zurückgegeben werden. Sie können Handles auch als Parameter an nachfolgende Vorgangsaufrufe übergeben. Handles sind Zeichenfolgendatentypen ( `xsd:string`).

Handles sind nur zur Verwendung während einer einzelnen Anwendungssitzung vorgesehen. Außerdem sollten Sie Handles persistent machen, da sich ihr Format zwischen IPS-Versionen ändern kann. Beim Schreiben interaktiver Anwendungen implementieren Sie Sitzungs-Timeouts und verwerfen alle Handles zwischen Sitzungen, insbesondere nach einem IPS-Upgrade. Wenn Sie nicht interaktive Anwendungen schreiben, rufen Sie die entsprechenden Vorgänge auf, um bei jeder Ausführung der Anwendung Handles abzurufen. Die folgenden Java/Axis2-Codebeispiele zeigen eine falsche und korrekte Codeausführung:

**Falscher Handle-Code**

Dieses Codebeispiel ist nicht korrekt, da es einen hartcodierten Wert (555) für das Handle des Unternehmens enthält.

```
SearchAssetsParam searchParam = new SearchAssetsParam(); searchParam.setCompanyHandle("555");// INCORRECT 
searchParam.setFolder("myFolder"); 
SearchAssetsReturn retVal = ipsApi.searchAssets(searchParam, authHeader);
```

**Richtiger Handle-Code**

Dieses Codebeispiel ist korrekt, da es `getCompanyInfo` , um einen gültigen Handle zurückzugeben. Es ist kein hartcodierter Wert erforderlich. Verwenden Sie diese Methode oder ein anderes IPS-API-Äquivalent, um den erforderlichen Handle zurückzugeben.

```
GetCompanyInfoParam companyInfoParam = new GetCompanyInfoParam(); 
companyInfoParam.setCompanyName("My Company"); GetCompanyInfoReturn companyInfoReturn = ipsApi.getCompanyInfo(companyInfoParam, authHeader); 
String companyHandle = companyInfoReturn.getCompanyInfo().getCompanyHandle(); 
SearchAssetsParam searchParam = new SearchAssetsParam(); searchParam.setCompanyHandle(companyHandle); //CORRECT 
searchParam.setFolder("myFolder"); 
SearchAssetsReturn retVal = ipsApi.searchAssets(searchParam, authHeader);
```

## Gängige Handlungstypen {#section-e683ac8283284f9688e63f51a494f7a0}

**companyHandle**

Bei den meisten Vorgängen müssen Sie einen Unternehmenskontext festlegen, indem Sie eine `companyHandle` -Parameter. Der Handle des Unternehmens ist ein Zeiger, der von bestimmten Vorgängen wie `getCompanyInfo`, `addCompany`, und `getCompanyMembership`.

**userHandle**

Die `userHandle` -Parameter ist ein optionaler Parameter für Vorgänge, die auf einen bestimmten Benutzer abzielen. Standardmäßig zielen diese Vorgänge auf den aufrufenden Benutzer ab (den Benutzer, dessen Anmeldeinformationen zur Authentifizierung übergeben werden). Admin-Benutzer mit den entsprechenden Berechtigungen können jedoch einen anderen Benutzer angeben. Beispiel: die `setPassword` -Vorgang legt normalerweise das Kennwort des authentifizierten Benutzers fest, ein Administrator kann jedoch die `userHandle` -Parameter, um das Kennwort für einen anderen Benutzer festzulegen.

Für Vorgänge, für die ein Unternehmenskontext erforderlich ist (mithilfe der Variablen `companyHandle` -Parameter), müssen sowohl die authentifizierten als auch die Zielbenutzer Mitglieder des angegebenen Unternehmens sein. Bei Vorgängen, für die kein Unternehmenskontext erforderlich ist, müssen die authentifizierten Benutzer und die Zielbenutzer beide Mitglieder von mindestens einem gemeinsamen Unternehmen sein.

Mit den folgenden Vorgängen können Benutzer-Handles abgerufen werden:

* `getUsers`
* `getAllUsers`
* `getUserInfo`
* `getCompanyMembers`
* `getGroupMembers`
* `addUser`

**accessUserHandle und accessGroupHandle**

Vorgänge, für die Zugriffsberechtigungen erforderlich sind (Lesen, Schreiben, Löschen), erfolgen standardmäßig im Berechtigungskontext des aufrufenden Benutzers. Bestimmte Vorgänge ermöglichen es Ihnen, diesen Kontext mit dem `accessUserHandle` oder `accessGroupHandle` -Parameter. Die `accessUserHandle` -Parameter ermöglicht es einem Administrator, die Identität eines anderen Benutzers zu übernehmen. Die `accessGroupHandle` ermöglicht es dem Aufrufer, im Kontext einer bestimmten Benutzergruppe zu arbeiten.

**responseFieldArray und excludeFieldArray**

Bei einigen Vorgängen kann der Aufrufer einschränken, welche Felder in der Antwort enthalten sind. Durch das Eingrenzen von Feldern können Sie die Zeit und den Arbeitsspeicher für die Verarbeitung der Anfrage reduzieren und die Größe der Antwortdaten reduzieren. Der Aufrufer kann eine bestimmte Feldliste anfordern, indem er eine `responseFieldArray` -Parameter oder mit einer Aufzählung der ausgeschlossenen Felder über die `excludeFieldArray` -Parameter.

Beide `responseFieldArray` und `excludeFieldArray` Felder mithilfe eines Knotenpfads angeben, der durch `/`. Um beispielsweise Folgendes anzugeben: `searchAssets` gibt nur den Namen, das Datum der letzten Änderung und die Metadaten für jedes Asset zurück, siehe Folgendes:

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

Beachten Sie, dass die Knotenpfade relativ zum Knoten &quot;return&quot;sind. Wenn Sie ein komplexes Typfeld ohne Unterelemente angeben (z. B. `assetArray/items/imageInfo`), werden alle zugehörigen Unterelemente einbezogen. Wenn Sie ein oder mehrere Unterelemente in einem Feld mit komplexem Typ angeben (z. B. `assetArray/items/imageInfo/originalPath`), werden nur die Unterelemente einbezogen.

Wenn Sie `responseFieldArray` oder `excludeFieldArray` in einer Anforderung werden alle Felder zurückgegeben.

**Gebietsschema**

Seit IPS 4.0 unterstützt die IPS-API das Festlegen des Gebietsschemas eines Vorgangs durch Übergabe der `authHeader` Gebietsschema-Parameter. Wenn der Parameter locale nicht vorhanden ist, wird der HTTP-Header `Accept-Language` verwendet. Wenn diese Kopfzeile ebenfalls nicht vorhanden ist, wird das standardmäßige Gebietsschema für den IPS-Server verwendet.

Bestimmte Vorgänge erfordern auch explizite Gebietsschemaparameter, die sich vom Gebietsschema-Kontext der Vorgänge unterscheiden können. Beispiel: die `submitJob` -Vorgang `locale` -Parameter, der das für die Auftragsprotokollierung und E-Mail-Benachrichtigung verwendete Gebietsschema festlegt.

Gebietsschemaparameter verwenden das Format `<language_code>[-<country_code>]`

Wenn der Sprachencode ein in Kleinbuchstaben verfasster Zweibuchstaben-Code ist, der in ISO-639 spezifiziert ist, und der optionale Ländercode ein in Großbuchstaben verfasster Zweibuchstaben-Code ist, der in ISO-3266 angegeben ist. Die Gebietsschema-Zeichenfolge für US-Englisch lautet beispielsweise `en-US`.
