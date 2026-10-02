# Bandit Level 08 → Level 09

## 🎯 Objectif

Le mot de passe du niveau suivant est stocké dans le fichier `data.txt`.

Le mot de passe constitue **la seule ligne qui apparaît une seule fois** dans le fichier.

---

## 🔎 Analyse

Le fichier contient un grand nombre de lignes.

L'objectif n'est pas de rechercher un mot précis, mais de trouver **la ligne qui n'est présente qu'une seule fois**.

Pour cela, je peux utiliser deux commandes Linux :

* `sort` → trier les lignes ;
* `uniq` → identifier les lignes répétées ou uniques.

---

## 🛠️ Méthode

Je commence par examiner le fichier :

```bash id="8fjf2z"
ls
```

Puis :

```bash id="v0uf8r"
cat data.txt
```

Comme le fichier contient beaucoup de lignes, je ne vais pas les analyser manuellement.

Je trie d'abord les lignes :

```bash id="h6ub8w"
sort data.txt
```

Puis j'utilise `uniq -u` pour afficher uniquement les lignes qui apparaissent une seule fois :

```bash id="k9y5fn"
sort data.txt | uniq -u
```

La sortie correspond au mot de passe du niveau suivant.

> Le mot de passe n'est pas publié dans ce dépôt.

---

## 🔍 Explication de la commande

```bash id="d9x6rd"
sort data.txt | uniq -u
```

### `sort`

```bash id="y7xwqz"
sort data.txt
```

Trie les lignes du fichier dans l'ordre.

Le tri est important car `uniq` compare principalement les lignes identiques lorsqu'elles sont consécutives.

### `|`

Le symbole `|`, appelé **pipe**, transmet la sortie de `sort` comme entrée de `uniq`.

### `uniq -u`

```bash id="l9k7cc"
uniq -u
```

Affiche uniquement les lignes qui apparaissent une seule fois.

---

## 🧠 Concepts appris

* `sort`
* `uniq`
* Pipe `|`
* Recherche de lignes uniques
* Traitement de données dans le terminal
* Combinaison de plusieurs commandes Linux

---

## 🔑 Commande à retenir

```bash id="8q3v0m"
sort data.txt | uniq -u
```

---

## 💡 Ce que je retiens

Certaines recherches ne consistent pas à chercher un mot précis, mais à identifier une caractéristique des données.

Ici, l'information importante était que le mot de passe était **la seule ligne unique**.

La combinaison :

```bash id="f2b6ec"
sort fichier | uniq -u
```

permet de retrouver efficacement une ligne qui n'apparaît qu'une seule fois.

Cette méthode est également utile pour analyser et filtrer des données en cybersécurité.
