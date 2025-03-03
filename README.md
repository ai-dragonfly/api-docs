# Documentation de l'API Dragonfly

Ce dépôt contient la documentation de l'API Dragonfly au format OpenAPI (Swagger). Cette documentation est destinée aux partenaires et développeurs qui souhaitent intégrer l'API Dragonfly dans leurs applications.

## Contenu du dépôt

- `swagger.yaml` : Documentation de l'API au format YAML
- `swagger.json` : Documentation de l'API au format JSON
- `index.html` : Interface utilisateur Swagger pour explorer la documentation de manière interactive

## Utilisation

Vous pouvez consulter la documentation de l'API de deux manières :

### 1. Via GitHub Pages

La documentation est disponible en ligne à l'adresse suivante : [https://ai-dragonfly.github.io/api-docs/](https://ai-dragonfly.github.io/api-docs/)

### 2. En local

Pour consulter la documentation en local :

1. Clonez ce dépôt :
   ```bash
   git clone https://github.com/ai-dragonfly/api-docs.git
   ```

2. Ouvrez le fichier `index.html` dans votre navigateur

## Authentification

Pour utiliser l'API Dragonfly, vous devez disposer d'un token d'authentification. Ce token doit être inclus dans l'en-tête `Authorization` de chaque requête sous la forme `Bearer YOUR_API_KEY`.

Pour obtenir un token d'API, veuillez contacter l'équipe Dragonfly.

## Environnements

L'API est disponible dans l'environnement suivant :

- **Production** : `https://ai.dragonflygroup.fr`

## Exemples d'utilisation

### Authentification

```bash
curl -X POST https://ai.dragonflygroup.fr/api/v1/login \
  -H "Content-Type: application/json" \
  -d '{
    "email": "user@example.com",
    "password": "your-password"
  }'
```

### Obtenir une complétion

```bash
curl -X POST https://ai.dragonflygroup.fr/api/v1/chat/completions \
  -H "Authorization: Bearer YOUR_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
    "messages": [{
      "role": "user",
      "content": [{ "type": "text", "text": "Hello, how can you assist me?" }]
    }],
    "model": "chatgpt-4o-latest",
    "temperature": 1,
    "top_p": 1,
    "promptSystem": "Tu es GPT-4o. Parles en francais de façon didactique.",
    "stream": false
  }'
```

## Support

Pour toute question ou problème concernant l'API, veuillez contacter l'équipe Dragonfly.
