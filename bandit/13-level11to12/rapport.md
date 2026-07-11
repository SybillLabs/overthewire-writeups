<h1 align="center">🐧 OverTheWire - Bandit : Level 11 -> 12</h1>

## 🧭 Objectif
L'objectif est de trouver le mot de passe pour l'utilisateur `bandit12` en utilisant les informations trouvées avec l'utilisateur `bandit11`.
> **Note** : Le mot de passe pour l'utilisateur `bandit12`se trouve dans le fichier `data.txt` où toutes les miniscules `a-z` et les majuscules `A-Z` ont été décalées de 13 positions.  
Il s'agit d'une technique de chiffrement appelée ROT13.

> **C'est quoi le ROT13 ?**  
Le ROT13 est une méthode de chiffrement par substitution simple qui remplace chaque lettre par la lettre située 13 positions plus loin dans l'alphabet. Par exemple, 'A' devient 'N', 'B' devient 'O', et ainsi de suite. Cette technique est souvent utilisée pour masquer du texte de manière légère, mais elle n'est pas sécurisée pour des applications sérieuses.

## 🛠️ Les commandes utilisés

```bash
# Je suis déjà connecté en tant que bandit11, je peux donc directement trouver le fichier data.txt.
ls -l /home/bandit11/
tr 'A-Za-z' 'N-ZA-Mn-za-m' < data.txt
    # tr pour traduire les caractères du fichier data.txt
    # 'A-Za-z' 'N-ZA-Mn-za-m' pour décaler les caractères de 13 positions dans l'alphabet (ROT13)
    # On sépare majuscules et minuscules et on réordonne chaque alphabet en deux blocs (N‑Z puis A‑M) car tr exige des plages continues pour appliquer correctement le décalage ROT13.
    # < data.txt pour lire le contenu du fichier data.txt et le passer à la commande tr
# Le mot de passe pour l'utilisateur bandit12 est maintenant affiché dans le terminal.
# Je me déconnecte de bandit11 et me connecte à bandit12
exit
ssh -p 2220 bandit12@bandit.labs.overthewire.org
```

## 📌 Résultat

Après avoir exécuté la commande SSH, j'ai réussi à me connecter au serveur du jeu. Le message de bienvenue indique que je suis maintenant connecté en tant que `bandit12`.

![Connexion réussie](/bandit/13-level11to12/solution.png)

---

<p align="center">  <i>⬅️ <a href="/bandit/12-level10to11/rapport.md">Previous level</a></i> | <i><a href="/bandit/14-level12to13/rapport.md">Next level</a> ➡️</i></p>
<p align="center">  <i>↪️ Back to <a href="/bandit/sommaire.md">Summary</a></i> | <i>📍 From <a href="https://github.com/SybillLabs">SybillLabs</a></i></p>