# Bandit Level 09 → Level 10

## 🎯 Objectif

Le mot de passe du niveau suivant est stocké dans le fichier `data.txt`.

Le fichier contient des données binaires ainsi que des chaînes de caractères lisibles par l'homme.

L'objectif est de trouver la chaîne lisible par l'homme qui est précédée de plusieurs caractères `=`.

---

## 🔎 Analyse

Je commence par identifier le type du fichier :

```bash id="m2t8zv"
file data.txt
```

Le fichier contient des données qui ne sont pas entièrement lisibles directement avec `cat`.

Je vais donc utiliser la commande `strings`.

---

## 🛠️ Extraction des chaînes lisibles

La commande :

```bash id="3y50jv"
strings data.txt
```

permet d'extraire les séquences de caractères lisibles présentes dans le fichier.

Comme l'énoncé indique que la chaîne recherchée est précédée de plusieurs caractères `=`, je peux filtrer le résultat avec `grep`.

```bash id="yl3p4w"
strings data.txt | grep "="
```

Cette commande permet de réduire les résultats et d'identifier la chaîne contenant le mot de passe.

---

## 🔍 Explication des commandes

### `file`

```bash id="z6x5c0"
file data.txt
```

Permet d'identifier le type de fichier.

### `strings`

```bash id="0p0c9w"
strings data.txt
```

Extrait les séquences de caractères imprimables présentes dans le fichier.

### `grep`

```bash id="axwztr"
strings data.txt | grep "="
```

Recherche uniquement les lignes contenant le caractère `=`.

### Pipe `|`

Le pipe permet d'envoyer la sortie de `strings` directement vers `grep`.

```text id="9y6s6x"
data.txt
   ↓
strings
   ↓
texte lisible
   ↓
grep "="
   ↓
résultats pertinents
```

Le résultat correspondant à l'indice fourni par l'énoncé contient le mot de passe du niveau suivant.

> Le mot de passe n'est pas publié dans ce dépôt.

---

## 🧠 Concepts appris

* Identification du type d'un fichier avec `file`
* Extraction de chaînes lisibles avec `strings`
* Recherche avec `grep`
* Utilisation du pipe `|`
* Analyse de fichiers contenant des données non directement lisibles
* Filtrage de résultats

---

## 🔑 Commandes à retenir

```bash
file data.txt
strings data.txt
strings data.txt | grep "="
```

---

## 💡 Ce que je retiens

Un fichier peut contenir des données binaires tout en contenant des chaînes de caractères lisibles.

La commande `strings` permet d'extraire ces chaînes sans avoir besoin d'interpréter directement les données binaires.

La combinaison :

```bash
strings fichier | grep "motif"
```

est particulièrement utile pour rechercher rapidement des informations textuelles dans des fichiers contenant des données mixtes.
