#  Advanced Demand Forecasting & Supply Chain Optimization

##   Description

Projet Python de bout en bout pour la **Prévision de la Demande** (Demand Forecasting), appliquant des techniques de **Data Science** avancées à un jeu de données complexe de **Chaîne d'Approvisionnement**. Le projet inclut une segmentation complète **ABC/XYZ**, une analyse de la **Volatilité de la Demande (CV)** et une modélisation par régression causale.

L'accent est mis sur la **quantification des risques** clés : les Écarts de Stock de Sécurité (Safety Stock Gaps), la Volatilité des Délais d'Approvisionnement (Lead Time Volatility) et le **Coût Élevé de la Non-Qualité (COQ)**, démontrant ainsi la maîtrise d'un spectre complet de processus et de compétences analytiques **S&OP (Sales & Operations Planning)**.

---

## 1. Objectif du Projet & Mandat S&OP

L'objectif principal de ce projet était d'établir une **base de décision S&OP** fondée sur les données en quantifiant deux domaines de risque critiques : l'**Incertitude de la Prévision** et la **Fiabilité de la Chaîne d'Approvisionnement**. Cette analyse transforme les données brutes en mandats spécifiques, **quantifiés financièrement**, destinés à la revue exécutive.

| KPI | Impact Commercial Cible |
| :--- | :--- |
| **Safety Stock Gap** | Quantifier le déficit de stock nécessaire pour atteindre l'objectif de **Niveau de Service de 95%**. |
| **Cost of Non-Quality (COQ)** | Isoler et chiffrer l'impact financier des problèmes de qualité et des échecs d'inspection. |
| **Working Capital** | Identifier les stocks à risque (**Slow-Moving/Obsolete**) pour améliorer les flux de trésorerie (cash flow). |
| **Forecast Baseline** | Établir une base de modèle statistique robuste pour minimiser le **Biais de Prévision (Forecast Bias)**. |

---

## 2. Méthodologie & Analyse Principale

### 2.1. Préparation Intégrée des Données (Logique SQL & Power Query M)

L'analyse a commencé par la simulation de la phase **ETL (Extract, Transform, Load)** requise pour agréger les données **ERP** :

* **Nettoyage des Données** : Standardisation des taux de défauts et clarification des composants du **Délai d'Approvisionnement (Lead Time) de bout en bout** (Traitement Interne vs. Fournisseur).
* **Ingénierie des Caractéristiques (Feature Engineering)** : Création du Chiffre d'Affaires Net (Net Revenue), des Coûts Totaux d'Approvisionnement (Total Supply Costs) et de la Valeur des Stocks (Inventory Value) pour tous les KPI financiers subséquents.

### 2.2. Segmentation Fondamentale (ABC/XYZ)

La **Matrice ABC/XYZ** a été établie pour prioriser les ressources, s'attaquant directement au cœur du rôle du Planificateur de Demande : allouer l'**Effort à Valeur Ajoutée de la Prévision (FVA)** là où il compte le plus.

| Technique | Output KPI | Constat |
| :--- | :--- | :--- |
| **Classification ABC** | % de Chiffre d'Affaires Cumulé | **39%** des SKUs sont de **Classe A**, générant **$\mathbf{79.81\%}$** du Chiffre d'Affaires Total. $\rightarrow$ Focus élevé requis. |
| **Classification XYZ** | Volatilité de la Demande (CV) | La catégorie *Haircare* est **$\mathbf{100\%}$ Volatile (Classe Z)**, exigeant une modélisation par Séries Temporelles avancée. |

### 2.3. Analyse des Risques et Modélisation Causale

| Technique | Output KPI | Constat |
| :--- | :--- | :--- |
| **Fiabilité Fournisseur** | Lead Time CV | Le Fournisseur 1 présente la Volatilité des Délais d'Approvisionnement la plus élevée (**$\mathbf{57.86\%}$**), augmentant directement les exigences de Stock de Sécurité. |
| **Analyse des Coûts** | Décomposition du Coût de Service (Cost to Serve) | **$\mathbf{90\%}$** du Coût de Service est généré par la Logistique (Transport), et non par la Fabrication. |
| **Modélisation Causale** | Régression R² | Le Prix n'est pas un moteur principal de la demande ($\mathbf{R^2} \approx \mathbf{0.001}$), nécessitant de se concentrer sur la **Modélisation Événementielle** (Promotions/Démographie) pour éviter le Biais de Prévision. |

---

## 3. Impact Commercial Quantifié & Alertes S&OP

L'analyse a transformé la volatilité des données en mandats financiers et opérationnels spécifiques :

| Catégorie de Risque | KPI Quantifié | Métrique \/ Valeur | Implication S&OP |
| :--- | :--- | :--- | :--- |
| **Risque Qualité** | Cost of Non-Quality (COQ) | **$996,950.00** | Perte directe de Working Capital due à un inventaire inutilisable. Doit être stoppé immédiatement. |
| **Défaillance Fournisseur** | Taux d'Échec d'Inspection | **66.67%** (Fournisseur 4) | Mandate l'implémentation d'un **Facteur de Sécurité $\mathbf{3\times}$** sur les quantités commandées pour sécuriser le Niveau de Service. |
| **Déficit de Stock** | Safety Stock Gap (Skincare) | **$\mathbf{8,764}$ Unités Manquantes** (pour atteindre 15 jours de DOS). | Sous-couverture critique dans un segment volatile/à forte demande. Risque élevé de rupture de stock (Stock Out). |
| **Efficacité du Processus** | Taux d'Absorption de la Production | **$\mathbf{\approx 30\%}$** | Indique un sur-forecast systématique ou une surcapacité, drainant le Working Capital. |
| **Risque Inventaire** | Valeur Obsolète | **$12,941.00** | Inventaire qui doit être liquidé pour libérer du Working Capital. |

---

## 4. Intégration Technique & Prochaines Étapes (Feuille de Route IA/ML)

### 4.1. Compétences Analytiques Démontrées

Ce projet démontre des compétences analytiques intégrées :

* **Analyse Python** : Utilisée pour la segmentation avancée (ABC/XYZ), la notation des risques (Lead Time CV, Taux d'Échec d'Inspection) et la modélisation corrélationnelle (**RLM**).
* **Logique Power BI/Excel** : Le résultat est conçu pour une intégration directe dans les rapports Power BI et les modèles Excel (VBA pour le calcul du Safety Stock et les seuils DOS).
* **Logique SQL/M** : La structure sous-jacente nécessite une maîtrise des opérations **ETL complexes** pour la récupération et le nettoyage des données.

### 4.2. Feuille de Route Future : Prévision Axée sur l'IA/ML

Pour atteindre le niveau supérieur de Précision des Prévisions, la feuille de route est clairement définie par les lacunes de données identifiées :

* **Exigence de Données** : Sécuriser les Données de Ventes Historiques (Séries Temporelles).
* **Intégration ML** : Implémenter des **Random Forest** ou **XGBoost Regressors** (en remplacement de RLM) pour modéliser les relations non linéaires et atteindre une **Base de Prévision (Forecast Baseline)** supérieure.
* **Optimisation FVA** : Utiliser l'Importance des Caractéristiques (**Feature Importance**) du modèle ML pour guider objectivement le processus d'Adhésion au Forecast Consensuel, garantissant que le jugement humain n'est appliqué que là où l'impact des données est le plus élevé.
