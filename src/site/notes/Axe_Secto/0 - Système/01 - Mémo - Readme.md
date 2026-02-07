---
{"dg-publish":true,"permalink":"/axe-secto/0-systeme/01-memo-readme/","tags":["gardenEntry"]}
---

## 1. Pourquoi Obsidian ?

Cette forme sémantique de **"double crochet"** [[...\|...]] permet de construire automatiquement des liens entre les concepts et les éléments.

- **Liberté et puissance :** Obsidian est gratuit, local, ne demande rien à personne. Il permet de construire une forme de "Connected Papers" personnel.
    
- **Recherche vectorielle :** Grâce au maillage, la fonction de recherche est infiniment plus puissante que l'explorateur Windows.
    
- **Lisibilité hybride :** Le Markdown, tout comme le XML, est extrêmement lisible par les modèles de langage (LLM). Mais contrairement au XML, il est lisible pour l'humain et très facile à écrire.
    
## 2. Pourquoi cette structure ?

L'axe sectoriel implique une imbrication en cascade, une forme d'**entonnoir naturel** vers :

- "La bonne forme de discours".
    
- "Les bons mots".
    
- "La bonne structure d'expérimentation".
    
Chaque domaine dispose de ses propres particularités sémantiques (ses marqueurs textuels) et sémiotiques (son sens propre). C'est un **paradigme** dont les modèles ont besoin pour être performants. On sait par expérience que certains domaines fonctionnent mal avec l'IA générative "brute".

**Les deux utilités de cette bibliothèque :**

1. **Pour l'humain (Rédacteur) :** Faciliter l'accessibilité et la recherche du "bon insert" de contexte scientifique. C'est le juste assez pour orienter un modèle de langage dans un coin de son entraînement où il performera.
    
2. **Pour la machine (Agents) :** Préparer le terrain pour que des agents de rédaction puissent, après analyse, parcourir ce répertoire et récupérer les marqueurs sémantiques (tokens forts).

## 3. Comment est-ce qu'on priorise ?

#### 3.1 L'argument des domaines "visuels" 
TL:DR - En gros : 
1. les mathématiques, l'informatique et les "sciences de la vie" surperforment ;
2. là où physiques, "sciences de la terre", sciences sociales sous-performent

![[evaluation_robustness_with_csit.html]]

![[Visual_Dependency_Restructured.html]]
#### 3.2 L'argument du pain point "humain"
On fait un sondage double : 
1. Dans votre domaine, quelle est la typologie la plus récurrente de sujets que vous rencontrez ?
	1. Insérez un exemple : *lien réseau*
	2. Exemple de ce qu'on attend comme réponse : "En informatique, dans le sous-domaine du Machine Learning, c'est l'entrainement des modèles d'IA qui est le sujet le plus récurrent"
2. Dans votre domaine, sur quelle typologie de sujets vous avez le plus de difficultés ?
	1. Same
	2. Same
3. Dans votre domaine, sur quelle typologie de sujets, les modèles d'IA générative (Claude), ont le plus de difficultés et/ou vous donne le moins de résultats satisfaisant ?
	1. Same
	2. Same

#### 3.3 L'argument de la valeur
On fait une matrice, surexpo data visuel / pain point / argent facturé dans ces domaines 
## 4. Quelle structure d'arborescence ?

L'enjeu est d'éviter la redondance par un mécanisme d'**héritage de contexte**. Nous utilisons une structure en cascade du "plus large" au "plus précis".

### Les quatre niveaux de la nomenclature

Les blocs ci-dessous sont les **Gabarits (Templates)** à utiliser pour créer les pages.

---

### Niveau 1 : Primaire "A" (Le paradigme)

Définit la vérité et l'épistémologie du grand domaine.

````
---
type: domaine
niveau: A
tags: [épistémologie, fondation]
---
# A - [Nom du domaine]

## 1. Cadre épistémologique
> **Critère de vérité :** [Comment prouve-t-on quelque chose ici ? ex: démonstration formelle, étude clinique randomisée, sources primaires].
> **Objectif :** [Finalité du domaine].

