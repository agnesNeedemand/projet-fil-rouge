# Bonnes pratiques sur GitHub

## Structure claire du dépôt (repo)

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

!!! Danger Attention
    Pas de projet dans le projet



## Commits clairs et fréquents

1. Des messages de commit explicites :
2. Commits fréquents = historique compréhensible et possibilité de revenir en arrière facilement.

  ```
  ✅ Bon : "Corrige bug d’affichage du tableau Markdown"
  ❌ Mauvais : "fix" ou "update"
  ```

#### 3. **Utilise les branches**

* Ne travaille **pas directement sur `main`**. Utilise une branche pour chaque fonctionnalité ou correction.

  ```
  git checkout -b feat/nouvelle-fonction
  ```

#### 4. **Pull Requests (PR)**

* Fais une **PR** pour intégrer ton travail à `main` et permettre la revue de code (même pour toi seul, c’est une bonne habitude !).

#### 5. **Issues**

* Utilise les **issues** pour suivre les bugs, idées ou tâches à faire.

---

### 📘 **Mettre de la documentation dans un repo**

Oui, c’est **tout à fait normal et recommandé** de mettre de la documentation dans un repo :

* **README.md** : pour l’intro et les instructions de base
* **`/docs/`** : pour des documents plus détaillés
* Tu peux aussi générer un site statique à partir de cette doc avec **GitHub Pages** (ex : avec MkDocs ou Docusaurus)

---

### 📄 **Tableaux Markdown mal affichés ?**

Oui, c’est possible si :

* Le tableau est mal formé
* Tu utilises un éditeur qui ne rend pas bien le Markdown
* GitHub n’interprète pas bien le format à cause d'un espace ou retour à la ligne manquant

#### ✅ Exemple correct :

```markdown
| Nom      | Âge | Métier        |
|----------|-----|---------------|
| Alice    | 30  | Développeuse  |
| Bob      | 25  | Designer      |
```

#### ❌ Exemple incorrect (lignes mal alignées ou séparateur incorrect) :

```markdown
| Nom | Âge | Métier
|---|--|---
Alice | 30 | Développeuse
Bob | 25 | Designer
```

Teste-le directement dans le **Preview** sur GitHub ou dans un éditeur comme **Typora** ou **Obsidian**.

---

### 🔧 Ressources pour apprendre GitHub

* [GitHub Docs (officiel)](https://docs.github.com/)
* [Git Handbook](https://guides.github.com/introduction/git-handbook/)
* [Le cours "Apprendre Git" d'OpenClassrooms](https://openclassrooms.com/fr/courses/2344111-gerez-votre-code-avec-git-et-github)

---

Souhaites-tu un mini-guide PDF pour t’entraîner étape par étape à utiliser Git/GitHub avec un exemple concret ?
