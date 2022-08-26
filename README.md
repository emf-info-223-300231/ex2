# ex2
Exercice 2 - Introduction JDBC
2. But de l’application
Créez une application capable de lire une table de personnes stockée dans une base de données MySQL/HSQLDB/Access via la librairie JDBC. Les deux boutons permettent de balayer les différentes personnes de la table chargée dans une liste.
3. Diagramme d’activité de l’application

4. Diagramme des classes
La vue est représentée par un fichier fxml, le contrôleur regroupe les écouteurs et les accès aux contrôles de l’application. Le worker et son interface exécute les tâches lourdes de l’application. Ce modèle à couches se retrouvera tout au long du module avec des extensions.  


La classe MyDBException fonctionne en en levant une exception et l'exception est ensuite catcher dans le contrôleur. 
Voici un exemple avec une connexion à une base de données avec une possible erreur et une levée d’exception avec construction du message qui apparaitra dans la popup d’erreur. 
Si vous installez la dernière version du serveur MySQL (8.0.x), il faut impérativement prendre le driver JDBC 8.0.x que vous pouvez copier dans le dossier NetBeans ide/modules/ext et changer la librairie de NetBeans.


Dans le contrôleur, on catch l’exception pour la mettre dans une popup. Vous pouvez remarquer que la méthode du worker est void, cela peut se faire si l’on utilise le throws.

 
5. Maquette de l’application

      


6. Comment débuter ?
L'interface JavaFX est fonctionnelle, la connexion et la déconnexion aussi. Il faut faire la requête et récupérer les données ainsi que la programmation des 2 boutons.
Pour cet exercice les tests unitaires sont également réalisé. Pour votre information, il est nettement plus rapide de rendre fonctionnelles les méthodes avec les tests unitaires (un facteur 10 à 100 plus rapide). Seulement ensuite, on intègre ces méthodes dans l’application principale.
Vous devez pour cet exercice réaliser les liaisons Ctrl à Worker.
Les méthodes a implémentées sont :
	· Ctrl > actionPrevious
	· Ctrl > actionNext
	· Wrk > lirePersonnes
	· Wrk > precedentPersonne
	· Wrk > suivantPersonne
7. La même chose avec MS-Access
Il est possible d'utiliser votre programme de manière transparente avec une autre base de données qui a une structure équivalente. Ajoutez une nouvelle méthode de connexion dans votre worker et dans laquelle vous configurez la connexion pour la base de données Access. 
Pour se connecter, la meilleur façon est d'utiliser un driver proposé par un autre canal (gratuit ou payant), par exemple: uCanAccess. 
Faites une classe de test pour Access de la même manière que pour MySQL, la base de données est dans le répertoire data.
8. Pour les rapides
Créez une base de données SQLite ![image](https://user-images.githubusercontent.com/3630367/186989985-7d2e68d4-4791-4e63-b07f-10cbdfdd2e29.png)
