<h1 align="center">🐧 OverTheWire - Bandit : Level 6 -> 7</h1>

## `> quickstart`
- **Objectif** : se connecter au serveur **OverTheWire** via une connexion SSH en tant que `bandit7`
- **Commandes utilisées** : 
```bash
ls -l /home/bandit5/inhere/
find / -type f -size 33c -user bandit7 -group bandit6 2>/dev/null
cat /var/lib/dpkg/info/bandit7.password
exit
ssh -p 2220 bandit7@bandit.labs.overthewire.org
```

## `> results`

**Connexion réussie en tant que `bandit6`**.

![Connexion réussie](/bandit/08-level6to7/solution.png)

---

<p align="center">  
    <i>⬅️ <a href="/bandit/07-level5to6/rapport.md">Previous level</a></i> | <i><a href="/bandit/09-level7to8/rapport.md">Next level</a> ➡️</i>
</p>
<p align="center">  
    <i>↪️ Back to <a href="/bandit/sommaire.md">OverTheWire : Bandit</a></i>
</p>