# GLOSSAIRE

- [Général](#général)
- [Front-end](#front-end)
- [UX / UI](#ux-ui)
- [Architecture](#architecture)
- [Modélisation / Base de données](#modélisation---base-de-données)
- [Symfony](#symfony)
- [Sécurité](#sécurité)
- [RGPD](#rgpd)
- [SEO](#seo)
- [Gestion de projets / DevOps](#gestion-de-projets---devops)
- [English](#english)

## Général

1. Quel est l’environnement à installer pour exécuter un script PHP ? Citer 2 exemples de logiciels permettant ce contexte
    - Le package Laragon permet d'executer des scripts PHP.

2. Qu’est-ce qu’un algorithme ?
   - Une suite d'instructions à effectuer dans un ordre précis.

3. Qu’est-ce qu’une variable ? Par quel symbole est préfixée une variable en PHP ?
   - Une valeur affectée à [un mot?]. Elle peut être de plusieurs types (string, int, bool).
     Sur PHP une variable est préfixée de '$'.

4. Qu’est-ce que la portée d’une variable ?
    - Cela indique si elle est accessible en dehors du bloc dans lequel elle a été déclarée. Cela dépend de comment elle a été déclarée, de sa position et de sa portée.

5. Qu’est-ce qu’une constante ? Quelle est la différence avec une variable ?
   - Tout comme une variable une constante est une valeur associée à un libellé, sauf qu'elle ne peut pas changer de valeur, d'où son nom.

6. Qu’est-ce qu’une superglobale, combien en existent-ils et donner un exemple d’utilisation
    - C'est une variable qui est toujours accessible. Il en existe 9 ($_SERVER, $_GET, $_POST, $_FILES, $_COOKIE, $_SESSION, $_ENV, $_REQUEST, $_GLOBALS). (ex: $_POST pour retrouver le contenu d'un post)

7. Quels sont les différents types (primitifs) que l’on peut associer à une variable en PHP ? Les citer et en donner des exemples (ne pas oublier le type d’une variable sans valeur)
    - string (chaîne de charactères)
    - int (nombre entier)
    - float (nombre décimal)
    - char (charactère)
    - bool (vrai/faux)
    - null (rien)

8. Existe-t-il plusieurs types de tableaux en PHP, si oui lesquels ?
   - Il y a les tableaux simples, avec seulement des valeurs:
        ```php
        array(10, 12, 8)
        ```
   - Et les tableaux associant une valeur à une clé:
        ```php
        array => ["Mickaël" => "FRA", "Virgile" => "ESP"];
        ```

9. Quelles sont les différentes structures de contrôles qu’il existe en algorithmie ? Donner un exemple pour chacune d’entre elles
    - Séquences : (bloc de code?)
    - Sélections :
        ```php
        if($condition) {
            // action
        }
        ```
    - Répétitions :
        ```php
        while($condition) {
            // action
        }
        ```
    - Alternatives
        ```php
        switch($valeur) {
            case 0:
                echo "!!";
                break;
            case 1:
                echo "??";
                break;
            default:
                echo "!?"
        }
        ```
    - Boucles
        ```php
        for($i = 0; $i < 10; i++) {
            // action
        }
        ```

10. Quelle est la fonction PHP permettant de demander la longueur d’une chaîne de caractères ?
    - strlen($array)

11. Qu’est-ce qu’une session ? Quelle fonction permet de démarrer une session en PHP ? Donner un exemple d’utilisation en PHP
    - session_start() permet de démarrer une session en PHP
    - créer un site d'achat avec un panier dans lequel les achats seraient stockés dans $_SESSION

12. Qu’est-ce qu’un cookie ? Donner un exemple d’utilisation en PHP
    - 

13. Quelle est la différence entre les instructions « require » et « include » en PHP
    - 

14. Comment effectuer une redirection en PHP ?
    - header("Location: location/path.php")

15. Définir la partie « front-end » et « back-end » d’une application
    - Le front-end c'est ce que l'utilisateur voit, comme le site
    - Le back-end c'est par exemple l'enregistrement des utilisateurs.

16. Définir le contrôle de version ? Qu’est-ce que Git ?
    - 

17. Qu’est-ce qu’un CMS ? Citer au moins 2 exemples
    - Content Management System, permet de créer un site web sans connaissances particulières en développement web (ex: Wordpress, ...)

## Front-end

18. Définir HTML
    - Langage permettant de créer des sites web à partir de balises.

19. Définir CSS
    - Permet de mettre le site en page grâce à des propriétés appliquées aux balises (couleur, largeur, arrangement)

20. Définir Javascript
    - Permet plus d'intéractivité grâce à l'exécution de scripts (eventListener sur un bouton HTML qui change le CSS)

21. Définir JSON. Dans quel contexte ce format est-il utilisé ?
    - JavaScript Object Notation, c'est un langage de base de données, il peut être utilisé dans de nombreuses situations qui nécessitent une base de données (genre les naissances à l'hôpital, avec nom, prénom, et date de naissance pour chaque personne)

22. Peut-on interpréter du Javascript côté serveur ? Si oui, comment ?
    - Oui c'est possible. Node.js rend ça possible.

23. Qu’est-ce qu’un sélecteur CSS ?
    - Une classe(ex: .box) ou un id(ex: #container) ou une balise(ex: header)

24. Quelle balise HTML permet de créer un lien hypertexte ?
    - <a></a>

25. Qu’est-ce qu’une requête AJAX ?
    - AJAX: Asynchronous JavaScript and XML => Déf web: méthode de communication entre un navigateur web et un serveur web qui permet de récupérer des données dynamiques sans recharger complètement la page web

26. Quel sélecteur CSS permet de sélectionner tous les éléments d’une classe spécifique ? D’un identifiant spécifique ?
    - ul > : sélectionne les enfants de ul
    - ul > li : sélectionne tous les li enfants de ul

27. Définir le responsive design
    - Le fait que la disposition et la taille des éléments s'adapte au format de l'appareil (pc, téléphone)

28. Qu’est-ce que le templating ?
    - Le fait d'avoir une template, c'est-à-dire un bout de code qui sera répêté partout et évitera les répétitions (ex: ob_start() et ob_get_clean() permettent d'"enregistrer" le contenu pour le répêter autre part)

29. Qu’est-ce qu’une fonction anonyme en Javascript ?
    - fonction sans nom (ex: const addFunc = (a, b) => a + b;)

30. Quelle méthode JavaScript est utilisée pour ajouter un élément à la fin d'un tableau ?
    - yourArray.push(eltToPush)

31. Qu’est-ce qu’un « media query » ?
    - Sert en CSS pour le responsive design. Permet de changer le CSS de tel ou tel élément en fonction de la taille du viewport.

32. Qu’est-ce qu’un pseudo élément en CSS ?
    - déf web: élément virtuel qui est ajouté à un sélecteur CSS pour styliser une partie spécifique d’un élément HTML
        - ::before => ajouter du contenu avant l'élément ciblé
        - ::after =>    ''    ''   ''    après   ''       ''
        - ::first-line => styliser la première ligne d'un bloc de texte
        - ::first-letter => styliser la première lettre d'un bloc de texte

33. Qu’est-ce que Bootstrap ? Donner d’autres exemples équivalent
    - Framework CSS qui facilite la mise en page
    - Tailwind CSS est aussi un framework CSS qui facilite la mise en style

34. Quand un formulaire HTML est créé, quelles sont les 2 méthodes qui peuvent lui être associées ? Donner la différence entre ces 2 méthodes
    - action="post" et action="??"

## UX UI

35. Quelle est la différence entre UX Design et UI Design ?
    - UX: user experience
    - UI: user interface
    - En général une bonne expérience utilisateur passe par une bonne interface utilisateur, qui se doit d'être agréable à l'oeil tout en restant intuitive à utiliser

36. Qu’est-ce qu’un wireframe ?
    - C'est le "squelette" d'un site, ce n'est pas une maquette complète, mais plutôt une maquette qui désigne l'emplacement des éléments (taille, agencement, ...) sans trop s'attarder sur le style (couleur, police d'écriture, ...)

37. Qu’est-ce qu’un prototype ?
    - 

38. Qu’est-ce que la hiérarchie visuelle en UI Design ?
    - 

39. Qu’est-ce que l’accessibilité en UX Design ?
    - C'est le fait de prendre à garde à ce que tout le site soit utilisable et compréensible par tout le monde, quels que puissent être leurs handicaps (daltonisme, ?malvoiyance?).
    - Il faut donc faire attention à, par exemple, rendre la couleur du texte facile à lire par rapport à l'arrière plan

40. Qu’est-ce qu’une grille de mise en page ?
    - 

41. Qu’est-ce que la notion d’affordance en UX Design ?
    - Le fait de suggérer des actions à l'utilisateur sans qu'il ait besoin de comprendre le fonctionnement du site (ex: changement de curseur au survol, contraste)
    - Contribue à l'UX dans la mesure où même un utilisateur nouveau pourra utiliser le site normalement

42. Qu’est-ce qu’un « mobile first design » ?
    - Le fait de commencer la maquette sur un format mobile, afin de s'assurer que les éléments ne sont pas envahissants, contrairement au desktop first, qui pourrait forcer à faire des compromis


## Programmation orientée objet (POO)

43. Donner une définition de la programmation orientée objet
    - Programmation qui utilise des classes et des objets avec héritage et tout, ce qui permet d'éviter la redondance

44. Qu’est-ce qu’une classe ? Comment la déclare-t-on ?
    - Ensemble d'attributs (ex: prix, modèle) et de fonctions (ex: addPrice(int $price)) qui permettent d'instancier un objet possédant ces attributs et fonctions 
    - class Name{...contenu...}

45. Qu’est-ce qu’un objet ?
    - Instance d'une classe (ex: Student $student Ici $student est une instance de la classe Student et possède toutes ses attributs et fonctions)

46. Définir la notion de propriété / attribut / méthode
    - propriété: zz
    - attribut: les caractéristiques d'un objet
        Exemple:
        ```php
        private $nom;
        private $prix;
        private $kilometrage = 0;
        ```
    - Méthode: Une fonction
        Exemple: 
        ```php
        public function addPrice(int $price): void
        {
            $this->price += $price;
        }
        ```

47. Qu’est-ce que la visibilité d’une propriété ou d’une méthode ? Citer les différents types de visibilité
    - Cela définit son accessibilité
    - public: accessibles à l'intérieur et à l'extérieur de la classe
    - private: accessibles à l'intérieur de la classe uniquement
    - protected: accessibles à l'intérieur de la classe uniquement ou à l'extérieur grâce à une méthode dérivée
        Exemple:
        ```php
        public function callProtected() {
            $this->protectedMethod();
        }
        ```

48. Quelle est la méthode spécifique utilisée pour créer un nouvel objet à partir d’une classe ?
    - $var = new NomObjet(paramètres);
        Exemple:
        ```php
        $auteur = new Auteur("Stephen King", "1247-09-21");
        ```
        Dans ce cas-là, la classe auteur contient un constructeur qui requiert deux paramètres: des strings correspondant aux attributs $nom et $dateNaissance

49. Qu’est-ce que l’encapsulation ?
    - Déf: regroupement des méthodes et attributs dans une même classe.

50. Que signifie « étendre une classe » ? Quelle est le concept clé mis en œuvre ? Donner un exemple
    - Étendre une classe, c'est le fait de la réutiliser pour une autre classe, par héritage
    - L'héritage permet de réutiliser des méthodes de la classe mère <br>
        Exemple:
        ```php
        class Enemy extends NPC {
            // contenu de la classe
        }
        ```

51. Définir l’opérateur de résolution de portée
    -

52. Définir une méthode / propriété statique
    - public static function functionName(){}
    - private static string $_name;

53. Définir le polymorphisme en POO
    - Permet de définir plusieurs versions d'une méthode, pour remplir des buts différents

54. Définir une méthode / classe abstraite ?
    - Une classe plus générale qui est parente d'autres classes dans lesquelles ses méthodes seront implémentées.

55. Définir le chaînage de méthodes
    - Permet d'accéder à des infos pas disponibles directement
        Exemple:
        ```php
        // Dans ce cas-là, l'attribut $voiture de User est de type Voiture, c-à-d que c'est une instance d'un autre objet, qui possède un getter pour son attribut $nom

        $user = new User;

        $nomVoitureUser = $user->getVoiture()->getNom();
        ```

56. Qu’est-ce que la méthode \_\_toString() ? Existe-t-il d’autres méthodes « magiques »
    - C'est une méthode qui renvoie ce qu'on lui demande de renvoyer pour éviter les redondances
        Exemple:
        ```php
        public function __toString() {
            return($this->prenom . " " . $this->nom);
        }
        ```
        Et alors il sera préférable d'appeler le __toString que de concaténer $prenom et $nomplein de fois

57. Qu’est-ce qu’un « autoload » ?
    - 

58. Comment appelle-t-on en français les « getters » et les « setters » ?
    - accesseur? Permet de mettre à jour une valeur ou d'aller la chercher.

59. Qu’est-ce que la sérialisation en PHP ?
    - 


## Architecture

60. Qu’est-ce que l’architecture client / serveur ? Grâce à quel type de requête peut-on interroger le serveur. Définir l’acronyme de ce type de requête. Si on ajoute un « S » à cet acronyme, expliquer la différence
61. Donner la définition d’un design pattern. Citer au moins 3 exemples de design pattern
62. Qu’est-ce que l’architecture MVC ?
    - MVC : Model - View - Controller

63. Quel est le rôle de chaque couche du design pattern MVC : Model, View, Controller ?
    - Model: Gestion de la connexion à la BDD et manipulation des données
    - View: Affichage des données sélectionnées
    - Controller: Lien entre Model et View, permet d'envoyer des requêtes spécifiques à Model, puis de sélectionner les données à envoyer à View

64. Quels sont les avantages de l’architecture MVC ?
    - 

65. Existe-t-il des variantes à l’architecture MVC ?
    - 

66. Qu’est-ce qu’une API ? Définir l’architecture REST
    - API: Application Programming Interface, en français interface de programmation d'application, sert à créer un lien (interface) en une BDD et l'utilisateur, peut fournir des actions (ex: shuffle() dans une API de jeu de carte)
    - API REST: 


## Modélisation - Base de données

67. Qu’est-ce que la modélisation de données ? Définir la méthode Merise
    - La modélisation de données est le fait de définir toutes les données nécessaires, leurs attributs et les liens entre eux afin de faciliter la création de la BDD/des Entity
    - Méthode Merise: Conceptualisation de la modélisation des données de telle sorte à rendre la communication entre le client et le programmeur plus facile, de par l'utilisation de verbes et de mots pour représenter les données (prose)

68. Quelles sont les 3 étapes principales de la méthode Merise ?
    a. Analyse, conception et réalisation
    b. Planification, exécution et contrôle
    c. Création, modification et suppression
    
69. Qu’est-ce qu’un modèle conceptuel de données (MCD) en Merise ?
70. Qu’est-ce qu’un modèle logique de données (MLD) en Merise ?
71. Donner la définition des mots suivants : <br>
    a. Entité: ... <br>
    b. Relation: ... <br>
    c. Cardinalité: ... <br>
    d. Clé primaire / clé étrangère: elt unique de l'entité qui permet de l'identifier / id d'une autre entité, qui fait le lien entre les deux entités 
72. Que devient une relation de type « Many To Many » dans le modèle logique de données ?
    - Elle génère une entité entre les deux entités, contenant au moins leurs clés, afin de les lier
73. Qu’est-ce qu’une base de données ?
    - Stockage des données des différentes entités, qui permet un accès et stockage

74. Définir les notions suivantes :
    a. SQL: Structured Query Language, peut effectuer des recherches spécifiques dans les BDD
    b. MySQL: Système de hestion de BDD, basé sur SQL
    c. SGBD (donner 2 exemples de SGBD): 
75. Dans une base de données, les données sont stockées dans des **_. Celles-ci sont constituées de lignes appelées _** et de colonnes appelées \_\_\_
76. Quelle est la différence entre une base de données relationnelle et non relationnelle ?
77. Qu’est-ce qu’une jointure dans une base de données ? En existe-t-il plusieurs ? Si oui lesquelles ?
78. A quoi sert une vue dans une base de données ?
79. Qu’est-ce que l’intégrité référentielle dans une base de données ?
80. Quelles sont les fonctions d’agrégation en SQL ?
81. Qu’est-ce qu’un CRUD dans le contexte d’une base de données ?
82. Quelles sont les clauses qui permettent de :
    a. Insérer un nouvel enregistrement dans une table
    b. Modifier un enregistrement dans une table
    c. Supprimer un enregistrement dans une table
    d. Supprimer la base de données
    e. Filtrer les résultats d’une requête SQL
    f. Trier les résultats d’une requête SELECT
    g. Regrouper les résultats d'une requête SELECT en fonction d'une colonne spécifique
    h. Concaténer 2 chaînes de caractères
83. Comment se connecter à une base de données en PHP ? Quelle est la classe native utilisée ?

## Symfony

84. Qu’est-ce que Symfony ?
85. Sur quel langage de programmation et design pattern repose Symfony ?
86. Quelle est la dernière version en date de Symfony ?
87. Qu’est-ce qu’un bundle ?
88. Quel est le moteur de template utilisé par défaut dans Symfony ?
89. Qu’est-ce qu’un ORM ? Quel est son utilité et comment s’appelle-t-il au sein de Symfony ?
90. Qu’est-ce que l’injection de dépendances ? Quel est l’outil utilisé dans ce contexte et quel fichier contient l’intégralité des dépendances du projet ?
91. Que permet le bundle Maker au sein de Symfony ?
92. Quel est le langage de requêtage exploité au sein d’un projet Symfony ?
93. Quel est le composant qui garantit l’authentification et l’autorisation des utilisateurs ?

## Sécurité

94. Qu’est-ce que l’injection SQL ? Comment s’en prémunir ?
    - par exemple dans une case où l'utilisateur peut écrire, il peut écrire du sql ('1=1' & SELECT...)
95. Qu’est-ce que la faille XSS ? Comment s’en prémunir ?
96. Qu’est-ce que la faille CSRF ? Comment s’en prémunir ?
97. Définir l’attaque par force brute et l’attaque par dictionnaire
98. Existe-t-il d’autres failles de sécurité ? Citer celles-ci et expliquer simplement leur comportement
99. A quoi servent l’authentification et l’autorisation dans un contexte d’application web ?
100.  Définir la notion de hachage d’un mot de passe et citer des algorithmes de hachage
101.  Qu’est-ce qu’une politique de mots de passe forts ?
102.  Qu’est-ce que l’hameçonnage ?


    - envoyer un mail frauduleux qui contient des fichiers malveillants à télécharger

103. Définir la « validation des entrées »

## RGPD

104. Qu’est-ce que le RGPD ?


    - règlement général de la protectino des données

105. Quel est son objectif principal ?


    - protéger les données privées des utilisateurs

106. Quelle est la date d’entrée en vigueur du RGPD ?
107. Quelles sont les sanctions possibles en cas de non-respect du RGPD ?


    - amendes? prison?

108. En France, quel est l’autorité administrative qui s’occupe de faire appliquer le RGPD ?


    - ANSEE

109. Quel est le consentement valide selon le RPGD ?
110. Qu’est-ce qu’une politique de confidentialité ?
111. Quelle est la durée de conservation maximale des données personnelles selon le RGPD ?
112. Quels sont les droits des utilisateurs selon le RGPD ?
113. Qu’est-ce que le principe de minimisation des données selon le RGPD ?

## SEO

114. Qu’est-ce que le SEO ?
     - Search Engine Optimization

116. Quel est l’objectif principal du SEO ?
     - Améliorer le référencement

118. Existe-t-il plusieurs types de référencement ? Lesquels ?
119. Qu’est-ce que la densité de mots-clés en SEO ?
120. Qu’est-ce qu’une balise « alt » ?
     - C'est une balise qui permet d'ajouter une description, notamment à une image, ce qui rendra le site plus accessible aux personnes malvoiyantes qui utiliseraient des narrateurs d'écran

122. Qu’est-ce que la balise « meta description » ?
     - Elle se situe dans la tête de page et permet de fournir une description fournie mais concise du contenu de la page actuelle

124. Qu’est-ce que le « nofollow » en SEO ?
125. Quelle est l'importance du contenu de qualité pour le référencement d'un site web ?


126. Pourquoi est-il important d'utiliser des balises de titre (h1, h2, h3, etc.) de manière structurée ?
     - Car les titres sont utilisés dans le SEO, mieux vaut mettre "Site de recettes de cuisine" en h1 que "Ingrédients: ", car le site sera mieux référencé en tant que site de cuisine

128. Quelle est la recommandation pour les URL d'un site web bien référencé ?
129. Qu'est-ce que le maillage interne et pourquoi est-il important pour le référencement ?
130. Qu'est-ce que l'optimisation des images pour le référencement ?
     - Privilégier des images "web friendly", comme webp ou jfif a png et jpg permet d'accélérer le chargement de la page, et par conséquent d'améliorer le "score" SEO

132. Qu'est-ce qu'un plan de site (sitemap) et pourquoi est-il important pour le référencement ?
     - Cela peut être une page du site ou bien un fichier texte, qui décrit l'architecture du site (l'agencement des pages) et qui permet d'indexer les pages, améliorant la SEO

## Gestion de projets - DevOps

127. Qu’est-ce que la gestion de projet ?
128. Qu’est-ce qu’une méthode Agile de gestion de projet ?
129. Expliquer la méthode MoSCoW en quelques lignes et citer ses avantages
     - Mo : Must have
     - S : Should have
     - Co : Could have
     - W : Won't have
     - Permet d'optimiser le travail en déterminant les fonctionnalités sur lesquelles travailler en premier (vues) avant le reste (style)

131. A quoi sert la méthodologie MVP ? Citer les caractéristiques clés
     - MVP : Minimum Viable Product, ce dont le site a besoin pour fonctionner, et c'est tout (rentre dans la partie Must have de la méthode MoSCoW)
     - Permet donc de déterminer le minimum nécessaire pour avoir un site fonctionnel (et même présentable, dans le cadre de notre projet de fin d'année)

133. Qu’est-ce que la planification itérative ?
134. Citer 3 méthodes Agiles dans le cadre d’un projet informatique
135. Qu’est-ce qu’une réunion de revue de projet ?
136. Qu’est-ce qu’un livrable dans un projet ?
137. Quels sont les 3 piliers SCRUM ? Définir chacun d’entre eux
138. Qu’est-ce que le DevOps et quel est son objectif principal ?
139. Qu’est-ce que l’intégration continue ?
140. Qu’est-ce que Docker ? Et en quoi est-il utile dans le cadre du DevOps ?
141. Qu’est-ce qu’un test unitaire ?
142. Quelle est l'unité de code testée lors d'un test unitaire ?
143. Quelles sont les caractéristiques d'un bon test unitaire ?
144. Qu'est-ce qu'une assertion dans un test unitaire ?



## English

1. What does JavaScript enable you to do on a website ?
   a. <span style="text-decoration: underline;">Add interactive behavior and dynamic content<span>
   b. Define the layout and design of web pages
   c. Handle server-side operations
2. Which programming language is primarily used for server-side web development ?
   a. PHP X
   b. JavaScript
   c. HTML
3. What is the purpose of a web browser ?
   a. To render and display web pages X
   b. To execute serve-side code
   c. To manage databases
4. What is the difference between GET and POST methods in HTTP ?
   a. GET retrieves data from a server, while POST submits data to a server X
   b. GET submits data to a server, while POST retrieves data from a server
   c. GET and POST methods are interchangeable
5. What is the purpose of version control systems (e.g., Git) in web development ?
   a. To track changes and manage collaborative development X
   b. To optimize website loading speed
   c. To handle server-side scripting
6. What is the purpose of a framework in web development ?
   a. To provide a structured environment for building web applications
   b. To handle network protocols and data transfer X
   c. To create visual designs and layouts for websites
7. What does NoSQL stand for ?
   a. Not Only SQL X
   b. Non-Structured Query Language
   c. New Object-Oriented Language
8. Which of the following is a characteristic of NoSQL databases ?
   a. Strict schema enforcement
   b. Support for complex transactions
   c. Scalability and flexible data models X
