🏎️ Projet Économétrie 2024 : Formule 1 & Performances des Écuries

Auteurs : Hugo Schneider, Lola Carpentier, Ugo Corbari
Date : 12 décembre 2024

🎯 Objectif du projet

Ce projet vise à explorer économétriquement la relation entre les budgets des équipes de Formule 1 et leurs performances sportives. L’étude couvre la période 2010 à 2022, et s’intéresse aux 10 principales écuries ayant participé au championnat du monde.

La question centrale est simple mais ambitieuse :
👉 Le budget d'une écurie influe-t-il réellement sur ses performances ?

📊 Données utilisées

Deux types principaux de données ont été collectés :

Données de performance (source : site officiel Formula 1) :
Nombre de points par saison
Nombre de pôles positions
Temps moyen passé aux stands
Données financières et structurelles (source : Sportune et estimations internes) :
Budget annuel (en millions €)
Nombre de salariés
Nombre de spectateurs par course
Spécifications techniques synthétisées
La base finale comprend 98 observations sur la période 2010–2022.

🧠 Méthodologie

Nous avons construit plusieurs modèles économétriques :

Modèle MCO simple : points en fonction du logarithme du budget
Modèle MCO multiple : intégration de variables de contrôle (salariés, pôles, temps aux stands, spectateurs)
Tests de diagnostic :
Breusch-Pagan pour l’homoscédasticité
Durbin-Watson pour l’autocorrélation
Régression GLS pour corriger l’autocorrélation constatée
📈 Résultats clés

Le budget seul explique environ 28 % de la variance des performances.
En incluant les variables de contrôle, le modèle atteint un R² ajusté de 0,78.
Les deux variables les plus significatives sont :
Le nombre de salariés (impact positif significatif)
Le nombre de pôles positions (fort impact positif)
Le budget n’est pas significatif dans le modèle enrichi, ce qui suggère un effet indirect ou conditionnel.
Présence d’autocorrélation des résidus, corrigée via GLS.
🧩 Limites

Données confidentielles inaccessibles, comme :
Détails sur les investissements technologiques
Nombre d’ingénieurs ou mises à jour aérodynamiques
Hétérogénéité non expliquée entre certaines écuries à budget similaire
📚 Conclusion

Le lien entre budget et performance en Formule 1 est complexe et non linéaire.
Les résultats mettent en avant l’importance de la qualité humaine (salariés) et des performances stratégiques (pôles) plutôt que du seul budget.

📌 En somme : dépenser plus ne garantit pas de gagner plus.
Ce travail ouvre la voie à des recherches plus fines, intégrant des données techniques internes et un traitement des effets fixes temporels ou d’équipe.