## 2. Instructions racines pour l'IA
*Ce bloc définit la personnalité de base.*
```text
CONTEXTE_RACINE : tu agis dans le macro-domaine "[Nom du domaine]".
RÈGLE D'OR : la validité de tes propos repose sur [Critère de vérité].
TON : [ex: neutre, analytique, académique].
INTERDIT : toute affirmation relevant de l'opinion ou non démontrable selon les standards du domaine.
````

---
### Niveau 2 : Secondaire "A.X" (Le secteur)

Définit l'environnement, les entrées et les sorties.

````
---
type: secteur
niveau: AX
parent: "[[A - [Nom du domaine\|A - [Nom du domaine]]]"
tags: [secteur, environnement]
---
# A.X - [Nom du secteur]

## 1. Héritage cumulatif (1)
![[A - [Nom du domaine]#2. Instructions racines pour l'IA\|A - [Nom du domaine]#2. Instructions racines pour l'IA]]

## 2. Terminologie et objets
*   **Terme anglais (EN) :** [Nom du secteur en anglais].
*   **Objets d'entrée (Inputs) :** [Ce qu'on traite. ex: données brutes, minerai].
*   **Objets de sortie (Outputs) :** [Ce qu'on produit. ex: information structurée, alliage].

## 3. Instructions sectorielles
```text
CONTEXTE_SECTEUR : spécialisation en [Nom du secteur] ([Terme EN]).
FOCUS : concentre-toi sur l'interaction entre [Objets d'entrée] et [Objets de sortie].
LIMITES : ne traite pas des aspects hors de ce périmètre (ex: aspects légaux ou financiers, sauf si demandé).
````

---
### Niveau 3 : Tertiaire "A.X.X" (La Discipline)

Définit la méthode et le langage de spécialité (Verbes & Collocations).

````
---
type: discipline
niveau: AXX
parent: "[[A.X - [Nom du secteur]]]"
tags: [méthode, technique]
---
# A.X.X - [Nom de la discipline]

## 1. Héritage cumulatif (1 + 2)
*Contexte paradigme :*
![[A - [Nom du domaine]#2. Instructions racines pour l'IA\|A - [Nom du domaine]#2. Instructions racines pour l'IA]]
*Contexte secteur :*
![[A.X - [Nom du secteur]#3. Instructions sectorielles\|A.X - [Nom du secteur]#3. Instructions sectorielles]]

## 2. Langage de spécialité (LSP)
*Vocabulaire métier indispensable et bilingue.*

| Concept Français | Concept Anglais (EN) | Verbes associés (Collocations) |
| :--- | :--- | :--- |
| **[Concept clé 1]** | *[Terme EN]* | [ex: implémenter, déployer] |
| **[Concept clé 2]** | *[Terme EN]* | [ex: titrer, précipiter] |

## 3. Méthodologie
*   **Approche théorique :** [ex: approche bayésienne, matérialisme historique].
*   **Outils standards :** [ex: Python/Pandas, HPLC, Ansys].

## 4. Instructions disciplinaires
```text
CONTEXTE_DISCIPLINE : expert en [Nom de la discipline] ([Terme EN]).
STYLE : utilise le vocabulaire technique précis (voir table de concepts ci-dessus).
MÉTHODE : résous les problèmes via l'approche [Approche théorique].
````

---
### Niveau 4 : Quaternaire "A.X.X.X" (Le Concept / L'Atome)

La fiche finale. Contient les tokens forts et le prompt utilisateur.

````
---
uid: [Code MESRE]
titre: [Nom du concept]
parent: "[[A.X.X - [Nom de la discipline\|A.X.X - [Nom de la discipline]]]"
aliases: [[Terme anglais], [Acronyme], [Synonyme\|Terme anglais], [Acronyme], [Synonyme]]
tags: [concept, définition]
---

# [Code MESRE] - [Nom du concept]

## 1. Héritage cumulatif (1 + 2 + 3)
*Contexte paradigme :*
![[A - [Nom du domaine]#2. Instructions racines pour l'IA]]
*Contexte secteur :*
![[A.X - [Nom du secteur]#3. Instructions sectorielles]]
*Contexte discipline :*
![[A.X.X - [Nom de la discipline]#4. Instructions disciplinaires\|A.X.X - [Nom de la discipline]#4. Instructions disciplinaires]]

## 2. Définition et désambiguïsation
> **Définition :** [Définition courte et précise].
> **Terme anglais :** *[Terme EN]*
> **Ce que ce n'est pas :** [Distinction critique avec un concept voisin].

## 3. Marqueurs sémantiques (tokens forts)
*Liste des mots-clés techniques (français et anglais) que l'IA DOIT utiliser.*
*   **Mots-clés (FR/EN) :** [Mot A] (*Word A*), [Mot B] (*Word B*).
*   **Phraséologie type :** "On dit qu'on *[Verbe]* une *[Chose]*".
*   **Acronymes / Formules :** [Formule ou constante].

## 4. Prompt génératif (l'insert final)
*Copier ce bloc pour l'injecter dans le LLM.*

```text
RÔLE : expert pointu sur le sujet [Nom du concept] ([Terme EN]).
CONTEXTE HÉRITÉ : applique la méthodologie complète définie ci-dessus (1+2+3).
TÂCHE : traite la demande en utilisant obligatoirement les termes techniques : [Liste des marqueurs].
ATTENTION : ne confonds pas ce concept avec [Concept voisin].
````