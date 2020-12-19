---
description: Löschen Sie alle Attribute für eine angegebene s7 elementID.
seo-description: Löschen Sie alle Attribute für eine angegebene s7 elementID.
seo-title: deleteAttr
solution: Experience Manager
title: deleteAttr
topic: Scene7 Image Serving - Image Rendering API
uuid: b1176c1a-9ec3-4a95-9f91-97f9f168c252
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '58'
ht-degree: 1%

---


# deleteAttr{#deleteattr}

Löschen Sie alle Attribute für eine gegebene s7:elementID.

`deleteAttr.elementID={attributeName%26attributeName}`

Wenn für ein FXG-Knotenelement ein `s7:elementID` definiert ist, können die Attribute für diesen Knoten mit diesem Befehl gelöscht werden.

## Beispiel {#section-dece7192384a412c9afdfbda6f08bc97}

`<Group x="130.494" y="102.2246" d:id="4" d:type="layer" d:userLabel="WhiteFrame" visible="true" s7:elementID="middle_area">`

`deleteAttr.middle_area={x%26y%26visible}`

`<Group d:id="4" d:type="layer" d:userLabel="WhiteFrame" s7:elementID="middle_area">`

In diesem Beispiel werden die Attribute *[!DNL x]*, *[!DNL y]* und *[!DNL visible]* aus dem ursprünglichen FXG-Knoten entfernt.
