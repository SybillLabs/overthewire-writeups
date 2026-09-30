<h1 align="center">🐧 OverTheWire - Bandit : Level 10 -> 11</h1>

## `> quickstart`
- **Objectif** : récupérer le mot de passe du compte `bandit11` depuis `bandit10`
- **Commandes utilisées** : 
```bash
ls -l /home/bandit10/
base64 -d data.txt
exit
ssh -p 2220 bandit11@bandit.labs.overthewire.org
```

## `> methods`
- **Constat** : le mot de passe se trouve dans `data.txt`, encodé en **Base64**
- **Action** : décodage du contenu de `data.txt` avec `base64 -d`, résultat lu directement en sortie standard

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