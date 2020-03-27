---
description: Befehlsmakros stellen benannte Tastaturbefehle für Befehlssätze bereit.
seo-description: Befehlsmakros stellen benannte Tastaturbefehle für Befehlssätze bereit.
seo-title: Befehlsmakros *
solution: Experience Manager
title: Befehlsmakros *
topic: Scene7 Image Serving - Image Rendering API
uuid: 0a131488-6296-4c7f-9bc7-3053df908899
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef

---


# Befehlsmakros *{#command-macros}

Befehlsmakros stellen benannte Tastaturbefehle für Befehlssätze bereit.

`$ *[!DNL name]*$`

** *[!DNL name]* ** Makroname

Makros sind in separaten Makro-Definitionsdateien definiert, die an Materialkataloge oder den Standardkatalog angehängt werden können.

*[!DNL name]* nicht zwischen Groß- und Kleinschreibung unterscheidet und aus einer beliebigen Kombination von ASCII-Buchstaben, -Zahlen, -Zeichen, -Zeichen, -Zeichen und -Zeichen bestehen kann. Zeichen.

Rufen Sie Makros an einer beliebigen Stelle in einer Anforderung nach dem &#39;?&#39; oder an einer beliebigen Stelle innerhalb eines `vignette::Modifier` Felds auf. Makros können nur einen oder mehrere vollständige Bildwiedergabebefehle darstellen und müssen von anderen Befehlen mit &quot;&amp;&quot;getrennt werden.

Makroaufrufe werden während der Analyse durch ihre Ersatzzeichenfolgen ersetzt. Befehle in Makros setzen dieselben Befehle in der Anforderung außer Kraft, wenn sie vor dem Makroaufruf in der Anforderung auftreten. Dies unterscheidet sich von `vignette::Modifier`dem, bei dem Befehle in der Anforderungszeichenfolge Befehle in der `vignette::Modifier` Zeichenfolge immer außer Kraft setzen, unabhängig von der Position in der Anforderung.

Befehlsmakros können keine Argumentwerte haben, aber benutzerdefinierte Variablen können verwendet werden, um Werte aus der Anforderung an das Makro zu übergeben.

Makros können nicht verschachtelt sein.

**Beispiel**

Makros können nützlich sein, wenn dieselben Befehle oder Attribute auf verschiedene gerenderte Bilder angewendet werden sollen.

`http://server/ir/render/cat/vig0?fmt=jpeg&qlt=80&sharpen=1&src=cat/matA&res=40 http://server/ir/render/cat/vig1?fmt=jpeg&qlt=80&sharpen=1&src=cat/matB&res=40 http://server/ir/render/cat/vig2?fmt=jpeg&qlt=95&sharpen=1&src=cat/matC&res=40`

Sie können ein Makro für die allgemeinen Attribute definieren:

`render vignette=cat/$vig$&fmt=jpg&qlt=80&sharpen=1&src=cat/$mat$&res=40`

Das Makro wird wie folgt verwendet:

`http://server/ir/render/cat/vig0?$mat=matc&$render$ http://server/ir/render/cat/vig0?$mat=matc&$render$ http://server/ir/render/cat/vig0?$mat=matc&$render$&qlt=95`

Da die dritte Anforderung unterschiedlich `qlt=` ist, überschreiben wir den Wert einfach, nachdem das Makro aufgerufen wurde (Angabe `qlt=`*vor *`$render$`hat keine Auswirkungen).

**Verwandte Themen**

`catalog::MacroFile`, `catalog::Modifier`Makrodefinitionsreferenz

<!--<a id="section_297B7FCB285F4891AA76DF8393089931"></a>-->

