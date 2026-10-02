# Bandit Level 03 → Level 04

## 🎯 Objectif

Trouver le mot de passe du niveau suivant dans le répertoire `inhere`.

## 🔎 Analyse

Je commence par examiner le contenu du répertoire :

```bash
ls -la
```

L'option `-a` permet d'afficher également les fichiers cachés.

Je me rends ensuite dans le répertoire :

```bash
cd inhere
```

Puis :

```bash
ls -la
```

Un fichier caché est présent.

## 🛠️ Lecture du fichier

Je peux lire directement le fichier caché avec :

```bash
cat .<nom_du_fichier>
```

Le contenu correspond au mot de passe du niveau suivant.

> Le mot de passe n'est pas publié dans ce dépôt.

## 🧠 Concepts appris

* Fichiers cachés sous Linux
* `ls -a`
* `ls -la`
* Convention des fichiers commençant par `.`
* Navigation avec `cd`
* Lecture avec `cat`

## 🔑 Commandes à retenir

```bash
ls -la
cd inhere
cat .<nom_du_fichier>
```

## 💡 Ce que je retiens

Sous Linux, les fichiers dont le nom commence par `.` sont généralement cachés. L'option `-a` de `ls` permet de les afficher.
