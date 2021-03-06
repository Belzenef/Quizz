Manuel d'utilisation
====================


Elaboration d'un Quizz en réseau dans le cadre du cours "Programmation réseau" de 4BIM.

Language utilisé: python3

Le but de ce projet est de créer un quizz en réseau. Il faut premièrement lancer le fichier Serveur.py (python3 Serveur.py) puis plusieurs clients avec le fichier Client.py. En se connectant, chaque participant choisit son pseudo. Il est également possible de choisir son pseudo directement en lançant le fichier Client.py (Exemple: python3 Client.py pseudo). Dans ce cas le pseudo ne sera pas demandé. Enfin, pour une utilisation en réseau avec plusieurs machines, il faut fournir le pseudo ainsi que l'adresse IP de la machine sur laquelle le serveur a été lancé (Exemple: python3 Client.py pseudo 134.214.XXX.XXX)

Il est possible de jouer en réseau sur n'importe quel ordinateur de l'INSA. Il faudra alors préciser l'adresse IP de l'ordinateur qui lance le serveur (Exemple: python3 Client.py pseudo 134.214.159.199). Pour obtenir l'adresse IP il est possible de rentrer la commande suivante dans un terminal : "curl ifconfig.me". Si on ne précise pas d'adresse IP, le quiz se lancera en local.

Une fois connectés, les joueurs doivent choisir entre:

    Attendre que d'autres joueurs se connectent ("wait")
    Lancer une partie ("start")
    Quitter le jeu ("quit") Si la saisie du client est invalide ou s'il ne répond pas au bout de 30 secondes, cela aura le même effet que "wait".

Lorsqu'un joueur lance une partie, tout les joueurs en "attente" vont alors jouer. En lançant une partie, le joueur devra sélectionner un thème parmis 3 et choisir le nombre de questions souhaitées. Les joueurs répondront simultanément aux questions par vrai(V) ou faux(F). Si un joueur met plus de 30 secondes à répondre il passe directement à la question suivante. A la fin de la partie, les joueurs obtiennent le nombre de points gagnés ainsi que le classement de la partie. Les points sont comptés de la façon suivante:

    +1 si le joueur répond correctement à la question
    -0.5 si le joueur donne une mauvaise réponse
    0 s'il ne répond pas

A l'issu du classement les clients reviennent au choix initial et peuvent choisir d'attendre, de lancer une partie ou de quitter.

Amusez vous bien!

