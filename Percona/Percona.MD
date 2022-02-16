# Percona
## Comprovacions
1. Un cop realitzada la instal·lació realitza una securització de la mateixa. Quin programa realitza aquesta tasca? Realitza una securització de la instal·lació indicant que la contrasenya de root sigui patata.
  - Agafem la contrasenya temporal del MySQL amb la comanda `cat /var/log/mysqld.log | grep password`
  - Cambien polítiques de contrasenya del Mysql amb les següents comandes per poder posar “patata” com a password `SET GLOBAL validate_password.policy=LOW` `SET GLOBAL validate_password.length=6`
  <p align="center">
  <img width="460" height="300" src="https://i.imgur.com/YZ4RFw3.png">
  </p>
  
2. 

