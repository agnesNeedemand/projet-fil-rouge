# Memo MkDocs

For full documentation visit [mkdocs.org](https://www.mkdocs.org).

## Installation 

```bash
pip install mkdocs-material
```

## Commands

* `mkdocs new [dir-name]` - Create a new project.
* `mkdocs serve` - Start the live-reloading docs server.
* `mkdocs build` - Build the documentation site.
* `mkdocs -h` - Print help message and exit.

## Project layout

    mkdocs.yml    # The configuration file.
    docs/
        index.md  # The documentation homepage.
        ...       # Other markdown pages, images and other files.


## Deployement de la doc

| Étape | À faire                            |
| ----- | ---------------------------------- |
| 1     | Installer MkDocs                   |
| 2     | Créer un dossier avec `mkdocs new` |
| 3     | Ajouter checklist en `.md`         |
| 4     | Tester en local avec `serve`       |
| 5     | Déployer avec `gh-deploy`          |

Note : Ctrl + C pour stop le serveur

!!! note 
    Ctrl + C dans le terminal pour stop le serveur


## Site accessible 

La publication se fait sur Git pages

```
https://TONUTILISATEUR.github.io/TONREPO/
```
