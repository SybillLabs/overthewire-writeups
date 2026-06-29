# 🎯 OverTheWire - Bandit Level 3 ->4

## 🧭 Contexte

Pour ce niveau, l'objectif est de trouver le mot de passe du compte `bandit4`. Voici les données qui m'ont été fournies :
- **Host** : bandit.labs.overthewire.org
- **Port** : 2220
- **Username** : bandit4
- **Username précédent** : bandit3
- **Password précédent** : (mot de passe du niveau 3)
- **Indication** : Le mot de passe du prochain niveau est stocké dans un fichier caché situé dans le dossier nommé `inhere` qui lui même est situé dans le `home directory`.

## 🛠️ Etapes de connexion

```bash
# Connexion au serveur de jeu avec les identifiants du niveau précédent
ssh -p 2220 bandit3@bandit.labs.overthewire.org
# Une fois connecté, j'ai vérifié si je me trouvais dans le home directory de bandit3
pwd
# Je suis dans le home directory de bandit3, je vais chercher le dossier inhere
ls -l ./inhere
# Je me rends dans le dossier inhere pour chercher les fichiers cachés
cd inhere
ls -la
# Je trouve un fichier caché nommé, je lis son contenu pour trouver le mot de passe du niveau 4
cat ./...Hiding-From-You
# Le mot de passe du niveau 4 est affiché dans le fichier ...Hiding-From-You que je note pour la prochaine connexion
# Je me déconnecte du niveau 3
exit
# Je me connecte au niveau 4 avec les nouveaux identifiants
ssh -p 2220 bandit4@bandit.labs.overthewire.org
# Je suis maintenant connecté au niveau 4
```

## ✅ Résultat

Après avoir exécuté les étapes ci-dessus, j'ai réussi à me connecter au serveur de jeu en tant que `bandit4`. Le message de bienvenue indique que je suis maintenant connecté en tant que `bandit4`.

![Connexion réussie](/bandit/level4/solution.png)

---

[![Sommaire](https://img.shields.io/badge/Back%20to-Sommaire-blue?style=social&logo=github)](/bandit/sommaire.md)