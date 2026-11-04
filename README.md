
# ⚙️ Transmission de puissance par engrenages

<div align="center">

### Étude mécanique | Dimensionnement | CAO | Fabrication additive

**Projet technique en ingénierie mécanique — Prototypage**

<img src="I1.jpg" alt="Mécanisme de transmission par engrenages" width="650">

*Étude géométrique et réalisation d'un mécanisme de transmission de puissance par engrenages cylindriques à denture droite.*

</div>

---

## 📌 Présentation du projet

Ce projet porte sur l'étude et la réalisation d'un système de transmission de puissance par engrenages cylindriques à denture droite.

Le mécanisme comprend deux roues dentées, un support mécanique, des axes de rotation et une manivelle permettant son entraînement manuel.

L'objectif est d'appliquer les principes fondamentaux de la mécanique à un système concret, depuis l'analyse géométrique jusqu'à la fabrication additive.

Les principaux domaines abordés sont :

- Analyse fonctionnelle des mécanismes.
- Dimensionnement géométrique des engrenages.
- Cinématique et transmission de puissance.
- Exploitation de modèles numériques 2D et 3D.
- Fabrication additive FDM.
- Jeux fonctionnels et tolérances.
- Vérification et documentation technique.

---

## 🎯 1. Problématique technique

**Comment réaliser un mécanisme de transmission de puissance par engrenages en garantissant la compatibilité géométrique des composants, le positionnement correct des axes et un fonctionnement mécanique satisfaisant ?**

Cette problématique implique plusieurs contraintes :

- Respecter le module et les caractéristiques des dentures.
- Déterminer l'entraxe théorique des engrenages.
- Assurer le guidage des arbres en rotation.
- Concevoir un support suffisamment rigide.
- Permettre l'entraînement du système par une manivelle.
- Tenir compte des contraintes de fabrication additive.
- Prévoir les jeux nécessaires à l'assemblage.

---

## ⚙️ 2. Étude et dimensionnement des engrenages

### 2.1 Hypothèses de calcul

L'étude théorique considère deux engrenages cylindriques extérieurs à denture droite.

Les hypothèses retenues sont :

- Module : m = 2 mm.
- Nombre de dents : Z1 = 60 et Z2 = 30.
- Angle de pression : α = 20°.
- Profil standard à développante de cercle.
- Absence de déport de profil.
- Saillie de dent : ha = m.
- Creux de dent : hf = 1,25m.

Ces hypothèses définissent la géométrie nominale étudiée. Les dimensions réelles du STL devront être vérifiées séparément.

### 2.2 Tableau des caractéristiques géométriques

| Paramètre | Formule | Z60 | Z30 |
|---|---|---:|---:|
| Nombre de dents | Z | 60 | 30 |
| Module | m | 2 mm | 2 mm |
| Diamètre primitif | d = m × Z | 120 mm | 60 mm |
| Diamètre extérieur | da = m × (Z + 2) | 124 mm | 64 mm |
| Diamètre de pied | df = m × (Z - 2,5) | 115 mm | 55 mm |
| Diamètre de base | db = d × cos(20°) | 112,76 mm | 56,38 mm |
| Rayon primitif | r = d / 2 | 60 mm | 30 mm |

### 2.3 Calcul des diamètres primitifs

La relation fondamentale est :

**d = m × Z**

Pour l'engrenage Z60 :

d1 = 2 × 60

**d1 = 120 mm**

Pour l'engrenage Z30 :

d2 = 2 × 30

**d2 = 60 mm**

### 2.4 Calcul des diamètres extérieurs

Pour une denture standard sans déport de profil :

**da = m × (Z + 2)**

Engrenage Z60 :

da1 = 2 × (60 + 2)

**da1 = 124 mm**

Engrenage Z30 :

da2 = 2 × (30 + 2)

**da2 = 64 mm**

### 2.5 Calcul des diamètres de pied

Pour le profil standard retenu :

**df = m × (Z - 2,5)**

Engrenage Z60 :

df1 = 2 × (60 - 2,5)

**df1 = 115 mm**

Engrenage Z30 :

df2 = 2 × (30 - 2,5)

