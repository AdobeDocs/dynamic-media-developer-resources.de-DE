---
title: Befehlsmakros
description: Befehlsmakros bieten benannte Tastaturbefehle für Befehlssätze.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 00f6d27e-9f6b-4eea-8f42-833fbc0f1c38
TQID: 'https://experienceleague.adobe.com/cXLJJQ5CS-Apmq-8qYV-ew-lcvfRjoNfIbl2qyyKB6U'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 4339f336345d7d7f3c05c7f5a18fbd28bcfd382b
workflow-type: tm+mt
source-wordcount: 232
ht-degree: 0%

---

# Befehlsmakros{#command-macros}

Befehlsmakros bieten benannte Tastaturbefehle für Befehlssätze.

`$ *[!DNL name]*$`

** *[!DNL name]* ** Makronamen

Makros werden in separaten Makrodefinitionsdateien definiert, die an Materialkataloge oder den Standardkatalog angehängt werden können.

*[!DNL name]* wird nicht zwischen Groß- und Kleinschreibung unterschieden und kann aus einer beliebigen Kombination von ASCII-Buchstaben, Zahlen , &#39;-&#39;, &#39;_&#39; und &#39;.&#39;-Zeichen bestehen.

Makros an einer beliebigen Stelle in einer Anfrage nach dem &quot;?“ oder an einer beliebigen Stelle in einem `vignette::Modifier` Feld aufrufen. Makros können nur einen oder mehrere Image-Rendering-Befehle darstellen und müssen von anderen Befehlen mit &quot;&amp;&quot;-Trennzeichen getrennt werden.

Makroaufrufe werden durch ihre Ersatzzeichenfolgen frühzeitig während der Analyse ersetzt. Befehle in Makros überschreiben dieselben Befehle in der Anfrage, wenn sie vor dem Makroaufruf in der Anfrage auftreten. Dieser Workflow unterscheidet sich von `vignette::Modifier`, bei dem Befehle in der Anfragezeichenfolge Befehle in der `vignette::Modifier`-Zeichenfolge überschreiben, unabhängig von der Position in der Anfrage.

Befehlsmakros dürfen keine Argumentwerte enthalten, jedoch können benutzerdefinierte Variablen verwendet werden, um Werte aus der Anforderung an das Makro zu übergeben.

Makros dürfen nicht verschachtelt sein.

**Beispiel**

Makros können hilfreich sein, wenn dieselben Befehle oder Attribute auf verschiedene gerenderte Bilder angewendet werden sollen.

`http://server/ir/render/cat/vig0?fmt=jpeg&qlt=80&sharpen=1&src=cat/matA&res=40 http://server/ir/render/cat/vig1?fmt=jpeg&qlt=80&sharpen=1&src=cat/matB&res=40 http://server/ir/render/cat/vig2?fmt=jpeg&qlt=95&sharpen=1&src=cat/matC&res=40`

Sie können ein Makro für die allgemeinen Attribute definieren:

`render vignette=cat/$vig$&fmt=jpg&qlt=80&sharpen=1&src=cat/$mat$&res=40`

Das Makro würde wie folgt verwendet:

`http://server/ir/render/cat/vig0?$mat=matc&$render$ http://server/ir/render/cat/vig0?$mat=matc&$render$ http://server/ir/render/cat/vig0?$mat=matc&$render$&qlt=95`

Da `qlt=` für die dritte Anfrage unterschiedlich ist, überschreibt die Software den Wert, nachdem das Makro aufgerufen wurde (die Angabe von `qlt=` *before* `$render$` ist ineffektiv).

**Siehe auch**

`catalog::MacroFile`, `catalog::Modifier`, Referenz zur Makrodefinition

<!--<a id="section_297B7FCB285F4891AA76DF8393089931"></a>-->

