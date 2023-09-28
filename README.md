# Projet_Recommandation_Livres

Le projet de Recommandation de Livres que nous avons développé vise à simplifier l'exploration du monde littéraire pour les utilisateurs de la plateforme de lecture. Dans un univers en constante expansion de livres, il est parfois difficile de savoir par où commencer ou de trouver le prochain livre qui captivera notre imagination. C'est là que notre outil entre en jeu.
Nous avons conçu ce projet en combinant des compétences en scraping de données, en analyse textuelle pour créer un système de recommandation de livres personnalisé. Il repose sur une base de données de livres provenant de Goodreads, plus précisément dans la section ‘what do read next’. Notre objectif était de créer un moyen simple et efficace pour les lecteurs de découvrir de nouveaux livres qui correspondent à leurs préférences de lecture plus  .

Le projet intègre plusieurs libraries, notamment Selenium pour le scraping de données, Pandas pour la manipulation des données et Scikit-Learn pour le calcul de la similarité cosinus. Tout cela dans le but de fournir aux utilisateurs une expérience fluide et agréable lors de la recherche de leurs prochaines lectures.
La lecture est une porte d'entrée vers des mondes imaginaires et des idées nouvelles, et notre projet sert à élargir cette porte en offrant des propositions de livres pertinentes et variées mis en avant avec  un système de recommandation basé sur la similarité entre les résumés et les genres des livres. Dans cette documentation, nous allons plonger dans les détails de notre projet et des étapes principales qui constituent le projet.

## Partie 1 : Extraction des Données (Scraping) 
Dans cette première partie du projet, nous utilisons la bibliothèque Selenium pour extraire les informations à partir du site web Goodreads. L'objectif principal est d'obtenir des données sur les livres qui seront la base de notre système de recommandation.
En utilisant Selenium nous collectons les données essentielles telles que les titres des livres, les noms des auteurs, les liens vers les pages individuelles des livres et les URL des couvertures de livres. 
Après avoir collecté ces informations de base, nous allons plus loin en accédant aux pages de chaque livre individuel. Là, nous extrayons des données complémentaires, telles que les résumés des livres, les notes attribuées par les utilisateurs et les genres auxquels chaque livre appartient.

## Partie 2 : Constitution des Bases de Données
Une fois les données extraites, nous passons à la constitution de bases de données structurées à l'aide de la bibliothèque Pandas. 
La première base de données contient les premières informations enregistrés telles que la couverture, le titre, l’auteur et le lien de chaque livre sur les cinq pages. La deuxième base contient les informations extraites à partir des liens de chaque livre telles que le résumé, la note et le genre.
Les données dans les deux data bases sont ensuite nettoyées et fusionnées dans une unique base de données ‘total_data’, ce qui nous permettra de les manipuler plus efficacement dans les étapes suivantes de notre projet.

## Partie 3 : Création du Système de Recommandation
Cette étape est cruciale pour le projet, car elle consiste à élaborer un système de recommandation efficace pour suggérer des livres similaires en fonction des préférences de l'utilisateur.
Nous utilisons la similarité cosinus pour mesurer à la fois la similitude entre les résumés des livres et entre les genres des livres. En attribuant des poids égaux aux recommandations basées sur les résumés et aux recommandations basées sur les genres, nous pouvons combiner ces deux mesures pour obtenir des recommandations finales. Cela permet aux utilisateurs de découvrir de nouveaux livres pertinents à ses préférences et qui correspondent à leurs goûts littéraires.

# Conclusion
En conclusion, notre projet de Recommandation de Livres a été créé dans le but de simplifier et  faciliter la découverte de nouvelles histoires pertinentes aux goûts des utilisateurs. Au cours de ce projet, nous avons relevé plusieurs défis, du scraping de données à la création d'un système de recommandation basé sur la similarité textuelle. Nous avons cherché à offrir aux utilisateurs une expérience transparente et interactive, où ils peuvent simplement saisir le titre d'un livre qui les intéresse et recevoir des recommandations instantanées.



