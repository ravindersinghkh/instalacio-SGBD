# Percona
## Comprovacions
1. Un cop realitzada la instal·lació realitza una securització de la mateixa. Quin programa realitza aquesta tasca? Realitza una securització de la instal·lació indicant que la contrasenya de root sigui patata.
    - Agafem la contrasenya temporal del MySQL amb la comanda `cat /var/log/mysqld.log | grep password`
    - Cambien polítiques de contrasenya del Mysql amb les següents comandes per poder posar “patata” com a password `SET GLOBAL validate_password.policy=LOW` `SET GLOBAL validate_password.length=6`
    - Per securitzar, utilitzarem la següent comanda `mysql_secure_installation`
     <p align="center">
    <img width= "50%" src="https://i.imgur.com/YZ4RFw3.png">
    </p>
     <p align="center">
    <img width= "50%" src="https://i.imgur.com/ovaS4Kk.png">
    </p>
    <p align="center">
    <img width= "50%" src="https://i.imgur.com/dkt9rEH.png">
    </p>
  
2. Quines són les instruccions per arrancar / verificar status / apagar servei de la base de dades de Percona Server en el CentOS 7
    - Per *arrancar*: `sudo systemctl start mysqld`
    - Per verificar *status*: `sudo systemctl status mysqld`
    - Per *apagar*: `sudo systemctl stop mysqld`
3. A on es troba i quin nom rep el fitxer de configuració del SGBD Percona Server?
    - Rep el nom **my.cnf** i es troba a `/etc/my.cnf`
    <p align="center">
    <img width= "50%" src="https://i.imgur.com/ojXfHq2.png">
    </p>
4. A on es troben físicament els fitxers de dades (per defecte). Com ho has sabut?
    - Es troben a `/var/lib/mysql/`
    - Ho pots saber amb la sèntencia SQL `SELECT @@datadir;` o en el fitxer de configuració *my.cnf* en la variable *datadir*
    <p align="center">
    <img width= "50%" src="https://i.imgur.com/HypbfnY.png">
    </p>
5. Crea un usuari anomenat asix en el sistema operatiu i en SGBD de tal manera que aquest usuari del sistema operatiu no hagi d'introduir l'usuari i password cada vegada que cridem al client mysql?
    - Creem l'usuari al Centos: `sudo adduser asix`
    - Creem l'usuari a la base de dades i li donem permissos `CREATE USER 'asix'@'%' IDENTIFIED by 'patata';` `GRANT ALL PRIVILEGES ON * . * TO 'asix'@'%';`
    - Afegim al fitxer de configuració *my.cnf* les següents línies i comprovem:
     <p align="center">
    <img width= "50%" src="https://i.imgur.com/HItLYM4.png">
    </p>
     <p align="center">
    <img width= "50%" src="https://i.imgur.com/HMUYSk6.png">
    </p>
    
6. El servei de MySQL (mysqld) escolta al port 3306. Quina modificació/passos caldrien fer per canviar aquest port a 33306 per exemple?

