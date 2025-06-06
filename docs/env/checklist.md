# ✅ Checklist de Production

Avant de livrer votre projet Fil Rouge, vous devez vous assurer que celui-ci respecte les bonnes pratiques attendues en environnement professionnel.  
Cette checklist vous aide à **valider les éléments techniques, qualité, sécurité et documentation** indispensables à une mise en production réussie.

---

## 📦 1. Structure du projet

- [ ] Le projet est organisé selon une structure cohérente et lisible.
- [ ] Les fichiers temporaires, inutiles ou sensibles (.env, node_modules, __pycache__, etc.) sont exclus via `.gitignore`.
- [ ] Le README est présent et à jour.
- [ ] Les dépendances sont correctement déclarées (`requirements.txt`, `composer.json`, `package.json`, etc.).

---

## 🧪 2. Fonctionnalités et tests

- [ ] Toutes les fonctionnalités principales sont développées et opérationnelles.
- [ ] Les erreurs critiques sont gérées (ex : routes non existantes, mauvaise saisie, etc.).
- [ ] Les scénarios de test manuel ou automatisé sont documentés ou implémentés.
- [ ] Aucun mot de passe ou donnée sensible n'est visible dans le code.

---

## 🔐 3. Sécurité

- [ ] Les mots de passe sont **hachés** et non stockés en clair.
- [ ] Les pages ou routes protégées nécessitent une authentification.
- [ ] Les entrées utilisateurs sont filtrées ou échappées (contre XSS, injections SQL...).
- [ ] Aucune clé API ou token d’accès n’est visible dans le code ou le dépôt public.

---

## 🎨 4. Qualité de code

- [ ] Le code est indenté et lisible.
- [ ] Les noms de variables et fonctions sont explicites.
- [ ] Les commentaires sont utiles, sans excès.
- [ ] Aucune portion de code n’est laissée “en travaux” (TODO, console.log inutiles, etc.).

---

## 🧭 5. Documentation

- [ ] Un guide d’installation est fourni (README ou page dédiée).
- [ ] La structure du projet est expliquée.
- [ ] Les routes/API sont décrites (si applicable).
- [ ] L’environnement de développement est précisé (Python, PHP, Docker, etc.).
- [ ] Un schéma de base de données est fourni (optionnel mais recommandé).

---

## 🚀 6. Préparation à la mise en ligne (si applicable)

- [ ] Une version prête à être déployée est disponible (ZIP, dossier `dist/`, etc.).
- [ ] Les variables d’environnement sont gérées correctement.
- [ ] Les fichiers sensibles sont bien exclus de la version publique.
- [ ] Le projet a été testé dans un environnement de production simulé (Docker, VM, etc.).

---

> 📌 **Conseil :** Cette checklist peut être utilisée comme outil de relecture avant chaque livrable, mais aussi comme critère pour valider votre soutenance technique.

---

