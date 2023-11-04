---
description: Image Serving unterstützt eine unbegrenzte Verschachtelung von Image Serving-Anforderungen, das Einbetten von Image Rendering-Anforderungen sowie das Einbetten von Bildern, die von ausländischen Servern abgerufen werden. Diese Mechanismen werden nur von Ebenenbildern und Ebenenmasken unterstützt.
solution: Experience Manager
title: Verschachtelung und Einbettung anfordern
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: b9c9d241-5a3d-4637-a90a-d8cdf29cc968
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '1044'
ht-degree: 0%

---

# Verschachtelung und Einbettung anfordern{#request-nesting-and-embedding}

Image Serving unterstützt eine unbegrenzte Verschachtelung von Image Serving-Anforderungen, das Einbetten von Image Rendering-Anforderungen sowie das Einbetten von Bildern, die von ausländischen Servern abgerufen werden. Diese Mechanismen werden nur von Ebenenbildern und Ebenenmasken unterstützt.

>[!NOTE]
>
>Bestimmte E-Mail-Clients und Proxy-Server können die geschweiften Klammern für die Verschachtelungs- und Einbettungssyntax kodieren. Anwendungen, bei denen dies ein Problem darstellt, sollten Klammern anstelle geschweifte Klammern verwenden.

## Verschachtelte Image-Serving-Anforderungen {#section-6954202119e0466f8ff27c79f4f039c8}

Eine gesamte Image Serving-Anfrage kann als Ebenenquelle verwendet werden, indem sie sie in der `src=` (oder `mask=`) unter Verwendung der folgenden Syntax verwenden:

`…&src=is( nestedRequest)&…`

Die `is` Beim Token wird zwischen Groß- und Kleinschreibung unterschieden.

Die verschachtelte Anforderung darf nicht den Serverstammpfad enthalten (normalerweise ` http:// *[!DNL server]*/is/image/'`).

>[!NOTE]
>
>Die verschachtelten Trennzeichen für Anforderungen ( `'(',')'`) und die Befehlstrennzeichen ( `'?'`, `'&'`, `'='`) innerhalb verschachtelter Anforderungen darf nicht HTTP-kodiert sein. Verschachtelte Anforderungen müssen genauso wie die äußere (Verschachtelungs-) Anforderung kodiert werden.

Vorverarbeitungsregeln werden auf verschachtelte Anforderungen angewendet.

Die folgenden Befehle werden ignoriert, wenn sie in verschachtelten Anforderungen angegeben werden (entweder in der Anforderungs-URL oder in `catalog::Modifier` oder `catalog::PostModifier`):

* `fmt=`
* `qlt=`
* `iccEmbed=`
* `printRes=`
* `quantize=`
* `req=`
* `bgc=`

Wenn das Ergebnisbild der verschachtelten Anforderungen Maskendaten (Alpha) enthält, wird es als Ebenenmaske an die Einbettungsebene übergeben.

Auch ignoriert `attribute::MaxPix`und `attribute::DefaultPix` des Bildkatalogs, der für die verschachtelte Anforderung gilt.

Das Bildergebnis einer verschachtelten IS-Anforderung kann optional zwischengespeichert werden, indem `cache=on`. Standardmäßig ist die Zwischenspeicherung von Zwischendaten deaktiviert. Die Zwischenspeicherung sollte nur aktiviert werden, wenn erwartet wird, dass das Zwischenbild innerhalb eines angemessenen Zeitraums in einer anderen Anforderung wiederverwendet wird. Es gilt die standardmäßige serverseitige Cacheverwaltung. Die Daten werden verlustfrei zwischengespeichert.

## Eingebettete Bildwiedergabeanforderungen {#section-69c5548db930412b9b90d9b2951a6969}

Wenn die Dynamic Media-Bildwiedergabe auf dem Server aktiviert ist, können Renderanforderungen als Ebenenquellen verwendet werden, indem sie sie im Befehl src= (oder mask=) angeben. Verwenden Sie die folgende Syntax:

` …&src=ir( *[!DNL renderRequest]*)&…`

Die `ir` Beim Token wird zwischen Groß- und Kleinschreibung unterschieden.

*[!DNL renderRequest]* ist die übliche Image Rendering-Anforderung, mit Ausnahme des HTTP-Stammpfads ` http:// *[!DNL server]*/ir/render/`.

