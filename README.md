CVE-2023-23752 décrit un contournement d'authentification qui permet à un attaquant de divulguer des informations privilégiées. Les exploits publics se concentrent sur la fuite des informations d'identification de la base de données MySQL de la victime - une perspective peu intéressante (nous pensions), car exposer la base de données à Internet est une mauvaise configuration dangereuse. L'accès à la base de données permet à l'attaquant de modifier le Joomla! Mot de passe du super utilisateur.

Recommandations:
Ouvrez votre invite de commande en mode administrateur
Faire : gem install httpx docopt paint et installer ruby
Entrez dans le dossier exploit-CVE-2023-23752-master et dans le sous dossier exploit-CVE-2023-23752-master
Faire : docker compose up -d
Une fois terminer allez sur le lein  localhost:4242 ou http://127.0.0.1:4242/installation/index.php.
Et faites les configurations suivantes
Nom du site :  CVE-2023-23752
Prénom superuser : John
Nom superuser : Doe
Mot de passe : root@12345 ou ce que vous voulez
Mail : john.doe@secret.corp
DB type: mysqli
DB host: mysql
DB user: root
DB password: demo-ppZ5hnvK2ZEpR9yhRKA7
DB name: joomla_db
DB prefix: krukc_

Validez les informations 
Vous aurez la page suivante 

![Capture d'écran 2023-06-07 094429](https://github.com/ATIGNONWilliam/-Joomla-v4.2.8---Divulgation-d-informations-non-authentifi-es/assets/132202083/b9628a8c-378f-40f9-8f17-d0cbcf6a0ce1)

Entrez dans le dossier exploit-CVE-2023-23752-master et dans le sous dossier exploit-CVE-2023-23752-master et faites : ruby exploit.rb -h pour voir les options de exploit.rb
Vous devez avoir la page suivante 
![Capture d'écran 2023-06-07 215638](https://github.com/ATIGNONWilliam/-Joomla-v4.2.8---Divulgation-d-informations-non-authentifi-es/assets/132202083/06b4bfda-9998-44ef-8964-bdb665f0c4ab)
Ensuite tapez : ruby exploit.rb  http://127.0.0.1:4242
![Capture d'écran 2023-06-07 223246](https://github.com/ATIGNONWilliam/-Joomla-v4.2.8---Divulgation-d-informations-non-authentifi-es/assets/132202083/6f773aec-b4a4-472e-9a0a-51d2edddd6d0)
Exploit.rb extrai les informations de la base de données.


