

## Catégorie : Reverse Engineering

### 1. Analyse statique

- **Objectif :** Comprendre la logique du binaire.

- **Outils utilisés :**
  - `IDA Pro` ou `Ghidra` : Outils d'analyse statique pour examiner le code assembleur.

#### Résultats

- Identification des fonctions importantes, des boucles et des structures de données.

### 2. Analyse dynamique

- **Objectif :** Observer le comportement du programme pendant son exécution.

- **Outils utilisés :**
  - `gdb` : Débogueur pour exécuter le binaire en mode débogage.

#### Résultats

- Placement de points d'arrêt pour observer les valeurs des registres et de la mémoire.

### 3. Désassemblage

- **Objectif :** Traduire le code machine en code assembleur.

- **Outils utilisés :**
  - `objdump` : Outil de désassemblage pour obtenir une représentation lisible du code assembleur.

#### Résultats

- Obtention d'une représentation lisible du code assembleur.

### 4. Patch et modification

- **Objectif :** Modifier le binaire pour comprendre le fonctionnement ou contourner des protections.

- **Outils utilisés :**
  - Éditeur hexadécimal comme `hexedit`.

#### Résultats

- Modification du binaire pour contourner des protections ou comprendre le fonctionnement.

### 5. Ré-ingénierie

- **Objectif :** Tenter de reconstituer le code source original.

- **Outils utilisés :**
  - `Radare2` ou `Hopper` : Outils de ré-ingénierie.

#### Résultats

- Tentative de reconstitution du code source original.
