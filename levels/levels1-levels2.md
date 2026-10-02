# Bandit Level 01 → Level 02

## 🎯 Objectif

Trouver le mot de passe du niveau suivant.

Après connexion avec l'utilisateur `bandit1`, je liste les fichiers présents :

```bash
ls
```

Un fichier nommé :

```text
-
```

est présent.

## 🔎 Analyse

Le nom du fichier est `-`.

Avec certaines commandes Linux, `-` peut être interprété comme une option plutôt que comme le nom d'un fichier.

Il faut donc indiquer explicitement le chemin du fichier.

## 🛠️ Lecture du fichier

J'utilise :

```bash
cat ./-
```

`./` indique que `-` correspond au fichier situé dans le répertoire courant.

Le contenu affiché correspond au mot de passe du niveau suivant.

> Le mot de passe n'est pas publié dans ce dépôt.

## 🧠 Concepts appris

* Noms de fichiers particuliers
* Chemins relatifs
* Utilisation de `./`
* `cat`
* Interprétation des options Linux

## 🔑 Commande à retenir

```bash
cat ./-
```

## 💡 Ce que je retiens

Lorsqu'un fichier possède un nom qui peut être interprété comme une option, utiliser son chemin (`./nom_du_fichier`) permet d'indiquer clairement à la commande qu'il s'agit d'un fichier.
