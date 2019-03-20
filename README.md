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
