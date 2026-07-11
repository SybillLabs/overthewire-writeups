# 🎯 OverTheWire - Bandit Level 11 -> 12

## 🧭 Contexte

Pour ce niveau, l'objectif est de trouver le mot de passe du compte `bandit12`. Voici les données qui m'ont été fournies :
- **Host** : bandit.labs.overthewire.org
- **Port** : 2220
- **Username** : bandit12
- **Username précédent** : bandit11
- **Password précédent** : (mot de passe du niveau 11)
- **Indication** : Le mot de passe est stocké dans un fichier nommé `data.txt` où tous les caractères (minusciles & majuscules) ont été décalés de 13 positions dans l'alphabet. Il s'agit d'une technique de chiffrement appelée ROT13.

> **C'est quoi le _ROT13_ ?**  
Le ROT13 est une méthode de chiffrement par substitution simple qui remplace chaque lettre par la lettre située 13 positions plus loin dans l'alphabet. Par exemple, 'A' devient 'N', 'B' devient 'O', et ainsi de suite. Cette technique est souvent utilisée pour masquer du texte de manière légère, mais elle n'est pas sécurisée pour des applications sérieuses.

## 🛠️ Etapes de connexion

```bash
# Connexion au serveur de jeu avec les identifiants du niveau précédent
ssh -p 2220 bandit11@bandit.labs.overthewire.org
# Comme le fichier contenant le mot de passe est stocké dans un fichier nommé data.txt où tous les caractères (minusciles & majuscules) ont été décalés de 13 positions dans l'alphabet, je vais chercher dans le répertoire home de l'utilisateur bandit11
ls -l .
tr 'A-Za-z' 'N-ZA-Mn-za-m' < data.txt
    # tr pour traduire les caractères du fichier data.txt
    # 'A-Za-z' 'N-ZA-Mn-za-m' pour décaler les caractères de 13 positions dans l'alphabet (ROT13)
    # < data.txt pour lire le contenu du fichier data.txt et le passer à la commande tr
# J'affiche le contenu du fichier data.txt et je décode les caractères décalés de 13 positions dans l'alphabet pour trouver le mot de passe du niveau 12 que je récupère
# Je me déconnecte du niveau 11 pour me connecter au niveau 12 avec les nouveaux identifiants
exit
ssh -p 2220 bandit12@bandit.labs.overthewire.org
# Je suis connecté au niveau 12
```

## ✅ Résultat

Après avoir exécuté les étapes ci-dessus, j'ai réussi à me connecter au serveur de jeu en tant que `bandit12`. Le message de bienvenue indique que je suis maintenant connecté en tant que `bandit12`.

![Connexion réussie](/bandit/level11to12/solution.png)

---

[![Sommaire](https://img.shields.io/badge/Back%20to-Sommaire-blue?style=social&logo=github)](/bandit/sommaire.md)
