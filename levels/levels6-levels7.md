# Bandit Level 06 → Level 07

## 🎯 Objectif

Le mot de passe du niveau suivant est stocké quelque part sur le serveur.

Le fichier possède les propriétés suivantes :

* appartient à l'utilisateur `bandit7` ;
* appartient au groupe `bandit6` ;
* sa taille est de **33 octets**.

---

## 🔎 Analyse

Contrairement aux niveaux précédents, le fichier peut se trouver n'importe où sur le système.

Je dois donc effectuer une recherche depuis la racine `/`.

L'énoncé fournit trois critères permettant d'identifier le fichier :

| Critère                | Option `find`    |
| ---------------------- | ---------------- |
| Fichier                | `-type f`        |
| Propriétaire `bandit7` | `-user bandit7`  |
| Groupe `bandit6`       | `-group bandit6` |
| Taille de 33 octets    | `-size 33c`      |

---

## 🛠️ Recherche du fichier

J'utilise la commande suivante :

```bash
find / -type f -user bandit7 -group bandit6 -size 33c 2>/dev/null
```

### Explication

* `find /` → recherche depuis la racine du système ;
* `-type f` → recherche uniquement les fichiers ;
* `-user bandit7` → fichier appartenant à l'utilisateur `bandit7` ;
* `-group bandit6` → fichier appartenant au groupe `bandit6` ;
* `-size 33c` → fichier d'une taille exacte de 33 octets ;
* `2>/dev/null` → masque les messages d'erreur liés aux permissions.

La commande permet de trouver directement le fichier correspondant aux trois critères.

---

## 🔍 Lecture du fichier

Une fois le chemin du fichier obtenu, je peux afficher son contenu avec :

```bash
cat /chemin/du/fichier
```

Le contenu du fichier correspond au mot de passe permettant d'accéder au niveau suivant.

> Le mot de passe n'est pas publié dans ce dépôt.

---

## 🧠 Concepts appris

* Recherche récursive avec `find`
* Recherche depuis la racine `/`
* Recherche par propriétaire
* Recherche par groupe
* Recherche par taille
* Redirection des erreurs avec `2>/dev/null`
* Lecture de fichiers avec `cat`
* Utilisation de métadonnées pour identifier un fichier

---

## 🔑 Commande à retenir

```bash
find / -type f -user bandit7 -group bandit6 -size 33c 2>/dev/null
```

---

## 💡 Ce que je retiens

Lorsqu'un fichier peut se trouver n'importe où sur un système Linux, il est possible d'utiliser `find` avec plusieurs critères pour réduire rapidement la recherche.

Les informations comme le propriétaire, le groupe et la taille permettent d'identifier un fichier sans avoir besoin d'examiner manuellement tous les fichiers du système.
