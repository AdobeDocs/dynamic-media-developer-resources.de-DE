---
description: Image Serving unterstützt das unbegrenzte Verschachteln von Image Serving-Anforderungen, das Einbetten von Image Rendering-Anforderungen sowie das Einbetten von Bildern, die von ausländischen Servern abgerufen werden. Diese Mechanismen werden nur von Ebenenbildern und Ebenenmasken unterstützt.
seo-description: Image Serving unterstützt das unbegrenzte Verschachteln von Image Serving-Anforderungen, das Einbetten von Image Rendering-Anforderungen sowie das Einbetten von Bildern, die von ausländischen Servern abgerufen werden. Diese Mechanismen werden nur von Ebenenbildern und Ebenenmasken unterstützt.
seo-title: Verschachtelung und Einbettung anfordern
solution: Experience Manager
title: Verschachtelung und Einbettung anfordern
topic: Scene7 Image Serving - Image Rendering API
uuid: 59031329-e65f-4631-bc7d-83f2540cc836
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Verschachtelung und Einbettung anfordern{#request-nesting-and-embedding}

Image Serving unterstützt das unbegrenzte Verschachteln von Image Serving-Anforderungen, das Einbetten von Image Rendering-Anforderungen sowie das Einbetten von Bildern, die von ausländischen Servern abgerufen werden. Diese Mechanismen werden nur von Ebenenbildern und Ebenenmasken unterstützt.

>[!NOTE] {class=&quot;- topic/note &quot;
>
>Bestimmte E-Mail-Clients und Proxyserver können die geschweiften Klammern für die Verschachtelungs- und Einbettungssyntax kodieren. Anwendungen, bei denen dies ein Problem ist, sollten Klammern anstelle geschweifter Klammern verwenden.

## Verschachtelte Image Serving-Anforderungen {#section-6954202119e0466f8ff27c79f4f039c8}

Eine gesamte Image Serving-Anforderung kann als Ebenenquelle verwendet werden, indem Sie sie mithilfe der folgenden Syntax im Befehl `src=` (oder `mask=`) angeben:

`…&src=is( nestedRequest)&…`

Beim `is` Token muss die Groß-/Kleinschreibung beachtet werden.

Die verschachtelte Anforderung darf nicht den Serverstammpfad enthalten (in der Regel ` http:// *[!DNL server]*/is/image/'`).

>[!NOTE] {class=&quot;- topic/note &quot;
>
>Die verschachtelten Anforderungstrennzeichen ( `'(',')'`) und die Befehlstrennzeichen ( `'?'`, `'&'`, `'='`) innerhalb verschachtelter Anforderungen dürfen nicht HTTP-kodiert sein. Verschachtelte Anforderungen müssen genauso wie die äußere (Verschachtelungs-) Anforderung kodiert werden.

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

Auch werden ignoriert `attribute::MaxPix`und `attribute::DefaultPix` der Bildkatalog, der für die verschachtelte Anforderung gilt.

Das Bildergebnis einer verschachtelten IS-Anforderung kann optional zwischengespeichert werden, indem `cache=on`sie einbezogen wird. Standardmäßig ist die Zwischenspeicherung von Zwischendaten deaktiviert. Die Zwischenspeicherung sollte nur aktiviert werden, wenn erwartet wird, dass das Zwischenbild in einer anderen Anforderung innerhalb eines angemessenen Zeitraums wiederverwendet wird. Es gilt die standardmäßige serverseitige Cacheverwaltung. Die Daten werden im verlustfreien Format zwischengespeichert.

## Eingebettete Bildwiedergabeanforderungen {#section-69c5548db930412b9b90d9b2951a6969}

Wenn Scene7 Image Rendering auf dem Server aktiviert ist, können Renderanforderungen als Ebenenquellen verwendet werden, indem sie im Befehl src= (oder mask=) angegeben werden. Verwenden Sie die folgende Syntax:

` …&src=ir( *[!DNL renderRequest]*)&…`

Beim `ir` Token muss die Groß-/Kleinschreibung beachtet werden.

*[!DNL renderRequest]* ist die übliche Image Rendering-Anforderung, mit Ausnahme des HTTP-Stammpfads ` http:// *[!DNL server]*/ir/render/`.

>[!NOTE] {class=&quot;- topic/note &quot;
>
>Die verschachtelten Anforderungstrennzeichen ( `'(',')'`) und die Befehlstrennzeichen ( `'?'`, `'&'`, `'='`) innerhalb verschachtelter Anforderungen dürfen nicht HTTP-kodiert sein. Eingebettete Anforderungen müssen genauso kodiert sein wie die äußere (Einbettungsanforderung).

Die folgenden Bildwiedergabebefehle werden ignoriert, wenn sie in verschachtelten Anforderungen angegeben werden:

* `fmt=`
* `qlt=`
* `icc=`
* `iccEmbed=`
* `printRes=`
* `req=`

Auch werden ignoriert `attribute::MaxPix` und `attribute::DefaultPix` der Materialkatalog, der für die verschachtelte Render-Anforderung gilt.

Das Bildergebnis einer verschachtelten IR-Anforderung kann optional zwischengespeichert werden, indem auch `cache=on`die Option einbezogen wird. Standardmäßig ist die Zwischenspeicherung von Zwischendaten deaktiviert. Die Zwischenspeicherung sollte nur aktiviert werden, wenn erwartet wird, dass das Zwischenbild in einer anderen Anforderung innerhalb eines angemessenen Zeitraums wiederverwendet wird. Es gilt die standardmäßige serverseitige Cacheverwaltung. Die Daten werden im verlustfreien Format zwischengespeichert.

## Eingebettete FXG-Renderanforderungen {#section-c817e4b4f7da414ea5a51252ca7e120a}

Wenn der FXG-Grafik-Renderer (alias [!DNL AGMServer]) mit Image Serving installiert und aktiviert ist, können FXG-Anforderungen als Ebenenquellen verwendet werden, indem sie in `src=` (oder `mask=`) Befehlen angegeben werden. Verwenden Sie die folgende Syntax:

`…&src=fxg( renderRequest)&…`

Beim `fxg` Token muss die Groß-/Kleinschreibung beachtet werden.

>[!NOTE] {class=&quot;- topic/note &quot;
>
>Das Rendering von FXG-Grafiken ist nur in der von Scene7 gehosteten Umgebung verfügbar und erfordert möglicherweise zusätzliche Lizenzen. Weitere Informationen erhalten Sie vom Scene7-Support.

*[!DNL renderRequest]* ist die übliche FXG-Renderanforderung, mit Ausnahme des HTTP-Stammpfads ` http:// *[!DNL server]*/agm/render/`.

>[!NOTE] {class=&quot;- topic/note &quot;
>
>Die Trennzeichen ( `'(',')'`) und die Befehlstrennzeichen ( `'?'`, `'&'`, `'='`) in verschachtelten Anforderungen dürfen nicht HTTP-kodiert sein. Eingebettete Anforderungen müssen genauso kodiert sein wie die äußere (Einbettungsanforderung).

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

Um eine ausländische URL für einen `src=` oder einen `mask=` Befehl anzugeben, trennen Sie die ausländische URL oder das URL-Fragment in Klammern:

`…&src=( foreignUrl)&…`

Wichtig: Die Trennzeichen ( `'(',')'`) und die Befehlstrennzeichen ( `'?'`, `'&'`, `'='`) in verschachtelten Anforderungen dürfen nicht HTTP-kodiert sein. Eingebettete Anforderungen müssen genauso kodiert sein wie die äußere (Einbettungsanforderung).

Vollständige absolute URLs (sofern festgelegt) und URLs relativ zu `attribute::AllowDirectUrls` `attribute::RootUrl` diesen sind zulässig. Ein Fehler tritt auf, wenn eine absolute URL eingebettet und ein Attribut: ist 0 `AllowDirectUrls` oder wenn eine relative URL angegeben ist und leer `attribute::RootUrl` ist.

Wenngleich ausländische URLs nicht direkt in der Pfadkomponente der Anforderungs-URL angegeben werden können, ist es möglich, eine Vorverarbeitungsregel einzurichten, um die Konvertierung relativer Pfade in absolute URLs zu ermöglichen (siehe Beispiel unten).

Ausländische Bilder werden vom Server gemäß den in der HTTP-Antwort enthaltenen Cache-Headern zwischengespeichert. Wenn weder ein `ETag` noch ein Last-Modified HTTP-Antwort-Header vorhanden ist, wird die Antwort nicht zwischengespeichert. Dies kann zu einer schlechten Leistung bei Wiederholungszugriffen für dasselbe fremde Bild führen, da Image Serving das Bild bei jedem Zugriff neu abrufen und überprüfen muss.

Dieser Mechanismus unterstützt dieselben Bilddateiformate, die vom Dienstprogramm &quot;Bildkonvertierung&quot;(IC) unterstützt werden, mit Ausnahme von Quellbildern mit 16 Bit pro Komponente.

>[!NOTE] {class=&quot;- topic/note &quot;
>
>Image Serving führt automatisch das Überprüfungsprogramm aus, wenn ein fremdes Bild zum ersten Mal verwendet wird, um sicherzustellen, dass das Bild gültig ist und während der Übertragung nicht beschädigt wurde. Dies kann beim ersten Zugriff zu einer leichten Verzögerung führen. Für eine optimale Leistung wird empfohlen, die Größe solcher Bilder zu begrenzen und/oder ein Bilddateiformat zu verwenden, das gut komprimiert wird.

## Restrictions {#section-fb68e3f0d40947feb94d7bf183b64929}

Die Größe des Bildes, das durch verschachtelte/eingebettete Anforderungen generiert wurde, wird normalerweise automatisch optimiert. Wenn die Zwischenspeicherung von verschachtelten Anforderungsbildern aktiviert ist, können durch Angabe der exakten Größe des verschachtelten Bildes inkrementelle Leistungssteigerungen erzielt werden, sodass bei der Wiederverwendung des Cache-Eintrags keine weitere Skalierung erforderlich ist.

Beim wichtigen Image-Server wird die Dublette von verschachtelten oder eingebetteten Anforderungen nicht unterstützt. Verschachtelte und eingebettete Anforderungen müssen wie einfache Anforderungen HTTP-kodiert sein.

## Beispiele {#section-d800cfc31abe46d2a964f8e7929231f1}

**Ebenenvorlage mit Zwischenspeicherung:**

Verwenden Sie die Verschachtelung, um einer Ebenenvorlage die Zwischenspeicherung hinzuzufügen. Eine begrenzte Anzahl von Hintergrundbildern wird mit stark variablem Text überlagert. Die anfängliche Vorlagenzeichenfolge könnte wie folgt aussehen:

`layer=0&src=$img$&size=300,300&layer=1&text=$txt$`

Mit leichten Änderungen können Sie das Bild der Ebene 0 vorskalieren und dauerhaft zwischenspeichern, um so die Serverlast zu reduzieren:

`layer=0&src=is(?src=$img$&size=300,300&cache=on)&layer=1&text=$txt$`

**Einbetten von Anforderungen für Scene7-Image Rendering**

Verwenden einer in [!DNL myCatalog/myTemplate]gespeicherten Vorlage; Erstellen Sie das Bild für Ebene2 der Vorlage mit Scene7 Image Rendering:

`http://server/is/image/myCatalog/myTemplate?layer=2&src=ir(myRenderCatalog/myRenderObject?id=myIdValue&sel=group&src=is(myCatalog/myTexture1?res=30)&res=30)&wid=300`

Beachten Sie die geschachtelten geschachtelten geschweiften Klammern. Die Image Rendering-Anforderung bettet einen Aufruf an Image Serving ein, um eine wiederholbare Textur abzurufen.

## Verwandte Themen {#section-109a0a9a3b144158958351139c8b8e69}

[src=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-src.md#reference-f6506637778c4c69bf106a7924a91ab1) , [mask=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-mask.md#reference-922254e027404fb890b850e2723ee06e), [Request PreProcessing](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-request-preprocessing.md#reference-c27976436bf04194bfbe9adf40ea98e3), Image Rendering Reference, [Templates](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e), [Image Serving Utilities](../../../../../is-api/is-utils/utilities/c-location-of-utilities.md#concept-bae61e53344449af978502cac6be8b5f)
