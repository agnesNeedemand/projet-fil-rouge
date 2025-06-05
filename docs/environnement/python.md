# Créer un environnement Python

Pour assurer une bonne isolation de votre projet, il est recommandé d'utiliser un environnement virtuel Python. 

Cet environnement permet d’installer des dépendances spécifiques sans impacter votre système global.

📌 Prérequis : Python 3.10 installé sur votre machine.

## ✅ Étapes pour créer un environnement virtuel avec `venv` :

1. **Aller dans le répertoire de travail :**

```bash
cd chemin/vers/ton/projet
```

2. **Créer l'environnement virtuel :**

```bash
python -m venv nom_de_l_environnement
```

   Par exemple :

```bash
python -m venv venv
```

3. **Activer l'environnement virtuel :**

   * **Sur Windows :**

```bash
.\venv\Scripts\activate
```

   * **Sur macOS / Linux :**

```bash
source venv/bin/activate
```

4. **(Facultatif) Vérifier que l'environnement est activé :**

```bash
which python   # macOS/Linux
where python   # Windows
```

ou

```bash
python --version
```

5. **Installer les dépendances dans l'environnement :**

```bash
pip install nom_du_module
```

6. **Désactiver l’environnement virtuel (quand tu as fini) :**

```bash
deactivate
```

## Avantages

### 1. Isolation des dépendances

Chaque environnement virtuel dispose de son propre ensemble de bibliothèques. Cela permet d’éviter les conflits entre différentes versions de dépendances nécessaires à plusieurs projets.

➡️ Cela évite les conflits entre versions de packages nécessaires à différents projets.

Exemple :

    Projet A utilise Django 3.2

    Projet B utilise Django 4.2
    
Sans environnement virtuel, ce serait un casse-tête à gérer.

### 2. Préservation du système global

Les paquets installés dans un environnement virtuel n’affectent pas l’interpréteur Python global du système. Cela limite les risques d’altérer des outils ou des projets existants.

### 3. Reproductibilité

Il est possible de figer les versions des bibliothèques dans un fichier requirements.txt, ce qui facilite le partage et le déploiement du projet dans un autre environnement (sur un serveur ou un autre poste de travail, par exemple).

➡️ Très utile pour déployer ton projet ailleurs (serveur, collaborateur, etc.).
```bash
pip freeze > requirements.txt
```
Et pour installer ensuite :

```bash
pip install -r requirements.txt
```
### 🧪 4. Expérimentation sans risque

L’environnement virtuel constitue un espace isolé dans lequel on peut tester de nouvelles bibliothèques ou versions sans conséquences sur d’autres projets.

➡️ Si ça ne marche pas, vous supprimez l’environnement sans toucher au reste.

### 5. Compatibilité avec les outils de développement
Les environnements virtuels sont reconnus par les principaux outils de développement (éditeurs de code, systèmes d’intégration continue, outils de déploiement, etc.).

C’est une question pertinente. L’utilisation d’un environnement virtuel avec `venv` a de nombreux avantages, mais il existe effectivement quelques inconvénients à prendre en compte, selon le contexte.


## Inconvénients et limitations 

### 1. Occupation supplémentaire de l’espace disque

Chaque environnement virtuel contient une copie (ou un lien symbolique) de l’interpréteur Python, ainsi que les bibliothèques installées spécifiquement pour le projet.
Cela peut représenter quelques dizaines à plusieurs centaines de mégaoctets, surtout si de nombreux paquets sont installés.

### 2. Multiplication des environnements

Lorsqu’on travaille sur de nombreux projets, chaque environnement virtuel prend de la place et il peut devenir difficile de les maintenir tous à jour ou de savoir lesquels sont encore utiles.

### 3. Risque d’oublier l’activation

Il est possible d’exécuter un script sans activer l’environnement virtuel, ce qui peut entraîner l’utilisation des mauvaises dépendances. Il faut donc rester vigilant.

### 4. Portabilité limitée sans gestion explicite

L’environnement virtuel lui-même n’est pas toujours portable entre systèmes d’exploitation (par exemple, un `venv` créé sous Windows ne fonctionnera pas sous Linux). Il est préférable d’utiliser un fichier `requirements.txt` pour recréer un environnement identique ailleurs.

### 5. Complexité perçue pour les débutants
Pour les personnes qui débutent en Python, la gestion d’environnements virtuels peut sembler une étape supplémentaire et inutile, surtout pour de petits scripts.


## Mémoire et performances

* **Mémoire RAM** : un environnement virtuel ne consomme pas plus de mémoire vive à l'exécution, sauf si les bibliothèques installées elles-mêmes sont plus lourdes.
* **Performances** : il n’y a pas de différence notable en termes de vitesse d’exécution ou de performance du code Python.

---

### Conclusion

L’utilisation d’un environnement virtuel ajoute un peu de complexité et d’occupation disque, mais ces inconvénients sont généralement négligeables au regard des bénéfices en matière de fiabilité, d’isolation et de reproductibilité. Dans un contexte professionnel ou multi-projets, l’usage d’environnements virtuels est vivement recommandé.

Voir aussi les outils `conda` et `pipenv`


