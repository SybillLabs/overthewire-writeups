# 🎯 OverTheWire - Bandit Level 5 -> 6

## 🧭 Contexte

Pour ce niveau, l'objectif est de trouver le mot de passe du compte `bandit6`. Voici les données qui m'ont été fournies :
- **Host** : bandit.labs.overthewire.org
- **Port** : 2220
- **Username** : bandit6
- **Username précédent** : bandit5
- **Password précédent** : (mot de passe du niveau 5)
- **Indication** : Le mot de passe du prochain niveau est stocké dans un fichier se trouvant dans le dossier `inhere` et dont  il a les propriétés suivantes :
    - Le fichier est lisible que par un humain
    - Le fichier fait exactement 1033 bytes
    - Le fichier est non exécutable

## 🛠️ Etapes de connexion

```bash
# Connexion au serveur de jeu avec les identifiants du niveau précédent
ssh -p 2220 bandit5@bandit.labs.overthewire.org
# Une fois connecté, j'ai vérifié si je me trouvais dans le home directory de bandit5
pwd
# Je suis dans le home directory de bandit5, je vérifier que le dossier n'est pas vide et tous les sous-dossiers présents
ls -la .
ls -la ./inhere
# Maintenant, je recherche le fichier qui correspond aux propriétés données dans l'indication
find . -type f -size 1033c ! -executable -exec file {} \; | grep "ASCII text"
    # find pour trouver
    # -type f pour ne chercher que les fichiers
    # -size 1033c pour ne chercher que les fichiers de 1033 bytes
    # ! -executable pour ne chercher que les fichiers non exécutables
    # -exec file {} \; pour exécuter la commande file sur chaque fichier trouvé
    # | grep "ASCII text" pour ne garder que les fichiers lisibles par un humain
# J'affiche le contenu du fichier trouvé pour trouver le mot de passe du niveau 6 que je récupère
cat ./inhere/maybehere07/.file2
# Je me déconnecte du niveau 5 pour me connecter au niveau 6 avec les nouveaux identifiants
exit
ssh -p 2220 bandit6@bandit.labs.overthewire.org
# Je suis connecté au niveau 6 avec le mot de passe récupéré dans le fichier
```

## ✅ Résultat

Après avoir exécuté les étapes ci-dessus, j'ai réussi à me connecter au serveur de jeu en tant que `bandit6`. Le message de bienvenue indique que je suis maintenant connecté en tant que `bandit6`.

![Connexion réussie](/bandit/level5to6/solution.png)

---

[![Sommaire](https://img.shields.io/badge/Back%20to-Sommaire-blue?style=social&logo=github)](/bandit/sommaire.md)