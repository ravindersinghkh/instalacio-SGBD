# MongoDB
## Instal·lació

1. Creem un fitxer a `/etc/yum.repos.d/<nom de la repo>.repo` per poder instal·lar MongoDB.
   - En el fitxer creat anteriorment, afegim el següent contingut: 
    <p align="center">
    <img width= "50%" src="https://i.imgur.com/SXzWqsZ.png">
    </p>
2. Guardem el fitxer i executem la comanda `sudo yum install -y mongodb-org-5.0`
    <p align="center">
    <img width= "50%" src="https://i.imgur.com/7UYE1cp.png">
    </p>
3. Posem en marxa el servei MongoDB amb la comanda `systemctl start mongod` i comprovem amb `systemctl status mongod`
    <p align="center">
    <img width= "50%" src="https://i.imgur.com/ixKag3K.png">
    </p>
4. Finalment, creem l'usuari root per poder accedir-hi a la BD:
    <p align="center">
    <img width= "50%" src="https://i.imgur.com/UShXGWr.png">
    </p>
## Connexió

1. Configurarem el fitxer `/etc/mongod.conf` per permitir la connexió des de diferents IP's i també activarem l'autenticació d'usuaris. Un cop fet aquests canvis, reiniciem el servei mongod amb la següent comanda `systemctl restart mongod`
    <p align="center">
    <img width= "50%" src="https://i.imgur.com/auHsDzn.png">
    </p>
  > En cas de que os doni error al iniciar el servei, heu de eliminar l’arxiu temporal anomenat "mongodb-40017.sock" que es troba a /tmp.
2. Per fer la connexió, utilitzarem el software *Robo 3T*, també podem utilitzar la pròpia Shell creada per Mongo, anomeada *mongosh*
3. En el software *Robo 3T* creem una connexió nova
    <p align="center">
    <img width= "50%" src="https://i.imgur.com/zv5pFBT.png">
    </p>
    <p align="center">IP de la màquina</p>
    <p align="center">
    <img width= "30%" src="https://i.imgur.com/909qadC.png">
    </p>
    <p align="center">Dades del usuari de mongoDB</p>
    <p align="center">
    <img width= "30%" src="https://i.imgur.com/mdfkY5R.png">
    </p>
    <p align="center">Activem el protocol SSH per connectar-nos de manera segura i posem les dades del usuari de la màquina virtual</p>
    <p align="center">
    <img width= "30%" src="https://i.imgur.com/DbtA2Q9.png">
    </p>
4. Fem un test per comprovar si es connecta
    <p align="center">
    <img width= "30%" src="https://i.imgur.com/et0dJ30.png">
    </p>
5. Finalment, ens connectem i comprovem que podem veure les base de dades que venen per defecte
    <p align="center">
    <img width= "30%" src="https://i.imgur.com/Eyw4SCx.png">
    </p>
    


  
