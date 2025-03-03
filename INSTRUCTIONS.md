# Instructions pour mettre à jour le dépôt GitHub

Ce document explique comment mettre à jour le dépôt GitHub [ai-dragonfly/api-docs](https://github.com/ai-dragonfly/api-docs) avec la nouvelle documentation Swagger de l'API.

## Prérequis

- Git installé sur votre machine
- Accès au dépôt GitHub [ai-dragonfly/api-docs](https://github.com/ai-dragonfly/api-docs)

## Étapes

1. Clonez le dépôt existant :
   ```bash
   git clone https://github.com/ai-dragonfly/api-docs.git
   cd api-docs
   ```

2. Supprimez tous les fichiers existants (sauf le dossier .git) :
   ```bash
   # Sur Linux/macOS
   rm -rf $(ls -A | grep -v "^\.git$")
   
   # Sur Windows (PowerShell)
   Get-ChildItem -Force | Where-Object { $_.Name -ne ".git" } | Remove-Item -Recurse -Force
   ```

3. Copiez les nouveaux fichiers dans le dépôt :
   ```bash
   # Remplacez /chemin/vers/api-docs-temp par le chemin absolu vers le dossier api-docs-temp
   cp -r /chemin/vers/api-docs-temp/* .
   ```

4. Committez et poussez les changements :
   ```bash
   git add .
   git commit -m "Mise à jour de la documentation API avec Swagger"
   git push origin main
   ```

5. Activez GitHub Pages (si ce n'est pas déjà fait) :
   - Allez sur la page du dépôt sur GitHub
   - Cliquez sur "Settings" (Paramètres)
   - Faites défiler jusqu'à la section "GitHub Pages"
   - Dans "Source", sélectionnez la branche "main" et le dossier racine (/)
   - Cliquez sur "Save" (Enregistrer)

6. Vérifiez que la documentation est bien déployée :
   - Attendez quelques minutes que GitHub Pages déploie le site
   - Visitez https://ai-dragonfly.github.io/api-docs/

## Remarques

- Si vous avez des problèmes avec GitHub Pages, assurez-vous que le dépôt est public ou que GitHub Pages est activé pour les dépôts privés dans votre organisation.
- Si vous souhaitez mettre à jour la documentation à l'avenir, répétez les étapes 1 à 4.
