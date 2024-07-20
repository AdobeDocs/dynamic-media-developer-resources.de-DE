---
title: Befehlsmakros
description: Befehlsmakros bieten spezifische Tastaturbefehle für Befehlssätze.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 00f6d27e-9f6b-4eea-8f42-833fbc0f1c38
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '232'
ht-degree: 0%

---

# Befehlsmakros{#command-macros}

Befehlsmakros bieten spezifische Tastaturbefehle für Befehlssätze.

`$ *[!DNL name]*$`

** *[!DNL name]* ** Makroname

Makros werden in separaten Makrodefinitionsdateien definiert, die an Materialkataloge oder den Standardkatalog angehängt werden können.

*[!DNL name]* unterscheidet nicht zwischen Groß- und Kleinschreibung und kann aus einer beliebigen Kombination aus ASCII-Buchstaben, Zahlen , &#39;-&#39;, &#39;_&#39; und &#39;.&#39; bestehen. Zeichen.

Rufen Sie Makros an einer beliebigen Stelle in einer Anforderung nach dem &quot;?&quot;oder an einer beliebigen Stelle in einem `vignette::Modifier` -Feld auf. Makros können nur einen oder mehrere Image Rendering-Befehle darstellen und müssen von anderen Befehlen mit &quot;&amp;&quot;Trennzeichen getrennt werden.

Makroaufrufe werden während des Parsens durch ihre Ersatzzeichenfolgen ersetzt. Befehle in Makros überschreiben dieselben Befehle in der Anfrage, wenn sie vor dem Makroaufruf in der Anfrage auftreten. Dieser Workflow unterscheidet sich von `vignette::Modifier`, bei dem Befehle in der Anforderungszeichenfolge Befehle in der Zeichenfolge `vignette::Modifier` außer Kraft setzen, unabhängig von der Position in der Anforderung.

Befehlsmakros können keine Argumentwerte haben, aber benutzerdefinierte Variablen können verwendet werden, um Werte aus der Anfrage an das Makro zu übergeben.

Makros können nicht verschachtelt sein.

**Beispiel**

Makros können nützlich sein, wenn dieselben Befehle oder Attribute auf verschiedene gerenderte Bilder angewendet werden sollen.

`http://server/ir/render/cat/vig0?fmt=jpeg&qlt=80&sharpen=1&src=cat/matA&res=40 http://server/ir/render/cat/vig1?fmt=jpeg&qlt=80&sharpen=1&src=cat/matB&res=40 http://server/ir/render/cat/vig2?fmt=jpeg&qlt=95&sharpen=1&src=cat/matC&res=40`

Sie können ein Makro für die allgemeinen Attribute definieren:

`render vignette=cat/$vig$&fmt=jpg&qlt=80&sharpen=1&src=cat/$mat$&res=40`

Das Makro würde wie folgt verwendet:

`http://server/ir/render/cat/vig0?$mat=matc&$render$ http://server/ir/render/cat/vig0?$mat=matc&$render$ http://server/ir/render/cat/vig0?$mat=matc&$render$&qlt=95`

Da `qlt=` für die dritte Anforderung unterschiedlich ist, überschreibt die Software den Wert, nachdem das Makro aufgerufen wurde (wobei `qlt=` *vor* `$render$`nicht aktiv ist).

**Siehe auch**

`catalog::MacroFile`, `catalog::Modifier`, Referenz zur Makrodefinition

<!--<a id="section_297B7FCB285F4891AA76DF8393089931"></a>-->
