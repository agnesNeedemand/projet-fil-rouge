# 🛠️ Projet partiellement terminé – Bonnes pratiques

Il est tout à fait acceptable de livrer un projet **partiellement terminé**, tant que certaines règles sont respectées.  
Dans un contexte professionnel, il est courant de livrer des versions itératives d’une application, à condition que chaque version soit **stable, fonctionnelle et documentée**.

---

## ✅ Conditions pour livrer un projet incomplet

Pour que la livraison reste professionnelle et acceptable, vous devez vous assurer que :
🔹 Les parties incomplètes sont **clairement identifiées**.
🔹 Le reste de l’application fonctionne **sans erreur**.
🔹 Les fonctionnalités non terminées ne bloquent pas l’usage global.
🔹 Vous fournissez une **documentation claire sur l’état d’avancement**.

---

## 📄 Comment le signaler proprement

Voici plusieurs manières de documenter ce qui reste à faire :

### 🗂️ 1. Fichier `RELEASENOTES.md` ou section “Reste à faire”

Créez un petit fichier texte ou ajoutez une section dans le `README.md` :

```markdown
## Reste à faire (Backlog non finalisé)

- Intégration du système de paiement (non prioritaire)
- Mise en place de l’export PDF
- Page de gestion des utilisateurs en cours de développement
```

🧭 2. Commentaires dans le code

Les parties non terminées peuvent être :

* commentées temporairement (// à finaliser)

* ou encadrées avec un avertissement clair, sans être actives dans la version de **production**.

```php
<?php
if($env != 'prod'){
    echo "TODO : implémenter la page des conditions générales";
}
?>
```

🚫 Ce qu’il ne faut pas faire

❌ Laisser du code cassé ou non fonctionnel dans la version finale.

❌ Livrer un projet sans mentionner les fonctionnalités manquantes.

❌ Inclure du contenu à moitié implémenté qui perturbe l’expérience utilisateur.

❌ Avoir des erreurs visibles à l’exécution ou à la compilation.

💡 Conseil pour la soutenance

Assumez ce qui n’est pas terminé :
expliquez ce qui manque, pourquoi, et comment vous l’auriez fait si le temps avait permis. Cela montre votre capacité à gérer un projet et à prioriser.

    🎓 Exemple :
    “La partie gestion des droits utilisateurs n’est pas encore fonctionnelle, mais j’ai préparé la structure de code pour l’intégrer plus tard. Le reste de l’application est stable.”

📌 Rappel

    👉 Un projet bien fini à 80 % vaut mieux qu’un projet instable à 100 %.