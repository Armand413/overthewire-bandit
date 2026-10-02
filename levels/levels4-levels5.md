# Bandit Level 04 → Level 05

## 🎯 Objectif

Le mot de passe du niveau suivant se trouve dans un fichier situé sous le répertoire `inhere`.

Plusieurs fichiers sont présents, mais un seul contient des données lisibles par l'homme.

## 🔎 Analyse

Je commence par examiner le contenu :

```bash
ls -la
```

Puis :

```bash
cd inhere
ls -la
```

Plusieurs fichiers sont présents. Plutôt que de lire chaque fichier manuellement, je peux utiliser la commande `file` pour déterminer leur type.

## 🛠️ Identification des fichiers

Pour examiner plusieurs fichiers :

```bash
file ./*
```

La commande permet d'identifier le type de contenu de chaque fichier.

Je recherche le fichier dont le contenu est identifié comme du texte ASCII ou comme un fichier texte lisible.

Une fois identifié :

```bash
cat ./<fichier>
```

Le contenu correspond au mot de passe du niveau suivant.

> Le mot de passe n'est pas publié dans ce dépôt.

## 🧠 Concepts appris

* Recherche de fichiers
* Fichiers binaires vs fichiers texte
* Commande `file`
* Wildcards avec `*`
* Lecture avec `cat`

## 🔑 Commandes à retenir

```bash
file ./*
cat ./<fichier>
```

## 💡 Ce que je retiens

La commande `file` permet d'identifier le type réel d'un fichier. Elle est particulièrement utile lorsqu'on possède plusieurs fichiers et qu'on ne sait pas lequel contient des données lisibles.
