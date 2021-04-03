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
* Signification des variables : * variables continues standardisées, skewed (asymétriques), test sanguin * age quantile : difficile d'interpreter ce graphique, clairement ces données ont été traitées, on pourrait penser 0-5, mais cela pourrait aussi etre une transformation mathématique. On peut pas savoir car la personne qui a mit ce dataset ne le précise nul part. Mais ca n'est pas tres important
