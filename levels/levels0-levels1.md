# Bandit Level 00 → Level 01

## 🎯 Objectif

Se connecter au serveur Bandit avec les identifiants fournis et trouver le mot de passe permettant d'accéder au niveau suivant.

## 🔐 Connexion

Connexion au serveur avec SSH :

```bash
ssh bandit0@bandit.labs.overthewire.org -p 2220
```

Après la connexion, je vérifie les fichiers présents :

```bash
ls
```

Un fichier nommé `readme` est présent.

## 🛠️ Lecture du fichier

Je lis son contenu avec :

```bash
cat readme
```

Le contenu du fichier contient le mot de passe permettant d'accéder au niveau suivant.

> Le mot de passe n'est pas publié dans ce dépôt.

## 🧠 Concepts appris

* SSH
* Connexion à distance
* Linux
* `ls`
* `cat`
* Lecture de fichiers

## 🔑 Commandes à retenir

```bash
ssh
ls
cat
```

## 💡 Ce que je retiens

La commande `ls` permet d'identifier les fichiers présents dans un répertoire et `cat` permet d'afficher le contenu d'un fichier texte.
