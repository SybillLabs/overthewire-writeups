<h1 align="center">🐧 OverTheWire - Bandit : Level 5 -> 6</h1>

## 🧭 Objectif
L'objectif est de trouver le mot de passe pour l'utilisateur `bandit6` en utilisant les informations trouvées avec l'utilisateur `bandit5`.
> **Note** : Le mot de passe pour l'utilisateur `bandit6`se trouve dans un fichier se trouvant quelque part dans le dossier `inhere` situé dans le répertoire `home directory`, avec les propriétés suivantes : **lisible seulement par l'humain**, **taille de 1033 octets** et **non exécutable**.

## 🛠️ Les commandes utilisés

```bash
# Je suis déjà connecté en tant que bandit5, je peux donc directement trouver le dossier inhere et le fichier avec les bonnes propriétés
# Toujours vérifié que le dossier et le fichier existent et que j'ai les permissions nécessaires pour le lire
ls -l /home/bandit5/inhere/
# Maintenant il faut trouver le bon fichier avec les bonnes propriétés
find /home/bandit5/inhere/ -type f -size 1033c ! -executable -exec file {} \; | grep "ASCII text"
    # find pour trouver
    # -type f pour ne chercher que les fichiers
    # -size 1033c pour ne chercher que les fichiers de 1033 bytes
    # ! -executable pour ne chercher que les fichiers non exécutables
    # -exec file {} \; pour exécuter la commande file sur chaque fichier trouvé
    # | grep "ASCII text" pour ne garder que les fichiers lisibles par un humain
# Lecture du fichier lisible seulement par l'humain pour obtenir le mot de passe
cat /home/bandit5/inhere/maybehere07/.file2
# Le mot de passe pour l'utilisateur bandit5 est maintenant affiché dans le terminal.
# Je me déconnecte de bandit5 et me connecte à bandit6
exit
ssh -p 2220 bandit6@bandit.labs.overthewire.org
```

## 📌 Résultat

Après avoir exécuté la commande SSH, j'ai réussi à me connecter au serveur du jeu. Le message de bienvenue indique que je suis maintenant connecté en tant que `bandit6`.

![Connexion réussie](/bandit/07-level5to6/solution.png)

---

<p align="center">  <i>⬅️ <a href="/bandit/06-level4to5/rapport.md">Previous level</a></i> | <i><a href="/bandit/08-level6to7/rapport.md">Next level</a> ➡️</i></p>
<p align="center">  <i>↪️ Back to <a href="/bandit/sommaire.md">Summary</a></i> | <i>📍 From <a href="https://github.com/SybillLabs">SybillLabs</a></i></p>