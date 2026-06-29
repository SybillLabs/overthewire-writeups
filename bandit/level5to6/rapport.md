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
# Je suis dans le home directory de bandit5, je vais chercher le dossier inhere
ls -l ./inhere
# Je me rends dans le dossier inhere pour chercher les fichiers
cd inhere

```