**df2 = 55 mm**

### 2.6 Calcul des diamètres de base

Le diamètre de base est défini par :

**db = d × cos(α)**

Avec α = 20°.

Engrenage Z60 :

db1 = 120 × cos(20°)

**db1 ≈ 112,76 mm**

Engrenage Z30 :

db2 = 60 × cos(20°)

**db2 ≈ 56,38 mm**

### 2.7 Calcul de l'entraxe

Pour deux engrenages extérieurs standards sans déport :

**a = (d1 + d2) / 2**

Application numérique :

a = (120 + 60) / 2

**a = 90 mm**

L'entraxe théorique constitue une donnée essentielle pour le positionnement des arbres.

### 2.8 Rapport de transmission

Pour deux engrenages extérieurs :

**ω2 / ω1 = -Z1 / Z2**

Si Z60 entraîne Z30 :

ω2 / ω1 = -60 / 30

**ω2 / ω1 = -2**

La roue Z30 tourne deux fois plus vite que la roue Z60, en sens opposé.

Si Z30 entraîne Z60 :

ω60 / ω30 = -30 / 60

**ω60 / ω30 = -0,5**

La roue Z60 tourne alors deux fois moins vite que la roue Z30.

En négligeant les pertes, la conservation de la puissance implique une variation inverse du couple et de la vitesse.

---

## 🛠️ 3. Étude du support mécanique

Le support mécanique assure le maintien des axes et le positionnement des engrenages.

### 3.1 Exigences fonctionnelles

Le support doit :

- Maintenir les axes de rotation.
- Garantir leur parallélisme.
- Respecter l'entraxe théorique.
- Assurer une rigidité suffisante.
- Limiter les déplacements indésirables.
- Permettre une rotation sans interférence avec la structure.

### 3.2 Dimensions préliminaires proposées

| Paramètre | Valeur proposée |
|---|---:|
| Longueur du support | 220 mm |
| Largeur du support | 100 mm |
| Épaisseur de la base | 10 mm |
| Entraxe nominal | 90 mm |
| Diamètre nominal des axes | 8 mm |
| Épaisseur des paliers | 12 mm |

**Remarque :** ces dimensions sont des propositions de pré-dimensionnement et ne constituent pas des cotes mesurées sur le modèle STL.

L'encombrement théorique des deux roues suivant la ligne des centres est :

L = 124 / 2 + 90 + 64 / 2

L = 62 + 90 + 32

**L = 184 mm**

Une base de 220 mm laisse donc une marge totale théorique de 36 mm dans cette direction, soit 18 mm de chaque côté si le mécanisme est centré.

Cette vérification ne tient pas compte de l'encombrement des paliers, des fixations et des autres éléments.

---

## 🔧 4. Étude de la manivelle

La manivelle permet d'appliquer un couple sur l'arbre moteur.

### 4.1 Dimensions proposées

| Paramètre | Valeur |
|---|---:|
| Longueur utile du bras | 80 mm |
| Section du bras | 15 × 10 mm |
| Diamètre nominal de fixation | 8 mm |
| Longueur de la poignée | 45 mm |
| Diamètre de la poignée | 20 mm |

Ces valeurs restent à adapter aux composants réels.

### 4.2 Calcul du couple

Le couple appliqué est :

**C = F × L**

Avec :

- C : couple en N·m.
- F : force tangentielle en N.
- L : bras de levier en m.

Pour un effort hypothétique de 20 N :

L = 80 mm = 0,08 m

C = 20 × 0,08

**C = 1,6 N·m**

Cette valeur constitue un exemple de sollicitation. Elle ne valide pas à elle seule la résistance mécanique de la manivelle.

---

## 📐 5. Documentation CAO et fichiers techniques

### 5.1 Modèle géométrique 3D

Le fichier STL contient la géométrie des composants destinés à la fabrication additive.

Le format STL représente les surfaces des pièces par un maillage triangulé.

**[📦 Télécharger le modèle 3D STL](Engrenagem+3++Junto.stl)**

### 5.2 Projection technique 2D

La projection 2D permet de visualiser les contours géométriques des composants.

<div align="center">

