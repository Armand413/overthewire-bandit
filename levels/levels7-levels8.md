# Bandit Level 07 → Level 08

## 🎯 Objectif

Le mot de passe du niveau suivant est stocké dans le fichier `data.txt`, à côté du mot `millionth`.

L'objectif est donc de rechercher la ligne contenant `millionth` dans le fichier.

---

## 🔎 Analyse

Le fichier `data.txt` peut contenir un grand nombre de lignes.

Plutôt que de parcourir le fichier manuellement, j'utilise la commande `grep` pour rechercher directement la chaîne de caractères `millionth`.

---

## 🛠️ Recherche avec grep

Je commence par vérifier la présence du fichier :

```bash
ls
```

Puis je recherche `millionth` dans `data.txt` :

```bash
grep "millionth" data.txt
```

La commande retourne la ligne contenant `millionth` ainsi que le mot de passe associé.

---

## 🔍 Explication de la commande

```bash
grep "millionth" data.txt
```

* `grep` → recherche du texte ;
* `"millionth"` → chaîne recherchée ;
* `data.txt` → fichier dans lequel effectuer la recherche.

Le résultat contient le mot `millionth` suivi du mot de passe du niveau suivant.

> Le mot de passe n'est pas publié dans ce dépôt.

---

## 🧠 Concepts appris

* Recherche de texte dans un fichier
* Utilisation de `grep`
* Filtrage de données
* Recherche efficace dans un fichier contenant de nombr
