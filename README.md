Pour mettre en place le projet:

git clone https://gitlab.com/CestVraimentTropDrole/td_docker.git

cd monprojet

cp env .env

Modifier {NOM_BD}, {USER_BD}, {PASS_BD}, {ROOT_PASS}

(docker build -t monlogindocker/monapache ./monapache) -peut-être pas nécessaire-

docker-compose up

Initialiser la base de données :
6.1. Ouvrir dans le navigateur : http://localhost:8080/
6.2. Se connecter avec : utilisateur : valeur de ${USER_BD}, mot de passe : valeur de ${PASS_BD}
6.3. Sélectionner la base ${NOM_BD}
6.4. Cliquer sur Importer, et choisir le fichier todos.sql

Tester le site : http://localhost/

Arrêter l'environnement Docker : docker-compose down
Supprimer les images + volumes : docker-compose down --volumes --rmi all
