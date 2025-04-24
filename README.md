# 🏎️ Projet d'Économétrie 2024 – F1 : Budget & Performance

**Auteurs :** Hugo Schneider, Lola Carpentier, Ugo Corbari  
**Date de rendu :** 12 décembre 2024  
**Cours :** Économétrie - M1 APE  

---

## 🎯 Objectif du projet

Ce projet vise à étudier la relation entre le **budget annuel des écuries de Formule 1** et leur **performance sportive** sur la période **2010 à 2022**.  
L’objectif principal est de déterminer si un lien économétrique existe entre les **dépenses engagées** et le **nombre de points** marqués dans le championnat du monde de F1.

> 🧐 *Les écuries les mieux financées sont-elles systématiquement les plus performantes ?*

---

## 📊 Données

### 🔗 Sources :
- [Formula 1 – Résultats officiels](https://www.formula1.com)
- [Sportune – Estimations budgétaires](https://www.sportune.fr)

### 📅 Période :
- 2010 à 2022

### 🔢 Échantillon :
- 10 écuries
- 98 observations

### 🧾 Variables utilisées :

| Variable       | Description                                              |
|----------------|----------------------------------------------------------|
| `Points`       | Points marqués par l'écurie en fin de saison             |
| `Budget`       | Budget annuel en millions d’euros (log-transformé)      |
| `Pole`         | Nombre de pole positions obtenues                        |
| `Time`         | Temps moyen aux stands (en secondes)                    |
| `Salariés`     | Nombre d’employés par écurie                             |
| `Specs`        | Indice synthétique de spécificité technique              |

---

## 🧠 Méthodologie

### 🔧 Modèles estimés

1. **MCO simple :**  
   `Points = β₀ + β₁ · log(Budget) + ε`  
   Résultat : R² = 0.284

2. **MCO multiple avec variables de contrôle :**  
   `Points = β₀ + β₁ · log(Budget) + β₂ · Salariés + β₃ · Pole + β₄ · Time + β₅ · Specs + ε`  
   Résultat : R² ajusté = 0.780

3. **GLS – Moindres carrés généralisés**  
   Objectif : corriger l’autocorrélation temporelle détectée

---

## 🧪 Tests économétriques

| Test                  | Résultat                              |
|-----------------------|----------------------------------------|
| Breusch-Pagan         | Pas d’hétéroscédasticité (p > 0.2)     |
| Durbin-Watson         | Autocorrélation détectée (DW ≈ 0.7)    |

---

## 📈 Résultats principaux

- Le **budget seul** explique une part modeste de la performance.
- Le **modèle enrichi** indique que :
  - Le **nombre de salariés** est fortement significatif (p < 0.01)
  - Le **nombre de pôles positions** est le facteur le plus explicatif
  - Le **budget** perd en significativité dans ce modèle
- Le **temps aux stands** et les **spectateurs** n’ont pas d’effet statistique significatif
- La **correction GLS** confirme les tendances mais ne résout pas totalement l’autocorrélation

---

## 📉 Visualisation

- **Graphique Budget vs Points :**  
  Montre une forte **dispersion** des points à budget équivalent, particulièrement entre 150 et 200 M€.  
  Cela suggère des **facteurs non observés** influençant fortement les performances.

---

## ⚠️ Limites

- **Autocorrélation persistante** même après correction GLS
- **Accès restreint** aux données internes des écuries (profil des ingénieurs, innovations)
- **Variables omises** possibles (qualité des pilotes, incidents en course, météo)

---

## 📚 Conclusion

Les résultats remettent en cause l’idée selon laquelle un plus grand budget garantit de meilleures performances.

> ✅ **Ce sont les choix stratégiques et humains qui comptent plus que le simple budget.**

Une analyse plus poussée avec des données qualitatives et des modèles dynamiques permettrait d’affiner cette conclusion.

---

## 🛠️ Stack technique

- **Langage** : R
- **Packages** : `dplyr`, `ggplot2`, `lmtest`, `nlme`, `car`
- **Sortie** : HTML via RMarkdown

---

## 📁 Structure du projet

