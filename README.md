
# ⚙️ Transmission de puissance par engrenages

### Étude mécanique • Dimensionnement • Fabrication additive • Analyse cinématique

**Projet technique en ingénierie mécanique — Orientation mécatronique**

---

## 1. Présentation du projet

Ce projet porte sur l'étude et la réalisation d'un mécanisme de transmission de puissance par engrenages cylindriques à denture droite.

Le système comprend deux roues dentées de **60 et 30 dents**, un support mécanique, des axes de rotation, des éléments de fixation et une manivelle permettant l'entraînement manuel.

L'objectif est de mettre en application les connaissances acquises en ingénierie mécanique, notamment dans les domaines suivants :

- Transmission de puissance et cinématique.
- Dimensionnement des engrenages.
- Analyse fonctionnelle des mécanismes.
- Fabrication additive FDM.
- Assemblage et jeux fonctionnels.
- Exploitation de fichiers techniques STL et DXF.

Ce projet constitue également un support de développement de compétences dans le cadre de ma recherche de stage en ingénierie mécanique et mécatronique.

---

## 2. Problématique technique

**Comment réaliser un mécanisme de transmission de puissance par engrenages tout en assurant la compatibilité géométrique des composants, la qualité de l'engrènement et un assemblage fonctionnel ?**

Cette problématique implique de prendre en compte :

- Les caractéristiques géométriques des engrenages.
- Le rapport de transmission.
- Le positionnement des axes.
- Les contraintes de fabrication additive.
- Les tolérances et les jeux d'assemblage.

---

## 3. Caractéristiques techniques des engrenages

### 3.1 Paramètres géométriques

Les caractéristiques nominales retenues pour l'étude sont les suivantes :

| Paramètre | Engrenage 1 | Engrenage 2 |
|---|---:|---:|
| Nombre de dents Z | 60 | 30 |
| Module m | 2 mm | 2 mm |
| Diamètre primitif d | 120 mm | 60 mm |
| Diamètre extérieur da | 124 mm | 64 mm |
| Diamètre de pied df | 115 mm | 55 mm |
| Rayon primitif | 60 mm | 30 mm |
| Angle de pression supposé | 20° | 20° |

Les diamètres sont calculés pour des dentures droites standards sans déport de profil.

### 3.2 Calcul du diamètre primitif

La relation fondamentale est :

**d = m × Z**

Pour l'engrenage Z60 :

d1 = 2 × 60 = **120 mm**

Pour l'engrenage Z30 :

d2 = 2 × 30 = **60 mm**

### 3.3 Calcul des diamètres extérieurs

**da = m × (Z + 2)**

Engrenage Z60 :

da1 = 2 × (60 + 2) = **124 mm**

Engrenage Z30 :

da2 = 2 × (30 + 2) = **64 mm**

### 3.4 Calcul de l'entraxe

L'entraxe théorique entre les deux axes de rotation est :

**a = (d1 + d2) / 2**

a = (120 + 60) / 2

**a = 90 mm**

Cette valeur constitue une donnée essentielle pour le positionnement des paliers et la conception du support mécanique.

### 3.5 Rapport de transmission

Pour deux engrenages extérieurs :

**ω2 / ω1 = -Z1 / Z2**

Si la roue Z60 est motrice et entraîne la roue Z30 :

ω2 / ω1 = -60 / 30 = **-2**

La roue de sortie tourne donc deux fois plus vite que la roue motrice, dans le sens opposé.

Dans le cas inverse, lorsque Z30 entraîne Z60, la vitesse est divisée par deux et le couple idéal est multiplié par deux.

---

## 4. Conception et dimensionnement du support

Le support assure le maintien des axes de rotation et le positionnement relatif des engrenages.

### Dimensions préliminaires de conception

| Paramètre | Valeur proposée |
|---|---:|
| Longueur du support | 220 mm |
| Largeur du support | 100 mm |
| Épaisseur de la base | 10 mm |
| Entraxe théorique | 90 mm |
| Diamètre nominal des axes | 8 mm |
| Hauteur des axes | 25 mm |
| Épaisseur minimale des paliers | 12 mm |

Ces dimensions sont des hypothèses de conception et doivent être vérifiées par rapport à la géométrie réelle des pièces et à leur assemblage.

### Fonctions mécaniques du support

- Assurer le maintien des axes.
- Garantir leur parallélisme.
- Respecter l'entraxe théorique.
- Limiter les déformations.
- Permettre une rotation libre des roues dentées.

---

## 5. Conception de la manivelle

La manivelle permet d'appliquer manuellement un couple sur l'arbre moteur.

### Dimensions proposées

| Paramètre | Valeur |
|---|---:|
| Longueur utile du bras | 80 mm |
| Section du bras | 15 × 10 mm |
| Diamètre nominal de fixation | 8 mm |
| Longueur de la poignée | 45 mm |
| Diamètre de la poignée | 20 mm |

### Calcul du couple d'entraînement

**C = F × L**

Avec :

- C : couple appliqué en N·m.
- F : effort tangentiel en N.
- L : longueur utile du bras en m.

Pour un effort hypothétique de 20 N :

C = 20 × 0,08

**C = 1,6 N·m**

Ce calcul représente un cas de sollicitation théorique et ne constitue pas une validation de résistance de la manivelle imprimée.

