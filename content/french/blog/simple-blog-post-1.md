---
title: "Prédiction tennis"
date: 2020-06-15T12:52:36+06:00
image_webp: images/blog/tennis.webp
image: images/blog/tennis.jpg
author: Deconinck Florian
description : "Prédiction Tennis en Régression logistique"
---

Passionné de sport et ayant pratiqué le tennis durant 7 années, quoi de plus intéressant que de commencer à étudier le Big Data avec un projet autour de ce thème. J'ai réalisé ce projet en troisième année, dans le cadre de mes études, avec un ami de longue date [Thomas CARIN](https://github.com/Thrynk). Dans ce projet nous avons essayé de répondre à la question suivante : peut-on essayer de prédire les résultats de tennis grâce aux données disponibles sur Internet ?

Nous avons eu 3 semaines pour récuperer les données et faire l'analyse. Les autres membres du groupe s'occupaient de créer un tableau de bord sur un site Web pour y mettre les derniers tweets concernant le tennis, afficher les différents résultats des matchs et lier nos pronostics.

Nous avons commencé l'analyse en se basant sur le classement Elo des joueurs et en utilisant une regression logistique. Nous avons obtenu grâce à cette méthode un précision de 65%. C'est déjà un bon score, mais nous avons ensuite essayé de faire une analyse plus approfondie.

Nous avons essayé d'utiliser plus de variables pour voir si nous pouvions améliorer cette précision :

Nous avons effectué différentes étapes pour atteindre notre objectif :

- Collecte des données : Nous avons obtenu nos données à partir d'un site Web qui fournit gratuitement une base de données pré-remplie avec des résultats de tennis et beaucoup d'informations sur les joueurs. Ce site Web est Ultimate Tennis Statistics.

- Nettoyage des données : Nous avons vérifié toutes les données pour voir si certaines importantes manquaient. Nous avons vu que nous avions les matchs en double, nous avons décidé de supprimer ces doublons et d'inverser la moitié des correspondances pour obtenir un échantillon équilibré (car le vainqueur était toujours le joueur numéro 1). Nous avons également abandonné des fonctionnalités qui ne nous intéressaient pas comme match_id, player_rank (nous avons préféré elo_rating qui est plus précis) et surface. Nous avons traité les valeurs NA en supprimant les données où les valeurs manquantes étaient essentielles pour les étapes futures. Nous avons également vu que les valeurs manquantes provenaient principalement de tournois atypiques comme la Coupe Davis ou l'ATP Finals.

- Mise à l'échelle des données : Nous avons ensuite mis à l'échelle nos données pour la régression logistique.

- Création de données : Nous avons calculé des nouvelles statistiques comme le pourcentage de succès du premier service, le pourcentage de victoires au premier service, les aces, le pourcentage de matchs gagnés et également les statistiques sur l'historiques des affrontements entre les joueurs. Nous avons ensuite effectué une différence entre les données des deux joueurs pour avoir la différence de niveaux entre les 2 joueurs sur ces statistiques.

- Sélection des données : Nous avons effectué une élimination des données récursives pour ne conserver que les données les plus importantes.

- Modélisation: Nous avons obtenu une précision de 64%, ce modèle n'a pas surpassé notre modèle précédent, nos fonctionnalités ne semblent pas apporter plus d'informations que le classement Elo.


En conclusion, avec plus de temps pour rechercher les données vraiment importantes et faire des analyses exploratoires ainsi que des tests statistiques pour évaluer nos fonctionnalités, nous pourrions nous attendre à améliorer notre modèle. Nous avons été un peu "déçus" non pas par notre travail mais par les résultats, mais nous reviendrons certainement sur cette étude, avec plus de connaissances puisque nous avons commencé notre majeure en Big Data et avec plus de temps pour créer un bon modèle, et étudier son retour sur investissement.

[Lien vers le Github](https://github.com/Thrynk/Tennis-prediction)
