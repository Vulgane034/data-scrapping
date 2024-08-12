# data-scrapping
collect et exploration des donnees provenant d un site de e-commerce au cameroun(iziway)
 










 	1

Table des matières

evaluation des competence : Réalisation d’un Scrapping de 5 sites de e-commerces	4
Cas de :	4
-Glothelo	4
-Iziway	4
Méthode de collecte : les donnes devront être enregistrés dans des Data Frame (enregistres en format csv)	5
Progression : récupération des informations sur le site iziway	5
TAF (deuxième semaine de juillet) :	5
Problème à résoudre	5
Travail du jour (23/07/2024) :	5
Travail à faire : compléter la liste d’éléments (24/07/2024)	5
Bilan de la dernière semaine de juillet	5
Travail demander :	5
Action réaliser	5
Exploration :	13
INTERPRETATION DU TABLEAU DE SYTHESE	14
Observation 1 :	15
Observation 2 :	16
Analyse 2 :	16
Observation 3	17
Analyse 3 :	17
OBSERVATION 4	18
Analyse 4 :	18
Recommandation :	19
 























Table des figures



Figure 1:exploration du code html du site	6
Figure 2:scrapping tes	7
Figure 3:stockage des info scraper (List)	7
Figure 4: normalisation du dictionnaire		8
Figure 5: définition du DataFrame à partir du dict.	8
Figure 6:fonction de Scrapping	9
Figure 7:fonction de normalisation	10
Figure 8:resultat de la normalisation du dictionnaire	10
Figure 9:vision d’ensemble du DataFrame obtenu	11
Figure 10:debut du preprocessing	11
Figure 11:initialisation des fonction de nettoyage	12
Figure 12 : observation et correction d’anomalie	12
Figure 13 :visualisation du DataFrame corriger(tableau de synthèse)	13
Figure 14 : Visualisation de l’ensemble du DataFrame	13
Figure 15 : Visualisation et interprétation du tableau de synthèse	14
Figure 16 : présentation de la fonction de catégorisation du DataFrame	15
Figure 17: Visualisation des prix réel par rapport aux anciens prix	15
Figure 18 : Visualisation des prix par catégories de produits	16
Figure 19 : Visualisation des prix par rapport au réduction	17
Figure 20 : répartition des taux des catégories par rapport au totale de distribution	18




evaluation des competence : Réalisation d’un Scrapping de 5 sites de e-commerces
Cas de :
-Glothelo
-Iziway
Objectif : élaboration d’un comparateur des prix et générateur d’alertes en cas de changement de prix d’un produit
 


         
         
colleter de facon automatiser

Souper c est egalement scrapper 
Définition : le web Scrapping est méthode qui consiste à récupérer les données provenant d’une source en ligne (site web, blog etc.…) dans le but d’effectuer de nombreuse opération l’analyse l’exploitation a des fin personnel ou opérationnel (Business Intelligent) 

