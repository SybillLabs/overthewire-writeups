# 🎯 OverTheWire - Bandit Level 2 -> 3

## 🧭 Contexte

Pour ce niveau, l'objectif est de trouver le mot de passe du compte `bandit3`. Voici les données qui m'ont été fournies :
- **Host** : bandit.labs.overthewire.org
- **Port** : 2220
- **Username** : bandit3
- **Username précédent** : bandit2
- **Password précédent** : (mot de passe du niveau 2)
- **Indication** : Le mot de passe du prochain niveau est stocké dans un fichier nommé `--spaces in this filename--` situé dans le `home directory`.

## 🛠️ Etapes de connexion

```bash
# Connexion au serveur de jeu avec les identifiants du niveau précédent
ssh -p 2220 bandit2@bandit.labs.overthewire.org
# Une fois connecté, j'ai vérifié si je me trouvais dans le home directory de bandit2
pwd
# Je suis dans le home directory de bandit2, je vais chercher le fichier nommé --spaces in this filename--
ls -l ./--spaces\ in\ this\ filename--
# Je lis le contenu du fichier --spaces in this filename-- pour trouver le mot de passe du niveau 3
cat ./--spaces\ in\ this\ filename--
# Le mot de passe du niveau 3 est affiché dans le fichier --spaces in this filename-- que je note pour la prochaine connexion
# Je me déconnecte du niveau 2
exit
# Je me connecte au niveau 3 avec les nouveaux identifiants
ssh -p 2220 bandit3@bandit.labs.overthewire.org
# Je suis maintenant connecté au niveau 3
```

## ✅ Résultat

Après avoir exécuté les étapes ci-dessus, j'ai réussi à me connecter au serveur de jeu en tant que `bandit3`. Le message de bienvenue indique que je suis maintenant connecté en tant que `bandit3`.

![Connexion réussie](/bandit/level3/solution.png)

---

[![Sommaire](https://img.shields.io/badge/Back%20to-Sommaire-blue?style=social&logo=github)](/bandit/sommaire.md)