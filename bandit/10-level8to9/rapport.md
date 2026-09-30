<h1 align="center">🐧 OverTheWire - Bandit : Level 8 -> 9</h1>

## `> quickstart`
- **Objectif** : se connecter au serveur **OverTheWire** via une connexion SSH en tant que `bandit9`
- **Commandes utilisées** : 
```bash
ls -l /home/bandit8/
sort data.txt | uniq -u
exit
ssh -p 2220 bandit9@bandit.labs.overthewire.org
```

## `> methods`
- **Constat** : le mot de passe se trouve dans `data.txt`, sur la seule ligne non dupliquée
- **Action** : tri du fichier puis filtrage des lignes uniques (`sort | uniq -u`), le tri préalable étant requis car `uniq` ne détecte que les doublons adjacents
- **Résultat** : mot de passe isolé en une commande, connexion à `bandit9` validée

## `> results`

**Connexion réussie en tant que `bandit9`**.

![Connexion réussie](/bandit/10-level8to9/solution.png)

---

<p align="center">  
    <i>⬅️ <a href="/bandit/09-level7to8/rapport.md">Previous level</a></i> | <i><a href="/bandit/11-level9to10/rapport.md">Next level</a> ➡️</i>
</p>
<p align="center">  
    <i>↪️ Back to <a href="/bandit/sommaire.md">OverTheWire : Bandit</a></i>
</p>