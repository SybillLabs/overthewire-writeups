# 🎯 OverTheWire - Bandit Level 9 -> 10

## 🧭 Contexte

Pour ce niveau, l'objectif est de trouver le mot de passe du compte `bandit10`. Voici les données qui m'ont été fournies :
- **Host** : bandit.labs.overthewire.org
- **Port** : 2220
- **Username** : bandit10
- **Username précédent** : bandit9
- **Password précédent** : (mot de passe du niveau 9)
- **Indication** : Le mot de passe est stocké dans un fichier nommé `data.txt` dans l'une des rares `strings` lisible par un humain et qui est précédé par plusieurs `=`.

## 🛠️ Etapes de connexion

```bash
# Connexion au serveur de jeu avec les identifiants du niveau précédent
ssh -p 2220 bandit9@bandit.labs.overthewire.org
# Comme le fichier contenant le mot de passe est stocké dans un fichier nommé data.txt dans l'une des rares strings lisible par un humain et qui est précédé par plusieurs =, je vais chercher dans le répertoire home de l'utilisateur bandit9
ls -l .
strings data.txt | grep ==
    # strings pour afficher les chaînes de caractères lisibles par un humain dans le fichier data.txt
    # | grep == pour ne garder que les chaînes de caractères précédées par plusieurs =
# J'affiche le contenu du fichier data.txt et je cherche la chaîne de caractères précédée par plusieurs = pour trouver le mot de passe du niveau 10 que je récupère
# Je me déconnecte du niveau 9 pour me connecter au niveau 10 avec les nouveaux identifiants
exit
ssh -p 2220 bandit10@bandit.labs.overthewire.org
# Je suis connecté au niveau 10
```

## ✅ Résultat

Après avoir exécuté les étapes ci-dessus, j'ai réussi à me connecter au serveur de jeu en tant que `bandit10`. Le message de bienvenue indique que je suis maintenant connecté en tant que `bandit10`.

![Connexion réussie](/bandit/level9to10/solution.png)

---

[![Sommaire](https://img.shields.io/badge/Back%20to-Sommaire-blue?style=social&logo=github)](/bandit/sommaire.md)