Pour le réaliser on utilise des outils comme BeautifulSoup, requests, selectolab et ou seletium
Méthode de collecte : les donnes devront être enregistrés dans des Data Frame (enregistres en format csv)
Progression : récupération des informations sur le site iziway
TAF (deuxième semaine de juillet) : les informations ont été encapsule dans un dictionnaire info = {}, possédant pour clé des chaines de caractères dont les valeurs sont des List à savoir :
Listing["description"] = []
Listing ["prix réel"] = []
Listing["prix_barre"] = []
Listing["reduction"] = []
Problème à résoudre : le dictionnaire présente un défaut de formage (apparition des caractère   \xa0)
Travail du jour (23/07/2024) :
Scrapping des informations particulières des produits du site (description : marque, prix avant réduction, prix après réduction
L’ensemble des données scraper ont été mise dans une structure de données (dictionnaire ayant pour clé des chaines de caractères dont les valeurs sont des listes
Le dictionnaire a été charger et enregistre sous format json
Travail à faire : compléter la liste d’éléments (24/07/2024)
Mettre sur pied une fonction qui parcours les balises du code source du site web qui retourne le contenu des balises sélectionné de manière spécifique
Bilan de la dernière semaine de juillet
Travail demander : il était question de collecter l’équivalent de 1000 ligne d’information du site iziway
Action réaliser


Analyse fondamentale : il était question ici de faire une analyse générale de la structure du site (distribution des balises de chaque page et évaluer les similitudes structurelles ainsi que les limite d’exploration liées au blocage volontaire si existant)

 
Figure 1:exploration du code html du site


Test Scripting : il s’agit de l’élaboration du premier script de code pour le scrapping il sert essentiellement de script de validation des hypothèses de l’analyse fondamentale


 
Figure 2:scrapping tes

 
Figure 3:stockage des info scraper (List)


 
 
Figure 4: normalisation du dictionnaire	 
Figure 5: définition du DataFrame à partir du dict.
Retro processing analysis : ici il était question après analyser de problématique de volume (quantité de donne à scraper) et de temps et utilisation des fondements de code élaborer lord du Scripting test élaborer un ensemble de fonction afin de réalisation de la manière la plus simple notre tache
Réalisation de la fonction de Scrapping : cette dernière prend en paramètre un dictionnaire définit de maière particulière ainsi que le lien de la page a scraper
 
  
Figure 6:fonction de Scrapping

Réalisation de la fonction de normalisation permettant de résoudre le problème d’indexation numpy en claire mettre les différentes tables à la même taille (valeurs des clé) cette dernière prend en      paramètre le dictionnaire précédemment obtenu
 
Figure 7:fonction de normalisation


 
Figure 8:resultat de la normalisation du dictionnaire


Exploration, pre-processing et analyse : l’action qui a été réellement réaliser en quasi-totalité c’est le pre-processing ou prétraitement du DataFrame
 
Figure 9:vision d’ensemble du DataFrame obtenu


Ici il était question de traite les anomalies tel que les NaN, les cases vides et le changement de type des séries du DataFrame
 
Figure 10:debut du preprocessing


 
Figure 11:initialisation des fonction de nettoyage
 
Figure 12 : observation et correction d’anomalie
 
Figure 13 :visualisation du DataFrame corriger(tableau de synthèse)

 
Figure 14 : Visualisation de l’ensemble du DataFrame



Exploration :
Après correction des anomalies du DataFrame il est ici temps pour nous de passer à l’exploration proprement dite de ce dernier
Description du DataFrame : ici cette procédure nous permet d’avoir une vision d’ensemble des paramètres descriptif du DataFrame cette opération est assurer par df.describe()
 
Figure 15 : Visualisation et interprétation du tableau de synthèse



INTERPRETATION DU TABLEAU DE SYTHESE
On peut Alor remarquer grâce à différent paramètre les caractéristiques descriptives du DataFrame nous énumérons entre autre
Count qui comptabilise le nombre d’élément retrouver dans le DataFrame (df. Count () pour la méthode utiliser sur le DataFrame) on peut facilement observe ici que notre DataFrame possède environs 1250 lignes d’informations pour chaque séries (colonne) du DataFrame
mean qui donne (calcul) la moyenne de chaque séries (colonnes) du DataFrame (la méthode utiliser est df. mean()) il donne les valeur moyenne du DataFrame
Std calcul l’écart type de chaque série du DataFrame (df.std ()) il est utilisé pour évaluer la dispersion entre les valeur d’un tableau statique
Min et max permettent de donner respectivement les valeur minimal et maximal du DataFrame




Apres observation et analyse des caractères descriptifs du DataFrame il est à cet effet nécessaire d effectue une répartition du DataFrame en catégorie pour une meilleure exploration de données
A cet effet nous avons formaliser la fonction Classify_descriptionde la manière suivante
 
Figure 16 : présentation de la fonction de catégorisation du DataFrame

Les mots keywords est un dictionnaire ayant pour clés des chaines de caractère représentant les catégories dont les valeurs sont des listes ; Des List contenant des mots clés
 
Figure 17: Visualisation des prix réel par rapport aux anciens prix

Observation 1 :
Ce graphique permet de faire état de la faite que le ratio global des nouvelles valeurs de tarification (prix) par rapport au anciens est drastiquement bas ce qui qui suggère qu’une trop grande réduction a été appliquer sur les différents articles pour cependant il existe une proportion qui fait état de la possibilité   mise en rayon de nouveau produit potentiellement méconnus des habituer (consommateur habituel)

 
Figure 18 : Visualisation des prix par catégories de produits

Observation 2 :
Ce graphique permet de visualiser les prix par rapport à la distribution (différente catégorie) du DataFrame
Analyse 2 :
Nous pouvons distingue une dispersion de valeur de prix dans la catégorie Tablette
Par contre nous notre un regroupe de valeur dans les autre catégorie (par ensemble spécifier de produit ou catégorie) c est cas des catégories téléphone, autres (note que cette catégorie est essentiellement constituée des catégorie électroménager et accessoire), électroménager, jouet
Le prix le prix élevé de 2.5*1000000=2500000FCFA et la valeur la plus basse est estime environs dans 25000FCFA
Ce qui suggère une distribution irrégulière des prix par catégorie


 
Figure 19 : Visualisation des prix par rapport au réduction


Observation 3 :
Ce graphique permet de visualiser les prix par rapport au réduction
On observe un regroupement de point sur l’intervalle -0.5 à -0.3 sur l’horizontale
Sur la verticale dans l’intervalle 0 à 0.2 on observe une population abondante de point avec des écarts entre les point (relativement non négligeable)
Sur l’intervalle -0.1 à 0 on observe tenant également des intervalles verticaux de 0.24 à 2 on observe une suit discontinu et croissant des point
Analyse 3 :
-0.8 a –0.02 sur l’horizontale les réductions applique sont relativement importante pour des valeur (prix) bas (en dessous 200000FCFA)
Et nul ou quasiment nul si les prix sont au-dessus de 200000FCFA
Risque liée à cette manière de procéder : appliquer des réductions significatives sur les de petite valeur pourrais pousser la clientèle a centrée les achats sur ces dernier (on pourrais donc noter une baisse significative du chiffre d’affaire)
Ou pire aller concurrence car pré sentant que les réductions ne s’appliquent pas aux marchandise de première nécessiter (au yeux du client) ce qui voudrait dire que l’entreprise ne pas totalement le client au centre de son attention


 
Figure 20 : répartition des taux des catégories par rapport au totale de distribution

OBSERVATION 4 :
Ce diagramme en tarte permet de visualiser la réparation des prix par catégorie et évalue l’ampleur par rapport au DataFrame entier
Analyse 4 :
Si l’on tient compte des analyses précédant par rapport à la catégorie Autres il ressort que la catégorie influençant plus le business (produisant la meilleur marge financière) est la catégorie électroménager (associer à la catégorie Autres) suivie de la catégorie accessoire (associer à la catégorie Autres) suivie de tabelle, téléphone
La catégorie jouet est négligeable 0.7%
Recommandation :
•	Il faut centrée son approvisionnement en marchandise sur les catégories qui représentent au moins 10% du chiffre d’affaire le reste (valeur<8%) constitue plus une charge qu’autre chose (cout supplémentaires et superflu en stockage en approvisionnement et en marketing)
•	Revoir les politiques de réductions sur les prix par catégorie il est recommandé de faire faire de petite réductions récurrente sur les produit de valeur élève (influençant significativement le chiffre d’affaire) afin d’attirer et de conserve la clientèle et ou offrir les articles de valeur très basses (dans cas ou on aurait appliqué aucune réduction sur les produit des catégories de valeur importante)
•	Homogénéiser la distribution des articles pour plus de diversité (choisir également une distribution liée au mots associe au description des articles pour mieux classe les catégories)
