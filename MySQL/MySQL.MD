# MySQL 8.0
## Comprovacions
1. A on es troben físicament els fitxers de dades?
    - Es trobem a `/var/lib/mysql/`
    - Ho podem saber amb la sentència SQL `SELECT @@datadir;`
    <p align="center">
    <img width= "50%" src="https://i.imgur.com/sUc5s6G.png">
    </p>
  
2. A on es troba el fitxer de configuració? Quin és el seu contingut?
    - Es troba a `/etc/my.cnf`
    - El seu contingut són *opcions globals* que llegeix el servei mysql a l'hora d'iniciar-se, proporcionant una manera còmoda d'especificar les opcions d'ús habitual de manera       que no cal que s'introdueixin a la línia d'ordres cada vegada que s'executi mysql
    <p align="center">
    <img width= "50%" src="https://i.imgur.com/K6rN8eJ.png">
    </p>
    
3. El procés de mysqld escolta al port 3306. Quina modificació/passos caldrien fer per canviar aquest port a 33306 per exemple?
    - Aturem el servei mysqld
    - Configurem el fitxer *my.cnf*
    - Sota l'opció [mysqld] afegim una variable anomenada `port=33306`. Guardem el fitxer i arrenquem el servei mysqld
    <p align="center">
    <img width= "50%" src="https://i.imgur.com/pdUPeww.png">
    </p>
4. Un cop finalitzada la instal·lació i veure que funciona, mostra el resultat de la comanda `ps -ef | grep mysql`
    <p align="center">
    <img width= "50%" src="https://i.imgur.com/YWz3q2j.png">
    </p>
5. 
6. 
  

    

