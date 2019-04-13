# ARE-Viralite
Projet mené par Noah Maupu, Gaetan Scart, Yanis Lacroix et Thomas Binga.

Déroulement du travail:

Nous savions que nous voulions utiliser des matrices (des listes de listes sur Python) pour créer des réseaux de connections entre personnes, nous avons donc commencé par faire des connections simples avec une matrice 5 par 5. Nous avons donc cherché à faire passer une information dans ce réseau de connections et observer selon quelles conditions l'information allait devenir virale/allait mourir. 
    
Une fois que nous avons compris le fonctionement, nous avons fait de jolis programmes pour créer des réseaux de connections automatiquement avec un nombre n de personnes. De plus nous avons modélisé nos schémas gràce à NetworkX qui nous permetde créer différents "réseaux neuronaux" que nous assimilons à un réseau de personnes reliées entre elles .
    
Nous avons ensuite cherché à ce que les personnes de nos réseaux puissent avoir des profils types qui leur donneront des caractéristiques différentes. Pour commencer nous avons crée 4 profils types(classique, marginal, geek, vieux) avec, comme différences entre les profils: le nombre moyen d'amis, la probabilité de voir l'information si ils l'ont reçu et la probabilité de la repartager. Nous avons aussi fait des schémas avec des couleurs différentes pour chaque type de personne.
    
## Mercredi 13 mars:
    
D'après le modèle de connections expliqué par Nicky Case, les réseaux seraient consitués de petits groupes de personnes proches avec des ponts entre les différents groupes. Nous avons donc décidé que nos réseaux, qui était composés d'environ 100 personnes, seraient ces fameux groupes. Pour cela, nous avons créé un programme générant un quantité voulue de groupes de tailles différentes. Nous avons ensuite cherché à créer des liaisons entre les groupes en prenant compte un nouveau paramètre pour chaque type de personne: la probabilité d'avoir des amis en dehors de leur groupe.

## Mercredi 20 mars:

Nous avons écrit un programme permettant de lier les différents groupes entre eux. De plus, nous avons commencé à nous pencher sur l'interface graphique afin d'avoir des beaux réseaux d'amis !  finalement nous nous sommes pris la tête avec github.

## Mercredi 27 mars:

Nous avons commencer a écrire un programme permettant de modéliser la diffusion d'une Fake News, en ajoutant au programme un profil "média". Ce dernier présente une probabilité de démentir la fake news au moment de la repartager. Le but de ce programme est de voir si une Fake News sera diffusée ou non en fonction du nombre de média présent, de la probabilité de démentir l'info.

De plus, nous avons fini le programme qui nous indique quel groupe fait des liaisons avec quel groupe et qui nous indique pour chaque liaisons, les personnes exactes qui font ses liaisons. C'est à dire Groupe 1: le geek 3 fait une liaison avec le vieux du groupe 2 etc ...

## Mercredi 3 avril:

Nous avons travaillé sur plusieurs fronts aujourd'hui, d'un côté, Gaëtan à avancé le système avec groupes afin de faire circuler l'information au sein d'une population comptant plusieurs groupes (des ajustements doivent encore être apportés mais le programme est cohérent et fonctionne dans les grandes lignes).

D'autre part, Yanis et Noah se sont occupés de modéliser le système avec fake news. Pour cela, ils ont poussé leur reflexion de la semaine précédente pour arriver au modèle suivant: un groupe présente au moins 1 profil média, capable de démentir l'information quand il la reçoit. S'il la dément, il va alors transmettre cette nouvelle information (appelée contre-info). Chaque personne recevant alors cette contre-info va de nouveau la partager à ses amis pour "prévenir" de l'impertinence de l'information transmise au préalable. De nouveaux cas apparaissent avec ce modèle qui commence à se complexifier, cela leur a posé quelques problèmes, notamment pour réussir à transmettre l'information correctement, car il leur a désormais fallu transmettre 2 information en parallèle. 

Enfin, Thomas a continué la partie graphique sous NetworkX afin d'obtenir une reprsentation du réseaux, indiquant quel agent possède l'information (point rouge ou blanc). Nous avons ensuite pensé à réaliser un GIF, qui nous permettrait d'observer l'évolution de la transmission de l'information.

## Mercredi 10 avril:
Afin de modélisé graphiquement les groupes de groupes, Gaëtan et Thomas ont changé d'idée. En effet, un groupe de groupe n'étant pas représentable simplement sous forme de matrice, nécessaire à la création du graphique, ils ont pensé simplement réaliser une matrice générale de liaisons, comprenant tous les agents tout groupe confondus. Les personnes d'un même groupe réalisant plus de liaisons avec une personne de leur groupe qu'avec une personne extérieure, la modélisation graphique nous a alors donné une représentation claire du réseau totale: plusieurs groupes très denses en liaisons, et quelques liaisons entre chaque groupe. Ce modèle nous a semblé très proche de la réalité sur les réseaux sociaux.

De leur côté, Noah et Yanis ont réussi à diffuser une fake news en intégrant la possibilité qu'une contre info puisse inverse la diffusion de la fake news. Utiliser plotly pour tracer les 2 courbes de l'évolution du nombre de personnes croyant ou non à la fake news leur a permis de valider leur modèle. En effet, selon les paramètres et les différents cas, soit la Fake News a été diffusée en majorité, soit elle a touché un grand nombre de personne, avant de redescendre, suite à la diffusion importante de la contre info.

Avant d'exploiter nos programmes pour obtenir des résultats en fonction de tous les paramètres (proba, nombre d'amis, qui commence à diffuser l'info...) nous souhaitons encore finaliser certaines choses : 
- réussir à obtenir le GIF de la diffusion d'une Fake News (avec contre-info) 
- tenter d'étendre le modèle de la diffusion de Fake News (avec contre-info) aux groupes de groupes