>[!NOTE]
>
>Die verschachtelten Trennzeichen für Anforderungen ( `'(',')'`) und die Befehlstrennzeichen ( `'?'`, `'&'`, `'='`) innerhalb verschachtelter Anforderungen darf nicht HTTP-kodiert sein. Eingebettete Anforderungen müssen genauso kodiert sein wie die äußere (Einbettungs-) Anforderung.

Die folgenden Image Rendering-Befehle werden ignoriert, wenn sie in verschachtelten Anforderungen angegeben werden:

* `fmt=`
* `qlt=`
* `icc=`
* `iccEmbed=`
* `printRes=`
* `req=`

Auch ignoriert `attribute::MaxPix` und `attribute::DefaultPix` des Materialkatalogs, der für die verschachtelte Renderanforderung gilt.

Das Bildergebnis einer verschachtelten IR-Anforderung kann optional zwischengespeichert werden, indem `cache=on`. Standardmäßig ist die Zwischenspeicherung von Zwischendaten deaktiviert. Die Zwischenspeicherung sollte nur aktiviert werden, wenn erwartet wird, dass das Zwischenbild innerhalb eines angemessenen Zeitraums in einer anderen Anforderung wiederverwendet wird. Es gilt die standardmäßige serverseitige Cacheverwaltung. Die Daten werden verlustfrei zwischengespeichert.

## Eingebettete FXG-Renderanforderungen {#section-c817e4b4f7da414ea5a51252ca7e120a}

Wenn der FXG-Grafikrenderer (auch [!DNL AGMServer]) mit Image Serving installiert und aktiviert ist, können FXG-Anforderungen als Ebenenquellen verwendet werden, indem sie sie in `src=` (oder `mask=`). Verwenden Sie die folgende Syntax:

`…&src=fxg( renderRequest)&…`

Die `fxg` Beim Token wird zwischen Groß- und Kleinschreibung unterschieden.

>[!NOTE]
>
>Das Rendering von FXG-Grafiken ist nur in der von Dynamic Media gehosteten Umgebung verfügbar und erfordert möglicherweise zusätzliche Lizenzen. Weitere Informationen erhalten Sie vom technischen Support von Dynamic Media.

*[!DNL renderRequest]* ist die übliche FXG-Renderanforderung, mit Ausnahme des HTTP-Stammpfads ` http:// *[!DNL server]*/agm/render/`.

>[!NOTE]
>
>Die Trennzeichen ( `'(',')'`) und die Befehlstrennzeichen ( `'?'`, `'&'`, `'='`) innerhalb verschachtelter Anforderungen darf nicht HTTP-kodiert sein. Eingebettete Anforderungen müssen genauso kodiert sein wie die äußere (Einbettungs-) Anforderung.

Die folgenden FXG-Befehle werden ignoriert, wenn sie in verschachtelten Anforderungen angegeben werden:

* `fmt=`
* `qlt=`
* `icc=`
* `iccEmbed=`
* `cache=`

## Ausländische Bildquellen {#section-84e83ecfcd1a43748cdfc7a6f8c04cb8}

Image Serving unterstützt den Zugriff auf Quellbilder auf ausländischen HTTP-Servern.

>[!NOTE]
>
>Für Remote-URLs wird nur das HTTP-Protokoll unterstützt.

So legen Sie eine fremde URL für eine `src=` oder `mask=` -Befehl, trennen Sie die ausländische URL oder das URL-Fragment mit Klammern:

`…&src=( foreignUrl)&…`

Wichtig Die Trennzeichen ( `'(',')'`) und die Befehlstrennzeichen ( `'?'`, `'&'`, `'='`) innerhalb verschachtelter Anforderungen darf nicht HTTP-kodiert sein. Eingebettete Anforderungen müssen genauso kodiert sein wie die äußere (Einbettungs-) Anforderung.

Vollständige absolute URLs (wenn `attribute::AllowDirectUrls` festgelegt ist) und URLs relativ zu `attribute::RootUrl` sind erlaubt. Ein Fehler tritt auf, wenn eine absolute URL eingebettet und das Attribut: `AllowDirectUrls` 0 ist oder wenn eine relative URL angegeben ist und `attribute::RootUrl` leer ist.

