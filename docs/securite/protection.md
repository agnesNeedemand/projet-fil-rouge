# Protection des données

Cette page présente les bonnes pratiques liées à la collecte, au traitement et à la conservation des données personnelles dans le cadre de votre projet Fil Rouge.

## 🔐 Principes généraux de protection des données

Avant de collecter ou de manipuler des données personnelles, il est essentiel de s’interroger sur leur utilité, leur traitement, et leur protection.

Ces réflexes ne sont pas uniquement juridiques : ils traduisent une responsabilité du développeur vis-à-vis des utilisateurs.

Les questions suivantes permettent de vérifier que le projet respecte les principes de base en matière de confidentialité, et qu’il s’inscrit dans une démarche conforme au RGPD et aux bonnes pratiques professionnelles.
    
### 🍀Les 4 questions clés à se poser :

**Quelles données personnelles sont collectées ?**

→ Nom, prénom, email, mot de passe, historique de navigation, préférences, etc.

**Pourquoi sont-elles collectées ? (Finalité)**

→ Authentification, personnalisation, statistiques, envoi d’emails, etc.

**Comment sont-elles stockées et protégées ?**

→ Base de données sécurisée, mot de passe chiffré, accès restreint.

**Qui peut y accéder ?**

→ Administrateurs uniquement ? Tous les membres du projet ? Est-ce journalisé ? 
    
    
!!! success  "En Bref"
    💡 collecter moins, mieux, et de manière transparente.


## 🤝 Respect des principes RGPD

Même dans un projet pédagogique, il est important de **montrer que l’on comprend les exigences du RGPD**, et que l’on est capable d’appliquer ses principes de base.

- [ ] L’utilisateur est informé de la collecte de données (par message ou mention).
- [ ] Il est possible de **demander la modification ou la suppression de ses données** (même simulé).
- [ ] Une mention ou un fichier `privacy.md` décrit la politique de gestion des données.

## 🍪 Cookies et sessions

- [ ] Les cookies utilisés sont uniquement fonctionnels (ex. : cookie de session).
- [ ] Les données personnelles ne sont pas stockées dans les cookies.
- [ ] Si vous utilisez des outils tiers ou du suivi (Google Fonts, services externes), mentionnez-le.
- [ ] Les sessions sont sécurisées : durée limitée, cookies `HttpOnly`, stockage côté serveur.

> 💡 Bon réflexe : tout cookie non essentiel **nécessite le consentement explicite** de l’utilisateur .

