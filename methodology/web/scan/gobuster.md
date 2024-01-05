

# Rapport d'Analyse gobuster

## Informations Générales
- **Cible du Scan :** [URL du site web cible]
- **Date et Heure du Scan :** [Date et heure du scan]

## 1. Scan avec Liste de Mots (`common.txt`)
### Commande :
```bash
gobuster dir -u https://www.example.com/ -w /usr/share/wordlists/dirb/common.txt
```
### Objectif :
Le scan avec une liste de mots vise à découvrir des répertoires et fichiers cachés en utilisant une liste de mots couramment utilisés.

### Analyse :
Le scan a identifié des répertoires et fichiers potentiellement intéressants en utilisant une liste de mots courants.

**Exemple de Réponse :**
```
/admin/ (Status: 200)
/test/ (Status: 403)
/backup/ (Status: 404)
```

## 2. Scan Aggressif avec Extension Spécifique
### Commande :
```bash
gobuster dir -u https://www.example.com/ -w /usr/share/wordlists/dirb/common.txt -x .php,.html
```
### Objectif :
Le scan aggressif avec une extension spécifique vise à cibler uniquement les fichiers avec des extensions particulières.

### Analyse :
Le scan a été focalisé sur les fichiers avec les extensions spécifiées, fournissant des informations plus précises sur les fichiers potentiellement vulnérables.

**Exemple de Réponse :**
```
/index.php (Status: 200)
/login.php (Status: 200)
/about.html (Status: 200)
```

## 3. Utilisation d'un Proxy (`--proxy`)
### Commande :
```bash
gobuster dir -u https://www.example.com/ -w /usr/share/wordlists/dirb/common.txt --proxy http://monproxy:port
```
### Objectif :
L'utilisation d'un proxy permet de masquer l'origine du scan.

### Analyse :
Le scan a été effectué en utilisant le proxy spécifié, ce qui peut être utile pour maintenir l'anonymat.

**Exemple de Réponse :**
```
/admin/ (Status: 200)
/test/ (Status: 403)
/backup/ (Status: 404)
```

## Conclusion
L'analyse `gobuster` avec les paramètres sélectionnés a permis d'identifier des répertoires et fichiers cachés sur le site web cible. Ces informations peuvent être utilisées pour évaluer la sécurité du site, détecter des points d'entrée potentiels, ou encore pour une évaluation plus approfondie de la surface d'attaque.