Auch wenn ausländische URLs nicht direkt in der Pfadkomponente der Anfrage-URL angegeben werden können, ist es möglich, eine Vorverarbeitungsregel einzurichten, um die Konvertierung relativer Pfade zu absoluten URLs zu ermöglichen (siehe Beispiel unten).

Ausländische Bilder werden vom Server gemäß den in der HTTP-Antwort enthaltenen Zwischenspeicherkopfzeilen zwischengespeichert. Wenn weder `ETag` noch ein HTTP-Antwort-Header mit der letzten Änderung vorhanden ist, wird die Antwort nicht zwischengespeichert. Dies kann zu einer schlechten Leistung bei Wiederholungszugriffen für dasselbe ausländische Bild führen, da die Bildbearbeitung das Bild bei jedem Zugriff neu abrufen und überprüfen muss.

Dieser Mechanismus unterstützt dieselben Bilddateiformate, die vom Dienstprogramm Image Convert (IC) unterstützt werden, mit Ausnahme von Quellbildern mit 16 Bit pro Komponente.

>[!NOTE]
>
>Image Serving führt automatisch das Überprüfungsdienstprogramm aus, wenn ein externes Bild zum ersten Mal verwendet wird, um sicherzustellen, dass das Bild gültig ist und während der Übertragung nicht beschädigt wurde. Dies kann zu einer leichten Verzögerung beim ersten Zugriff führen. Für eine optimale Leistung wird empfohlen, die Größe solcher Bilder zu begrenzen und/oder ein Bilddateiformat zu verwenden, das gut komprimiert ist.

## Einschränkungen {#section-fb68e3f0d40947feb94d7bf183b64929}

Die Größe des von verschachtelten/eingebetteten Anforderungen generierten Bildes wird normalerweise automatisch optimiert. Wenn die Zwischenspeicherung verschachtelter Anfragebilder aktiviert ist, können durch Angabe der exakten Größe des verschachtelten Bildes inkrementelle Leistungssteigerungen erzielt werden, sodass bei der Wiederverwendung des Cache-Eintrags keine weitere Skalierung erforderlich ist.

&quot;Wichtiges Image Serving&quot;unterstützt keine doppelte Kodierung verschachtelter oder eingebetteter Anforderungen. Verschachtelte und eingebettete Anforderungen müssen wie einfache Anforderungen HTTP-kodiert sein.

## Beispiele {#section-d800cfc31abe46d2a964f8e7929231f1}

**Ebenenvorlage mit Zwischenspeicherung:**

Verwenden Sie die Verschachtelung, um die Zwischenspeicherung zu einer Ebenenvorlage hinzuzufügen. Eine begrenzte Anzahl von Hintergrundbildern wird mit stark variablem Text überlagert. Die anfängliche Vorlagenzeichenfolge könnte wie folgt aussehen:

`layer=0&src=$img$&size=300,300&layer=1&text=$txt$`

Bei geringfügigen Änderungen können wir das Bild der Ebene 0 vorskalieren und dauerhaft zwischenspeichern, wodurch die Serverlast reduziert wird:

`layer=0&src=is(?src=$img$&size=300,300&cache=on)&layer=1&text=$txt$`

**Einbetten von Anforderungen für Dynamic Media Image Rendering**

Verwenden einer in gespeicherten Vorlage [!DNL myCatalog/myTemplate]; generieren Sie das Bild für Layer2 der Vorlage mithilfe des Dynamic Media Image Rendering:

`http://server/is/image/myCatalog/myTemplate?layer=2&src=ir(myRenderCatalog/myRenderObject?id=myIdValue&sel=group&src=is(myCatalog/myTexture1?res=30)&res=30)&wid=300`

Beachten Sie die geschachtelten geschachtelten geschweiften Klammern. Die Image Rendering-Anfrage bettet einen Aufruf zurück an Image Serving ein, um eine wiederholbare Textur abzurufen.

## Verwandte Themen {#section-109a0a9a3b144158958351139c8b8e69}

[src=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-src.md#reference-f6506637778c4c69bf106a7924a91ab1) , [mask=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-mask.md#reference-922254e027404fb890b850e2723ee06e), [Request PreProcessing](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-request-preprocessing.md#reference-c27976436bf04194bfbe9adf40ea98e3), Bild-Rendering-Referenz, [Vorlagen](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e), [Image Serving Utilities](../../../../../is-api/is-utils/utilities/c-location-of-utilities.md#concept-bae61e53344449af978502cac6be8b5f)
