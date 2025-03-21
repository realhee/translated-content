---
title: DataView.prototype.getInt16()
slug: Web/JavaScript/Reference/Global_Objects/DataView/getInt16
tags:
  - DataView
  - JavaScript
  - Méthode
  - Prototype
  - Reference
  - TypedArrays
translation_of: Web/JavaScript/Reference/Global_Objects/DataView/getInt16
original_slug: Web/JavaScript/Reference/Objets_globaux/DataView/getInt16
---
{{JSRef}}

La méthode **`getInt16()`** permet de lire un entier signé sur 16 bits (type _short_ par analogie avec C) à l'octet donné par rapport au début de {{jsxref("DataView")}}.

{{EmbedInteractiveExample("pages/js/dataview-getint16.html")}}

## Syntaxe

    dataview.getInt16(positionOctet [, littleEndian])

### Paramètres

- `positionOctet`
  - : La position, exprimée en nombre d'octets depuis le début de la vue, à laquelle lire les données.
- `littleEndian`
  - : {{optional_inline}} indique si la valeur sur 16 bits est enregistrée dans l'ordre des octets {{Glossary("Endianness", "de poids faible")}}. Si le paramètre vaut `false` ou `undefined`, la valeur sera lue dans l'ordre des octets de poids forts.

### Valeur de retour

Un entier signé sur 16 bits.

### Erreurs renvoyées

- {{jsxref("RangeError")}}
  - : Renvoyée si `positionOctet` est tel qu'il est en dehors de la vue.

## Description

Il n'y a pas de contrainte d'alignement, les valeurs codées sur plusieurs octets peuvent être obtenues depuis n'importe quelle position.

## Exemples

### Utilisation de la méthode `getInt16`

```js
var buffer = new ArrayBuffer(8);
var dataview = new DataView(buffer);
dataview.getInt16(1); // 0
```

## Spécifications

| Spécification                                                                                                            | État                             | Commentaires                                    |
| ------------------------------------------------------------------------------------------------------------------------ | -------------------------------- | ----------------------------------------------- |
| {{SpecName('Typed Array')}}                                                                                     | {{Spec2('Typed Array')}} | Remplacée dans ECMAScript 2015.                 |
| {{SpecName('ES2015', '#sec-dataview.prototype.getint16', 'DataView.prototype.getInt16')}} | {{Spec2('ES2015')}}         | Définition initiale au sein d'un standard ECMA. |
| {{SpecName('ESDraft', '#sec-dataview.prototype.getint16', 'DataView.prototype.getInt16')}} | {{Spec2('ESDraft')}}     |                                                 |

## Compatibilité des navigateurs

{{Compat("javascript.builtins.DataView.getInt16")}}

## Voir aussi

- {{jsxref("DataView")}}
- {{jsxref("ArrayBuffer")}}
