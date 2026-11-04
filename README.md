
# ⚙️ Transmission de puissance par engrenages

### Étude mécanique | Dimensionnement | CAO | Fabrication additive | Analyse cinématique

**Projet technique en ingénierie mécanique — Orientation mécatronique**

---

## 1. Présentation du projet

Ce projet porte sur l'étude et la réalisation d'un système de transmission de puissance par engrenages cylindriques à denture droite, composé de deux roues dentées, d'un support mécanique, d'axes de rotation et d'une manivelle.

L'objectif est de mettre en application les connaissances acquises en ingénierie mécanique et de développer une démarche technique allant de l'analyse géométrique à la fabrication additive.

Ce projet mobilise plusieurs compétences :

- Analyse fonctionnelle des systèmes mécaniques.
- Dimensionnement des engrenages.
- Étude cinématique et transmission de puissance.
- Exploitation de fichiers CAO 2D et 3D.
- Préparation et réalisation de pièces par impression 3D.
- Étude des jeux et tolérances d'assemblage.
- Documentation et communication technique.

---

## 2. Problématique technique

**Comment réaliser un mécanisme de transmission de puissance par engrenages tout en garantissant la compatibilité géométrique des composants, le respect des entraxes et la qualité de l'engrènement ?**

Cette problématique nécessite une étude des caractéristiques géométriques, des conditions d'assemblage et des contraintes de fabrication additive.

---

## 3. Étude et dimensionnement des engrenages

### 3.1 Caractéristiques géométriques

Le mécanisme étudié comprend deux engrenages cylindriques à denture droite.

| Paramètre | Engrenage 1 | Engrenage 2 |
|---|---:|---:|
| Nombre de dents Z | 60 | 30 |
| Module m | 2 mm | 2 mm |
| Diamètre primitif d | 120 mm | 60 mm |
| Diamètre extérieur da | 124 mm | 64 mm |
| Diamètre de pied df | 115 mm | 55 mm |
| Rayon primitif | 60 mm | 30 mm |
| Angle de pression supposé | 20° | 20° |

*Les dimensions calculées correspondent à une denture standard sans déport de profil.*

### 3.2 Calcul des diamètres primitifs

La relation fondamentale est :

**d = m × Z**

Pour l'engrenage Z60 :

d1 = 2 × 60 = **120 mm**

Pour l'engrenage Z30 :

d2 = 2 × 30 = **60 mm**

### 3.3 Calcul des diamètres extérieurs

**da = m × (Z + 2)**

Pour Z60 :

da1 = 2 × (60 + 2) = **124 mm**

Pour Z30 :

da2 = 2 × (30 + 2) = **64 mm**

### 3.4 Calcul de l'entraxe

L'entraxe théorique est :

**a = (d1 + d2) / 2**

a = (120 + 60) / 2

**a = 90 mm**

Cette valeur est fondamentale pour le positionnement des axes et le dimensionnement du support.

### 3.5 Rapport de transmission

Pour deux engrenages extérieurs :

**ω2 / ω1 = -Z1 / Z2**

Si Z60 entraîne Z30 :

ω2 / ω1 = -60 / 30 = **-2**

La roue de sortie tourne donc deux fois plus vite que la roue motrice, dans le sens opposé.

Dans le cas inverse, Z30 entraînant Z60, la vitesse est divisée par deux et le couple idéal est multiplié par deux.

---

## 4. Conception et dimensionnement du support

Le support mécanique assure le maintien des axes de rotation et le positionnement des deux roues dentées.

### Dimensions préliminaires proposées

| Paramètre | Dimension |
|---|---:|
| Longueur du support | 220 mm |
| Largeur du support | 100 mm |
| Épaisseur de la base | 10 mm |
| Entraxe des axes | 90 mm |
| Diamètre nominal des axes | 8 mm |
| Hauteur des axes | 25 mm |
| Épaisseur minimale des paliers | 12 mm |

