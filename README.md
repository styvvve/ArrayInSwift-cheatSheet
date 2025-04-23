# 📘 Swift Array Cheat Sheet

## 🔹 Création
- `Array(repeating: value, count: n)` : Crée un array avec *n* fois la même valeur.
- `[]` : Array vide.
- `[Type]()` : Initialisation vide avec type explicite.

## 🔹 Propriétés
- `array.count` : Nombre d'éléments.
- `array.isEmpty` : Booléen, vrai si l'array est vide.
- `array.first` : Premier élément (optionnel).
- `array.last` : Dernier élément (optionnel).
- `array.capacity` : Capacité actuelle en mémoire.
- `array.indices` : Indices valides de l'array.
- `array.startIndex`, `array.endIndex` : Début et fin des indices.

## 🔹 Accès & sous-ensembles
- `array[i]` : Accès à l'élément à l'indice *i*.
- `array[start..<end]` : Sous-array.
- `array.prefix(n)` : Premiers *n* éléments.
- `array.suffix(n)` : Derniers *n* éléments.
- `array.dropFirst(n)` : Ignore les *n* premiers.
- `array.dropLast(n)` : Ignore les *n* derniers.

## 🔹 Modification (mutating)
- `array.append(x)` : Ajoute *x* à la fin.
- `array.append(contentsOf: xs)` : Ajoute plusieurs éléments.
- `array.insert(x, at: i)` : Insère *x* à l'indice *i*.
- `array.insert(contentsOf: xs, at: i)` : Insère plusieurs.
- `array.remove(at: i)` : Supprime l'élément à *i*.
- `array.removeFirst()` / `removeLast()` : Supprime premier / dernier.
- `array.removeAll()` : Vide l'array.
- `array.removeSubrange(range)` : Supprime une plage.
- `array.replaceSubrange(range, with: xs)` : Remplace une plage.
- `array.reserveCapacity(n)` : Réserve de la mémoire.
- `array.swapAt(i, j)` : Échange deux éléments.
- `array.sort()` : Trie sur place.
- `array.reverse()` : Inverse l'ordre.

## 🔹 Transformation / lecture
- `array.map { ... }` : Transforme chaque élément.
- `array.compactMap { ... }` : Ignore les `nil`.
- `array.flatMap { ... }` : Aplati un niveau.
- `array.filter { ... }` : Garde ceux qui passent le test.
- `array.reduce(init) { acc, x in ... }` : Accumule une valeur.
- `array.reduce(into: init) { acc, x in ... }` : Variante plus rapide.
- `array.forEach { ... }` : Itère sans retour.
- `array.enumerated()` : Paire (index, élément).
- `array.contains(x)` : Vérifie la présence de *x*.
- `array.contains(where:)` : Vérifie avec condition.
- `array.first(where:)` / `last(where:)` : Trouve premier / dernier qui passe.
- `array.allSatisfy { ... }` : Tous doivent valider.
- `array.sorted()` : Retourne une version triée.
- `array.shuffled()` : Retourne en ordre aléatoire.
- `array.reversed()` : Retourne inversé (non mutant).
- `array.joined(separator:)` : Concatène (si String).
- `array.split(separator:)` : Coupe en morceaux.
- `array.randomElement()` : Élément aléatoire (optionnel).

## 🔹 Recherche
- `array.firstIndex(of: x)` : Premier indice de *x*.
- `array.lastIndex(of: x)` : Dernier indice de *x*.
- `array.firstIndex(where:)` / `lastIndex(where:)` : Indice selon condition.

## 🔹 Comparaison
- `==`, `!=` : Comparaison complète.
- `array.elementsEqual(other)` : Même contenu ?
- `array.starts(with: prefix)` : Commence par *prefix* ?
- `array.lexicographicallyPrecedes(other)` : Ordre lexicographique.
