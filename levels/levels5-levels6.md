# Bandit Level 05 → Level 06

## 🎯 Objectif

Le mot de passe du niveau suivant est stocké dans un fichier situé quelque part sous le répertoire `inhere`.

Le fichier possède les propriétés suivantes :

* lisible par l'homme ;
* taille de **1033 octets** ;
* non exécutable.

---

## 🔎 Analyse

Le répertoire `inhere` contient plusieurs sous-répertoires et fichiers.
Il serait inefficace de parcourir chaque fichier manuellement.

J'utilise donc la commande `find` afin de rechercher automatiquement les fichiers correspondant aux critères donnés.

---

## 🛠️ Recherche du fichier

Première recherche avec le critère de taille :

```bash
find inhere -type f -size 1033c
```

Explication :

* `find inhere` → recherche dans `inhere` et tous ses sous-répertoires ;
* `-type f` → recherche uniquement des fichiers ;
* `-size 1033c` → recherche les fichiers dont la taille est exactement de 1033 octets ;
* `c` signifie que la taille est exprimée en octets.

Pour ajouter le critère indiquant que le fichier ne doit pas être exécutable :

```bash
find inhere -type f -size 1033c ! -executable
```

Cette commande permet de réduire directement la recherche au fichier correspondant aux critères de l'énoncé.

---

## 🔍 Vérification du fichier

Une fois le fichier identifié, j'utilise `file` pour vérifier son type :

```bash
file <chemin_du_fichier>
```

Puis je lis son contenu avec :

```bash
cat <chemin_du_fichier>
```

Le contenu obtenu correspond au mot de passe permettant d'accéder au niveau suivant.

> Le mot de passe n'est pas publié dans ce dépôt.

---

## 🧠 Concepts appris

* Recherche récursive avec `find`
* Recherche par type de fichier
* Recherche par taille
* Vérification des permissions d'exécution
* Utilisation de `file`
* Lecture d'un fichier avec `cat`
* Transformation des indices d'un énoncé en critères de recherche Linux

---

## 🔐 Commande principale à retenir

```bash
find inhere -type f -size 1033c ! -executable
```

## 💡 Ce que je retiens

Plutôt que de parcourir manuellement un grand nombre de fichiers, il est plus efficace d'utiliser les caractéristiques fournies par l'énoncé comme critères pour `find`.

Cette approche est particulièrement utile lors de recherches de fichiers sur un système Linux.
