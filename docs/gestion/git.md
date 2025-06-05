# Bonnes pratiques sur GitHub

## 🔧 Préparation du projet

- Créer le dépôt GitHub
- Ajouter un fichier README.md
- Ajouter un `.gitignore`
- Définir un fichier `LICENSE`

## 📁 Structure claire du dépôt

!!! note
    repo = dépot

1. Utiliser une structure propre
2. Le fichier README.md est essentiel pour expliquer l'objectif du projet, comment l’installer, l’utiliser, etc.

Exemple : 

```bash
/mon-projet
├── README.md
├── CONTRIBUTING.md
├── docs/
├── src/
├── tests/
└── .gitignore
```

!!! Warning Attention
    Pas de projet dans le projet

## 💬 Commits clairs et fréquents

1. Des messages de commit explicites :
2. Commits fréquents = historique compréhensible et possibilité de revenir en arrière facilement.

  ```
  ✅ Bon : "Corrige bug d’affichage du tableau Markdown"
  ❌ Mauvais : "fix" ou "update"
  ```

## ➰ Utilisation de branches

1. Ne travaille **pas directement sur `main`**. Utilise une branche pour chaque fonctionnalité ou correction.

```bash
git checkout -b feat/nouvelle-fonction
```

## ✅ Pull Requests (PR)

Faire une **PR** pour intégrer ton travail à `main` et permettre la revue de code (même pour un seul developpeur, c’est une bonne habitude !).

## 📝 Utilisation des Issues

Utiliser les **issues** pour suivre les bugs, idées ou tâches à faire.

## 📘 Documentation 

Mettre de la documentation dans un repo

Il est **recommandé** de mettre de la documentation dans un repo :

* **README.md** : pour l’intro et les instructions de base
* **`/docs/`** : pour des documents plus détaillés
* Génération d'un site statique à partir de cette doc avec **GitHub Pages** (ex : avec MkDocs ou Docusaurus)


## ❌ Les fichiers ignorés

Le fichier .gitignore sert à exclure certains fichiers ou dossiers du suivi Git. Cela évite d’envoyer sur GitHub des fichiers sensibles, inutiles, temporaires ou propres à votre environnement local.

### Que faut-il généralement ignorer ?

Voici une base typique :
```markdown
# Fichiers système
.DS_Store
Thumbs.db

# Environnements virtuels et variables sensibles
venv/
.env
*.env

# Fichiers de configuration personnels (Python, logs, cache)
*.pyc
*.log
*.sqlite3
__pycache__/

# Dossiers générés (build / static / MkDocs / dist)
site/
dist/
build/

# Dépendances
node_modules/
vendor/

# Fichiers d’IDE ou éditeurs
.vscode/
.idea/
```

### Bonnes pratiques associées

Ne jamais commettre de fichiers dans node_modules/ ou vendor/ — ces dossiers sont recréés automatiquement via npm install ou composer install.

Fournir un fichier package.json ou composer.json (équivalent de requirements.txt) dans votre dépôt pour faciliter l’installation des dépendances.

Conserver les scripts de build (ex. : build.sh, Makefile, ou mkdocs.yml) dans le dépôt pour que le projet reste facilement reproductible.


## 🛠️ Les variables d'environnement

### Le fichier .env

Le fichier .env contient des variables d’environnement sensibles, comme :

```ini
API_KEY=abcdefgh12345678
DATABASE_URL=postgres://user:pass@host/db
SECRET_KEY=super-secret-value
```

Ce fichier ne doit jamais être versionné, car il contient des données confidentielles.

Vous devez donc ajouter .env dans votre .gitignore :
```gitignore
.env
```

### Le fichier .env.example

Ce fichier est une copie publique du fichier .env, sans les valeurs sensibles, mais avec les noms des variables attendues.

!!! note 
    Cela permet aux autres contributeurs de comprendre quelles variables ils doivent définir.

Exemple :
```ini
# .env.example
API_KEY=your-api-key-here
DATABASE_URL=your-db-url-here
SECRET_KEY=change-me
```

Cela montre clairement à vos collègues ou utilisateurs quelles variables sont nécessaires sans exposer vos propres données.


## 🧹 Suppression de fichier

Horreur, j'ai des fichiers que je veux supprimer sur mon repo, car j'ai oublié de les ignorer.

Pas de panique, cela arrive à tout le monde ! Voici comment **supprimer proprement des fichiers déjà suivis par Git** mais que vous souhaitez désormais ignorer via `.gitignore`.

### Étapes pour supprimer des fichiers déjà versionnés

Même si vous ajoutez les fichiers ou dossiers à `.gitignore`, Git continue de les suivre **tant qu’ils sont déjà dans l’historique**. Voici comment corriger cela :

#### 1. Ajouter les fichiers/dossiers à `.gitignore`

Par exemple, vous ajoutez :

```gitignore
node_modules/
.env
site/
```

#### 2. Supprimer les fichiers du suivi Git **sans les supprimer localement**

Utilisez la commande suivante :

```bash
git rm --cached -r node_modules/ .env site/
```

* `--cached` : supprime **du suivi Git**, mais **pas du disque local**.
* `-r` : pour supprimer récursivement dans les dossiers.

💡 Vous pouvez remplacer la liste par n’importe quel fichier ou dossier que vous voulez "désuivre".

#### 3. Committez les changements

```bash
git commit -m "Supprime les fichiers ignorés du suivi Git"
```

#### 4. Poussez les changements vers GitHub

```bash
git push
```

#### Astuce bonus : tout réinitialiser (optionnel)

Si vous avez modifié beaucoup de choses, vous pouvez forcer Git à ne suivre **que les bons fichiers**, avec :

```bash
git rm -r --cached .
git add .
git commit -m "Nettoyage complet des fichiers suivis par erreur"
git push
```

⚠️ Cette commande est radicale, utilisez-la seulement si vous êtes sûr que tout est bien prêt dans `.gitignore`.