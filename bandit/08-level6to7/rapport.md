<h1 align="center">🐧 OverTheWire - Bandit : Level 6 -> 7</h1>

## 🧭 Objectif
L'objectif est de trouver le mot de passe pour l'utilisateur `bandit7` en utilisant les informations trouvées avec l'utilisateur `bandit6`.
> **Note** : Le mot de passe pour l'utilisateur `bandit7`se trouve quelque part dans le serveur, avec les propriétés suivantes : **appartient à l'utilisateur bandit7**, **appartient au groupe bandit6**, **taille de 33 octets**.

## 🛠️ Les commandes utilisés

```bash
# Je suis déjà connecté en tant que bandit6, je peux donc directement trouver le dossier inhere et le fichier avec les bonnes propriétés
# Maintenant il faut trouver le bon fichier avec les bonnes propriétés à la racine du serveur
find / -type f -size 33c -user bandit7 -group bandit6 2>/dev/null
    # find pour trouver
    # / pour chercher dans la racine du serveur
    # -type f pour ne chercher que les fichiers
    # -size 33c pour ne chercher que les fichiers de 33 bytes
    # -user bandit7 pour ne chercher que les fichiers appartenant à l'utilisateur bandit7
    # -group bandit6 pour ne chercher que les fichiers appartenant au groupe bandit
    # 2>/dev/null pour ne pas afficher les erreurs de permission
# Lecture du fichier lisible seulement par l'humain pour obtenir le mot de passe
cat /var/lib/dpkg/info/bandit7.password
# Le mot de passe pour l'utilisateur bandit7 est maintenant affiché dans le terminal.
# Je me déconnecte de bandit6 et me connecte à bandit7
exit
ssh -p 2220 bandit7@bandit.labs.overthewire.org
```

## 📌 Résultat

Après avoir exécuté la commande SSH, j'ai réussi à me connecter au serveur du jeu. Le message de bienvenue indique que je suis maintenant connecté en tant que `bandit7`.

![Connexion réussie](/bandit/08-level6to7/solution.png)

---

<p align="center">  <i>⬅️ <a href="/bandit/07-level5to6/rapport.md">Previous level</a></i> | <i><a href="/bandit/09-level7to8/rapport.md">Next level</a> ➡️</i></p>
<p align="center">  <i>↪️ Back to <a href="/bandit/sommaire.md">Summary</a></i> | <i>📍 From <a href="https://github.com/SybillLabs">SybillLabs</a></i></p>