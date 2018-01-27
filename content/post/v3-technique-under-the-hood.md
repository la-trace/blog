---
title: "V3 Technique Under the Hood"
date: 2018-01-02T10:19:01+01:00
bigimg: [{src: "/img/code.jpg", desc: ""}]
draft: false
---

Voici un petit point technique sur les technologies utilisées pour la refonte de
la v3 : Base de données, API, Front End et hébergement.

<!--more-->

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
