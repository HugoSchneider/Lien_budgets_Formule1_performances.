🏎️ Projet d'Économétrie 2024 – F1 : Budget & Performance

Auteurs : Hugo Schneider, Lola Carpentier, Ugo Corbari
Date de rendu : 12 décembre 2024
Cours : Économétrie - M1 APE

🎯 Objectif du projet

Ce projet vise à étudier la relation entre le budget annuel des écuries de Formule 1 et leur performance sportive sur la période 2010 à 2022. L’objectif principal est de déterminer si un lien économétrique existe entre les dépenses engagées et le nombre de points marqués dans le championnat du monde de Formule 1.

Nous avons ainsi tenté de répondre à la question suivante :

"Les écuries les mieux financées sont-elles systématiquement les plus performantes ?"
🧾 Données

Source principale :
Site officiel de la Formula 1
Estimations de Sportune.fr
Période couverte : 2010 à 2022
Échantillon : 10 principales écuries du championnat, soit 98 observations
📌 Variables principales :

Variable	Description
Points	Points obtenus en fin de saison
Budget	Budget annuel en M€ (log-transformé pour l’analyse)
Pole	Nombre de pole positions obtenues par saison
Time	Temps moyen aux stands (en secondes)
Salariés	Nombre d’employés dans l’écurie
Specs	Spécificité technique (indice synthétique)
📊 Méthodologie

🔧 Modèles estimés :
MCO simple :
Points
=
β
0
+
β
1
log
⁡
(
Budget
)
+
ϵ
Points=β 
0
​	
 +β 
1
​	
 log(Budget)+ϵ
Résultat : 
R
2
=
0.284
R 
2
 =0.284
MCO multiple avec variables de contrôle :
Points
=
β
0
+
β
1
log
⁡
(
Budget
)
+
β
2
Salari
e
ˊ
s
+
β
3
Pole
+
β
4
Time
+
β
5
Specs
+
ϵ
Points=β 
0
​	
 +β 
1
​	
 log(Budget)+β 
2
​	
 Salari 
e
ˊ
 s+β 
3
​	
 Pole+β 
4
​	
 Time+β 
5
​	
 Specs+ϵ
Résultat : 
R
a
j
u
s
t
e
ˊ
2
=
0.780
R 
ajust 
e
ˊ
 
2
​	
 =0.780
GLS (Moindres Carrés Généralisés) pour corriger l’autocorrélation
Corrige l’erreur structurelle temporelle détectée dans les tests Durbin-Watson
🧪 Tests économétriques
Homoscédasticité : test de Breusch-Pagan
➤ Aucun problème détecté (p > 0.2)
Autocorrélation : test de Durbin-Watson
➤ Présence d’autocorrélation importante (DW ≈ 0.7, p < 10⁻¹²)
📈 Résultats et interprétations

Budget seul : effet significatif dans le modèle simple, mais devient non significatif dans le modèle enrichi.
Variables significatives (p < 0.01) :
Nombre de salariés : effet positif robuste
Pole positions : effet très fortement corrélé aux performances
Temps moyen aux stands et spectateurs : effets non significatifs
Modèle GLS : confirme les effets observés mais ne corrige pas totalement l’autocorrélation (DW = 0.66)
📉 Visualisations clés

Graphique Budget vs Points :
➤ Forte hétérogénéité des résultats à budget équivalent, surtout entre 150–200 M€
➤ Dispersion importante qui suggère l’importance de facteurs non observés
⚠️ Limites du projet

Autocorrélation persistante dans les résidus, même après GLS
Accès limité aux données internes (stratégies d’upgrade, profils des ingénieurs)
Possibles variables omises (qualité des pilotes, météo, incidents)
📚 Conclusion

Les résultats de notre étude remettent en question l’idée reçue selon laquelle un gros budget garantit automatiquement de meilleures performances.

✅ Ce sont les compétences humaines et la stratégie (pole positions), plus que le seul budget, qui expliquent la réussite des écuries.
Ce projet ouvre la voie à des recherches intégrant des modèles dynamiques, des effets fixes par équipe, ou des données plus qualitatives sur les ressources internes.
