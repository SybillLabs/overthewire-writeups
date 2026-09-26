<h1 align="center">🐧 OverTheWire - Bandit : Level 5 -> 6</h1>

## `> quickstart`
- **Objectif** : se connecter au serveur **OverTheWire** via une connexion SSH en tant que `bandit6`
- **Commandes utilisées** : 
```bash
ls -l /home/bandit5/inhere/
find /home/bandit5/inhere/ -type f -size 1033c ! -executable -exec file {} \; | grep "ASCII text"
cat /home/bandit5/inhere/maybehere07/.file2
exit
ssh -p 2220 bandit6@bandit.labs.overthewire.org
```

## `> results`

**Connexion réussie en tant que `bandit6`**.

![Connexion réussie](/bandit/07-level5to6/solution.png)

---

<p align="center">  
    <i>⬅️ <a href="/bandit/06-level4to5/rapport.md">Previous level</a></i> | <i><a href="/bandit/08-level6to7/rapport.md">Next level</a> ➡️</i>
</p>
<p align="center">  
    <i>↪️ Back to <a href="/README.md">OverTheWire : Bandit</a></i>
</p>