<img src="Transmission_engrenages_plan_2D.png" alt="Plan technique 2D" width="750">

*Projection géométrique 2D du mécanisme.*

</div>

**[📐 Télécharger le fichier DXF](Transmission_engrenages_projection_2D.dxf)**

Le fichier DXF permet une exploitation des contours dans un logiciel de CAO compatible.

Une projection issue d'un STL ne constitue pas automatiquement un plan de fabrication coté et tolérancé.

---

## 🖥️ 6. Préparation de la fabrication additive

### 6.1 Moyens techniques

| Caractéristique | Configuration |
|---|---|
| Imprimante | ELEGOO Centauri Carbon |
| Logiciel | ELEGOO Slicer |
| Procédé | FDM |
| Matériau | PLA |
| Diamètre de buse | 0,40 mm |
| Hauteur de couche de référence | 0,20 mm |

Les paramètres de fabrication doivent être confirmés à partir du profil de tranchage réellement utilisé.

### 6.2 Préparation des composants

La préparation de fabrication nécessite :

1. L'importation du modèle STL.
2. L'analyse de l'orientation des pièces.
3. La disposition des composants sur le plateau.
4. La configuration des paramètres d'impression.
5. Le tranchage du modèle.
6. La vérification des trajectoires et des supports éventuels.

### Capture 1 — Préparation du mécanisme

<div align="center">

<img src="E1.png" alt="Préparation du mécanisme dans ELEGOO Slicer" width="750">

</div>

### Capture 2 — Disposition des composants

<div align="center">

<img src="E2.png" alt="Disposition des composants mécaniques" width="750">

</div>

### Capture 3 — Implantation sur le plateau

<div align="center">

<img src="E3.png" alt="Implantation sur le plateau ELEGOO" width="750">

</div>

---

## 🏭 7. Réalisation physique du mécanisme

La fabrication additive permet de réaliser les composants à partir de leur géométrie numérique.

Cette étape met en évidence les contraintes suivantes :

- Précision dimensionnelle des pièces.
- Qualité de fabrication des dentures.
- État de surface.
- Résistance mécanique des composants.
- Qualité des alésages.
- Jeux nécessaires à l'assemblage.
- Orientation des couches d'impression.

### 7.1 Documentation photographique

#### Photographie 1 — Réalisation du projet

<div align="center">

<img src="I1.jpg" alt="Réalisation mécanique - photographie 1" width="650">

</div>

#### Photographie 2 — Documentation du projet

<div align="center">

<img src="I2.jpg" alt="Réalisation mécanique - photographie 2" width="650">

</div>

#### Photographie 3 — Documentation du projet

<div align="center">

<img src="I3.jpg" alt="Réalisation mécanique - photographie 3" width="650">

</div>

#### Photographie 4 — Documentation du projet

<div align="center">

<img src="I4.jpg" alt="Réalisation mécanique - photographie 4" width="650">

</div>

### 7.2 Vidéo du projet

La vidéo documente les étapes de réalisation du mécanisme.

**[🎥 Visionner la vidéo du projet](VID.mp4)**

---

## 🔄 8. Chaîne numérique de fabrication

Le projet illustre une démarche d'exploitation de données géométriques et de fabrication numérique.

### Chaîne principale

**Modèle STL → Préparation dans ELEGOO Slicer → Tranchage → Impression FDM → Assemblage → Vérifications fonctionnelles**

### Documentation complémentaire

**Modèle STL → Extraction de contours → Projection 2D → Fichier DXF**

Cette organisation distingue la préparation de fabrication de la documentation géométrique.

---

## 📏 9. Métrologie et vérification fonctionnelle

La qualité du mécanisme dépend notamment de la précision des dentures, du positionnement des axes et des jeux fonctionnels.

### Contrôles à réaliser

| Élément | Vérification |
|---|---|
| Engrenages | Diamètres et qualité des dentures |
| Support | Géométrie et rigidité |
| Axes | Alignement et parallélisme |
| Entraxe | Comparaison avec 90 mm théoriques |
| Alésages | Dimensions et jeux fonctionnels |
| Manivelle | Fixation et transmission du couple |
| Assemblage | Liberté de rotation |
| Mécanisme complet | Fonctionnement sans point dur |

