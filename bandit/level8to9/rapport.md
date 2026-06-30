# 🎯 OverTheWire - Bandit Level 8 -> 9

## 🧭 Contexte

Pour ce niveau, l'objectif est de trouver le mot de passe du compte `bandit9`. Voici les données qui m'ont été fournies :
- **Host** : bandit.labs.overthewire.org
- **Port** : 2220
- **Username** : bandit9
- **Username précédent** : bandit8
- **Password précédent** : (mot de passe du niveau 8)
- **Indication** : Le mot de passe est stocké dans un fichier nommé `data.txt`et c'est la seule ligne du fichier qui n'apparait qu'une seule fois.

## 🛠️ Etapes de connexion

```bash
# Connexion au serveur de jeu avec les identifiants du niveau précédent
ssh -p 2220 bandit8@bandit.labs.overthewire.org
# Comme le fichier contenant le mot de passe est stocké dans un fichier nommé data.txt et c'est la seule ligne du fichier qui n'apparait qu'une seule fois, je vais chercher dans le répertoire home de l'utilisateur bandit8
ls -l .
sort data.txt | uniq -u
    # sort pour trier les lignes du fichier data.txt
    # uniq -u pour ne garder que les lignes uniques du fichier data.txt
# J'affiche le contenu du fichier data.txt et je cherche la seule ligne qui n'apparait qu'une seule fois pour trouver le mot de passe du niveau 9 que je récupère
# Je me déconnecte du niveau 8 pour me connecter au niveau 9 avec les nouveaux identifiants
exit
ssh -p 2220 bandit9@bandit.labs.overthewire.org
# Je suis connecté au niveau 9
```

## ✅ Résultat

Après avoir exécuté les étapes ci-dessus, j'ai réussi à me connecter au serveur de jeu en tant que `bandit9`. Le message de bienvenue indique que je suis maintenant connecté en tant que `bandit9`.

![Connexion réussie](/bandit/level8to9/solution.png)

---

[![Sommaire](https://img.shields.io/badge/Back%20to-Sommaire-blue?style=social&logo=github)](/bandit/sommaire.md)