---
description: Der Abschnitt "Abfrage"von Anforderungen und Vignettenmodifizierer-Zeichenfolgen kann benutzerdefinierte Variablen enthalten.
seo-description: Der Abschnitt "Abfrage"von Anforderungen und Vignettenmodifizierer-Zeichenfolgen kann benutzerdefinierte Variablen enthalten.
seo-title: Benutzerdefinierte Variablen
solution: Experience Manager
title: Benutzerdefinierte Variablen
topic: Scene7 Image Serving - Image Rendering API
uuid: 933fba00-759c-4bd3-bada-eec751426d9e
translation-type: tm+mt
source-git-commit: e8e5b07329bde3e23ee095d5022da62d67e9478c
workflow-type: tm+mt
source-wordcount: '260'
ht-degree: 0%

---


# Custom variables{#custom-variables}

Der Abschnitt &quot;Abfrage&quot;von Anforderungen und die Zeichenfolgen &quot;vignette::Modifier&quot;können benutzerdefinierte Variablen enthalten.

` $ *[!DNL name]*= *[!DNL value]*`

** *[!DNL name]* **Variable name. Kann aus einer beliebigen Kombination aus Alpha-, Ziffernzeichen- und sicheren Zeichen bestehen, mit Ausnahme von &#39;$&#39;.

** *[!DNL value]* ** Wert, auf den die Variable gesetzt werden soll (Zeichenfolge).

Variablen werden ähnlich wie andere Serverbefehle definiert, wobei die obige Syntax verwendet wird. Variablen müssen definiert werden, bevor auf sie verwiesen werden kann. Variablen, die in definiert sind, `vignette::Modifier` können in der URL-Anforderung referenziert werden und umgekehrt.

>[!NOTE]
>
>*[!DNL value]* muss für eine sichere HTTP-Übertragung mit einem Pass URL-kodiert sein. Eine Dublette-Kodierung ist erforderlich, wenn die Übertragung über HTTP erfolgt. *[!DNL value]* Dies ist der Fall, wenn eine verschachtelte ausländische Anforderung ersetzt *[!DNL value]* wird.

Variablen werden referenziert, indem der Variablenname (durch einen vorangestellten und einen nachfolgenden $) an einer beliebigen Stelle in Befehlswerte eingebettet wird. Beispiel: zwischen dem &#39;=&#39; hinter dem Befehlsnamen und dem nachfolgenden &#39;&amp;&#39; oder dem Ende der Anforderung. Der Server ersetzt jedes dieser Vorkommen von $ *[!DNL name]*$ durch *[!DNL string]*. Bei Vorkommen von $ *[!DNL name]*$ in Befehlsnamen (vor dem Gleichheitszeichen eines Befehls) und im Pfadteil der Anforderung werden keine Ersetzungen vorgenommen.

Benutzerdefinierte Variablen werden möglicherweise nicht verschachtelt. Vorkommnisse von $ *[!DNL name]*$ innerhalb *[!DNL string]* werden nicht ersetzt. Das Anforderungsfragment `$var2=apple&$var1=my$var2$tree&text=$var1$` wird beispielsweise in `text=my$var2$tree`aufgelöst.

$ ist kein reserviertes Zeichen; es kann andernfalls in der Anforderung auftreten. Beispiel: `src=my$texture$file.tif` ist ein gültiger Befehl (vorausgesetzt, dass ein Materialkatalogeintrag oder eine Texturdatei mit dem Namen [!DNL my$texture$file.tif] vorhanden ist), `wid=$number$` dies jedoch nicht, da ein numerisches Argument erforderlich `wid=` ist.
