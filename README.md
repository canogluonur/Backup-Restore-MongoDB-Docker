# Backup-Restore-MongoDB-Docker
Backup and restore data from Mongodb in a Docker container.


In the docker-compose.yml file, we are adding a directory named ./backup to the volumes section, linking it to compose.yml as - ./backup:/backup.




Afterward, we enter the MongoDB container.
``` 
$ docker exec -ti <mongodb's container name> bash
$ cd backup
```


### This command is used to backup data from a MongoDB database.
```
$ mongodump --username <user> --password <pass> --out=/backup/
```


### restore the database
```
$ mongorestore --db=<dbname> --username=<user> --password=<pass> /backup/<dbname>
```

