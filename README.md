# Tip Calculator

Calculatrice de pourboire.

## Ce qui a été fait

- **Hissage d'état** : l'état (`amountInput`) a été sorti de `EditNumberField` pour être placé dans `TipTimeLayout`. `EditNumberField` est devenu **sans état** : il reçoit `value` et `onValueChange`.
- **Recomposition** : quand l'utilisateur tape, `onValueChange` met à jour l'état, Compose recompose, et le pourboire se recalcule tout seul. `remember` garde la valeur entre les recompositions.
- **Interface** : `singleLine = true` et clavier numérique avec `KeyboardType.Number`.
- **Champ réutilisable** : ajout du paramètre `label` (`@StringRes`) pour utiliser le même composable pour « Bill Amount » et « Tip Percentage ».
- **Pourcentage personnalisé** : nouvel état `tipInput`, converti en `tipPercent`, et passé à `calculateTip(amount, tipPercent)` au lieu du 15 % fixe.