---

## 6. Modèle 3D et documentation CAO

### 6.1 Modèle géométrique 3D

Le modèle STL permet de visualiser les composants du mécanisme et de préparer leur fabrication additive.

📁 **[Consulter le modèle STL](modeles-3D/engrenages.stl)**

Le format STL décrit les surfaces à l'aide d'un maillage triangulé.

### 6.2 Projection technique 2D

Une représentation 2D a été extraite du modèle géométrique afin de faciliter l'analyse des contours et la documentation technique.

![Projection technique 2D](images/plan_2D.png)

📐 **[Télécharger le fichier DXF](plans/transmission_2D.dxf)**

Le DXF permet de réutiliser les contours 2D dans un logiciel de CAO compatible.

**Remarque :** la projection DXF issue d'un STL ne constitue pas une reconstruction paramétrique complète ni un plan de fabrication coté et tolérancé.

---

## 7. Préparation de la fabrication additive

### 7.1 Moyens de fabrication

| Caractéristique | Configuration |
|---|---|
| Imprimante | ELEGOO Centauri Carbon |
| Technologie | FDM |
| Matériau | PLA |
| Hauteur de couche | 0,20 mm |
| Diamètre de buse | 0,40 mm |
| Logiciel | ELEGOO Slicer |

### 7.2 Implantation des composants

Les différents composants du mécanisme sont disposés sur le plateau virtuel avant la génération des trajectoires d'impression.

L'implantation doit prendre en compte :

- Les dimensions des composants.
- Leur orientation.
- L'adhérence au plateau.
- La nécessité éventuelle de supports.
- La qualité dimensionnelle recherchée.

### Vue générale de la préparation

![Préparation des composants dans ELEGOO Slicer](images/slicer_vue_1.png)

### Vue détaillée des engrenages et de la manivelle

![Engrenages et manivelle](images/slicer_vue_2.png)

### Implantation sur le plateau d'impression

![Implantation des composants](images/slicer_vue_3.png)

---

## 8. Fabrication et réalisation physique

Le mécanisme est réalisé par fabrication additive selon le procédé FDM.

Cette étape permet d'étudier les contraintes associées à la production de pièces mécaniques comportant des géométries fonctionnelles.

Une attention particulière est portée :

- À la précision des dentures.
- À la qualité des alésages.
- Aux jeux d'assemblage.
- À l'état de surface.
- À l'orientation d'impression.
- À la résistance mécanique des composants.

### Vidéo de fabrication

🎥 **[Consulter la vidéo d'impression 3D](videos/impression.mp4)**

---

## 9. Assemblage et vérification fonctionnelle

Les vérifications prévues pour le mécanisme concernent :

1. Le positionnement des axes de rotation.
2. La conformité de l'entraxe.
3. L'alignement des engrenages.
4. La liberté de rotation.
5. La qualité de l'engrènement.
6. Le fonctionnement de la manivelle.
7. L'identification des frottements et des jeux.

Les résultats des essais seront ajoutés après validation du mécanisme assemblé.

---

## 10. Compétences techniques mobilisées

| Domaine | Compétences |
|---|---|
| Conception mécanique | Analyse fonctionnelle et compréhension des mécanismes |
| Dimensionnement | Calculs géométriques et entraxes |
| Transmission de puissance | Rapports de transmission et cinématique |
| CAO | Exploitation et analyse de géométries 2D/3D |
| Fabrication additive | Préparation des pièces et impression FDM |
| Métrologie | Étude des jeux et tolérances dimensionnelles |
| Résolution de problèmes | Analyse des contraintes et recherche d'améliorations |
| Documentation technique | Structuration des calculs, modèles et résultats |

---

## 11. Analyse critique et perspectives

Les principales limites à examiner concernent :

- Les écarts dimensionnels entre le modèle et les pièces imprimées.
- Les défauts éventuels d'engrènement.
- Les frottements entre pièces mobiles.
- Les performances mécaniques du PLA.
- La tenue des axes et des paliers.
- L'influence des paramètres d'impression sur la précision.

Les améliorations envisageables comprennent l'optimisation des tolérances, l'intégration de roulements et la réalisation d'essais sous charge.

---

## 12. Valorisation professionnelle

Ce projet constitue une application pratique de plusieurs enseignements fondamentaux en ingénierie mécanique.

Il illustre mon intérêt pour l'étude des mécanismes, la transmission de puissance, la fabrication additive et l'analyse des systèmes techniques.

**Actuellement étudiant en ingénierie mécanique avec une orientation vers la mécatronique, je suis à la recherche d'un stage permettant de mettre mes connaissances en application dans un environnement industriel.**

Je souhaite notamment contribuer à des projets liés à la conception mécanique, au dimensionnement, à la fabrication et à l'amélioration de systèmes mécaniques.

---

## 13. Conclusion

L'étude de ce système de transmission par engrenages permet de relier les principes théoriques de cinématique et de dimensionnement aux contraintes pratiques de fabrication et d'assemblage.

Le projet met en évidence l'importance de la cohérence géométrique, de la précision dimensionnelle et de la démarche de validation dans la réalisation d'un mécanisme fonctionnel.

**Mots-clés :** Ingénierie mécanique, engrenages, transmission de puissance, CAO, DXF, STL, fabrication additive, FDM, mécatronique.