Ces dimensions constituent une proposition de conception à vérifier selon la géométrie réelle des composants.

### Fonctions du support

- Maintenir les axes de rotation.
- Assurer le parallélisme des arbres.
- Respecter l'entraxe théorique.
- Limiter les déplacements indésirables.
- Permettre une rotation libre des engrenages.

---

## 5. Conception de la manivelle

La manivelle permet l'entraînement manuel du mécanisme en appliquant un couple sur l'arbre moteur.

### Caractéristiques proposées

| Paramètre | Valeur |
|---|---:|
| Longueur utile du bras | 80 mm |
| Section du bras | 15 × 10 mm |
| Diamètre nominal de fixation | 8 mm |
| Longueur de la poignée | 45 mm |
| Diamètre de la poignée | 20 mm |

### Calcul du couple

**C = F × L**

Avec :

- C : couple en N·m.
- F : effort tangentiel en N.
- L : longueur utile du bras en m.

Pour un effort hypothétique de 20 N :

C = 20 × 0,08

**C = 1,6 N·m**

Ce résultat représente un cas de calcul théorique et non une validation de résistance mécanique.

---

## 6. Documentation CAO et fichiers techniques

### 6.1 Modèle géométrique 3D

Le modèle STL représente les composants du mécanisme et permet leur préparation pour la fabrication additive.

**[📦 Consulter le fichier STL](modeles-3D/Engrenagem+3++Junto.stl)**

Le format STL décrit les surfaces des composants à l'aide d'un maillage triangulé.

### 6.2 Projection technique 2D

Une projection 2D a été réalisée à partir de la géométrie 3D afin de documenter les contours du mécanisme.

![Plan technique 2D](images/Transmission_engrenages_plan_2D.png)

**[📐 Télécharger le fichier DXF](plans/Transmission_engrenages_projection_2D.dxf)**

Cette projection permet d'exploiter les contours dans un environnement de CAO compatible avec le format DXF.

La conversion STL vers DXF ne reconstitue pas automatiquement les esquisses paramétriques d'origine.

---

## 7. Préparation de la fabrication additive

### 7.1 Moyens techniques

| Caractéristique | Configuration |
|---|---|
| Imprimante | ELEGOO Centauri Carbon |
| Logiciel | ELEGOO Slicer |
| Procédé | FDM |
| Matériau | PLA |
| Diamètre de buse | 0,40 mm |
| Hauteur de couche | 0,20 mm |

### 7.2 Implantation des composants

Les composants du mécanisme sont positionnés sur le plateau virtuel afin de préparer les trajectoires de fabrication.

Cette étape nécessite de prendre en compte :

- L'orientation des pièces.
- Leur encombrement.
- L'adhérence au plateau.
- Les surfaces nécessitant des supports.
- La qualité dimensionnelle recherchée.

### Capture 1 — Préparation du mécanisme

![Préparation du mécanisme](images/E1.png)

### Capture 2 — Disposition des composants

![Disposition des engrenages](images/E2.png)

### Capture 3 — Implantation sur le plateau

![Plateau ELEGOO Slicer](images/E3.png)

---

## 8. Fabrication et réalisation physique

La fabrication des composants est réalisée par impression 3D FDM sur une ELEGOO Centauri Carbon.

Cette phase permet d'étudier les contraintes associées à la réalisation de pièces mécaniques fonctionnelles.

Les points techniques à considérer sont :

- La précision des dentures.
- La qualité des alésages.
- Les tolérances dimensionnelles.
- Les jeux d'assemblage.
- La résistance des pièces imprimées.
- L'influence des paramètres de fabrication.

### 8.1 Documentation photographique

Les photographies suivantes présentent les différentes étapes et les résultats de la réalisation physique.

#### Photographie 1

![Photographie du projet 1](images/I1.jpg)

#### Photographie 2

![Photographie du projet 2](images/I2.jpg)

#### Photographie 3

