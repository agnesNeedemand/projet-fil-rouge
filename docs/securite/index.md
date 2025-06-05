# ✅ Check-list Sécurité

## ⚙️ Code Backend 

- [x] Utiliser des requêtes préparées (PDO, Doctrine, Eloquent, etc.)
- [x] Valider toutes les données en entrée
    - Filtrer les caractères indésitables
    - Vérifier le format ( numérique, chaine de caractère, date ...)
    - Vérifier eventuellement avec une expression régulière ( email ...)
    - Vérifier la longueur des données

- [x] Echapper toutes les données en sortie ( HTML, JSON, ... ) au cas ou il y aurait du code mal vaillant dans votre base de données.

- [x] Gérer les erreurs sans les afficher
    - Enregistrer des logs
    - Afficher des messages utilisateurs neutres ( Ne pas dévoiler trop d'information )

- [x] Implémenter une authentification sécurisée
    - Hash avec bcrypt ou argon2
    - Rate limiting (bruteforce)
    - Jetons CSRF pour les formulaires (prevu par les framework)

- [x] Gérer les rôles et permissions (RBAC)
- [x] Journaliser les actions sensibles (connexion, modification de données, etc.)
- [x] Utiliser un analyseur de code statique PHPStan (niveau 5 minimum ) 

## 🖼️ Frontend

- [x] Valider les formulaires côté client (feedback immédiat, economie de requete serveur)

- [x] Ne jamais faire confiance aux données entrées par l'utilisateur

- [x] Empêcher l'insersion de HTML brut dans une page à partir d'une variable (attaque XSS)

 Si c'est vraiment nécéssaire (Exemple l'utilisateur doit ecrire du texte avec des balises de code) Il faut nettoyer le HTML avant de l'afficher. 
 Eventuellement utiliser **DOMpurify**, accessible par npm ou CDN.

- [x] Utiliser npm audit pour détecter les dépendances vulnérables
- [x] Éviter le stockage de données sensibles dans le localStorage/sessionStorage

## 🗄️ Base de données

- [x] Utiliser un utilisateur MySQL avec droits limités
- [x] Définir des contraintes d’intégrité (clé étrangère, NOT NULL, UNIQUE…)

!!! danger "Attention !"
    Ne pas rendre un champs nullable parce que c'est plus simple à coder

- [x] Ajouter des triggers pour protéger les données sensibles ou historiques
- [x] Mettre en place des sauvegardes régulières
- [x] Limiter les acces avec GANTT si possible
- [x] Conserver des historiques, rien n'est vraiment effacer mais tout est archiver.
