
#  Analyse quantitative: Resilience du luxe europpéen (1990-2026)

## Présentation du Projet
Ce dépôt héberge le framework quantitatif développé dans le cadre de la recherche sur la résilience boursière et le statut de valeur refuge du secteur du luxe européen. À travers l'analyse de 20 groupes d'entreprises cotées sur une période de 36 ans, ce projet évalue la performance ajustée au risque, le pricing power (Alpha de Jensen) et la dynamique comportementale des actifs face aux crises macroéconomiques majeures.

---

## Architecture Technique & Frameworks
Le projet est entièrement implémenté en **Python 3.9+** et repose sur les environnements scientifiques suivants :

* **Collecte de Données :** `yfinance` (Extraction automatisée des *Adjusted Close* / Total Shareholder Return).
* **Data Science & Analytics :** `pandas`, `numpy` (Alignement temporel, traitement des matrices glissantes).
* **Modélisation Économétrique :** `statsmodels` (Régression linéaire par les Moindres Carrés Ordinaires - MCO).
* **Dataviz & Validation :** `matplotlib`, `seaborn` (Analyse de la variance, homoscédasticité, normalité des résidus).

---

## Modèles Économétriques Implémentés

### 1. Ratio de Sharpe (Approche Ex-Post)
Mesure de l'efficience globale du secteur par rapport au risque de volatilité historique :
$$\text{Ratio de Sharpe} = \frac{R_p - R_f}{\sigma_p}$$
*En conformité avec les travaux de **Damodaran (2026)**, le taux sans risque ($R_f$) est fixé à 0 par convention de long terme.*

### 2. Alpha de Jensen & Bêta (Modèle CAPM)
Évaluation du Pricing Power ($\alpha$) et de la sensibilité systémique ($\beta$) face au benchmark de marché (CAC 40) :
$$R_p - r_f = \alpha + \beta (R_m - r_f) + \epsilon$$

---

## Indicateurs Clés & Résultats Stratégiques

| Métrique Financière | Index Soft Luxury | Index Hard Luxury | Index Lifestyle | Benchmark (CAC 40) |
| :--- | :---: | :---: | :---: | :---: |
| **Rendement Annuel Moyen** | **~15.00 %** | ~8.50 % | ~9.10 % | 2.94 % |
| **Ratio de Sharpe (35 ans)**| **0.51** | 0.34 | 0.39 | 0.28 |
| **Alpha de Jensen (α)** | **Positif (>0)** | Négatif (<0) | Négatif (<0) | 0.00 |
| **Bêta Systémique (β)** | **> 1.00 (Agressif)** | ~1.00 | < 1.00 (Défensif) | 1.00 |

>  **Rapport Statistique :** L'indice *Soft Luxury* s'établit comme le seul segment capable de générer un Alpha structurellement positif sur le long terme, confirmant un Pricing Power autonome face aux fluctuations macroéconomiques.

---

## Guide d'Exécution

### 1. Clonage et Dépendances
```bash
git clone [https://github.com/lynalabchri/luxe-resilience-analysis.git](https://github.com/lynalabchri/luxe-resilience-analysis.git)
cd luxe-resilience-analysis
pip install -r requirements.txt

```

### 2. Lancement de la Pipeline Quantitative

Pour exécuter l'extraction des données, le calcul des indices dynamiques, les régressions MCO et générer les graphiques de diagnostic :

```bash
python run_analysis.py

```

---

##  Structure du Répertoire

```text
├── data/                  # Données brutes et extractions sérialisées
├── src/                   # Scripts sources du modèle quantitatif
│   ├── data_loader.py     # Pipeline d'extraction yfinance & calcul du TSR
│   ├── metrics.py         # Fonctions Sharpe, Alpha, Beta, Max Drawdown
│   └── regressions.py     # Modélisation MCO et tests d'homoscédasticité
├── plots/                 # Sorties graphiques haute résolution (300 DPI)
├── main_analysis.py       # Script principal d'exécution
└── README.md              # Documentation du projet

```

---

## Références & Fondements

* **Damodaran, A. (2026).** *Equity Risk Premiums (ERP): Determinants, Estimation and Implications*. Stern School of Business.
* **Veblen, T. (1899).** *The Theory of the Leisure Class*. Macmillan.
* **Kapferer, J.-N. (2016).** *Luxury Branding Challenges*.

---

**Auteur :** **Lyna LABCHRI** – Parcours Finance, Université Paris 8.


```

### Pourquoi cette version fait très "pro" :
1. **Sobriété des émojis :** On supprime le côté "bling-bling" pour ne garder que des icônes de data science (`📊`, `🛠️`, `💻`).
2. **Formules mathématiques précises :** Les blocs de formules en notation LaTeX s'afficheront parfaitement sur GitHub.
3. **Structure de projet type :** La section *Structure du Répertoire* montre que ton code est propre, modulaire et structuré comme celui d'un véritable ingénieur financier/analyste de données.

```
