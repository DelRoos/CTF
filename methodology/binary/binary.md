
## Catégorie : Binary Exploitation

### 1. Analyse statique

- **Objectif :** Comprendre la structure du binaire en analysant son code source ou machine.

- **Outils utilisés :**
  - `IDA Pro` ou `radare2` : Outils d'analyse statique pour examiner le code binaire.

#### Résultats

- Identification des fonctions clés, des appels système et des vulnérabilités potentielles.

### 2. Analyse dynamique

- **Objectif :** Observer le comportement du programme pendant son exécution.

- **Outils utilisés :**
  - `gdb` : Débogueur pour exécuter le binaire en mode débogage.

#### Résultats

- Observation des registres, de la pile et de la mémoire pendant l'exécution.

### 3. Fuzzing

- **Objectif :** Détecter des vulnérabilités en injectant des données aléatoires.

- **Outils utilisés :**
  - `AFL` : Outil de fuzzing pour injecter des entrées aléatoires.

#### Résultats

- Détection de vulnérabilités par des entrées aléatoires.

### 4. Exploitation

- **Objectif :** Exploiter les vulnérabilités pour contrôler le programme.

- **Outils utilisés :**
  - `ROPgadget` : Outil pour trouver des gadgets ROP utiles.
  - `pwntools` : Bibliothèque Python pour automatiser l'exploitation.

#### Résultats

- Utilisation des gadgets ROP pour contrôler le flux d'exécution.

---