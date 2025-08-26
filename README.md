# hugotest

Ce dépôt contient un site statique généré avec Hugo et déployé automatiquement sur GitHub Pages via GitHub Actions.

## Commandes principales

```sh
# Cloner le dépôt
 git clone https://github.com/<ton-user>/<ton-repo>.git
 cd <ton-repo>

# Créer le site Hugo
 hugo new site .

# Ajouter le thème Ananke
 git submodule add https://github.com/theNewDynamic/gohugo-theme-ananke themes/ananke
 echo 'theme = "ananke"' >> hugo.toml

# Définir l’URL de base
 echo 'baseURL = "https://<ton-user>.github.io/<ton-repo>/"' >> hugo.toml

# Créer une première page
 hugo new content posts/hello-world.md
```

## Déploiement automatique

Le workflow GitHub Actions dans `.github/workflows/hugo.yml` permet de publier le site sur GitHub Pages à chaque push sur `main`.
