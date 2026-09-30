<h1 align="center">🐧 OverTheWire - Bandit : Level 9 -> 10</h1>

## `> quickstart`
- **Objectif** : se connecter au serveur **OverTheWire** via une connexion SSH en tant que `bandit10`
- **Commandes utilisées** : 
```bash
ls -l /home/bandit9/
strings data.txt | grep '=='
exit
ssh -p 2220 bandit10@bandit.labs.overthewire.org
```

## `> methods`
- Mot de passe stocké dans **data.txt**, fichier **binaire** non lisible en clair
- `strings` retenu pour extraire les chaînes lisibles du binaire ; `grep '=='` pour isoler le mot de passe parmi les chaînes extraites

## `> results`

**Connexion réussie en tant que `bandit10`**.

![Connexion réussie](/bandit/11-level9to10/solution.png)

---

<p align="center">  
    <i>⬅️ <a href="/bandit/10-level8to9/rapport.md">Previous level</a></i> | <i><a href="/bandit/12-level10to11/rapport.md">Next level</a> ➡️</i>
</p>
<p align="center">  
    <i>↪️ Back to <a href="/bandit/sommaire.md">OverTheWire : Bandit</a></i>
</p>