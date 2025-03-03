# Instructions pour publier la documentation sur GitHub Pages

Suivez ces étapes pour créer une organisation GitHub et publier la documentation Swagger via cette organisation.

## 1. Créer l'organisation GitHub

1. Connectez-vous à votre compte GitHub
2. Cliquez sur votre photo de profil en haut à droite
3. Sélectionnez "Your organizations"
4. Cliquez sur "New organization"
5. Sélectionnez un plan (le plan gratuit est suffisant)
6. Entrez "ai.dragonfly" comme nom d'organisation
7. Entrez votre adresse e-mail
8. Sélectionnez "My personal account" comme propriétaire
9. Acceptez les conditions d'utilisation et cliquez sur "Next"
10. Vous pouvez inviter des membres maintenant ou plus tard
11. Cliquez sur "Complete setup"

## 2. Créer un repository dans l'organisation

1. Accédez à la page de l'organisation nouvellement créée
2. Cliquez sur "New repository"
3. Entrez "api-docs" comme nom du repository
4. Ajoutez une description (par exemple, "Documentation de l'API Dragonfly AI")
5. Sélectionnez "Public" comme visibilité
6. Ne cochez pas "Initialize this repository with a README" car nous avons déjà créé un README
7. Cliquez sur "Create repository"

## 3. Pousser les fichiers vers le repository

Exécutez les commandes suivantes dans le terminal (remplacez `<your-github-username>` par votre nom d'utilisateur GitHub) :

```bash
cd ai-dragonfly-api-docs
git remote add origin https://github.com/ai.dragonfly/api-docs.git
git branch -M main
git push -u origin main
```

## 4. Activer GitHub Pages

1. Accédez au repository sur GitHub
2. Cliquez sur "Settings"
3. Dans le menu de gauche, cliquez sur "Pages"
4. Dans la section "Source", sélectionnez "Deploy from a branch"
5. Dans la section "Branch", sélectionnez "main" et "/ (root)" puis cliquez sur "Save"
6. Attendez quelques minutes que GitHub Pages déploie votre site

## 5. Accéder à la documentation

Une fois le déploiement terminé, vous pourrez accéder à la documentation à l'adresse suivante :
```
https://ai.dragonfly.github.io/api-docs/
```

Vous pouvez partager cette URL avec votre partenaire pour lui donner accès à la documentation de l'API.
