# Etude-Coronavirus

## Objectif :

* Comprendre du mieux possible nos données
* Développer une premiere stratégie de modélisation 

## Analyse de Forme :

* variable target : SARS-Cov-2 exam result
* lignes et colonnes : 5644 et 111
* types de variables : qualitatives : 70, quantitatives : 41
* Analyse des valeurs manquantes :
  * Beaucoup de NaN (moitié des variables > 90% de NaN)
  * 2 groupes de données 76% -> Test viral, 89% -> taux sanguins 

## Analyse de Fond :

* Visualisation de la target : 10% de positifs (558 / 5000)
* Signification des variables : 
 * variables continues standardisées, skewed (asymétriques), test sanguin 
 * age quantile : difficile d'interpreter ce graphique, clairement ces données ont été traitées, on pourrait penser 0-5, mais cela pourrait aussi etre une transformation mathématique. On ne peut pas savoir car la personne qui a mit ce dataset ne le précise nul part (mais ca n'est pas très important).
 * variable qualitative : binaire (0, 1), viral, Rhinovirus qui semble tres élevée

* Relation Variables / Target :
 * target / blood : les taux de Monocytes, Platelets, Leukocytes semblent liés au covid-19 (hypothèse a testée)
 * target/age : les individus de faibles âge sont très peu contaminés ? -> attention on ne connait pas l'âge, et on ne sait pas de   quand date le dataset (s'il s'agit des enfants on sait que les enfants sont touchés autant que les adultes). En revanche cette variable pourra être intéressante pour la comparer avec les résultats de tests sanguins.
 * target / viral : les doubles maladies sont très rares. Rhinovirus/Enterovirus positif -> covid-19 négatif ? (hypothèse a testée) mais il est possible que la région est subie une épidémie de ce virus. De plus on peut très bien avoir 2 virus en même temps. Tout ca n'a aucun lien avec le covid-19.

## Analyse plus détaillée

* Relation Variables / Variables :
 * blood_data / blood_data : certaines variables sont tres corrélées : +0.9
 * blood_data / age : tres faible corrélation entre age et taux sanguins
 * viral / viral : influenza rapid test donne de mauvais résultats, il fauda peut-etre la laisser tomber
 * relation maladie / blood data : Les taux sanguins entre malades et covid-19 sont différents
 * relation hospitalisation / blood : intéressant dans le cas ou on voudrait prédire dans quelle service un patient devrait aller

## hypotheses nulle (H0):
 * Les individus atteints du covid-19 ont des taux de Leukocytes, Monocytes, Platelets significativement différents
 * H0 = Les taux moyens sont ÉGAUX chez les individus positifs et négatifs
 * Les individus atteints d'une quelconque maladie ont des taux significativement différents

