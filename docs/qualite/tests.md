# Les différents types de tests

## 1. Les tests unitaires

Objectif : Vérifier qu’une fonction ou une méthode isolée fonctionne correctement.

Ce sont les tests les plus proches du code source.

Ils sont généralement écrits par le développeur lui-même.

Exemple : tester qu’une fonction de calcul de la TVA retourne bien le résultat attendu pour une valeur donnée.

Outils courants :
- Python : unittest, pytest
- Java : JUnit
- JavaScript : Jest
- PHP : PHPUnit, Pest

🧠 Bon à savoir : Les tests unitaires doivent être nombreux, rapides et exécutés souvent. Ils ne testent qu'une petite partie de code. (D'où le mot unitaire)

## 2. Les tests d'intégration

Objectif : Vérifier que plusieurs modules fonctionnent correctement ensemble.

- Ils permettent de tester les interactions entre composants : base de données, API, services...

- Exemple : tester qu’une commande est bien enregistrée en base après validation par le client.

Quand les utiliser ? Une fois que vos modules sont testés unitairement, vous voulez vous assurer que leur assemblage ne crée pas de dysfonctionnement.

## 3. Les tests fonctionnels

Objectif : Vérifier que le logiciel respecte les exigences fonctionnelles définies par le client.

Ils s’effectuent souvent à partir d’un cahier des charges ou d’un backlog Agile.

Exemple : “Un utilisateur non connecté ne peut pas accéder à la page de profil.”

Ces tests peuvent être automatisés ou réalisés manuellement.

## 3. Les tests d’acceptation

Objectif : Permettre au client ou utilisateur final de valider que l’application répond bien à ses besoins.

Ils sont souvent préparés avec ou par le **client**.

Ils se basent sur des scénarios métier concrets.

Exemple : “Créer une commande avec trois produits et vérifier que le total est bien calculé avec la remise.”

Ils marquent souvent la fin d’un [sprint]('./gestion/sprint.md') ou d’un projet.

## 4. tests exploratoires

Les tests exploratoires sont une forme de test non scripté, où le testeur explore librement l’application pour détecter des comportements inattendus, des erreurs ou des incohérences.

👉 Le principe est simple :
Le testeur utilise l'application comme un utilisateur réel, mais avec un regard critique et une attention particulière à ce qui pourrait mal fonctionner.

🎯 Objectif
- Trouver des bugs que les tests automatisés ou unitaires ne couvrent pas
- Observer le système dans son ensemble
- Tester les scénarios imprévus ou atypiques

🧠 Qui fait ces tests ?

- Le plus souvent : les développeurs, les testeurs ou les utilisateurs finaux
- Parfois, le client peut y participer, mais ce n’est pas le but premier

C’est une démarche plus intuitive que formelle. Le testeur n’a pas un plan détaillé, mais une charte d’exploration ou un objectif comme :

> “Tester ce qui se passe quand un utilisateur entre une date invalide dans le formulaire de réservation.”

