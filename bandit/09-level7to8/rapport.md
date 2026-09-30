<h1 align="center">🐧 OverTheWire - Bandit : Level 7 -> 8</h1>

## `> quickstart`
- **Objectif** : récupérer le mot de passe du compte `bandit8` depuis `bandit7`
- **Commandes utilisées** : 
```bash
ls -l /home/bandit7/
cat /home/bandit7/data.txt | grep "millionth"
exit
ssh -p 2220 bandit8@bandit.labs.overthewire.org
```

## `> methods`
- **Constat** : le mot de passe se trouve dans `data.txt`, à côté du mot **millionth**
- **Action** : lecture de `data.txt` avec `cat`, puis filtrage des lignes contenant **millionth** avec `grep`

## `> results`

**Connexion réussie en tant que `bandit8`**.

![Connexion réussie](/bandit/09-level7to8/solution.png)

---

<p align="center">  
    <i>⬅️ <a href="/bandit/08-level6to7/rapport.md">Previous level</a></i> | <i><a href="/bandit/10-level8to9/rapport.md">Next level</a> ➡️</i>
</p>
<p align="center">  
    <i>↪️ Back to <a href="/bandit/sommaire.md">OverTheWire : Bandit</a></i>
</p>