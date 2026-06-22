# Forme linguistique & Confiance envers l'IA — PIR 2025-2026

Analyse statistique du Projet d'Initiation à la Recherche (PIR) examinant l'influence
de la forme linguistique des réponses générées par une IA sur la confiance perçue des
utilisateurs, indépendamment de la véracité du contenu.

**Auteure** : Yousra MEDJIDEL
**Encadrant** : Adrian CHIFU
**Filière** : Master MIAGE — Aix-Marseille Université

## Contexte de l'étude

Design expérimental 2×2 à mesures répétées (N = 52 participants) croisant deux
facteurs :

- **Forme linguistique** : soignée vs. dégradée
- **Exactitude du contenu** : vrai vs. faux

Quatre conditions expérimentales en résultent (A, B, C, D), chaque participant
évaluant les quatre réponses sur une échelle de confiance de Likert à 7 points
couvrant quatre dimensions (cognitive, affective, comportementale, forme perçue).

Deux hypothèses sont testées :

- **H1** : la forme linguistique influence significativement la confiance,
  indépendamment du contenu informationnel.
- **H2** : un utilisateur peut accorder une confiance élevée à une réponse
  bien formulée même lorsqu'elle est factuellement incorrecte.

## Contenu du dépôt

```
.
├── Analyse_PIR_Confiance_IA_clean.ipynb   # Notebook d'analyse complet
├── RéponsesPIR ConfianceIA.xlsx           # Données brutes (export Google Forms)
├── figures/
│   ├── distributions_shapiro.png
│   ├── figure1_interaction.png
│   ├── figure2_boxplots.png
│   ├── figure3_dimensions_barres.png
│   ├── figure4_gradient_dimensions.png
│   ├── figure5_meta_reflexifs.png
│   ├── figure6_classement.png
│   └── figure7_detection_conscience.png
└── README.md
```

## Structure du notebook

1. Chargement et préparation des données
2. Statistiques descriptives par dimension
3. Cohérence interne — alpha de Cronbach
4. Vérification des postulats (normalité, homogénéité)
5. ANOVA à mesures répétées 2×2 — test de H1
6. Tests post-hoc — Wilcoxon signé avec correction de Bonferroni
7. ANOVA par dimension de la confiance
8. Items méta-réflexifs, classement comparatif et détection des erreurs
9. Données complémentaires — fréquence d'utilisation de l'IA

## Utilisation

### Prérequis

```bash
pip install pandas numpy scipy pingouin matplotlib openpyxl
```

### Exécution

1. Cloner le dépôt et s'assurer que le fichier `RéponsesPIR ConfianceIA.xlsx`
   se trouve à la racine, au même niveau que le notebook.
2. Ouvrir `Analyse_PIR_Confiance_IA_clean.ipynb` dans Jupyter ou Google Colab.
3. Exécuter les cellules dans l'ordre — les figures sont générées et
   sauvegardées automatiquement dans le dossier courant.

## Résultats principaux

- Effet principal de la forme linguistique très significatif et de grande
  taille (F(1,51) = 39,96, p < ,001, η²p = ,439).
- Aucun effet significatif de l'exactitude du contenu (p = ,432).
- H2 directement confirmée par la comparaison B vs C : une réponse fausse
  mais bien écrite obtient une confiance significativement supérieure à une
  réponse vraie mais mal formulée (p < ,001).

Le détail complet de la méthodologie, des résultats et de la discussion est
disponible dans le mémoire PIR associé à ce dépôt.

## Licence

Projet académique réalisé dans le cadre d'un PIR à Aix-Marseille Université.
