# Documenter une API 

Voici un exemple de endpoint documenter. 

> GET /users

> **Description** : Liste tous les utilisateurs

> **Paramètres** :

>  - `page` (int) : Numéro de page

> **Réponse** :

```json

[
  { "id": 1, "nom": "Jean" },
  { "id": 2, "nom": "Marie" }
]
```

Cette structure assez classique apporte sufisament d'information pour comprendre l'API sans même la tester.

## Critères d’une bonne documentation d’API

- **Clarté** : Décrivez précisément chaque endpoint, paramètre, et réponse.

- **Exemples** : Fournissez des exemples de requêtes (curl, Postman, etc.)

- **Formatage** : Utilisez une structure claire (titres, tableaux, code formaté).

- **Actualisation** : Gardez la documentation à jour avec les changements de l’API.

- **Navigation facile** : Table des matières, liens entre sections, recherche.

- **Testabilité** : Intégration avec des outils comme Swagger, Postman ou Insomnia pour tester directement.

- **Contextualisation** : Expliquez les cas d’usage, limitations, erreurs courantes.


## Documentation avec Postman

Créer une documentation avec Postman

**Postman** est à la fois un client d’API et un outil de documentation. Voici les étapes :

### 📌 Étapes

1. **Créer une collection** : Regroupe vos requêtes (GET, POST, etc.) dans une collection Postman.
2. **Documenter chaque requête** :

   * Nom clair
   * Description (but, paramètres, exemple de réponse)
   * Ajouter des exemples de requêtes/réponses
3. **Générer la documentation automatiquement** :

   * Cliquez sur la collection → "View Documentation"
   * Personnalisez le rendu
   * Cliquez sur "Publish Docs" pour partager un lien public ou privé

### ✅ Avantages

- Facile à utiliser
- Interface graphique
- Documentation interactive


## Documentation avec OpenAPI

**OpenAPI** (anciennement Swagger) est un standard de description d’API REST.

### 📌 Étapes

1. **Créer un fichier YAML ou JSON** qui décrit l'API :

```yaml
   openapi: 3.0.0
   info:
     title: API de gestion de tâches
     version: 1.0.0
   paths:
     /taches:
       get:
         summary: Liste des tâches
         responses:
           '200':
      
             description: Succès
```

**yaml** (Yet Another Markup Language) : Langage de sérialisation de données utilisé pour l'écriture de fichier de configuration.  

2. **Utiliser un outil comme Swagger UI ou Redoc** pour afficher une documentation lisible :

   * Swagger Editor ([https://editor.swagger.io](https://editor.swagger.io))
   * Redoc ([https://github.com/Redocly/redoc](https://github.com/Redocly/redoc))

### ✅ Avantages

* Standard reconnu
* Compatible avec de nombreux outils
* Génération automatique de code possible

---

## Documentation avec Bruno

**Bruno** est un outil open-source pour tester des API REST, alternatif à Postman.

### 📌 Étapes

1. Créez un projet Bruno (dans un dossier local)
2. Chaque requête est un fichier `.bru` (au format texte)
3. Les métadonnées permettent d’ajouter des descriptions, des tags, etc.
4. Bruno ne génère pas automatiquement une documentation HTML mais facilite une structuration textuelle propre dans Git.

### ✅ Avantages

* Léger et basé sur des fichiers texte
* Idéal pour Git
* Open-source et rapide

---

## Faire une documentation vanilla

Il est possible de créer sans logiciel. Par exemple, avec un **document Markdown**, Word ou PDF :

### Structure typique

```
# API de gestion des utilisateurs

## GET /users
- **Description** : Liste tous les utilisateurs
- **Paramètres** :
  - `page` (int) : Numéro de page
- **Réponse** :
[
  { "id": 1, "nom": "Jean" },
  { "id": 2, "nom": "Marie" }
]

## POST /users

* **Description** : Crée un nouvel utilisateur
* **Corps JSON** :
{
  "nom": "Jean Dupont"
}
```



Tu peux aussi utiliser **Google Docs, Notion, ou même un README.md sur GitHub**.



---

