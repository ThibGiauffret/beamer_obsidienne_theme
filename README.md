# Obsidienne : un thème pour Beamer

<h2>Présentation</h2>

Beamer est le pendant de Microsoft PowerPoint permettant de réaliser des présentations à l’aide du formalisme LaTeX.<br>

De nombreux styles existent de manière native pour réaliser des présentations. Cependant, ne trouvant pas de thème me convenant, je me suis penché sur la création d’un thème personnalisé. </p>

<p align="center">
<img src="https://www.ensciences.fr/git/images/article_beamer/page1.svg"/>

<img src="https://www.ensciences.fr/git/images/article_beamer/page2.svg"/>

<img src="https://www.ensciences.fr/git/images/article_beamer/page3.svg"/>
</p>

<h2>A propos de la mise en forme</h2>

<p>Le thème a pour objectif de proposer une présentation sobre et efficace : pour cela les informations essentielles doivent être directement accessibles.

<h3>Le choix des couleurs</h3>

Le design tend à aller vers l’essentiel en proposant un jeu de couleurs sobre (un peu moins agressif ou fade que certains autres styles Beamer). Le fort contraste permet une meilleur lisibilité.

<h3>Le choix de la police</h3>

Toujours dans une optique  de lisibilité, la police choisie est assez ronde et grasse afin qu’elle puisse aussi bien ressortir en présentation qu’à l’impression. Le thème utlise l'option "structurebold" de Beamer.

<h3>Les informations sur la diapositive</h3>

Les sections et leur arborescence sont mises en avant par une diapositive "plan" à chaque début de section. L'arborescence n’apparait pas sur chaque diapositive (je trouvais cela un peu trop lourd…). Le nom de la section apparaît au dessus du titre de la diapositive (afin de savoir quand même où on en est). Sur la gauche, le nom de l’auteur et de la présentation apparaissent. En bas à droite, le numéro de page. Rien de plus, rien de moins, l’essentiel est là !




<h2>Comment l'utiliser ?</h2>

Pour utiliser ce thème, deux choses sont requises : les fichiers du thème et certaines commandes dans l'entête de votre document.

<h3>Les fichiers essentiels</h3>

Un seul fichier de style est requis. Il est disponible dans l’archive sous le nom : <em>beamerthemeobsidienne.sty</em>

<h3>La structure minimale de l'entête et les commandes</h3>


    %!TEX TS-program = xelatex
    \documentclass{beamer}
    \usepackage[utf8]{inputenc}
    \usepackage[T1]{fontenc}

    \graphicspath{{figures/}} % Emplacement des figures.

    \def\illustration{1} % Illustration en première page (1=activé, 0=désactivé). Penser à placer un fichier "illustration" dans le dossier des figures. Format préféré : 12,8cm par 4,8cm.

    \def\logo{1} % Logo en première page (1=activé, 0=désactivé). Penser à placer un fichier "logo" dans le dossier des figures.
    
    \def\outline{1} % Plan à chaque début de section (1=activé, 0=désactivé).
     \usetheme{obsidienne} % Fichiers du thème obsidienne
     
    \title{Votre titre} % Titre
    \subtitle{Votre sous-titre} % Sous-titre
    \date{La date} % Date
    \author[Vos initiales]{Votre nom} % Auteur
    \institute{Votre institution} % Etablissement

<h2>Comment se l’approprier/le modifier ?</h2>

Une première manière de se l’approprier est d’apposer vos propres logo et illustration en première page. Si vous ne souhaitez pas en avoir, ces options peuvent être désactivées. 

Si vous voulez en faire plus, il va falloir mettre les mains dans le camboui (à savoir modifier directement le fichier <em>beamerthemeobsidienne.sty</em>). Vous pourrez alors y modifier les couleurs, la structure, les informations affichées…
