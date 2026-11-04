# ⚙️ Conception et réalisation d'un système de transmission de puissance par engrenages

**Ingénierie mécanique | Dimensionnement | CAO | Fabrication additive**

## 1. Présentation du projet

Ce projet consiste à étudier et réaliser un système de transmission mécanique composé de deux engrenages cylindriques à denture droite, d'un support et d'une manivelle permettant l'entraînement manuel du mécanisme.

L'objectif est de mettre en application les principes de dimensionnement mécanique, de transmission de mouvement et de fabrication additive.

## 2. Caractéristiques des engrenages

| Paramètre | Engrenage 1 | Engrenage 2 |
|---|---:|---:|
| Nombre de dents | 60 | 30 |
| Module | 2 mm | 2 mm |
| Diamètre primitif | 120 mm | 60 mm |
| Diamètre extérieur | 124 mm | 64 mm |
| Diamètre de pied | 115 mm | 55 mm |
| Angle de pression supposé | 20° | 20° |

### Calcul de l'entraxe

a = (d₁ + d₂) / 2

a = (120 + 60) / 2

**Entraxe théorique = 90 mm**

### Rapport de transmission

i = Z₁ / Z₂ = 60 / 30 = 2

Lorsque l'engrenage Z60 entraîne Z30, la vitesse de rotation de sortie est multipliée par deux, avec inversion du sens de rotation.

## 3. Dimensionnement du support

Le support doit maintenir les deux axes parallèles, garantir un entraxe de 90 mm et permettre une rotation libre des engrenages.

### Dimensions préliminaires proposées

| Élément | Dimension |
|---|---|
| Longueur du support | 220 mm |
| Largeur du support | 100 mm |
| Épaisseur de la base | 10 mm |
| Entraxe des deux arbres | 90 mm |
| Diamètre nominal des axes | 8 mm |
| Hauteur des axes au-dessus de la base | 25 mm |
| Épaisseur minimale des paliers imprimés | 12 mm |

Les axes seront disposés parallèlement, avec un positionnement permettant l'engrènement des deux roues.

Le support devra comporter des logements adaptés aux axes ou aux roulements retenus.

## 4. Dimensionnement de la manivelle

La manivelle permet l'entraînement manuel de l'arbre moteur.

### Dimensions proposées

| Paramètre | Valeur |
|---|---|
| Longueur utile de la manivelle | 80 mm |
| Section du bras | 15 × 10 mm |
| Diamètre de fixation sur l'arbre | 8 mm nominal |
| Longueur de la poignée tournante | 45 mm |
| Diamètre de la poignée | 20 mm |

### Couple appliqué

Le couple d'entraînement est donné par :

C = F × L

Avec :

- F : effort tangentiel appliqué sur la poignée (N)
- L : longueur utile de la manivelle (m)

Pour un effort de 20 N et un bras de 0,08 m :

**C = 20 × 0,08 = 1,6 N·m**

Cette valeur représente un cas de calcul et non un couple admissible vérifié pour les composants imprimés.

## 5. Fabrication additive

| Paramètre | Configuration |
|---|---|
| Imprimante | ELEGOO Centauri Carbon |
| Procédé | FDM |
| Matériau | PLA |
| Hauteur de couche | 0,20 mm |
| Pièces concernées | Engrenages, support et manivelle |

Le choix des orientations d'impression, du remplissage et des épaisseurs devra tenir compte des sollicitations mécaniques et de la précision des assemblages.

## 6. Vérifications mécaniques

Les vérifications prévues concernent :

- Le respect de l'entraxe de 90 mm.
- L'alignement et le parallélisme des axes.
- Les jeux entre arbres et paliers.
- La qualité de l'engrènement.
- La liberté de rotation des deux roues.
- La tenue mécanique de la manivelle et de ses fixations.

## 7. Compétences valorisées

Ce projet mobilise des compétences en :

- Analyse fonctionnelle et conception mécanique.
- Dimensionnement géométrique des engrenages.
- Cinématique et transmission de puissance.
- Conception de supports et de liaisons pivot.
- Fabrication additive et préparation d'impression.
- Métrologie et vérification dimensionnelle.
- Résolution de problèmes techniques.
- Documentation et communication technique.

## 8. Objectif professionnel

Étudiant en ingénierie mécanique, orienté vers la mécatronique, je développe à travers ce projet mes compétences en conception, dimensionnement et réalisation de systèmes mécaniques.

Cette réalisation s'inscrit dans ma démarche de recherche de stage en ingénierie mécanique, afin de mettre en application mes connaissances sur des projets industriels concrets.

## Conclusion

Ce projet illustre l'application des connaissances en transmission de puissance, géométrie des engrenages et fabrication additive à un mécanisme réel.

Il constitue un support d'apprentissage pour approfondir les notions de dimensionnement, d'assemblage, de tolérances et de validation mécanique.
