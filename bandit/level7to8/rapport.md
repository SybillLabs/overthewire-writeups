# 🎯 OverTheWire - Bandit Level 7 -> 8

## 🧭 Contexte
Pour ce niveau, l'objectif est trouver le mot de passe du compte `bandit8`. Voici les données qui m'ont été fournies :
- **Host** : bandit.labs.overthewire.org
- **Port** : 2220
- **Username** : bandit8
- **Username précédent** : bandit7
- **Password précédent** : (mot de passe du niveau 7)
- **Indication** : Le mot de passe est stocké dans un fichier nommé `data.txt`à côté du mot `millionth`.

## 🛠️ Etapes de connexion

```bash
# Connexion au serveur de jeu avec les identifiants du niveau précédent
ssh -p 2220 bandit7@bandit.labs.overthewire.org
# Comme le fichier contenant le mot de passe est stocké dans un fichier nommé data.txt à côté du mot millionth, je vais chercher dans le répertoire home de l'utilisateur bandit7
ls -l .
cat data.txt | grep millionth
# J'affiche le contenu du fichier data.txt et je cherche le mot millionth pour trouver le mot de passe du niveau 8 que je récupère
    # J'ai utilisé la fonction grep pour chercher le mot millionth dans le fichier data.txt car il y a beaucoup de lignes dans le fichier et je ne voulais pas toutes les afficher
# Je me déconnecte du niveau 7 pour me connecter au niveau 8 avec les nouveaux identifiants
exit
ssh -p 2220 bandit8@bandit.labs.overthewire.org
# Je suis connecté au niveau 8
```

## ✅ Résultat

Après avoir exécuté les étapes ci-dessus, j'ai réussi à me connecter au serveur de jeu en tant que `bandit8`. Le message de bienvenue indique que je suis maintenant connecté en tant que `bandit8`.

![Connexion réussie](/bandit/level7to8/solution.png)

---

[![Sommaire](https://img.shields.io/badge/Back%20to-Sommaire-blue?style=social&logo=github)](/bandit/sommaire.md)