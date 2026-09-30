<h1 align="center">🐧 OverTheWire - Bandit : Level 6 -> 7</h1>

## `> quickstart`
- **Objectif** : récupérer le mot de passe du compte `bandit7` depuis `bandit6`
- **Commandes utilisées** : 
```bash
ls -l /home/bandit5/inhere/
find / -type f -size 33c -user bandit7 -group bandit6 2>/dev/null
cat /var/lib/dpkg/info/bandit7.password
exit
ssh -p 2220 bandit7@bandit.labs.overthewire.org
```

## `> methods`
- **Constat** : le mot de passe est stocké dans un fichier dont l'emplacement sur le serveur est inconnu, mais dont les propriétés sont connues :
    - propriétaire : utilisateur `bandit7`
    - groupe propriétaire : `bandit6`
    - taille : 33 octets
- **Action** : recherche du fichier depuis la racine (`/`) avec `find`, en filtrant sur le type fichier, le propriétaire, le groupe et la taille, erreurs d'accès refusé ignorées (`2>/dev/null`), puis lecture du fichier trouvé avec `cat`

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