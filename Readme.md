
Brief Construire un moteur de recherche d'emploi

le rendu de ce brief s'articule autour de 4 documents:



1. Bref mongodb

il s'agit d'un résumé de l'ensemble des commandes appliquées pour la création de la base mongodb, l'insertion d'un document, la recherche et l'indexation. Ces commandes sont à taper d'un un sell mongodb.


2. Mongo.ipynb
Un Un




3. flashboot.py 

un programme python qui permet de récupérer les données du site en question.
pour le lancer , il faudrait suivre les étapes suivantes à partir du terminal :

- Créer  un dossier flashboot 
- tapper la commande suivvant : 

$ scrapy start projet flashbot. 


Nous obtenons l'arborescence suivante :

scrapy.cfg
flasbot
	__init__.py 
	items.py  
	middlewares.py 
  	pipelines.py  
  	posts.json  
 	__pycache__ 
 	settings.py 
 	spiders
 		flashbot.py 
 		__init__.py  
 		__pycache__
 		
 Le fichier flashbot.py se trouve ds le dossier spliders.
 le fichier pipelines.py permet d'insérer les documents extraits dans la base (reste à faire).
 L'extraction, dans notre cas se fait au travers d'un fichier  Mongo.ipynb par le biais un fichier "json".
Avant de lancer le flashbot, dans le fichier settings.py, il faudrait désavctiver cette ligne afin d'indiquer à Scrapy d'envoyer le résultat du crawl dans "item", qui sera récupérer dans le fihier piplines.py.


ITEM_PIPELINES = {
   'flashbotN.pipelines.FlashbotnPipeline': 300,
}


ce dernier se chargera par la suite d'inserer les données dans la base mongodb. 

Pour lancer le flasbot, il faut se positionner dans le dossier ou se trouve le "scrapy.cfg" et tapper la commande suivante :

$ scrapy crawl flashbot





 
