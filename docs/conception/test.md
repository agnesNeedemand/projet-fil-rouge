# Testabilité

***Intégrez les tests dès la conception***

La qualité d’un projet informatique ne se mesure pas uniquement à son bon fonctionnement apparent, mais aussi à sa capacité à être vérifié, maintenu et validé de manière continue. C’est pourquoi il est essentiel d’**intégrer la réflexion sur les tests dès la phase de conception**.

## Anticiper les scénarios de test

Dès que vous définissez les fonctionnalités, posez-vous la question : 
> *comment vais-je tester cela ?* 

Chaque exigence fonctionnelle doit être associée à un ou plusieurs scénarios de test, permettant de vérifier qu’elle est bien respectée. Cela vous aidera aussi à identifier les cas limites et les erreurs potentielles.

## Favoriser une architecture testable

Concevoir pour tester, c’est aussi faire des choix techniques et architecturaux qui permettent l’automatisation des tests :

* Privilégiez des **fonctions pures** et des **composants indépendants**, facilement testables unitairement.
* Appliquez le principe **d’injection de dépendances** pour faciliter les tests isolés (mocking, stubs).
* Respectez les principes **SOLID**, notamment la responsabilité unique (Single Responsibility Principle), pour rendre vos modules plus simples à tester.

**mocking** : En programmation orientée objet, les mocks (simulacres ou mock object) sont des objets simulés qui reproduisent le comportement d'objets réels de manière contrôlée. Un programmeur crée un mock dans le but de tester le comportement d'autres objets, réels, mais liés à un objet inaccessible ou non implémenté.

**stub** : Un stub est un composant "factice" (ou simulé) que l’on utilise lors des tests pour remplacer une vraie dépendance du système. Son rôle est de fournir une réponse prévisible, sans faire appel au vrai service, à la vraie base de données ou à une API externe.

## Mettre en place une stratégie de tests

Dès la conception, vous pouvez définir les différents niveaux de test à mettre en œuvre :

* **Tests unitaires** : pour vérifier le bon fonctionnement de chaque composant ou fonction.
* **Tests d’intégration** : pour valider l’interaction entre différents modules.
* **Tests fonctionnels** : pour s’assurer que les fonctionnalités correspondent aux besoins exprimés.
* **Tests de non-régression** : pour garantir que les nouvelles modifications ne détériorent pas l’existant.

## 🛠️ Prévoir les outils et l’automatisation

Planifiez l’utilisation d’outils adaptés à votre environnement technique

Même avec des ressources limitées, il est essentiel d’intégrer progressivement des pratiques de test dans votre projet informatique. Voici comment adapter votre démarche selon les outils disponibles.
Écriture des tests unitaires

Utilisez des frameworks standards, selon le langage de programmation que vous employez :

- Python : unittest (intégré) ou pytest (puissant et simple à utiliser)
- Java : JUnit, souvent intégré dans les IDE comme IntelliJ IDEA ou Eclipse
- JavaScript : Jest, Mocha ou Vitest pour des tests rapides et modulaires
- PHP : PHPUnit ou Pest pour une syntaxe plus expressive

Lancez vos tests manuellement à chaque étape importante du développement (nouvelle fonctionnalité, correction de bug, refactorisation).

### Automatiser les tests (quand c’est possible)

Une chaîne automatisée permet de garantir une qualité constante sans dépendre de vérifications manuelles. Trois niveaux peuvent être mis en place :

- ✅ Scripts locaux : utilisez un script simple (bash, batch, Makefile) pour lancer automatiquement les tests avec une seule commande. Cela facilite la régularité des tests, même sans infrastructure en ligne.

- Intégration continue (si vous avez accès à un dépôt Git distant) :
    - GitHub Actions (gratuit avec GitHub)
    - GitLab CI/CD (disponible avec GitLab en ligne ou auto-hébergé)
    - Jenkins (open source, mais nécessite une machine pour l’hébergement)

- Plateformes de gestion de la qualité :

Outils comme SonarQube, TestRail, ou Xray permettent d’analyser la couverture de test, les duplications de code, la dette technique…

Ces outils sont souvent payants ou complexes à installer.

## **Impliquer les utilisateurs dans la validation**

Enfin, dès la conception, pensez à la **recette utilisateur**. Identifiez les critères d’acceptation avec les parties prenantes, pour que les tests finaux soient alignés avec les attentes métier. 

Cela peut passer par des **tests exploratoires** ou des **démos régulières**.





En intégrant les tests dès la conception, vous gagnez en sérénité, en rigueur, et vous réduisez considérablement les risques en phase de développement. Cela participe pleinement à une démarche de qualité logicielle.

Souhaitez-vous également un exemple concret ou un modèle de plan de tests pour illustrer cette démarche ?
