---
title: "V3 et publication Open Source"
date: 2017-12-26T10:07:24+01:00
draft: false
---

# la-trace.com v3

## tl;dr

> La version 3 de la-trace.com est actuellement disponible en test à l'adresse
suivante [https://v3.la-trace.com/](v3.la-trace.com). Il s'agit d'une réécriture
**complète** qui sera désormais **opensource**. Le code est hébérgé sur
[https://github.com/la-trace](https://github.com/la-trace)

<!--more-->

## Constat

Le site à vu le jour en mars 2011. Après deux évolutions du site et après avoir
remporté le premier prix du concours IGN/Géoportail en 2013, force était de
constater que j'avais de moins en moins de temps pour m'occuper de ce projet que
je développe et gère seul depuis le début.

Néanmoins le site continue son petit bonhomme de chemin et continue de générer
du trafic et bon nombre de **traces GPS** continuent d'y être publiées.

Par ailleurs, le site n'a jamais eu pour vocation de générer des revenus et les
quelques publicité que j'ai pu y mettre ont servi à m'aider à financer
l'hébergement. J'ai à chaque fois refusé les quelques propositions de rachat.

N'ayant pas l'envie de laisser mourrir à petit feu ce projet qui m'a tant
apporté sur le plan professionnel comme sur le plan personnel, il était temps de
trouver une **solution pour péreniser le site et son contenu**.

Voilà maintenant plus d'un an, j'ai commencé une refonte complète du site :
*Base de données*, *API* et *front-end* et hébergement, je suis reparti d'une
feuille blanche.

J'ai clairement sous estimé l'ampleur de la tâche, développer à nouveau chaque
brique s'est avéré être un chantier colossal qui a eu raison de ma motivation à
plusieurs reprises.

J'ai laissé le projet de côté des **mois durant**... et ce **plusieurs fois**...
Chaque reprise était chaque fois un peu plus dure car il fallait reprendre
presque depuis zéro, le temps de se remettre dans le bain. J'ai clairement perdu
un temps fou.

Bref ce fut une longue aventure parsemée de démotivation.

![fail](https://media.giphy.com/media/XsUtdIeJ0MWMo/giphy.gif)

## Evolution v3 et Migration Open Source

Le but était double : faire un **lifting technique** et ouvrir le projet en **open source**.

#### Lifting technique:

Le projet a débuté en 2011, il a été mis à jour fin 2013 où j'ai publié la
version 2. Depuis il n'y a eu que **peu ou prou de mises à jour**. De plus la dette
technique, héritée des débuts du projet, n'avait pas été éliminée.

Quatre ans pour un projet web ce n'est pas long... **c'est une éternité** !
Pendant ce temps les techologies, les outils et les méthodologies évoluent.

Si vous n'agissez pas vous vous retrouver vite avec un projet dit **legacy** :
un projet inmaintenable où chaque intervention se termine par un hideux
rustinage au sommet d'un assemblage des plus douteux.

> Legacy code
![Legacy code](https://media.giphy.com/media/hcFmJ2LqGqGBi/giphy.gif)

#### Ouverture du projet en opensource

L'autre ambition de cette refonte, c'est de péreniser le projet et de ne plus
être seul à pouvoir y contribuer.

De plus comme le projet n'a pas une vocation à générer des profits, le choix
d'ouvrir le code en `opensource` sur github s'est imposé tout naturellement.

Désormais, chacun pourra apporter sa pierre à l'édifice en contribuant au code
source (sous forme de pull-request) mais également en indiquant des bugs via le
gestionnaire d'issue mis à disposition par github.

## Aspect technique

Pour ce que ça interesse voici les technologies mises en oeuvre :

#### Base de données

La base de données est intégralement migrée de `mySQL` vers `PostGIS`, c'est un
point majeur car c'est une base avec un moteur `geospatial` qui donne la
possibilité d'implémenter tout un tas de fonctionnalités spécifiques aux données
géographiques.

A titre d'exemple les fichiers GPX ne sont plus stockés tel quel mais intégrés
comme des formes géométriques directement dans la base, facilitant grandement
les recherches par exemple.

#### API

L'architecture de cette nouvelle version s'appuie sur une API Rest, pouvant
alimenter le site web mais aussi, plus tard, une application mobile. C'est le
langage `Go` qui a été employé pour cette API. Go est connu pour ses
performances et sa simplicité. Par ailleurs, c'est le langage que j'utilise au
quotidien dans mon activité professionnelle.

#### Site Web aka Front End

Le site web utilise cette API Rest afin de mettre en scène les données. C'est le
framework Javascript `vue.js` qui a été choisi. C'est un framework puissant avec
une courbe d'apprentissage assez courte.

#### Hébergement

Toutes ces briques fonctionnelles sont embarquées sour forme de container
`Docker`.

## Conclusion

Ce fut un long chantier que cette refonte, mais un mal plus que nécessaire pour
péréniser le projet et son contenu. Mais cela ne répresente qu'une moitué du
chemain, il faut désormais constituer une communauté de contributeur pour faire
évoluer le site, n'hésitez donc pas à participer ainsi qu'à partager
l'information autour de vous !