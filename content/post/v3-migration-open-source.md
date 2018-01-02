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

## Un peu d'histoire

Le site à vu le jour en mars 2011. Après deux évolutions du site et après avoir
remporté le **premier prix du concours IGN/Géoportail en 2013**, force était de
constater que j'avais de moins en moins de temps pour m'occuper de ce projet que
je développe et gère seul depuis le début.

Néanmoins le site continue son petit bonhomme de chemin et continue de générer
du trafic et bon nombre de **traces GPS** continuent d'y être publiées.

Le site n'a jamais eu pour vocation de générer des revenus et les quelques
publicité que j'ai pu y mettre ont servi à m'aider à financer l'hébergement.
J'ai à chaque fois refusé les quelques propositions de rachat que j'ai pu avoir.

N'ayant pas l'envie de voir mourrir à petit feu ce projet qui m'a
tant apporté sur le plan professionnel comme sur le plan personnel, il était
temps de trouver une **solution pour péreniser le site et son contenu**.

Voilà maintenant plus d'un an, j'ai commencé une refonte complète du site :
**Base de données**, **API**, **front-end** et **hébergement**, je suis reparti
d'une feuille blanche.

El là ...

![fail](https://media.giphy.com/media/XsUtdIeJ0MWMo/giphy.gif)

... J'ai clairement sous estimé l'ampleur de la tâche, développer à nouveau
chaque brique s'est avéré être un chantier colossal qui a eu raison de ma
motivation à plusieurs reprises.

J'ai laissé le projet de côté des **mois durant**... et ce **plusieurs fois**...
Chaque reprise était un peu plus dure que la précedente, car il fallait
reprendre presque depuis zéro, le temps de se remettre dans le bain. J'ai
clairement perdu un temps fou.

Bref ce fut une longue aventure passionante et **parsemée de démotivation**.

## L'enjeu de la v3 et l'intérêt de l'Open Source

Le but est double : faire un **lifting technique** et ouvrir le projet en
**open source**.

#### Lifting technique:

Le projet a débuté en 2011, puis mis à jour — essentiellement esthétiquement —
fin 2013 où j'ai publié la version 2. Depuis il n'y a eu que **peu ou prou de
mises à jour**. De plus la dette technique, héritée des débuts du projet,
n'avait pas été éliminée.

Quatre ans pour un projet web ce n'est pas long... **c'est une éternité** !
Pendant ce temps les techologies, les outils et les méthodologies évoluent.
Chaque mise à jour devient de plus en plus compliquée.

Si vous n'agissez pas vous vous retrouver vite avec un projet dit **legacy** :
un projet inmaintenable où chaque intervention se termine par un hideux
rustinage au sommet d'un assemblage des plus douteux.

> Legacy code ![Legacy code](https://media.giphy.com/media/hcFmJ2LqGqGBi/giphy.gif)

#### Ouverture du projet en opensource

L'autre ambition de cette refonte, c'est de péreniser le projet et de ne plus
être **seul à pouvoir y contribuer**.

De plus comme le projet n'a pas une vocation à générer des profits, le choix
d'ouvrir le code en `opensource` sur github s'est imposé tout naturellement.

Désormais, chacun pourra apporter sa pierre à l'édifice en contribuant au code
source mais également en indiquant des bugs ou proposer des évolutions via le
gestionnaire d'issues mis à disposition par github.

Vous êtes libre de faire de `la-trace.com` l'outil que vous souhaitez.

## Aspect technique

Pour ce que ça interesse voici un billet au sujet des [technologies mises en
oeuvre]({{< relref "v3-technique-under-the-hood.md" >}})

## Conclusion

Ce fut un long chantier que cette refonte, mais un mal plus que nécessaire pour
péréniser le projet et son contenu.

Cela ne répresente qu'**une moitié du chemin**, il faut désormais constituer une
communauté de contributeurs pour faire évoluer le site, n'hésitez donc pas à
participer ainsi qu'à partager l'information autour de vous !