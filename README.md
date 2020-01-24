# Reconnaissance-contexte-ML

Depuis quelques années,  dans plusieurs domaine ils ont commencé une transformation digitale profonde de leurs services. Cette transformation, accompagnée de l’émergence des nouvelles techniques d’analyse et de prédiction, vient impacter la façon de penser. Ainsi, aujourd’hui ils ont amené à s’approprier aux outils et méthodes de « l’intelligence artificielle » afin d’en maîtriser les risques, mais surtout d’être en adéquation avec les nouveaux besoins de plus en plus connectés. Reconnaissance de context La reconnaissance consiste à identifier le sujet dans article grâce au traitement de texte d’une manière automatique, cela pourrait être utile pour des projets qui travaillait sur la compréhension de texte, il peut-être très utile comme une variable dans dataset, ou d’autres domaine.

## Scraper crawler 
J’ai collecté des données textuelles sur des sites proposés par google avec un mot clé en entré, dans mon projet j’ai collecter des sujets autour de 4 sujets ['hotel','informatique','science','technologie']. Nous pouvons élargir le nombre de sujets autant qu’on le souhaite mais pour cela il faut assez de mémoir de stockage des données massive.
J’ai utilisé BeautifulSoup et Selenium et pour scraper les données, ma méthode est de taper des mots clés sur google est récupéré les données textuelles à partir de 35 sites proposer par google (si il existe), je stocke dans des fichiers .txt avec le nom de sujet. 
Avec `Selenium` je récupère la page de recherche google, pour pouvoir récupérer les liens de sites proposés puis je scraper `BeautifulSoup` les urls un par un


## Dataset 

À partir des données brute stocker en format texte, je récupère les ligne en lui attribuant un label de son sujet dans fichier CSV, j’ai effectué un traitement sur le texte au même temps, j'ai utilisé le package `nltk` et les `Regex` pour récupérer les tokens nltk à partir de text et créer un texte nltk, et la suppression de brute `re.sub(r'[.|,|\|!|"|#|$|%|&|\|*|+|-|/:|;||?|@|^']',' ', raw) `, et normalise les mots en les transformant en minuscules, puis supprimer les mots qui sont tellement commun qu'il est inutile de l'indexer ou de l'utiliser dans une recherche appelé les mots vides. Puis je construite un dataset avec tout le corpus dont il existe tout les domaine choisi.