![Photographie du projet 3](images/I3.jpg)

#### Photographie 4

![Photographie du projet 4](images/I4.jpg)

### 8.2 Vidéo du projet

La vidéo permet de documenter la fabrication du mécanisme et de présenter les composants réalisés.

**[🎥 Voir la vidéo du projet](videos/VID.mp4)**

---

## 9. Chaîne numérique de fabrication

Le projet illustre une démarche d'exploitation de données géométriques et de fabrication numérique.

**Modèle 3D STL → Analyse géométrique et projection DXF → Préparation dans ELEGOO Slicer → Impression FDM → Assemblage et vérification fonctionnelle**

Les différentes étapes permettent de relier la représentation numérique du mécanisme à sa réalisation physique.

---

## 10. Assemblage et vérifications fonctionnelles

Les vérifications techniques prévues portent sur :

1. Le positionnement des axes de rotation.
2. Le respect de l'entraxe de 90 mm.
3. Le parallélisme des arbres.
4. La liberté de rotation des roues.
5. La qualité de l'engrènement.
6. Le fonctionnement de la manivelle.
7. Les jeux et frottements entre composants.

Les résultats expérimentaux seront documentés après les vérifications correspondantes.

---

## 11. Compétences techniques mobilisées et développées

| Domaine | Compétences |
|---|---|
| Conception mécanique | Analyse fonctionnelle et étude des mécanismes |
| Dimensionnement | Calculs géométriques et détermination des entraxes |
| Transmission de puissance | Cinématique et rapports de transmission |
| CAO | Exploitation de modèles STL et de projections DXF |
| Fabrication additive | Préparation des impressions et fabrication FDM |
| Métrologie | Analyse des jeux et des tolérances |
| Résolution de problèmes | Identification des contraintes et recherche de solutions |
| Documentation technique | Présentation structurée d'un projet mécanique |

---

## 12. Analyse critique et perspectives

Les principales limites techniques à étudier concernent :

- Les écarts dimensionnels liés à l'impression.
- La précision des dentures.
- Les frottements entre pièces mobiles.
- Les jeux au niveau des axes.
- Les performances mécaniques du PLA.
- La tenue des paliers et de la manivelle.

### Améliorations envisageables

- Optimisation des jeux fonctionnels.
- Vérification dimensionnelle des engrenages.
- Intégration éventuelle de roulements.
- Étude de matériaux plus adaptés aux sollicitations.
- Essais de transmission sous charge.
- Motorisation du mécanisme pour une étude expérimentale.

---

## 13. Valorisation professionnelle

Ce projet constitue une application pratique de plusieurs enseignements fondamentaux en ingénierie mécanique.

Il illustre mon intérêt pour l'étude des mécanismes, le dimensionnement, la transmission de puissance et la fabrication additive.

**Étudiant en ingénierie mécanique, avec une orientation vers la mécatronique, je suis actuellement à la recherche d'un stage afin de mettre mes connaissances en application dans un environnement industriel.**

Je souhaite notamment contribuer à des projets liés à :

- La conception et au dimensionnement mécanique.
- La CAO et à la documentation technique.
- La fabrication et à l'industrialisation.
- L'analyse et à l'amélioration des systèmes mécaniques.
- La mécatronique et aux systèmes automatisés.

---

## 14. Conclusion

Ce projet permet de relier les connaissances théoriques en transmission de puissance et en dimensionnement mécanique à la réalisation physique d'un mécanisme par fabrication additive.

Il met en évidence l'importance de la cohérence géométrique, des tolérances dimensionnelles et de la validation fonctionnelle dans le développement d'un système mécanique.

Il constitue également une expérience technique valorisable dans le cadre de mon parcours en ingénierie mécanique et de ma recherche de stage.

---

**Mots-clés :** Ingénierie mécanique • Engrenages • Transmission de puissance • CAO • DXF • STL • Fabrication additive • FDM • Métrologie • Mécatronique
