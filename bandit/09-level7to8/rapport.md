<h1 align="center">🐧 OverTheWire - Bandit : Level 7 -> 8</h1>

## 🧭 Objectif
L'objectif est de trouver le mot de passe pour l'utilisateur `bandit8` en utilisant les informations trouvées avec l'utilisateur `bandit7`.
> **Note** : Le mot de passe pour l'utilisateur `bandit8`se trouve dans le fichier `data.txt` à côté du mot `millionth`.

## 🛠️ Les commandes utilisés

```bash
# Je suis déjà connecté en tant que bandit7, je peux donc directement trouver le fichier data.txt.
ls -l /home/bandit7/
cat /home/bandit7/data.txt | grep "millionth"
    # cat pour afficher le contenu du fichier data.txt
    # | grep "millionth" pour ne garder que la ligne contenant le mot millionth
# Le mot de passe pour l'utilisateur bandit8 est maintenant affiché dans le terminal.
# Je me déconnecte de bandit7 et me connecte à bandit8
exit
ssh -p 2220 bandit8@bandit.labs.overthewire.org
```

## 📌 Résultat

Après avoir exécuté la commande SSH, j'ai réussi à me connecter au serveur du jeu. Le message de bienvenue indique que je suis maintenant connecté en tant que `bandit8`.

![Connexion réussie](/bandit/09-level7to8/solution.png)

---

<p align="center">  <i>⬅️ <a href="/bandit/08-level6to7/rapport.md">Previous level</a></i> | <i><a href="/bandit/10-level8to9/rapport.md">Next level</a> ➡️</i></p>
<p align="center">  <i>↪️ Back to <a href="/bandit/sommaire.md">Summary</a></i> | <i>📍 From <a href="https://github.com/SybillLabs">SybillLabs</a></i></p>