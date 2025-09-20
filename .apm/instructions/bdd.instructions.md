applyTo: '**/*.feature'
description: 'Rules and best practices for Behavior Driven Development (BDD) in this project.'
# ---
# Version 0.1 — 20 septembre 2025
# ---

# Instructions pour le Behavior Driven Development (BDD)

## Objectif
Ces instructions définissent le workflow, la structure et les meilleures pratiques pour le BDD dans ce projet. Elles garantissent que les scénarios BDD sont actionnables, maintenables et servent de documentation vivante ainsi que de base pour les tests automatisés.

## Objectifs
- Réduire l’écart entre les équipes métier et techniques
- Livrer un logiciel de valeur grâce à la collaboration et au feedback rapide
- Utiliser des spécifications exécutables comme documentation et base de tests

## Workflow
Le BDD en JavaScript est un processus itératif basé sur trois pratiques clés :

1. **Discovery (Découverte)**
   - Organiser des ateliers pour clarifier les besoins utilisateurs et définir des exemples concrets
   - Collaborer entre les rôles (métier, dev, QA) pour construire une compréhension partagée
   - Documenter les user stories et critères d’acceptation

2. **Formulation**
   - Rédiger les scénarios en syntaxe Gherkin (Given/When/Then)
   - Utiliser le langage métier et la terminologie du domaine
   - S’assurer que les scénarios sont lisibles par les humains et les outils
   - Valider les scénarios avec toutes les parties prenantes

3. **Automation (Automatisation)**
   - Automatiser les scénarios avec **Cucumber.js**
   - Implémenter le code pour satisfaire chaque scénario, en commençant par des tests en échec (Jest ou Vitest)
   - Utiliser les scénarios comme tests de non-régression et documentation vivante

## Règles de rédaction des scénarios
- Utiliser la syntaxe Gherkin : `Feature`, `Scenario`, `Given`, `When`, `Then`, `And`, `But`
- Un scénario par cas métier ou critère d’acceptation
- Utiliser un nommage explicite et cohérent (voir coding-style-sonar-rules.instructions.md)
- Éviter le jargon technique ; privilégier le langage métier
- Garder les scénarios courts, ciblés et indépendants
- Ajouter des commentaires pour les étapes complexes ou non triviales
- Lier les scénarios aux user stories et aux exigences

## Organisation des fichiers
- Placer les fichiers de features dans `features/[feature]/`
- Les tests unitaires dans `tests/unit/`, les tests d’intégration dans `tests/integration/`
- Le code métier dans `src/domain/`, la logique applicative dans `src/application/`, l’infrastructure dans `src/infrastructure/`
- Nommer explicitement les fichiers et scénarios (ex : `login.feature`, `Scenario: Connexion réussie`)
- Garder tous les fichiers sous gestion de version (Git)

## Outils recommandés
- **Cucumber.js** pour l’automatisation BDD
- **Jest** ou **Vitest** pour les tests unitaires et d’intégration
- **Sinon.js** pour les mocks avancés
- **ESLint** et **Prettier** pour le style de code
- Intégration CI/CD (GitHub Actions, GitLab CI, etc.)

## Bonnes pratiques JS
- Collaboration active entre métier, dev et QA pour la rédaction des scénarios
- Relire et mettre à jour les scénarios et les tests à chaque évolution
- Utiliser les scénarios comme documentation vivante et base des tests automatisés
- Automatiser l’exécution des tests et scénarios dans la CI/CD (ex : GitHub Actions, GitLab CI)
- Éviter la duplication et supprimer les scénarios obsolètes
- Documenter les liens entre scénarios, user stories et code source

## Exemple BDD complet

Scénario Gherkin :
```gherkin
Fonctionnalité : Connexion utilisateur
  En tant qu’utilisateur enregistré
  Je veux me connecter au système
  Afin d’accéder à mon compte

  Scénario : Connexion réussie
    Étant donné un utilisateur enregistré avec des identifiants valides
    Quand l’utilisateur soumet le formulaire de connexion
    Alors l’utilisateur doit être redirigé vers le tableau de bord
    Et un message de bienvenue doit s’afficher
```

Step definitions Cucumber.js :
const { Given, When, Then } = require('@cucumber/cucumber');
const assert = require('assert');


Given('un utilisateur enregistré avec des identifiants valides', function () {
  user = { email: 'test@exemple.com', password: 'secret' };
});

When("l'utilisateur soumet le formulaire de connexion", function () {
Then("l'utilisateur doit être redirigé vers le tableau de bord", function () {
  assert.strictEqual(result.redirect, '/dashboard');
});

Then('un message de bienvenue doit s\'afficher', function () {
  assert.strictEqual(result.message, 'Bienvenue !');
});
```

## Références
- [Cucumber.js Documentation](https://github.com/cucumber/cucumber-js)
- [Jest Documentation](https://jestjs.io/)
- [Vitest Documentation](https://vitest.dev/)
- [Sinon.js Documentation](https://sinonjs.org/)
- [ESLint](https://eslint.org/)
- [Prettier](https://prettier.io/)
- [Gherkin Syntax](https://cucumber.io/docs/gherkin/)
- [Instructions projet : unit-and-integration-tests, domain-driven-design, coding-style-sonar-rules, object-calisthenics]
