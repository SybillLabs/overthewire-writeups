<h1 align="center">🐧 OverTheWire - Bandit : Level 10 -> 11</h1>

## `> quickstart`
- **Objectif** : se connecter au serveur **OverTheWire** via une connexion SSH en tant que `bandit11`
- **Commandes utilisées** : 
```bash
ls -l /home/bandit10/
base64 -d data.txt
exit
ssh -p 2220 bandit11@bandit.labs.overthewire.org
```

## `> methods`
- Mot de passe stocké dans un fichier **data.txt**, où un encodage `Base64` a été appliqué
- Commande `base64 -d` retenu, outil natif pour décoder du **Base64**

## `> results`

**Connexion réussie en tant que `bandit11`**.

![Connexion réussie](/bandit/12-level10to11/solution.png)

---

<p align="center">  
    <i>⬅️ <a href="/bandit/11-level9to10/rapport.md">Previous level</a></i> | <i><a href="/bandit/13-level11to12/rapport.md">Next level</a> ➡️</i>
</p>
<p align="center">  
    <i>↪️ Back to <a href="/bandit/sommaire.md">OverTheWire : Bandit</a></i>
</p>