Les résultats expérimentaux devront être renseignés après mesure ou essai.

---

## 📊 10. Analyse technique

### 10.1 Contraintes identifiées

La fabrication additive de pièces mécaniques fonctionnelles implique plusieurs limites :

- Précision des dimensions imprimées.
- Déformations possibles lors du refroidissement.
- Rugosité des surfaces en contact.
- Anisotropie mécanique des pièces FDM.
- Frottements au niveau des axes.
- Usure éventuelle des dentures.
- Résistance mécanique du PLA sous charge.

### 10.2 Pistes d'amélioration

Les améliorations envisageables comprennent :

- Ajustement des jeux fonctionnels.
- Optimisation de l'orientation d'impression.
- Intégration de roulements ou de bagues.
- Étude de matériaux plus adaptés aux sollicitations.
- Mesure des écarts dimensionnels.
- Essais sous différentes charges.
- Évaluation du rendement mécanique.
- Motorisation pour des essais expérimentaux.

---

## 🎓 11. Compétences techniques mobilisées et développées

| Domaine | Compétences |
|---|---|
| Ingénierie mécanique | Analyse fonctionnelle et étude de mécanismes |
| Dimensionnement | Calcul des caractéristiques géométriques |
| Cinématique | Étude des rapports de transmission |
| CAO | Exploitation de modèles STL et de fichiers DXF |
| Fabrication additive | Préparation et fabrication FDM |
| Métrologie | Prise en compte des jeux et tolérances |
| Analyse technique | Identification des contraintes et améliorations |
| Communication | Rédaction d'une documentation structurée |

---

## 💼 12. Valorisation professionnelle

Ce projet constitue une application concrète des connaissances en ingénierie mécanique, notamment en transmission de puissance, dimensionnement et fabrication additive.

Il illustre mon intérêt pour l'étude, la réalisation et l'amélioration des systèmes mécaniques.

**Étudiant en ingénierie mécanique, avec une orientation vers la mécatronique, je suis actuellement à la recherche d'un stage afin de mettre mes connaissances en application dans un environnement industriel.**

Mes domaines d'intérêt comprennent :

- La conception et le dimensionnement mécanique.
- La CAO et la documentation technique.
- La fabrication et l'industrialisation.
- L'analyse et l'amélioration des systèmes mécaniques.
- La mécatronique et les systèmes automatisés.

---

## 📁 13. Fichiers du projet

Tous les fichiers sont disponibles à la racine de ce dépôt.

| Fichier | Description |
|---|---|
| [Engrenagem+3++Junto.stl](Engrenagem+3++Junto.stl) | Modèle géométrique 3D |
| [Transmission_engrenages_plan_2D.png](Transmission_engrenages_plan_2D.png) | Projection technique 2D |
| [Transmission_engrenages_projection_2D.dxf](Transmission_engrenages_projection_2D.dxf) | Fichier de projection DXF |
| [E1.png](E1.png) | Capture ELEGOO Slicer 1 |
| [E2.png](E2.png) | Capture ELEGOO Slicer 2 |
| [E3.png](E3.png) | Capture ELEGOO Slicer 3 |
| [I1.jpg](I1.jpg) | Photographie 1 |
| [I2.jpg](I2.jpg) | Photographie 2 |
| [I3.jpg](I3.jpg) | Photographie 3 |
| [I4.jpg](I4.jpg) | Photographie 4 |
| [VID.mp4](VID.mp4) | Vidéo du projet |

---

## 🏁 14. Conclusion

Ce projet permet de relier les principes fondamentaux de la transmission de puissance par engrenages à leur application dans un mécanisme fabriqué par impression 3D.

L'étude met en évidence l'importance :

- Du dimensionnement géométrique.
- Du respect des entraxes.
- De la précision de fabrication.
- Des jeux fonctionnels.
- De la vérification des assemblages.

Il constitue une expérience technique valorisable dans le cadre de mon parcours en ingénierie mécanique et de ma recherche de stage.

---

<div align="center">

**Ingénierie mécanique • Transmission de puissance • CAO • Fabrication additive • Mécatronique**

</div>
