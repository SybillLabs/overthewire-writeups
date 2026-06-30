# 🎯 OverTheWire - Bandit Level 6 -> 7

## 🧭 Contexte
Pour ce niveau, l'objectif est de trouver le mot de passe du compte `bandit7`. Voici les données qui m'ont été fournies :
- **Host** : bandit.labs.overthewire.org
- **Port** : 2220
- **Username** : bandit7
- **Username précédent** : bandit6
- **Password précédent** : (mot de passe du niveau 6)
- **Indication** : Le mot de passe est stocké quelque part dans le serveur et dont il a les propriétés suivantes :
    - Le fichier est `owned by user bandit7`
    - Le fichier est `owned by group bandit6`
    - Le fichier fait exactement 33 bytes

## 🛠️ Etapes de connexion

```bash
# Connexion au serveur de jeu avec les identifiants du niveau précédent
ssh -p 2220 bandit6@bandit.labs.overthewire.org
# Comme le fichier contenant le mot de passe est stocké quelque part dans le serveur, je vais chercher dans la racine du serveur
find / -type f -size 33c -user bandit7 -group bandit6 2>/dev/null
    # find pour trouver
    # / pour chercher dans la racine du serveur
    # -type f pour ne chercher que les fichiers
    # -size 33c pour ne chercher que les fichiers de 33 bytes
    # -user bandit7 pour ne chercher que les fichiers appartenant à l'utilisateur bandit7
    # -group bandit6 pour ne chercher que les fichiers appartenant au groupe bandit
    # 2>/dev/null pour ne pas afficher les erreurs de permission
# J'affiche le contenu du fichier trouvé pour trouver le mot de passe du niveau 7 que je récupère
cat /var/lib/dpkg/info/bandit7.password
# Je me déconnecte du niveau 6 pour me connecter au niveau 7 avec les nouveaux identifiants
exit
ssh -p 2220 bandit7@bandit.labs.overthewire.org
# Je suis connecté au niveau 7
```

## ✅ Résultat

Après avoir exécuté les étapes ci-dessus, j'ai réussi à me connecter au serveur de jeu en tant que `bandit7`. Le message de bienvenue indique que je suis maintenant connecté en tant que `bandit7`.

![Connexion réussie](/bandit/level6to7/solution.png)

---

[![Sommaire](https://img.shields.io/badge/Back%20to-Sommaire-blue?style=social&logo=github)](/bandit/sommaire.md)