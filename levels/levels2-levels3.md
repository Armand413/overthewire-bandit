# Bandit Level 02 → Level 03

## 🎯 Objectif

Trouver le mot de passe du niveau suivant parmi les fichiers présents dans le répertoire courant.

## 🔎 Analyse

Je commence par afficher les fichiers présents :

```bash
ls -la
```

Le nom du fichier contient des espaces.

Un nom de fichier contenant des espaces doit être correctement interprété par le shell. Je peux utiliser des guillemets ou échapper les espaces.

## 🛠️ Méthode

Je peux lire le fichier avec :

```bash
cat "nom du fichier"
```

ou en échappant les espaces :

```bash
cat nom\ du\ fichier
```

Le contenu du fichier correspond au mot de passe du niveau suivant.

> Le mot de passe n'est pas publié dans ce dépôt.

## 🧠 Concepts appris

* Noms de fichiers contenant des espaces
* Guillemets dans Bash
* Échappement avec `\`
* Lecture de fichiers avec `cat`

## 🔑 Commandes à retenir

```bash
ls -la
cat "nom du fichier"
```

## 💡 Ce que je retiens

Les espaces sont interprétés par le shell comme des séparateurs entre arguments. Les guillemets ou le caractère `\` permettent de traiter un nom contenant des espaces comme un seul argument.
