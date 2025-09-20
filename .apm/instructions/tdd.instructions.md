applyTo: '**/*.test.{js,ts}'
description: 'Rules and best practices for Test Driven Development (TDD) in this project.'
# ---
# Version 0.1 — 20 septembre 2025
# ---

# Instructions pour le Test Driven Development (TDD)

## Objectif
Ces instructions définissent le workflow, la structure et les meilleures pratiques pour le TDD dans ce projet. Elles visent à aider une IA et un développeur à produire un code fiable, maintenable et évolutif en suivant les principes du TDD.

## Objectifs
- Garantir la qualité et la robustesse du code dès la conception
- Favoriser la documentation vivante et la compréhension du code
- Permettre un refactoring sécurisé et une évolution rapide

## Workflow
Le TDD se déroule en trois étapes principales :

1. **Écriture du test (Red)**
   - Commencer par écrire un test unitaire qui exprime le comportement attendu
   - Le test doit échouer (Red) car la fonctionnalité n’est pas encore implémentée
   - Utiliser un nom explicite pour le test, reflétant le cas métier

2. **Implémentation minimale (Green)**
   - Écrire le code minimal pour faire passer le test
   - Se concentrer sur la simplicité et la clarté
   - Vérifier que tous les tests passent

3. **Refactoring**
   - Améliorer la structure du code sans modifier son comportement
   - Refactorer le code et les tests pour plus de lisibilité et de maintenabilité
   - S’assurer que tous les tests restent au vert

## Bonnes pratiques
- Un test par cas métier ou critère d’acceptation
- Utiliser des assertions claires et précises
- Nommer les tests de façon explicite et cohérente
- Isoler les tests : éviter les dépendances externes ou les effets de bord
- Garder les tests rapides et déterministes
- Mettre à jour les tests lors de toute évolution du code
- Utiliser des outils comme Jest ou Vitest pour l’automatisation

## Guidelines pour IA et développeur
- Générer d’abord les tests avant le code métier
- Proposer des cas limites et des scénarios d’erreur
- Suggérer des refactorings après chaque cycle Red/Green
- Documenter le comportement attendu dans les tests
- Vérifier la couverture de code et viser l’exhaustivité

## Structure recommandée
- Fichiers de test dans le même dossier que le code source ou dans un dossier `__tests__`
- Utiliser le suffixe `.test.js` ou `.test.ts`
- Grouper les tests par fonctionnalité ou module

## Exemple de cycle TDD
```js
// Exemple avec Jest

describe('calculatrice', () => {
  it('additionne deux nombres', () => {
    expect(add(2, 3)).toBe(5);
  });
});

// Implémentation minimale
function add(a, b) {
  return a + b;
}
```

## Ressources
- [TDD by Example – Kent Beck]
- [Jest Documentation](https://jestjs.io/)
- [Vitest Documentation](https://vitest.dev/)
