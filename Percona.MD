# Percona
## Comprovacions
1. Un cop realitzada la instal·lació realitza una securització de la mateixa. Quin programa realitza aquesta tasca? Realitza una securització de la instal·lació indicant que la contrasenya de root sigui patata.
  - Agafem la contrasenya temporal del MySQL amb la comanda `cat /var/log/mysqld.log | grep password`
  - Cambien polítiques de contrasenya del Mysql amb les següents comandes per poder posar “patata” com a password `SET GLOBAL validate_password.policy=LOW` `SET GLOBAL validate_password.length=6`
  - ![password](password.jpg)
2. 
