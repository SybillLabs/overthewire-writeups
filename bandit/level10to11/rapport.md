# 🎯 OverTheWire - Bandit Level 10 -> 11

## 🧭 Contexte

Pour ce niveau, l'objectif est de trouver le mot de passe du compte `bandit11`. Voici les données qui m'ont été fournies :
- **Host** : bandit.labs.overthewire.org
- **Port** : 2220
- **Username** : bandit11
- **Username précédent** : bandit10
- **Password précédent** : (mot de passe du niveau 10)
- **Indication** : Le mot de passe est stocké dans un fichier nommé `data.txt` qui contient des données encodées en `base64`.

## 🛠️ Etapes de connexion

```bash
# Connexion au serveur de jeu avec les identifiants du niveau précédent
ssh -p 2220 bandit10@bandit.labs.overthewire.org
# Comme le fichier contenant le mot de passe est stocké dans un fichier nommé data.txt qui contient des données encodées en base64, je vais chercher dans le répertoire home de l'utilisateur bandit10
ls -l .
base64 -d data.txt
    # base64 -d pour décoder les données encodées en base64 dans le fichier data.txt
# J'affiche le contenu du fichier data.txt et je décode les données encodées en base64 pour trouver le mot de passe du niveau 11 que je récupère
# Je me déconnecte du niveau 10 pour me connecter au niveau 11 avec les nouveaux identifiants
exit
ssh -p 2220 bandit11@bandit.labs.overthewire.org
# Je suis connecté au niveau 11
```

## ✅ Résultat

Après avoir exécuté les étapes ci-dessus, j'ai réussi à me connecter au serveur de jeu en tant que `bandit11`. Le message de bienvenue indique que je suis maintenant connecté en tant que `bandit11`.

![Connexion réussie](/bandit/level10to11/solution.png)

---

[![Sommaire](https://img.shields.io/badge/Back%20to-Sommaire-blue?style=social&logo=github)](/bandit/sommaire.md)