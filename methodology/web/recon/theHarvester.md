
# Rapport d'Analyse theHarvester avec Paramètres Intéressants

## Informations Générales
- **Domaine Cible :** example.com
- **Date et Heure de l'Analyse :** [Date et heure de l'analyse]

## 1. Recherche d'Informations sur les Emails
### Commande :
```bash
theHarvester -d example.com -l 100 -b all
```
### Objectif :
La recherche d'informations sur les emails vise à recueillir des adresses email associées au domaine cible.

### Analyse :
La recherche d'informations a identifié des adresses email associées au domaine, ce qui peut être utile pour des attaques ciblées.

**Exemple de Réponse :**
```
[+] Emails trouvés pour le domaine example.com :
    - contact@example.com
    - support@example.com
    - admin@example.com
    - ...

```

## 2. Recherche d'Informations sur les Noms de Domaine
### Commande :
```bash
theHarvester -d example.com -l 100 -b all
```
### Objectif :
La recherche d'informations sur les noms de domaine vise à identifier d'autres domaines liés au domaine cible.

### Analyse :
L'outil a trouvé des domaines supplémentaires associés à example.com, ce qui peut être pertinent pour une évaluation plus approfondie de la surface d'attaque.

**Exemple de Réponse :**
```
[+] Noms de domaine trouvés pour le domaine example.com :
    - subdomain1.example.com
    - subdomain2.example.com
    - ...

```

## 3. Recherche d'Informations sur les Réseaux
### Commande :
```bash
theHarvester -d example.com -l 100 -b all
```
### Objectif :
La recherche d'informations sur les réseaux vise à identifier des informations liées aux serveurs et aux sous-réseaux du domaine cible.

### Analyse :
Des informations sur les serveurs et les sous-réseaux associés au domaine cible ont été récupérées, ce qui peut être utile pour comprendre l'infrastructure.

**Exemple de Réponse :**
```
[+] Informations sur les réseaux trouvées pour le domaine example.com :
    - 203.0.113.0/24
    - 198.51.100.0/24
    - ...

```

## 4. Limiter la Recherche aux Sources Publiques (`-b google` et `-b bing`)
### Commande :
```bash
theHarvester -d example.com -l 100 -b google
```
### Objectif :
La limitation de la recherche à des sources spécifiques, comme Google, permet d'obtenir des résultats plus ciblés.

### Analyse :
En limitant la recherche à Google, les résultats peuvent être plus pertinents en fonction des informations disponibles publiquement.

**Exemple de Réponse :**
```
[+] Emails trouvés pour le domaine example.com (via Google) :
    - contact@example.com
    - support@example.com
    - admin@example.com
    - ...

```

## Conclusion
L'analyse `theHarvester` avec les paramètres sélectionnés a fourni des informations sur les emails, les noms de domaine et les réseaux associés au domaine cible. Ces informations peuvent être utilisées pour la planification d'attaques ciblées, la compréhension de l'infrastructure et l'évaluation de la surface d'attaque.
