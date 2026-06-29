# 🎯 OverTheWire - Bandit Level 1 -> 2

## 🧭 Contexte

Pour ce niveau, l'objectif est de trouver le mot de passe du compte `bandit2`. Voici les données qui m'ont été fournies :
- **Host** : bandit.labs.overthewire.org
- **Port** : 2220
- **Username** : bandit2
- **Username précédent** : bandit1
- **Password précédent** : (mot de passe du niveau 1)
- **Indication** : Le mot de passe du prochain niveau est stocké dans un fichier nommé `-` situé dans le `home directory`.

## 🛠️ Etapes de connexion

```bash
# Connexion au serveur de jeu avec les identifiants du niveau précédent
ssh -p 2220 bandit1@bandit.labs.overthewire.org
# Une fois connecté, j'ai vérifié si je me trouvais dans le home directory de bandit1
pwd
# Je suis dans le home directory de bandit1, je vais chercher le fichier nommé -
ls -l ./-
# Je lis le contenu du fichier - pour trouver le mot de passe du niveau 2
cat ./-
# Le mot de passe du niveau 2 est affiché dans le fichier - que je note pour la prochaine connexion
# Je me déconnecte du niveau 1
exit
# Je me connecte au niveau 2 avec les nouveaux identifiants
ssh -p 2220 bandit2@bandit.labs.overthewire.org
# Je suis maintenant connecté au niveau 2
```

## ✅ Résultat

Après avoir exécuté les étapes ci-dessus, j'ai réussi à me connecter au serveur de jeu en tant que `bandit2`. Le message de bienvenue indique que je suis maintenant connecté en tant que `bandit2`.

![Connexion réussie](/bandit/level1to2/solution.png)

---

[![Sommaire](https://img.shields.io/badge/Back%20to-Sommaire-blue?style=social&logo=github)](/bandit/sommaire.md)