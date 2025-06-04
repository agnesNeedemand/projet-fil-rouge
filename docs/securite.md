# ✅ Check-list Sécurité pour un Projet Fil Rouge (CDA)

## Code Backend 

- [ ] Utiliser des requêtes préparées (PDO, Doctrine, Eloquent, etc.)
- [ ] Valider toutes les données en entrée
    - Filtrer les caractères indésitables
    - Vérifier le format ( numérique, chaine de caractère, date ...)
    - Vérifier eventuellement avec une expression régulière ( email ...)
    - Vérifier la longueur des données

- [ ] Echapper toutes les données en sortie ( HTML, JSON, ... ) au cas ou il y aurait du code mal vaillant dans votre base de données.

- [ ] Gérer les erreurs sans les afficher
    - Enregistrer des logs
    - Afficher des messages utilisateurs neutres ( Ne pas dévoiler trop d'information )

- [ ] Implémenter une authentification sécurisée
    - Hash avec bcrypt ou argon2
    - Rate limiting (bruteforce)
    - Jetons CSRF pour les formulaires (prevu par les framework)

- [ ] Gérer les rôles et permissions (RBAC)
- [ ] Journaliser les actions sensibles (connexion, modification de données, etc.)
- [ ] Utiliser un analyseur de code statique PHPStan (niveau 5 minimum ) 