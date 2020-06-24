# Projet-DataScience-Machine-Learning
# 1. Exploratory Data Analysis (EDA)  

## Objectif : 
- Comprendre du mieux possible nos données 
- Développer une premiere stratégie de modélisation   

#### Analyse de la forme   
- **variable target (variable à expliquer)** : SARS-Cov-2 exam result  
- **linges et colonnes** :5644, 111   
- **types de variables (variables explicatives)**: quantitatives :70 , qualitatives : 40  
- **Analyse des valeurs manquantes** :     
  - beaucoup de NaN (moitié des variables > 90% de NaN)    
   - 2 groupes de données 76% -> Test viral, 89% -> taux sanguins       
#### Analyse de Fond : 
  - **Visualisation de la target** :     - 10% de positifs (558 / 5000)          
  - **Signification des variables** :     -  variables continues standardisées, skewed (asymétriques), test sanguin    
  - age quantile : difficile d'interpreter ce graphique, clairement ces données ont été traitées, on pourrait penser 0-5, mais cela pourrait aussi etre une transformation mathématique. On peut pas savoir car la personne qui a mit ce dataset ne le précise nul part. Mais ca n'est pas tres important     
  - variable qualitative : binaire (0, 1), viral, Rhinovirus qui semble tres élevée.   
  
  - **Relation Variables / Target** :     - target / blood : les taux de Monocytes, Platelets, Leukocytes semblent liés au covid-19 -> hypothese a tester.        
  - target/age : les individus de faible age sont tres peu contaminés ? -> attention on ne connait pas l'age, et on ne sait pas de quand date le dataset (s'il s'agit des enfants on sait que les enfants sont touchés autant que les adultes). En revanche cette variable pourra etre intéressante pour la comparer avec les résultats de tests sanguins        
  - target / viral : les doubles maladies sont tres rares. Rhinovirus/Enterovirus positif 
  - covid-19 négatif ? -> hypothese a tester ? mais il est possible que la région est subie une épidémie de ce virus. De plus on peut tres bien avoir 2 virus en meme temps. Tout ca n'a aucun lien avec le covid-19.       
  
  ## Analyse plus détaillée  
  
  - **Relation Variables / Variables** :     
  - **Relation quanti * quanti **         - blood_data / blood_data : certaines variables sont tres corrélées : +0.9 (a suveiller plus tard)              
  - **Relation quanti * quali **         - blood_data / age : tres faible corrélation entre age et taux sanguins             
  - **Relation quali * quali **          - viral / viral : influenza rapid test donne de mauvais résultats, il fauda peut-etre la laisser tomber      
  - relation maladie / blood data : Les taux sanguins entre malades et covid-19 sont différents       
  - relation hospitalisation / est malade :          
  - relation hospitalisation / blood : intéressant dans le cas ou on voudrait prédire dans quelle service un patient devrait aller   
  - **NaN analyse** : viral : 1350(92/8), blood : 600(87/13), both : 90  ### hypotheses nulle (H0):  
  - Les individus atteints du covid-19 ont des taux de Leukocytes, Monocytes, Platelets significativement différents    
  - H0 = Les taux moyens sont ÉGAUX chez les individus positifs et négatifs  - Les individus atteints d'une quelconque maladie ont des taux significativement différents  
  
  # 2. Machine Learning (ML) 
  
   ## train- test
   ## encodage, imputation et nettoyage (Pretraitement / Prepossecing)
   ## Modelisation
   ## Precision de la qalité
   ## Matrice de confusion
