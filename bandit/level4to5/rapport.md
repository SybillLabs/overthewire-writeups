# 🎯 OverTheWire - Bandit Level 4 -> 5

## 🧭 Contexte
Pour ce niveau, l'objectif est de trouver le mot de passe du compte `bandit5`. Voici les données qui m'ont été fournies :
- **Host** : bandit.labs.overthewire.org
- **Port** : 2220
- **Username** : bandit5
- **Username précédent** : bandit4
- **Password précédent** : (mot de passe du niveau 4)
- **Indication** : Le mot de passe du prochain niveau est stocké dans un fichier situé dans le dossier `inhere`. Cependant, ce dossier contient plusieurs fichiers, et le mot de passe est stocké dans le fichier qui est seulement lisible par un humain.

## 🛠️ Etapes de connexion

```bash
# Connexion au serveur de jeu avec les identifiants du niveau précédent
ssh -p 2220 bandit4@bandit.labs.overthewire.org
# Une fois connecté, j'ai vérifié si je me trouvais dans le home directory de bandit4
pwd
# Je suis dans le home directory de bandit4, je vais chercher le dossier inhere
ls -l ./inhere
# Je me rends dans le dossier inhere pour chercher les fichiers
cd inhere
ls -l
# Je trouve plusieurs fichiers, je vais chercher celui qui est seulement lisible par un humain grâce à la commande file 
file ./-file0*
# Je trouve le fichier qui est seulement lisible par un humain (noté ASCII text), je lis son contenu pour trouver le mot de passe du niveau 5
cat ./-file07
# Le mot de passe du niveau 5 est affiché dans le fichier -file07 que je note pour la prochaine connexion
# Je me déconnecte du niveau 4
exit
# Je me connecte au niveau 5 avec les nouveaux identifiants
ssh -p 2220 bandit5@bandit.labs.overthewire.org
# Je suis maintenant connecté au niveau 5
```

## ✅ Résultat

Après avoir exécuté les étapes ci-dessus, j'ai réussi à me connecter au serveur de jeu en tant que `bandit5`. Le message de bienvenue indique que je suis maintenant connecté en tant que `bandit5`.

![Connexion réussie](/bandit/level4to5/solution.png)

---

[![Sommaire](https://img.shields.io/badge/Back%20to-Sommaire-blue?style=social&logo=github)](/bandit/sommaire.md)