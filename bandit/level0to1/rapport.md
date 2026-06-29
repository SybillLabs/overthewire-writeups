# 🎯 OverTheWire - Bandit Level 0 -> 1

## 🧭 Contexte

Pour ce niveau, l'objectif est de trouver le mot de passe du compte `bandit1`. Voici les données qui m'ont été fournies :
- **Host** : bandit.labs.overthewire.org
- **Port** : 2220
- **Username** : bandit1
- **Username précédent** : bandit0
- **Password précédent** : bandit0
- **Indication** : Le mot de passe du prochain niveau est stocké dans un fichier nommé `readme` situé dans le `home direcotory`.

## 🛠️ Etapes de connexion

```bash
# Connexion au serveur de jeu avec les identifiants du niveau précédent
ssh -p 2220 bandit0@bandit.labs.overthewire.org
# Une fois connecté, j'ai vérifié si je me trouvais dans le home directory de bandit0
pwd
# Je suis dans le home directory de bandit0, je vais chercher le fichier readme
ls -l readme
# Je lis le contenu du fichier readme pour trouver le mot de passe du niveau 1
cat readme
# Le mot de passe du niveau 1 est affiché dans le fichier readme que je note pour la prochaine connexion
# Je me déconnecte du niveau 0
exit
# Je me connecte au niveau 1 avec les nouveaux identifiants
ssh -p 2220 bandit1@bandit.labs.overthewire.org
```

## ✅ Résultat

Après avoir exécuté les étapes ci-dessus, j'ai réussi à me connecter au serveur de jeu en tant que `bandit1`. Le message de bienvenue indique que je suis maintenant connecté en tant que `bandit1`.

![Connexion réussie](/bandit/level1/solution.png)

---

[![Sommaire](https://img.shields.io/badge/Back%20to-Sommaire-blue?style=social&logo=github)](/bandit/sommaire.md)